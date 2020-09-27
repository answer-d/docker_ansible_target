FROM pycontribs/centos:7
RUN true && \
    yum -y install openssh-server openssh-clients && \
    yum -y clean all && \
    true
RUN echo -n "root:P@ssw0rd" | chpasswd
CMD ["/sbin/init"]
