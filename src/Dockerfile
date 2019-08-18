FROM lchaia/xmrig

USER root

RUN apk --no-cache add nodejs \
    wget \
    && wget https://raw.githubusercontent.com/MoneroOcean/meta-miner/master/mm.js -P /xmrig \
    && chmod +x /xmrig/mm.js \
    && apk --no-cache del wget

USER miner

WORKDIR /xmrig
ENTRYPOINT [ "./mm.js" ]
