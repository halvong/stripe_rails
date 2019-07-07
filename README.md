Rails Stripe, Linkedin
7/7/2019, Sun

#Rails
1. docker run -i -t --rm -v ${PWD}:/usr/src/app ruby:2.6.3 bash
   gem install rails
   rails new myapp -d postgresql --skip-test --skip-bundle
   exit
2. docker build -t docker_rails .

3. Gemfile, pg75 
	gem 'pg', '~> 1.0'
    
4. docker-compose run --rm database psql -U postgres -h database
   docker-compose rm -f database
   docker-compose up -d database
   docker-compose up -d --force-recreate web
   docker-compose up -d --force-recreate database
   
5. docker volume [ls rm]
