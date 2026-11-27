FROM ubuntu:22.04

COPY --from=node:16 /usr/local/bin /usr/local/bin
COPY --from=node:16 /usr/local/lib/node_modules /usr/local/lib/node_modules

WORKDIR /usr/src/app

COPY . .

RUN npm install && \
    npm run build && \
    npm install -g serve

EXPOSE 5001

CMD ["serve", "-s", "-l", "5001", "build"]
