FROM alpine 
MAINTAINER Howard Young <howard@zadarastorage.com>

RUN apk update
RUN apk add openssh 

RUN mkdir /var/run/sshd
RUN ssh-keygen -A -N ''

RUN echo 'root:zadara' | chpasswd

#RUN sed -i 's/PermitRootLogin without-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN echo 'UseDNS no' >> /etc/ssh/sshd_config
RUN echo 'PermitRootLogin yes' >> /etc/ssh/sshd_config

ADD start.sh /start.sh

EXPOSE 22
CMD /start.sh
