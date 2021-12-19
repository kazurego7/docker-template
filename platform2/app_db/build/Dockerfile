FROM postgres:14-bullseye

# locale
RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.utf8

# timezone
ENV TZ="Asia/Tokyo"

# config
COPY config/postgresql.conf /etc/postgresql/postgresql.conf
COPY config/pg_hba.conf /etc/postgresql/pg_hba.conf
