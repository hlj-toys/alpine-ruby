FROM alpine:3.2
MAINTAINER Beta CZ <hlj8080@gmail.com>

# ruby 2.2.4-p0
RUN apk --update add ca-certificates \
    ruby ruby-minitest ruby-irb \
    ruby-io-console \
    ruby-bigdecimal \
    ruby-json \
    ruby-rake \
    ruby-bundler && rm -rf /var/cache/apk/*

# Set the gem sources to ruby.taobao.org
RUN gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/

# skip installing gem documentation
RUN echo 'gem: --no-rdoc --no-ri' >> ~/.gemrc &&  rm -rf /usr/share/ri