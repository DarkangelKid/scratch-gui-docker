FROM node:20.17.0-alpine

ENV PORT 8601

RUN apk add --no-cache git \
    && git clone --depth=1 https://github.com/DarkangelKid/scratch-gui.git \
    && cd scratch-gui \
    && npm install \
    && npm run build

WORKDIR /scratch-gui
EXPOSE 8601
CMD ["npm","start"]