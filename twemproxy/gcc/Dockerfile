FROM gcc
COPY ./nutcracker-0.4.1 /usr/src/myapp
WORKDIR /usr/local/sbin/twemproxy
RUN cd /usr/src/myapp && ./configure --prefix=/usr/local/sbin/twemproxy && make && make install