# Dockerfile for building jekyll based documentation
FROM alpine:latest
MAINTAINER Derek Feichtinger (derek.feichtinger@psi.ch)

CMD ["/bin/sh"]

RUN apk --no-cache add libatomic readline readline-dev libxml2 libxml2-dev \
    ncurses-terminfo-base ncurses-terminfo \
    libxslt libxslt-dev zlib-dev zlib \
    ruby ruby-dev yaml yaml-dev \
    libffi-dev build-base git nodejs; \
    gem install bundler --no-document
    
RUN echo 'source "https://rubygems.org"' > Gemfile; \
    echo 'gem "jekyll", "~> 3.8.5"' >> Gemfile; \
    echo 'gem "jekyll-seo-tag", "~> 2.0"' >> Gemfile; \
    echo 'gem "rake", "~> 12.3.1"' >> Gemfile; \
    echo 'gem "json", "~> 2.2"' >> Gemfile; \
    echo 'gem "bigdecimal", "~> 1.4"'  >> Gemfile; \
    bundler install




