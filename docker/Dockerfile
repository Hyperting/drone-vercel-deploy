FROM node:lts-alpine
LABEL org.opencontainers.image.source https://github.com/Hyperting/drone-vercel-deploy
LABEL org.opencontainers.image.authors="Hyperting<hello@hyperting.com>"

LABEL description="A Drone plugin deploy applications to vercel"

RUN apk -Uuv add bash curl ca-certificates jq

RUN npm i --location=global vercel

ADD run.sh /bin/
RUN chmod +x /bin/run.sh

USER root

CMD ["/bin/run.sh"]
