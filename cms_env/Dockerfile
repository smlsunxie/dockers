FROM smlsunxie/rudy-node:latest

RUN gem install compass
RUN gem install bootstrap-sass
RUN gem install sass

RUN npm install -g grunt-cli
RUN npm install -g bower
RUN npm install -g coffee-script
RUN npm install -g gulp
RUN npm install -g mocha
RUN npm install -g strongloop


RUN git clone https://github.com/smlsunxie/mobius-cms.git

WORKDIR /mobius-cms



RUN npm i
RUN bower i --allow-root --config.interactive=false --config.directory=app/bower_components


RUN /bin/bash -c "source /home/.bashrc && gulp"
