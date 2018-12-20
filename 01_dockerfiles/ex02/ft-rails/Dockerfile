FROM ruby
RUN apt-get update -y && \
	apt-get install -y nodejs sqlite3 build-essential libpq-dev

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000

ONBUILD RUN bundle install && \
			rake db:migrate && \
			rake db:seed


# to build
# docker build -t ft-rails:on-build .
