FROM ruby:2.1.7

RUN gem install gemirro
RUN mkdir /data

WORKDIR /data

RUN gemirro init

ADD ./config.rb /data/config.rb

RUN gemirro update

EXPOSE 2000

CMD gemirro server --start && tail -f /data/logs/access.log
