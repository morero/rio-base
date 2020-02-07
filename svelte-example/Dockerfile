FROM mhart/alpine-node:11.14

# install dependencies
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci --production

###
# Only copy over the Node pieces we need
# ~> Saves 35MB
###
FROM node:alpine

WORKDIR /app
COPY --from=0 /app .
COPY . .

CMD ["/usr/local/bin/npm","run","dev"]
