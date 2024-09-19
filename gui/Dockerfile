FROM node:20.17.0-alpine

ENV PORT 80

RUN apk add --no-cache git \
    && git clone --depth=1 https://github.com/scratchfoundation/scratch-gui \
    && cd scratch-gui \
    && npm install --no-optional \
    && npm fund && npm audit fix \
    && npm run build

WORKDIR /scratch-www
EXPOSE 80
CMD ["npm","start"]