docker build . -t custom-nginx-docker

docker run -p 1935:1935 custom-nginx-docker


```
ffmpeg -re -i f1.mp4 -vcodec libx264 -profile:v main -preset:v medium -r 30 -g 60 -keyint_min 60 -sc_threshold 0 -b:v 2500k -maxrate 2500k -bufsize 2500k -sws_flags lanczos+accurate_rnd -acodec aac -b:a 96k -ar 48000 -ac 2 -f flv rtmp://localhost:1935/live
```