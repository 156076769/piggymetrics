FROM mongo:3
MAINTAINER Alexander Lukyanchikov <sqshq@sqshq.com>

ADD init.sh /init.sh
ADD ./dump /

RUN \
 chmod +x /init.sh && \
 apt-get update && apt-get install psmisc
# chmod +x /init.sh && \
# apt-get update && apt-get dist-upgrade -y --force-yes && \
# apt-get install psmisc -y -q && \
# apt-get autoremove -y && apt-get clean && \
# rm -rf /var/cache/* && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/init.sh"]
