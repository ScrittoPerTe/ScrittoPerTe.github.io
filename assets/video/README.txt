Aggiungi qui i file video usati nella home (overlay):
- bg.mp4  (H.264/AAC, -movflags +faststart)
- bg.webm (VP9)

Consiglio i comandi ffmpeg:
ffmpeg -i input.mp4 -vf "scale=1280:-2" -c:v libx264 -preset slow -crf 23 -movflags +faststart -an assets/video/bg.mp4
ffmpeg -i input.mp4 -vf "scale=1280:-2" -c:v libvpx-vp9 -b:v 0 -crf 30 -an assets/video/bg.webm
