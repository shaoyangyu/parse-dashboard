FROM node:8-slim
ENV NPM_CONFIG_LOGLEVEL error
WORKDIR /src
ADD . /src
RUN cd /src \
 && npm install \
 && npm run build \
 && npm cache verify \
 && rm -rf ~/.npm \
 && rm -rf /var/lib/apt/lists/*
CMD npm run dashboard
