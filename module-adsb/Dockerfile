FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install build-essential wget pkg-config unzip -y 
RUN apt-get install librtlsdr-dev -y
RUN wget https://github.com/antirez/dump1090/archive/refs/heads/master.zip
RUN unzip master.zip
RUN cd dump1090-master && make
WORKDIR dump1090-master/
# Run it 
CMD ["./dump1090", "--net", "--interactive"]
