FROM node:20.13.0-alpine3.18
EXPOSE 8080
RUN adduser -S roboshop $$ adduser -S roboshop -G roboshop
WORKDIR /opt/server
ENV MONGO=true
RUN chown roboshop:roboshop /opt/server/
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]