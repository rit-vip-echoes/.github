# DevOps
Work in progress, come back later. 


## GitHub Discord Integration
Discord integration can provide valuable messages that trigger on certain GitHub actions.

[Discord WebHook Tutorial](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks)

## Autobuild for WebGL
```
name: Build project
on: 
  push:
    branches: [ main, dev ]
  pull_request:
    branches: [ main ]
  # Also trigger on tag pushes
  create:
    tags:
      - 'v*'
  # Manual trigger for testing
  workflow_dispatch:

jobs:
  buildForAllSupportedPlatforms:
    name: Build for ${{ matrix.targetPlatform }}
    runs-on: ubuntu-latest
    strategy:
      fail-fast: false
      matrix:
        targetPlatform:
          - WebGL  
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0  # Important: fetches all history for tags
          lfs: true
      
      # Simplified version creation
      - name: Generate Version
        id: version
        run: |
          # Simple versioning - uses run number
          VERSION="1.0.${{ github.run_number }}"
          
          # Get build metadata
          SHORT_SHA=$(git rev-parse --short HEAD)
          DATE=$(date +'%Y%m%d')
          TIME=$(date +'%H%M')
          
          # Output all version info
          echo "version=$VERSION" >> $GITHUB_OUTPUT
          echo "version_with_meta=${VERSION}+${SHORT_SHA}" >> $GITHUB_OUTPUT
          echo "date=$DATE" >> $GITHUB_OUTPUT
          echo "time=$TIME" >> $GITHUB_OUTPUT
          echo "datetime=${DATE}-${TIME}" >> $GITHUB_OUTPUT
          
          echo "Building version: $VERSION (build #${{ github.run_number }})"
      
      # Cache for faster builds
      - uses: actions/cache@v3
        with:
          path: Sample2DProject/Library
          key: Library-${{ matrix.targetPlatform }}-${{ hashFiles('Sample2DProject/Assets/**', 'Sample2DProject/Packages/**', 'Sample2DProject/ProjectSettings/**') }}
          restore-keys: |
            Library-${{ matrix.targetPlatform }}-
            Library-
      
      # Free up space for Android builds
      - if: matrix.targetPlatform == 'Android'
        uses: jlumbroso/free-disk-space@v1.3.1
      
      # Build with Unity
      - uses: game-ci/unity-builder@v4
        env:
          UNITY_LICENSE: ${{ secrets.UNITY_LICENSE }}
          UNITY_EMAIL: ${{ secrets.UNITY_EMAIL }}
          UNITY_PASSWORD: ${{ secrets.UNITY_PASSWORD }}
        with:
          targetPlatform: ${{ matrix.targetPlatform }}
          projectPath: Sample2DProject
          buildName: Sample2DProject
          versioning: Custom
          version: ${{ steps.version.outputs.version }}
          # WebGL specific settings
          allowDirtyBuild: true
      
      # Create version info file with jam details
      - name: Create Version Info
        run: |
          mkdir -p version-info
          
          cat > version-info/version.txt << EOF
          Perennial - GMTK Game Jam 2025
          Theme: Loop
          Version: ${{ steps.version.outputs.version }}
          Build: #${{ github.run_number }}
          Date: ${{ steps.version.outputs.date }}
          Time: ${{ steps.version.outputs.time }}
          Platform: ${{ matrix.targetPlatform }}
          Commit: ${{ github.sha }}
          Branch: ${{ github.ref_name }}
          Builder: ${{ github.actor }}
          EOF
          
          # Also create a simple version.json for game to read
          cat > version-info/version.json << EOF
          {
            "name": "Perennial",
            "event": "GMTK Game Jam 2025",
            "version": "${{ steps.version.outputs.version }}",
            "build": ${{ github.run_number }},
            "platform": "${{ matrix.targetPlatform }}",
            "date": "${{ steps.version.outputs.date }}",
            "commit": "${{ github.sha }}"
          }
          EOF
          
          echo "Version files created successfully"
      
      # Prepare WebGL
      - name: Prepare WebGL Build
        if: matrix.targetPlatform == 'WebGL'
        run: |
          # Create index.html wrapper if needed
          if [ -f "build/WebGL/WebGL/index.html" ]; then
            echo "WebGL build prepared"
          fi

      - uses: actions/upload-artifact@v4
        with:
          name: Sample2DProject-${{ matrix.targetPlatform }}-b${{ github.run_number }}
          path: |
            build/${{ matrix.targetPlatform }}
            version-info/
      ```
