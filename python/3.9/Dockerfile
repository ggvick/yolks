FROM        --platform=$TARGETOS/$TARGETARCH python:3.9-slim

LABEL       author="ggvick" maintainer="ggvick@ggvick.tk"

RUN         apt update \
            && apt -y install python3 git gcc g++ ca-certificates dnsutils curl iproute2 ffmpeg procps python3-pip \
            && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
