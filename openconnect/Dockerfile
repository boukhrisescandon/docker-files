FROM sboukhris/base-debian-jessie

COPY run.sh /run.sh
RUN chmod 0755 /run.sh
RUN mkdir -p /var/run/sshd
RUN apt-get update && \
    apt-get install -y openconnect openssh-server netcat-traditional ocproxy dnsutils telnet rdesktop  && \
    apt-get clean && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/lib/apt/lists/* 

ENTRYPOINT ["/run.sh"]
