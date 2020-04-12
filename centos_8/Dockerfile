FROM pycontribs/centos:8
RUN true && \
    dnf -y install openssh-server openssh-clients && \
    dnf -y clean all && \
    true
RUN echo -n "root:P@ssw0rd" | chpasswd
CMD ["/sbin/init"]
