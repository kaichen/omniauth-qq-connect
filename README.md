# Omniauth::Qq::Connect

This is the OmniAuth strategy for authenticating to QQ connect. To
use it, you'll need to sign up for an OAuth2 Application Key and Secret
on the [QQ Open SNS Page](http://connect.qq.com/intro/login/).

## Installation

Add this line to your application's Gemfile:

    gem 'omniauth-qq-connect'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install omniauth-qq-connect

## Usage

    use OmniAuth::Builder do
      provider :qq_connect, ENV['QQ_CONNECT_APP_KEY'], ENV['QQ_CONNECT_APP_SECRET']
    end

*Notice* you only allow send the auth request from host(w/o port) list of application.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
