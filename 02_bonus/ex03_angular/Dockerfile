FROM ubuntu

WORKDIR angular

RUN apt-get update  && apt-get install -y curl bash gnupg sudo git
RUN	curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
RUN apt-get install -y nodejs
RUN npm install -y --unsafe-perm -g @angular/cli
RUN ng new my-app

WORKDIR /angular/my-app

EXPOSE 4200

ENTRYPOINT ng serve --host 0.0.0.0

# to build
# docker build -t ex03_angular .

# to run
# docker run -ti --rm -p 4200:4200 ex03_angular