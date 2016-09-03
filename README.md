# dangerfile-gem-template

An opinionated template for creating a Dangerfile gem with the following features:

- Git as the source control management system.
- Clean folder structure.
- MIT license.
- Rake as task management tool.

## Usage

    $ ./configure dangerfile-foo

It will generate a Dangerfile gem, which will expose a Dangerfile via a `dangerfile-foo` gem.

## Going from there

- Add descriptions to the Gem specification, README and command itself.
- Implement your Dangerfile, documentation is available at http://danger.systems.
- Add Danger plugin dependencies to .gemspec.
- Release the gem with `rake release`.
