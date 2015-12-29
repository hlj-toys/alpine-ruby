FROM alpine:3.2
MAINTAINER Beta CZ <hlj8080@gmail.com>

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

# Enable auto completion, auto indent and history
RUN echo 'require "irb/completion"' >> "$HOME/.irbrc" && \
    echo 'IRB.conf[:AUTO_INDENT] = true' >> "$HOME/.irbrc" && \
    echo 'IRB.conf[:SAVE_HISTORY] = 1000' >> "$HOME/.irbrc"
    
CMD [ "irb" ]