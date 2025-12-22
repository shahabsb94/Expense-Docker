#FROM node:20
FROM node:20.18.3-alpine3.21 
# create a group and user --- in Alpine model format 
RUN addgroup -S expense && adduser -S expense -G expense && \
# explicitly create a directory
    mkdir /opt/backend && \
# give full permisiion to user expense to that directory 
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
RUN npm install
ENV DB_HOST="mysql"
USER expense
CMD [ "node", "index.js" ]
