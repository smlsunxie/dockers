FROM ubuntu:14.04

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -qy build-essential libssl-dev git man curl
RUN DEBIAN_FRONTEND=noninteractive apt-get install -qy python-software-properties python g++ make
RUN DEBIAN_FRONTEND=noninteractive apt-get install -qy libsqlite3-dev

USER root
ENV HOME /root
ENV NODE_VER iojs-v1.8


RUN git clone https://github.com/creationix/nvm.git $HOME/.nvm

RUN echo '. ~/.nvm/nvm.sh' >> $HOME/.profile

RUN /bin/bash -l -c "nvm install ${NODE_VER}; nvm alias default ${NODE_VER};"

RUN /bin/bash -l -c "npm install -g grunt-cli node-pre-gyp node-gyp &&  \
    npm install -g bower && \
    npm install -g mocha"

RUN /bin/bash -l -c "npm install -g ember-cli"

RUN apt-get install -y python
