# Octopoller 🦑
Octopoller is a micro gem for polling and retrying, perfect for making repeating requests.

```ruby
Octopoller.poll(timeout: 15.seconds) do
  begin
    client.make_that_request # raises an Error sometimes
  rescue Error
    :re_poll
  end
end

# => { "status" => 200,  "body" => "🦑" }
```

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'octopoller'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install octopoller

## Usage

TODO: Write usage instructions here

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/BenEmdon/octopoller. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Octopoller project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/BenEmdon/octopoller/blob/master/CODE_OF_CONDUCT.md).
