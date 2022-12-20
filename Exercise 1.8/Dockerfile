FROM ubuntu:20.04

RUN apt-get update

RUN apt-get install -y curl

COPY hello.sh .
RUN chmod +x hello.sh

CMD ./hello.sh