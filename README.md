# Capistrano::Rocket::Chat
rocket.chat webhook plugin for Capistrano 3. 

## Installation

Add this line to your application's *Gemfile*:

```ruby
gem 'capistrano-rocket-chat'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install capistrano-rocket-chat

In your *Capfile* add this line:

```ruby
  require 'capistrano/rocket_chat'
```

Add the rocket.chat webhook url including the webhook token to your *deploy.rb* file:

```ruby
set :rocket_chat_webhook_url, "https://mychat.com/hooks/MYTOKEN"
```

And you are ready to go

## Usage

The webhook fires automatically on the following capistrano events: 
* deploy:starting
* deploy:failed
* deploy:finished

Additionally you will need a parser script for your rocket.chat for the incoming webhook integration.

If you don't want to code one yourself, here is a working script with basic functionality for you:
https://github.com/cbajohr/capistrano-rocket-chat/wiki/rocket.chat-parser-script-example

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/cbajohr/capistrano-rocket-chat. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

