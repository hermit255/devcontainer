FROM ubuntu:24.04
RUN apt-get update && apt-get install -y curl git unzip

RUN apt-get install -y php
COPY --from=composer /usr/bin/composer /usr/bin/composer
ENV COMPOSER_ALLOW_SUPERUSER=1
RUN composer global require phpstan/phpstan

RUN apt-get install -y nodejs
RUN apt-get install -y golang-go
# would not work on M4　chip
RUN apt-get install -y plantuml
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install