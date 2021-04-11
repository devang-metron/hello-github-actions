FROM debian:9.5-slim

ADD QRadarAppSDK-2.0.1.zip /tmp/QRadarAppSDK-2.0.1.zip
WORKDIR /tmp

RUN unzip QRadarAppSDK-2.0.1.zip -d qradar
WORKDIR /tmp/qradar
RUN ./install.sh

WORKDIR /

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]