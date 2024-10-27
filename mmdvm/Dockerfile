FROM alpine:latest

RUN set -x \
	&& apk update \
	&& apk add make g++ git \
	&& git clone https://github.com/g4klx/MMDVMHost.git \
	&& cd /MMDVMHost \
	&& make \
	&& install -m755 MMDVMHost /usr/bin/MMDVMHost \
	&& rm -rf /MMDVMHost \
	&& apk del make g++ git \
	&& rm -rf /var/cache/apk/*

CMD ["/usr/bin/MMDVMHost", "/data/MMDVM.ini"]
