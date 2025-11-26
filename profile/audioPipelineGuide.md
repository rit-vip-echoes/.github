# **Audio Asset Pipeline**

## Created by: Max White

# **Key Points:**

Before you render out a piece of audio, try your best to make sure that:

* **LUFS \= –23 (±0.5) LUFS**: Try to keep the average volume of the piece at a reasonable level that will not cause damage to, or annoy, the listener.   
* **Sample Rate \= 48kHz and Bit Depth \= 24-bit**: Aim for a balance between good quality and (relatively) small file size.   
* **File Type \= MP4, MP3, or AAC**: Try to render to a MP4 or AAC file so that Unity can process it (MP3 is also okay).

# **LUFS (Loudness Units relative to Full Scale) and**  **LKFS (Loudness, K-weighted, relative to Full Scale)**

Recommended Max Integrated LUFS \= –23 (±0.5) LUFS

Please note that LUFS and LKFS are the same thing nowadays (though they used to refer to slightly different measurements in the past) \[1\]. I will refer to both as LUFS. 

LUFS are “a standard way of measuring audio that blends the perceived loudness from human hearing and the true intensity of an audio signal together,” \[2\].  Basically, it is the measure of the average volume for a sound/song that also takes into account how humans perceive the loudness of different frequencies. RMS is another measurement of average loudness but does not take into account how humans perceive loudness \[3\].

Across standards in film, TV, gaming, and streaming, LUFS typically range from \-14 to \-24 LUFS. Although there is no standard that I could find for sound in WebGL, the European TV broadcast standard of –23 (±0.5) LUFS should suffice \[4\]. 

Sometimes you do want a sound/song to be very loud so that it overpowers other sounds/songs. In this case, you could theoretically ignore the LUFS of the sound/song but this is not recommended. In the case that the player is already playing the game at a high volume, an even louder noise could cause damage to the player’s speaker(s) and/or ears in the worst case. 

Basically, keep your sounds/songs at relatively the same volume level whenever possible so that the player won’t get hurt or annoyed. 

\[1\] More information about the history of the difference between LUFS and LKFS:   
[What's the difference between LKFS and LUFS? by Garry Taylor](https://gameaudionoise.blogspot.com/2012/02/whats-difference-between-lkfs-and-lufs.html)	

\[2\] More information about LUFS:  
[What are LUFS: The Complete Beginner's Guide by Kate Brunotts](https://emastered.com/blog/what-are-lufs)

\[3\] More information about LUFS and its comparison to RMS:   
[LUFS vs Peak vs RMS – what are they, what’s the difference and when you should use them by Sam McNiece](https://mixdownmag.com.au/features/peak-vs-rms-vs-lufs-what-are-they-whats-the-difference-and-when-you-should-use-them/)

\[4\] More information on LUFS levels for different standards and streaming services:   
[Loudness Standards – Full Comparison Table (music, film, podcast) by Julijan Nikolic](https://youlean.co/loudness-standards-full-comparison-table/) 

# **Sample Rate and Bit Depth**

Recommended Sample Rate \= 48kHz

Recommended Bit Depth \= 24-bit 

Sample rate can be thought of as a sort of “quality of sound”. Generally, the higher the sample rate, the higher the sound quality and vice versa. At a technical level, sample rate is the “number of audio samples in waveform per second,” \[5\]. Note that the higher the sample rate, the larger the file size. Much like other assets, quality and file size are negatively correlated. 

Bit depth is the amount of data that can be captured by a single sample at a given instance. Generally, “more bits \= more resolution and dynamic range,” \[6\]. Note that the higher the bit depth, the larger the file size. Again, quality and file size are negatively correlated.

I recommend “a sample rate of 48kHz at 24-bit depth \[which\] provides the best combination of audio quality and performance,” \[6\]. If your Digital Audio Interface (DAW) cannot render at that high of a rate, then 44.1kHz is good too. If your DAW cannot render at that high of a bit depth, 16-bit is good too. 

When importing an audio file into Unity, Unity will automatically preserve the original sample rate of the file \[7\]; This is what we want as although downsampling can reduce file size, it will reduce the quality of the audio file and can leave “warbly” sound artifacts. If this is your intended effect, I recommend changing the sample rate when exporting or using downsampling effects/plugins in your DAW so that you have more control over the downsampling effect. 

\[5\] More information about sample rate:   
[What is Sample Rate in Audio? Its Types and Impact on Sound by Ahsen Jawed](https://www.hollyland.com/blog/tips/what-is-sample-rate-in-audio)

\[6\] More information on sample rate and bit depth for game audio:  
[What sample rate should I use for gaming? by By James Dorn](https://expertbeacon.com/what-sample-rate-should-i-use-for-gaming/)

\[7\] Article by Made Indrayana on sample rates in Unity:  
[Sample Rate \- What Audio Resolution Has to Do with Your Game by Made Indrayana](https://medium.com/@made-indrayana/sample-rate-what-audio-resolution-has-to-do-with-your-game-d360025c0cc6)	

# **File Type**

Recommended Audio File Types \= MP4, MP3, or AAC

The AAC format has multiple filename extension names so AAC files will have any of the following file extensions: .3gp, .aac, .adif, .adts, .m4a, .m4b, .m4p, .m4r, .mp4 \[8\]. The MP4 format will always have the .mp4 file extension. 

AAC encoded audio files are typically packaged in an MP4 container \[9\] so they can be considered the same format. From here on out, I will refer to both file types as MP4. 

The format of all audio assets in Unity when baked for WebGL is MP4. Technically, audio file types such as MP3 or WAV still work; However, when you build to WebGL, Unity will bake these audio files into MP4 \[10\]. So MP3, WAV, MP4, and AAC will all work but we can take advantage of the (generally) higher sound quality of MP4 and just render audio files in MP4.

\[8\]Wikipedia article that explains specific of the AAC file type:  
[Wikipedia \- Advanced Audio Coding](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)		

\[9\] Explanation by Norvan Martin of AAC and MP4 file formats:  
[AAC vs. MP4: A Comparison by Norvan Martin](https://boomspeaker.com/aac-vs-mp4/)	

\[10\] Unity forum discussion on Audio file types (and sizes):   
[Unity Discussions \- Music file size in WebGL](https://discussions.unity.com/t/music-file-size-in-webgl/735649)	

Unity documentation on Audio for WebGL:   
[Unity Documentation \- Audio in WebGL](https://docs.unity3d.com/2022.3/Documentation/Manual/webgl-audio.html)
