# Technical Requirements
1. The game build as a whole should not exceed 100 megabytes in order to keep our total deployment size to Vercel low.
   - This is also in line with [itch.io](http://itch.io)’s [upload limit](https://itch.io/docs/creators/html5#zip-file-requirements) since we need to be able to upload to itch.io to be able to submit to games publications such as the [Game Poems magazine](https://www.gamepoems.com/).
2. Textures should remain small, at max 2048 x 2048.
   - Textures should be powers of 2 in size as to make division easier for the GPU.
   - We are already using a medium not known for its fastest computation, so let’s not make it worse.
   - Try to make the game build as small as possible without sacrificing much quality.
3. Remember that not all players will have a GPU and may be running in a web browser on minimal hardware.
   - We avoid shaders & other GPU-intensive operations as much as possible.
4. The game aspect ratio MUST be 1280x720.
   - All games deployed to [echoes-vip](https://www.echoes-vip.org/) will be displayed at this ratio/size regardless of how they were built!

# Building
1. Ensure WebGL Build Support is installed to Unity.
  
2. Use [this custom minimal template](https://github.com/seleb/Better-Minimal-WebGL-Template)
  
3. Select `WebGL` from build options. Switch to the `WebGL` Platform. 
<img width="1904" height="604" alt="Screenshot 2025-08-18 201828" src="https://github.com/user-attachments/assets/4edbe606-2bd4-46db-95d6-7161b9a82720" />

4. Update `Player Settings`:
   - Set the `Company Name` to: "echoes VIP @ RIT"
   - Set the `Product Name` to the game title
   - Under `Resolution and Presentation`:
     - Set Default Canvas Width to 1280 and Default Canvas Height to 720
   - Under publishing settings, set `Compression Format` to `Disabled`.

5. Select `Build` or `Build and Run`.
   
6. Ensure the Build Path is under the `docs` folder within the repository if the build is intended to be pushed.
   
7. Wait.......
    
8. If `Build and Run` was selected, the game should pop up to be tested when the build is finished.
    
9. Otherwise, [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) from VS-Code can be used to run the index.html file on a local server to test the build.
   <img width="1531" height="997" alt="image" src="https://github.com/user-attachments/assets/13173774-60c3-4b6a-a346-826ff8ed2a65" />

# Common Issues
WebGL can have tons of problems building/running successfully.
If a problem comes up and is not listed, add it below.

| Problem | Solutions |
|---------|-----------|
| Compression format could cause build to crash | - Ensure Compression Format is disabled in build settings.<br>- Double-check platform-specific texture compression overrides.<br> |
| Textures look bad at a distance | - Adjust anisotropic filtering settings for the texture/material.<br> |
| Web Browser runs out of memory | - Reduce asset quality (audio, textures, etc) to reduce size of textures.<br> - Remove uneeded assets from scenes. <br> - Adjust build settings to increase allowed memory usage. |
| Build size is over 100mb  | - [Reduce File Size](https://docs.unity3d.com/6000.0/Documentation/Manual/ReducingFilesize.html). A build profile can help to determine where issues lie. <br>- Reduce texture resoltution (Try first with textures that require less detail (AO, Roughness, Metallic) and try to avoid textures that provide a lot of detail (Albedo, Normal)). <br> - Increase shader stripping/remove excess shaders. <br> Compress audio to reduce its size (in Unity), often audio doesn't sound much different at a lower quality]
| FPS is low but in WebGL only | WebGL doesn't support standard batching practice to reduce draw calls.<br> - Disable `Static` batching.<br> - If using terrain, ensure batching of trees/details is turned off. |
| VFXGraph Compatibility | - WebGL builds do not support Compute Shaders, so it is impossible to utilize VFX Graph, use Particle System instead, which is CPU based. |
| Shader exceeds 16 sampler texture limit | - One of your shaders is trying to sample more than the 16 limit textures, try to simplify the number of textures used or combine multiple textures together in separate channel if not every channel is needed. |
| The build was seemingly working fine, but when it gets deployed on GitHub Pages, a scary pop-up from the browser appears with a weirdly garbled-looking error message | - Hard reload the page to force the web browser to ignore the cache (ctrl-shift-R on Chrome and Firefox, option-cmd-E on Safari, ctrl-f5 on IE and Opera). Your build is probably fine, your browser just thinks it isn't because it's trying to use cached data that isn't actually there in your build anymore. May be Chrome-specific; not totally sure. |
