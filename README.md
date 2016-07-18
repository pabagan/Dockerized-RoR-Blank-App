# Ruby on Rails Blank APP
Dockerized Ruby on Rails starter APP.

## Gems
```ruby
source 'https://rubygems.org'

gem 'rails', '4.2.3'
gem 'sqlite3'
gem 'sass-rails', '~> 5.0'
gem 'uglifier', '>= 1.3.0'
gem 'coffee-rails', '~> 4.1.0'
gem 'therubyracer', platforms: :ruby
gem 'jquery-rails'
gem 'turbolinks'
gem 'jbuilder', '~> 2.0'
gem 'sdoc', '~> 0.4.0', group: :doc

gem 'web-console', '~> 2.0', group: :development

group :development, :test do
  gem 'byebug'
  gem 'spring'
  gem 'guard'   # livereload
  gem 'guard-livereload', '~> 2.5', require: false
end

group :test do
 gem 'rspec-rails', '~> 3.0'
end
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# JSON deal
# gem 'httparty'

```


## Build and Run
```bash
# Clone repository 
git clone git@github.com:pabagan/Dockerizez-RoR-Blank-App.git

# Build container
docker-compose build

# Start container
docker-compose up
# run at background
docker-compose up -d  

# Log container
./sh/log.sh
# Run and log container
./sh/run.sh

# Watch files with Guard (once logged)
root@ddd5a2258e94:/app# $ bundle exec guard
```

You might be able to see Rails wellcome page at your [http://localhost:3000](http://localhost:3000)


## References
* [Guard](https://github.com/guard/guard): watch files.
* [Guard LiveReload](https://github.com/guard/guard-livereload): browser notification.

## Requirements
* [Docker Engine](https://docs.docker.com/installation/)
* [Docker Compose](https://docs.docker.com/compose/)
* [Docker Machine](https://docs.docker.com/machine/) (Mac and Windows only)
