FROM node:14

RUN git clone https://github.com/TerriaJS/TerriaMap.git

WORKDIR /TerriaMap

ENV NODE_OPTIONS=--max_old_space_size=4096

RUN rm -rf package-lock.json yarn.lock node_modules
RUN yarn install && yarn gulp

CMD [ "node", "./node_modules/terriajs-server/lib/app.js", "--config-file", "serverconfig.json" ]
