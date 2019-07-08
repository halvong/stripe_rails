Rails Stripe, Linkedin
7/7/2019, Sun

chp 3.1
Signing up for Stripe

#user
1. halvong@yahoo.com:123456

#urls
http://localhost:3000/products/new

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
8. docker-compose exec web rails g devise:install -- 2.2 
   docker-compose exec web rails g devise:views   -- 2.2 
9. docker-compose exec web rails g devise User stripe_id stripe_subscription_id card_brand card_last4 card_exp_month card_exp_year expires_at:datetime 
   docker-compose exec web rails db:migrate
10. getbootstrap.com


---
Version Gemfile
Fetching rake 12.3.2
Installing rake 12.3.2
Fetching concurrent-ruby 1.1.5
Installing concurrent-ruby 1.1.5
Fetching i18n 1.6.0
Installing i18n 1.6.0
Fetching minitest 5.11.3
Installing minitest 5.11.3
Fetching thread_safe 0.3.6
Installing thread_safe 0.3.6
Fetching tzinfo 1.2.5
Installing tzinfo 1.2.5
Fetching activesupport 5.2.3
Installing activesupport 5.2.3
Fetching builder 3.2.3
Installing builder 3.2.3
Fetching erubi 1.8.0
Installing erubi 1.8.0
Fetching mini_portile2 2.4.0
Installing mini_portile2 2.4.0
Fetching nokogiri 1.10.3
Installing nokogiri 1.10.3 with native extensions
Fetching rails-dom-testing 2.0.3
Installing rails-dom-testing 2.0.3
Fetching crass 1.0.4
Installing crass 1.0.4
Fetching loofah 2.2.3
Installing loofah 2.2.3
Fetching rails-html-sanitizer 1.0.4
Installing rails-html-sanitizer 1.0.4
Fetching actionview 5.2.3
Installing actionview 5.2.3
Fetching rack 2.0.7
Installing rack 2.0.7
Fetching rack-test 1.1.0
Installing rack-test 1.1.0
Fetching actionpack 5.2.3
Installing actionpack 5.2.3
Fetching nio4r 2.3.1
Installing nio4r 2.3.1 with native extensions
Fetching websocket-extensions 0.1.4
Installing websocket-extensions 0.1.4
Fetching websocket-driver 0.7.1
Installing websocket-driver 0.7.1 with native extensions
Fetching actioncable 5.2.3
Installing actioncable 5.2.3
Fetching globalid 0.4.2
Installing globalid 0.4.2
Fetching activejob 5.2.3
Installing activejob 5.2.3
Fetching mini_mime 1.0.1
Installing mini_mime 1.0.1
Fetching mail 2.7.1
Installing mail 2.7.1
Fetching actionmailer 5.2.3
Installing actionmailer 5.2.3
Fetching activemodel 5.2.3
Installing activemodel 5.2.3
Fetching arel 9.0.0
Installing arel 9.0.0
Fetching activerecord 5.2.3
Installing activerecord 5.2.3
Fetching mimemagic 0.3.3
Installing mimemagic 0.3.3
Fetching marcel 0.3.3
Installing marcel 0.3.3
Fetching activestorage 5.2.3
Installing activestorage 5.2.3
Fetching execjs 2.7.0
Installing execjs 2.7.0
Fetching autoprefixer-rails 9.6.1
Installing autoprefixer-rails 9.6.1
Fetching bcrypt 3.1.13
Installing bcrypt 3.1.13 with native extensions
Fetching bindex 0.7.0
Installing bindex 0.7.0 with native extensions
Fetching msgpack 1.3.0
Installing msgpack 1.3.0 with native extensions
Fetching bootsnap 1.4.4
Installing bootsnap 1.4.4 with native extensions
Fetching ffi 1.11.1
Installing ffi 1.11.1 with native extensions
Fetching sassc 2.0.1
Installing sassc 2.0.1 with native extensions
Fetching bootstrap-sass 3.4.1
Installing bootstrap-sass 3.4.1
Using bundler 1.17.2
Fetching byebug 11.0.1
Installing byebug 11.0.1 with native extensions
Fetching coffee-script-source 1.12.2
Installing coffee-script-source 1.12.2
Fetching coffee-script 2.4.1
Installing coffee-script 2.4.1
Fetching method_source 0.9.2
Installing method_source 0.9.2
Fetching thor 0.20.3
Installing thor 0.20.3
Fetching railties 5.2.3
Installing railties 5.2.3
Fetching coffee-rails 4.2.2
Installing coffee-rails 4.2.2
Fetching orm_adapter 0.5.0
Installing orm_adapter 0.5.0
Fetching responders 3.0.0
Installing responders 3.0.0
Fetching warden 1.2.8
Installing warden 1.2.8
Fetching devise 4.6.2
Installing devise 4.6.2
Fetching jbuilder 2.9.1
Installing jbuilder 2.9.1
Fetching rb-fsevent 0.10.3
Installing rb-fsevent 0.10.3
Fetching rb-inotify 0.10.0
Installing rb-inotify 0.10.0
Fetching ruby_dep 1.5.0
Installing ruby_dep 1.5.0
Fetching listen 3.1.5
Installing listen 3.1.5
Fetching pg 1.1.4
Installing pg 1.1.4 with native extensions
Fetching puma 3.12.1
Installing puma 3.12.1 with native extensions
Fetching sprockets 3.7.2
Installing sprockets 3.7.2
Fetching sprockets-rails 3.2.1
Installing sprockets-rails 3.2.1
Fetching rails 5.2.3
Installing rails 5.2.3
Fetching sass-listen 4.0.0
Installing sass-listen 4.0.0
Fetching sass 3.7.4
Installing sass 3.7.4
Fetching tilt 2.0.9
Installing tilt 2.0.9
Fetching sass-rails 5.0.7
Installing sass-rails 5.0.7
Fetching spring 2.1.0
Installing spring 2.1.0
Fetching spring-watcher-listen 2.0.1
Installing spring-watcher-listen 2.0.1
Fetching turbolinks-source 5.2.0
Installing turbolinks-source 5.2.0
Fetching turbolinks 5.2.0
Installing turbolinks 5.2.0
Fetching uglifier 4.1.20
Installing uglifier 4.1.20
Fetching web-console 3.7.0
Installing web-console 3.7.0