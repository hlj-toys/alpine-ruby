FROM gliderlabs/alpine:3.2
MAINTAINER Beta CZ <hlj8080@gmail.com>

# ruby 2.2.4-p0
RUN apk-install ca-certificates ruby=2.2.4-r0 ruby-bundler

# Set the gem sources to ruby.taobao.org
RUN gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/

# skip installing gem documentation
RUN echo 'gem: --no-rdoc --no-ri' >> ~/.gemrc &&  rm -rf /usr/share/ri