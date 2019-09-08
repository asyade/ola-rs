FROM debian:stretch

RUN echo 'deb http://deb.debian.org/debian jessie main' >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install libcppunit-dev libcppunit-1.13-0v5 uuid-dev pkg-config \
      libncurses5-dev libtool autoconf automake g++ libmicrohttpd-dev \
      libmicrohttpd10 protobuf-compiler libprotobuf-lite10 python-protobuf \
      libprotobuf-dev libprotoc-dev zlib1g-dev bison flex make libftdi-dev \
      libftdi1 libusb-1.0-0-dev liblo-dev libavahi-client-dev python-numpy -y
COPY ./ola /ola
WORKDIR /ola
RUN automake --add-missing
RUN autoreconf
RUN ./configure
ENTRYPOINT make