FROM geerlingguy/docker-centos8-ansible

RUN dnf install -y gcc openssl-devel bzip2-devel libffi-devel wget make tar \
    && cd /usr/src \
    && wget https://www.python.org/ftp/python/3.9.18/Python-3.9.18.tgz \
    && tar xzf Python-3.9.18.tgz \
    && cd Python-3.9.18 \
    && ./configure --enable-optimizations \
    && make altinstall \
    && ln -s /usr/local/bin/python3.9 /usr/bin/python3 \
    && dnf clean all

CMD ["/sbin/init"]
