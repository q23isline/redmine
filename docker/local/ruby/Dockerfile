# <https://docs.docker.com/samples/rails/>
FROM ruby:2.7

RUN apt-get update -qq && apt-get install -y nodejs
WORKDIR /var/www/html
COPY Gemfile /var/www/html/Gemfile
COPY Gemfile.lock /var/www/html/Gemfile.lock
RUN bundle install

# Add a script to be executed every time the container starts.
COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]
EXPOSE 3000
