FROM        --platform=$TARGETOS/$TARGETARCH node:18-slim

LABEL       author="IkdanYT" maintainer="ikdan@ikdan.ru"

LABEL       org.opencontainers.image.source="https://github.com/IkdanYT/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apt-get -y update
RUN         apt-get -y install git build-essential iproute2 python3
RUN			useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]
