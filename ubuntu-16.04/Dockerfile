FROM imunes/template:ubuntu-16.04-min
MAINTAINER Valter Vasic <valter.vasic@gmail.com>
MAINTAINER Denis Salopek <denis.sale@gmail.com>

ENV HOME=/root VTYSH_PAGER=more TERM=vt100 PAGER=less
ADD common /build
RUN true
COPY ubuntu-16.04/* /build/

RUN /build/prepare.sh && \
 /build/extras.sh && \
 /build/cleanup.sh

CMD ["/bin/bash"]
