FROM betacz/alpine-ruby:2.2.4
MAINTAINER Beta CZ <hlj8080@gmail.com>

# ruby 2.2.4-p0
RUN apk --update add  build-base ruby-dev && rm -rf /var/cache/apk/*

# Enable auto completion, auto indent and history
RUN echo 'require "irb/completion"' >> "$HOME/.irbrc" && \
    echo 'IRB.conf[:AUTO_INDENT] = true' >> "$HOME/.irbrc" && \
    echo 'IRB.conf[:SAVE_HISTORY] = 1000' >> "$HOME/.irbrc"
    
CMD [ "irb" ]