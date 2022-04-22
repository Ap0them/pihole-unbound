FROM pihole/pihole:latest
RUN apt update && apt install -y unbound

COPY unbound-pihole.conf /etc/unbound/unbound.conf.d/pi-hole.conf
COPY crontabs-root /var/spool/cron/crontabs/root
COPY unbound.conf /etc/unbound/unbound.conf
COPY timesyncd.conf /etc/systemd/timesyncd.conf

ENTRYPOINT ./s6-init
