FROM debian

ENV TS3SERVER_LICENSE=accept
EXPOSE 9987/udp 10011 30033

RUN apt-get update -y && \
	apt-get install curl -y && \
	apt-get install bzip2 -y && \
	curl -O http://dl.4players.de/ts/releases/3.5.0/teamspeak3-server_linux_amd64-3.5.0.tar.bz2 && \
	bzip2 -d teamspeak3-server_linux_amd64-3.5.0.tar.bz2 && \
	tar -xf teamspeak3-server_linux_amd64-3.5.0.tar

ENTRYPOINT sh ./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

# to build
# docker build -t ex01 .

# to run
# docker run --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
