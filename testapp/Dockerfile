FROM ubuntu:14.04

RUN apt-get update -q
RUN apt-get install -qy ruby
RUN gem install rubygems-update --no-ri --no-rdoc
RUN update_rubygems
RUN gem install bundler sinatra --no-ri --no-rdoc

#Add rails project to project directory
ADD ./ /app

# set WORKDIR
WORKDIR /app
#RUN bundle install

# Publish port 80
EXPOSE 80

CMD ["/usr/bin/ruby","/app/app.rb"]
