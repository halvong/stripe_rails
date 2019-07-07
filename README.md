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
6. docker-compose exec web rails g scaffold Product name description:text secret:text
6b. gem 'devise', '~> 4.2'
    gem 'bcrypt'
    gem 'bootstrap-sass', '~> 3.3', '>= 3.3.7'
7. docker-compose exec web rails db:migrate
