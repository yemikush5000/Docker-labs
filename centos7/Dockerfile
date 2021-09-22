FROM centos

RUN yum install -y openssh-server 

RUN useradd remote_user && \
    echo "remote_user:xxxxxxxxxx" | chpasswd && \
    mkdir /home/remote_user/.ssh && \
    chown 0700 /home/remote_user/.ssh

COPY remote-key.pub /home/remote_user/.ssh/authorized_keys

RUN chown -R remote_user:remote_user /home/remote_user/.ssh/ && \
    chmod 600 /home/remote_user/.ssh/authorized_keys

RUN ssh-keygen -A

RUN yum install -y unzip

RUN yum install -y mysql

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

RUN unzip awscliv2.zip

RUN ./aws/install

CMD /usr/sbin/sshd -D 
