FROM nginx:1.13.9

LABEL maintainer="johannes.wenzel@schoenhofer.de"

ENV http_proxy $http_proxy
ENV https_proxy $https_proxy
ENV no_proxy $no_proxy
ENV PATH /usr/local/bin:$PATH


RUN apt-get update && \
    apt-get -y install wget unzip && \
    cd /tmp && \
    wget  https://github.com/bricaud/graphexp/archive/master.zip && \
    unzip master.zip && \
    sed 's/const HOST = "localhost"/const HOST = self.location.hostname/' graphexp-master/scripts/graphConf.js > graphConf.js && \
    mv graphConf.js graphexp-master/scripts && \
    mv graphexp-master/*  /usr/share/nginx/html && \
    rm -R /tmp/graphexp-master && \
    apt-get remove -y wget && \
    apt-get remove -y unzip && \
    rm -R /var/lib/apt/lists/*



	
WORKDIR  /usr/share/nginx/html

	


