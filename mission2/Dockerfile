FROM debian:jessie
MAINTAINER valandinos@hotmail.com

RUN apt-get update \
&& apt-get install postfix dovecot-imapd dovecot-pop3d -y supervisor \
&& rm -rf /var/lib/apt/lists/*

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 25 110 143 587

CMD ["/usr/bin/supervisord", "n"]
