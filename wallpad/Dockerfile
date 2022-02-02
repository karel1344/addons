#ARG BUILD_FROM="alpine:latest"
ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

# Copy data for add-on
COPY run.sh /
COPY js /js

#WORKDIR /share

# Install requirements for add-on

#RUN apk add --no-cache jq npm make gcc g++ python3 linux-headers udev
#RUN npm init -f
#RUN npm install mqtt
##RUN npm install serialport --build-from-source=serialport
#RUN npm install serialport --unsafe-perm --build-from-source=serialport

##RUN apk add --no-cache jq npm make gcc g++ python3 linux-headers udev

#RUN chmod a+x /run.sh
##RUN npm install

#CMD [ "/run.sh" ]


RUN apk add --no-cache jq npm make gcc g++ python3 linux-headers udev

WORKDIR /
COPY package.json /
RUN npm install

RUN chmod a+x /run.sh
CMD [ "/run.sh" ]
