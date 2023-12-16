FROM        --platform=$TARGETOS/$TARGETARCH node:16-bullseye-slim

LABEL       author="IkdanYT" maintainer="ikdan@ikdan.ru"

LABEL       org.opencontainers.image.source="https://github.com/IkdanYT/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apt-get -y update
RUN         apt-get -y install curl jo ca-certificates openssl ffmpeg git tar python3 build-essential iproute2 sqlite3
RUN			useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]
