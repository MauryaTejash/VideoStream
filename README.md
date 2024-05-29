# Video Player

- This is a video player which is able to play a video when video is uploaded through the user from the frontend. It is totally based on FFmpeg which provide all the feature of video player.
- In FFmpeg command the video is divided into segments of defined length and during running time of video it plays it load in segments.
-  The FFmpeg Command used here is
    - ***const ffmpegCommand = `ffmpeg -i ${videoPath} -codec:v libx264 -codec:a aac -hls_time 10 -hls_playlist_type vod -hls_segment_filename "${outputPath}/segment%03d.ts" -start_number 0 ${hlsPath}***
- Multer is used to store the video and it create the segment of video file of defined length.
- **m3u8** is used which is a UTF-8 incoded file. It is plain text file used to store URL path of streaming audio or video information
- Multer middleware is used to provide the unique name to the videos.
- HLS is used to break down the video into smaller HTTP downloadble files.

  # POSTMAN
  ![h3](https://github.com/MauryaTejash/VideoStream/assets/93006244/77e21fca-8587-420e-a117-24a42a907bb0)

  # Output
  
  ![h2](https://github.com/MauryaTejash/VideoStream/assets/93006244/0278be0f-5388-4440-8def-cf52ab90463c)
