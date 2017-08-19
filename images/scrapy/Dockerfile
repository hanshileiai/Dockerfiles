FROM ubuntu:14.04
MAINTAINER Ray <shilei@magicmoma.com>

COPY sources.list /etc/apt/
# add scrapy sources
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 627220E7 && \
        echo 'deb http://archive.scrapy.org/ubuntu scrapy main' | sudo tee /etc/apt/sources.list.d/scrapy.list && \
        apt-get update --fix-missing

# install python and scrapy
RUN apt-get install -y python python-pip python-dev build-essential libxml2-dev libxslt-dev libffi-dev libssl-dev libmysqlclient-dev && \
        pip install --upgrade pip && pip install --upgrade virtualenv && \ 
        pip install lxml && pip install pyopenssl && pip install Scrapy && pip install --upgrade scrapy && \
        pip install --upgrade twisted && \
        pip install MySQL-python && \
        pip install service-identity && \
        pip install pyasn1 --upgrade && \
        pip install unidecode && \
        pip install tldextract && \
        pip install python-dateutil