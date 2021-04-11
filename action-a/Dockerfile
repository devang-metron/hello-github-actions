FROM python:3.6

ADD QRadarAppSDK-2.0.1.zip /tmp/QRadarAppSDK-2.0.1.zip
WORKDIR /tmp

RUN apt update && apt install unzip && unzip QRadarAppSDK-2.0.1.zip -d qradar
WORKDIR /tmp/qradar
RUN ./install.sh

WORKDIR /

RUN rm -rf /tmp/qradar /tmp/QRadarAppSDK-2.0.1.zip

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]