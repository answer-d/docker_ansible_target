FROM pycontribs/centos:7

RUN true && \
    yum -y install openssh-server openssh-clients && \
    yum -y clean all && \
    true

RUN true && \
    useradd -s /bin/bash -m ansible && \
    usermod -aG wheel ansible && \
    echo -n "ansible:ansible" | chpasswd && \
    true

RUN echo 'LANG=ja_JP.utf8' > /etc/locale.conf

CMD ["/sbin/init"]
