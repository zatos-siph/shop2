FROM docker.io/node:19-alpine3.16

ENV HOST=0.0.0.0
ENV PORT=3000

WORKDIR /app

RUN addgroup --system api && \
    adduser --system -G api api

COPY dist/apps/api/ .
RUN yarn install && \
    chown -R api:api .

CMD [ "node", "main.js" ]
