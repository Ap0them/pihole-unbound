FROM pihole/pihole:latest
RUN apt update && apt install -y unbound

COPY unbound-pihole.conf /etc/unbound/unbound.conf.d/pi-hole.conf

ENTRYPOINT ./s6-init
