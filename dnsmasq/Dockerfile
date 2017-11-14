FROM alpine:edge

RUN apk --no-cache add dnsmasq gettext \
  && mkdir -p /srv/tftp \
  && wget http://boot.ipxe.org/undionly.kpxe -O /srv/tftp/undionly.kpxe
ADD ./dnsmasq.conf.template /etc/dnsmasq.conf.template

EXPOSE 53 53/udp

CMD ["dnsmasq", "-k"]
