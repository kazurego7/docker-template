FROM tomcat:9-jdk17-openjdk-bullseye

# locale
RUN apt-get update -y && apt-get install -y \
    locales \
    && rm -rf /var/lib/apt/lists/*
RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.utf8

# timezone
ENV TZ="Asia/Tokyo"

# config
COPY config/logging.properties /usr/local/tomcat/conf/logging.properties