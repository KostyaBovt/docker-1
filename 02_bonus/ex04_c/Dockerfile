FROM debian

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install git -y
RUN apt-get install make -y
RUN apt-get install gcc -y

RUN git clone https://github.com/klange/nyancat.git

WORKDIR nyancat

RUN make && cd src

CMD ./src/nyancat

# to build
# docker build -t nyancat .

# to run
# docker run --rm -it nyancat