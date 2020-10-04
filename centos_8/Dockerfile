FROM pycontribs/centos:8

RUN true && \
    dnf -y update && \
    dnf -y install glibc-locale-source && \
    dnf -y install openssh-server openssh-clients && \
    dnf -y clean all && \
    true

RUN true && \
    useradd -s /bin/bash -m ansible && \
    usermod -aG wheel ansible && \
    echo -n "ansible:ansible" | chpasswd && \
    true

RUN true && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8 && \
    ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    true

ENV LANG="ja_JP.UTF-8" \
    LANGUAGE="ja_JP:ja" \
    LC_ALL="ja_JP.UTF-8" \
    TZ="Asia/Tokyo"

RUN true && \
    echo "ansible ALL=(ALL) NOPASSWD: ALL" | EDITOR='tee -a' visudo && \
    true

CMD ["/sbin/init"]
