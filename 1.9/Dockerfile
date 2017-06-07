FROM xqdocker/ubuntu-for-ruby:1.1.1
MAINTAINER Xiaoqi Cao <thomascxq@gmail.com>

#Install Ruby 1.9

RUN apt-get update \
    && apt-get -y install software-properties-common \
    && add-apt-repository -y ppa:brightbox/ruby-ng \
    && apt-get update \
    && apt-get -y install \
        ruby1.9.1 \
        ruby1.9.1-dev \
    && rm -rf /var/lib/apt/lists/*

RUN echo 'gem: --no-document' > /usr/local/etc/gemrc \
    && gem update \
    && gem install bundler
