# Minimalist FFmpeg Docker image
This is an FFmpeg Docker image based on Alpine Linux with a small footprint.

## Image Download Sizes
* latest (3.2.1): [![](https://images.microbadger.com/badges/image/alfpark/ffmpeg.svg)](http://microbadger.com/images/alfpark/ffmpeg)
* 3.2.1-nvenc: [![](https://images.microbadger.com/badges/image/alfpark/ffmpeg:3.1.3-nvenc.svg)](http://microbadger.com/images/alfpark/ffmpeg:3.2.1-nvenc)

## Features
### latest (3.2.1)
Output of `docker run --rm -it alfpark/ffmpeg -buildconf`:
```
ffmpeg version 3.2.1 Copyright (c) 2000-2016 the FFmpeg developers
  built with gcc 5.3.0 (Alpine 5.3.0)
  configuration: --disable-debug --enable-version3 --enable-small --enable-gpl --enable-nonfree --enable-postproc --enable-openssl --enable-avresample --enable-libfreetype --enable-libmp3lame --enable-libx264 --enable-libx265 --enable-libopus --enable-libass --enable-libwebp --enable-librtmp --enable-libtheora --enable-libvorbis --enable-libvpx --enable-libxvid
  libavutil      55. 34.100 / 55. 34.100
  libavcodec     57. 64.101 / 57. 64.101
  libavformat    57. 56.100 / 57. 56.100
  libavdevice    57.  1.100 / 57.  1.100
  libavfilter     6. 65.100 /  6. 65.100
  libavresample   3.  1.  0 /  3.  1.  0
  libswscale      4.  2.100 /  4.  2.100
  libswresample   2.  3.100 /  2.  3.100
  libpostproc    54.  1.100 / 54.  1.100

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
    --enable-libxvid
```

### 3.2.1-nvenc
Output of `nvidia-docker run --rm -it alfpark/ffmpeg:3.1.3-nvenc -buildconf`:
```
ffmpeg version 3.2.1 Copyright (c) 2000-2016 the FFmpeg developers
  built with gcc 4.8 (Ubuntu 4.8.4-2ubuntu1~14.04.3)
  configuration: --disable-debug --enable-version3 --enable-small --enable-gpl --enable-nonfree --enable-postproc --enable-nvenc --enable-openssl --enable-avresample --enable-libfreetype --enable-libmp3lame --enable-libx264 --enable-libx265 --enable-libopus --enable-libass --enable-libwebp --enable-librtmp --enable-libtheora --enable-libvorbis --enable-libvpx --enable-libxvid
  libavutil      55. 34.100 / 55. 34.100
  libavcodec     57. 64.101 / 57. 64.101
  libavformat    57. 56.100 / 57. 56.100
  libavdevice    57.  1.100 / 57.  1.100
  libavfilter     6. 65.100 /  6. 65.100
  libavresample   3.  1.  0 /  3.  1.  0
  libswscale      4.  2.100 /  4.  2.100
  libswresample   2.  3.100 /  2.  3.100
  libpostproc    54.  1.100 / 54.  1.100

  configuration:
    --disable-debug
    --enable-version3
    --enable-small
    --enable-gpl
    --enable-nonfree
    --enable-postproc
    --enable-nvenc
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
    --enable-libxvid
```

