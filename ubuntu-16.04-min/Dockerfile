FROM ubuntu:16.04
MAINTAINER Valter Vasic <valter.vasic@gmail.com>
MAINTAINER Denis Salopek <denis.sale@gmail.com>

ENV HOME=/root VTYSH_PAGER=more TERM=vt100 PAGER=less
ADD common /build
RUN true
COPY ubuntu-16.04-min/* /build/

RUN /build/prepare.sh && \
 /build/system_services.sh && \
 /build/utilities.sh && \
 /build/cleanup.sh

CMD ["/bin/bash"]
