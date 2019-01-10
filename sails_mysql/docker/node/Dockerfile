FROM node:6.16.0

VOLUME [ "/opt/app" ]
WORKDIR /opt/app

RUN chown -R node:node /opt/app

USER root
RUN cd /opt/app && npm install -g sails@0.11.2  && npm install -g node-inspect
USER node

EXPOSE 1337
EXPOSE 9229

CMD [ "node", "--inspect=0.0.0.0", "/opt/app/app.js" ]
#CMD [ "tail", "-f", "/dev/null" ]