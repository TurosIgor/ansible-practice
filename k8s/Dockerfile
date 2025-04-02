FROM ubuntu:24.10

USER root

RUN apt update && apt install -y openssh-server

RUN mkdir -p /root/.ssh

COPY authorized_keys /root/.ssh/authorized_keys

RUN chmod 600 /root/.ssh/authorized_keys

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]