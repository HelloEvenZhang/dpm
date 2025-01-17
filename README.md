[English](README.md) | [简体中文](README.zh-CN.md)

# DPM

Docker Package Manager, makes using your containers as easy as package managers (`apt`, `yml`, `brew`).

## Installation

```bash
gem install dpmrb
```

## Usage

```bash
dpm help                       # Show help
dpm list                       # docker ps --filter "name=dpm-"
dpm start mysql                # docker run --name=dpm-mysql -d --rm -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes ...
dpm stop mysql                 # docker stop dpm-mysql
dpm status mysql               # docker ps --filter "name=dpm-mysql"
dpm start elasticsearch:7.10.2 # docker run --name=dpm-elasticsearch-7.10.2 -d --rm -p 9200:9200 -e discovery.type=single-node ...
dpm start mysql:5.7            # docker run --name=dpm-mysql-5.7 -d --rm -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes ...
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/songhuangcn/dpm. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/songhuangcn/dpm/blob/main/CODE_OF_CONDUCT.md).

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the DPM project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/songhuangcn/dpm/blob/main/CODE_OF_CONDUCT.md).
