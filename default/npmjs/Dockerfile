FROM node:0.12.8

RUN npm install -g npm-lazy-mirror
RUN npm install -g npm-registry-client
RUN mkdir /data

EXPOSE 3000

CMD npm-lazy-mirror -p 3000 -a npmjs.default.kube.cluster.local -b 0.0.0.0 --cache_dir /data
