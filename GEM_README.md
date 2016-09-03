## ${GEM_NAME}

[Danger](http://danger.systems) runs during the CI process, and gives you a chance to automate common code review chores.

[![Build Status](https://travis-ci.org/${USER_NAME}/${GEM_NAME}.svg?branch=master)](https://travis-ci.org/${USER_NAME}/${GEM_NAME})

### Setup

Enable Danger for your project.

#### Set DANGER_GITHUB_API_TOKEN in Travis-CI

In Travis-CI, choose _Settings_ and add `DANGER_GITHUB_API_TOKEN` in _Environment Variables_. Set the value to the API key for a bot user. See [Getting Set Up](http://danger.systems/guides/getting_started.html) for more information.

#### Add Danger

Add `${GEM_NAME}` to `Gemfile`.

```ruby
gem '${GEM_NAME}', '~> 0.1.0', require: false
```

#### Add Dangerfile

Commit a `Dangerfile`.

```ruby
danger.import_dangerfile(gem: '${GEM_NAME}')
```

#### Add Danger to Travis-CI

Add Danger to `.travis.yml`.

```yaml
matrix:
  include:
    - rvm: 2.3.1
      script:
        - bundle exec danger
```

#### Commit via a Pull Request

To test things out, make a pull request.

## License

MIT License. See [LICENSE](LICENSE) for details.
