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

*Notice* you only allow send the auth request from host(w/o port) list of
application.

## Configuring

You can configure several options(currently only one), which you pass in to
the provider method via a Hash:

scope: A comma-separated list of permissions you want to request from the
user. See the official docs for a full list of available permissions:
<http://wiki.opensns.qq.com/wiki/%E3%80%90QQ%E7%99%BB%E5%BD%95%E3%80%91API%E6%96%87%E6%A1%A3>
Default: `get_user_info`(获取用户在QQ空间的个人资料)

Example:

    use OmniAuth::Builder do
      provider :qq_connect,
        ENV['QQ_CONNECT_API_KEY'], ENV['QQ_CONNECT_API_SECRET'],
        scope: "get_user_info,add_share"
    end

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
