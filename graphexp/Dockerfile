FROM python:slim

MAINTAINER Johannes Wenzel <johannes.wenzel@schoenhofer.de>

ENV http_proxy $http_proxy
ENV https_proxy $https_proxy
ENV no_proxy $no_proxy
ENV PATH /usr/local/bin:$PATH


RUN apt-get update && \
    apt-get -y install git && \
    git clone https://github.com/bricaud/graphexp.git
	
WORKDIR /graphexp

EXPOSE 8183

CMD ["python3",  "-m", "http.server",  "8183"]
	


