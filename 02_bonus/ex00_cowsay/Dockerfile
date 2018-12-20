FROM debian

RUN apt-get update && apt-get install -y cowsay fortune lolcat

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat

# to build
# docker build -t ex00_cowsay .

# to run
# docker run --rm -t ex00_cowsay
