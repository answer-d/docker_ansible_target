FROM pycontribs/centos:8

RUN true && \
    dnf -y install openssh-server openssh-clients && \
    dnf -y clean all && \
    true

RUN true && \
    useradd -s /bin/bash -m ansible && \
    usermod -aG wheel ansible && \
    echo -n "ansible:ansible" | chpasswd && \
    true

RUN echo 'LANG=ja_JP.utf8' > /etc/locale.conf

CMD ["/sbin/init"]
