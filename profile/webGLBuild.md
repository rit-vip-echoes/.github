# Building to WebGL
## How To
1. Ensure WebGL Build Support is installed to Unity.
  
2. [Legacy Build (pre 6.0)](https://docs.unity3d.com/2020.1/Documentation/Manual/webgl-building.html)
  
3. Select `WebGL` from build options. Switch to the `WebGL` Platform. 
<img width="1904" height="604" alt="Screenshot 2025-08-18 201828" src="https://github.com/user-attachments/assets/4edbe606-2bd4-46db-95d6-7161b9a82720" />

5. Update player settings:
   - Under `Resolution and Presentation` set Default Canvas Width to 1080 and Default Canvas Height to 720 (or use a similarly sized aspect ratio).
   - Under publishing settings, set `Compression Format` to `Disabled`.

7. Select `Build` or `Build and Run`.
   
8. Ensure the Build Path is under the `docs` folder within the repository if the build is intended to be pushed.
   
9. Wait.......
    
10. If `Build and Run` was selected, the game should pop up to be tested when the build is finished.
    
11. Otherwise, [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) from VS-Code can be used to run the index.html file on a local server to test the build.
   <img width="1531" height="997" alt="image" src="https://github.com/user-attachments/assets/13173774-60c3-4b6a-a346-826ff8ed2a65" />

## Common Issues
WebGL can have tons of problems building/running successfully.
If a problem comes up and is not listed, add it below.

| Problem | Solutions |
|---------|-----------|
| Compression format could cause build to crash | - Ensure Compression Format is disabled in build settings.<br>- Double-check platform-specific texture compression overrides.<br> |
| Textures look bad at a distance | - Adjust anisotropic filtering settings for the texture/material.<br> |
| Web Browser runs out of memory | - Reduce asset quality (audio, textures, etc) to reduce size of textures.<br> - Remove uneeded assets from scenes. <br> - Adjust build settings to increase allowed memory usage. |
| Build size is over 100mb  | - [Reduce File Size](https://docs.unity3d.com/6000.0/Documentation/Manual/ReducingFilesize.html). A build profile can help to determine where issues lie. <br>- Reduce texture resoltution. <br> - Increase shader stripping/remove excess shaders. <br> Compress audio to reduce its size (in Unity), often audio doesn't sound much different at a lower quality]
| FPS is low but in WebGL only | WebGL doesn't support standard batching practice to reduce draw calls.<br> - Disable `Static` batching.<br> - If using terrain, ensure batching of trees/details is turned off. |


