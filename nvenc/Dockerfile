# Dockerfile for FFmpeg-GPU for use with Batch Shipyard on Azure Batch

FROM nvidia/cuda:7.5-devel
MAINTAINER Fred Park <https://github.com/Azure/batch-shipyard>

# add nvidia video codec sdk
ADD nvidia_video_sdk_6.0.1.tar.gz /tmp/
# install base
RUN apt-get update \
    && apt-get install -y --no-install-recommends software-properties-common \
    && add-apt-repository ppa:mc3man/trusty-media \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
	build-essential nasm ca-certificates curl \
        libssl-dev zlib1g-dev yasm libmp3lame-dev libfreetype6 libopus-dev \
        librtmp-dev libx264-dev libx265-dev libxvidcore-dev libass-dev libwebp-dev \
        libvorbis-dev libogg-dev libtheora-dev libvpx-dev \
    && cp -r /tmp/nvidia_video_sdk_6.0.1/Samples/common/inc/* /usr/local/include/ \
    && ln -sf /usr/local/nvidia/lib64/libnvidia-encode.so.1 /usr/lib/x86_64-linux-gnu/libnvidia-encode.so \
    # build and install ffmpeg
    && FFMPEG_VER=3.1.3 \
    export CPPFLAGS=-I/tmp/nvidia_video_Sdk_6.0.1/Samples/common/inc \
    && curl -s http://ffmpeg.org/releases/ffmpeg-${FFMPEG_VER}.tar.gz | tar zxvf - -C . \
    && cd ffmpeg-${FFMPEG_VER} \
    && ./configure \
        --disable-debug --enable-version3 --enable-small --enable-gpl \
        --enable-nonfree --enable-postproc --enable-nvenc \
        --enable-openssl --enable-avresample --enable-libfreetype \
        --enable-libmp3lame --enable-libx264 --enable-libx265 \
        --enable-libopus --enable-libass --enable-libwebp --enable-librtmp \
        --enable-libtheora --enable-libvorbis --enable-libvpx \
        --enable-libxvid \
    && make -j"$(nproc)" install \
    && cd .. \
    && rm -rf ffmpeg-${FFMPEG_VER} \
    # cleanup
    && apt-get remove --purge -y nasm curl \
    && apt-get autoremove -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /tmp/nvidia_video_sdk_6.0.1

ENTRYPOINT ["ffmpeg"]
