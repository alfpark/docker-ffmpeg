# Minimalist FFmpeg Docker image
This is an FFmpeg Docker image based on Alpine Linux with a small footprint.

Compressed size:

Output of `docker run --rm -it alfpark/ffmpeg -buildconf`:

```
ffmpeg version 3.1.3 Copyright (c) 2000-2016 the FFmpeg developers
  built with gcc 5.3.0 (Alpine 5.3.0)
  configuration: --disable-debug --enable-version3 --enable-small --enable-gpl --enable-nonfree --enable-postproc --enable-openssl --enable-avresample --enable-libfreetype --enable-libmp3lame --enable-libx264 --enable-libx265 --enable-libopus --enable-libass --enable-libwebp --enable-librtmp --enable-libtheora --enable-libvorbis --enable-libvpx
  libavutil      55. 28.100 / 55. 28.100
  libavcodec     57. 48.101 / 57. 48.101
  libavformat    57. 41.100 / 57. 41.100
  libavdevice    57.  0.101 / 57.  0.101
  libavfilter     6. 47.100 /  6. 47.100
  libavresample   3.  0.  0 /  3.  0.  0
  libswscale      4.  1.100 /  4.  1.100
  libswresample   2.  1.100 /  2.  1.100
  libpostproc    54.  0.100 / 54.  0.100

  configuration:
    --disable-debug
    --enable-version3
    --enable-small
    --enable-gpl
    --enable-nonfree
    --enable-postproc
    --enable-openssl
    --enable-avresample
    --enable-libfreetype
    --enable-libmp3lame
    --enable-libx264
    --enable-libx265
    --enable-libopus
    --enable-libass
    --enable-libwebp
    --enable-librtmp
    --enable-libtheora
    --enable-libvorbis
    --enable-libvpx
```

