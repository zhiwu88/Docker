FROM centos:latest
RUN yum install -y passwd  openssh-server  net-tools  vim-enhanced
RUN yum clean all
#RUN echo 'root:123456' |chpasswd
RUN echo '123456' | passwd --stdin root
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N ''
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_ecdsa_key -N ''
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_ed25519_key -N ''
EXPOSE 22
#CMD ["/usr/sbin/sshd","-D"]
ENTRYPOINT ["/usr/sbin/sshd","-D"]
