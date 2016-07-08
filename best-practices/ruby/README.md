Ruby
----

* Avoid optional parameters. Does the method do too much?
* Avoid monkey-patching.
* Generate necessary [Bundler binstubs] for the project, such as `rake` and
  `rspec`, and add them to version control.
* Prefer classes to modules when designing functionality that is shared by
  multiple models.
* Prefer `private` when indicating scope. Use `protected` only with comparison
  methods like `def ==(other)`, `def <(other)`, and `def >(other)`.

[Bundler binstubs]: https://github.com/sstephenson/rbenv/wiki/Understanding-binstubs

Ruby Gems
---------

* Declare dependencies in the `<PROJECT_NAME>.gemspec` file.
* Reference the `gemspec` in the `Gemfile`.
* Use [Appraisal] to test the gem against multiple versions of gem dependencies
  (such as Rails in a Rails engine).
* Use [Bundler] to manage the gem's dependencies.
* Use [Travis CI] for Continuous Integration, indicators showing whether GitHub
  pull requests can be merged, and to test against multiple Ruby versions.

[Appraisal]: https://github.com/thoughtbot/appraisal
[Bundler]: http://bundler.io
[Travis CI]: http://travis-ci.org

Ruby JSON APIs
--------------

* Review the recommended practices outlined in Heroku's [HTTP API Design Guide]
  before designing a new API.
* Use a fast JSON parser, e.g. [`oj`][oj]
* Write integration tests for your API endpoints. When the primary consumer of
  the API is a JavaScript client maintained within the same code base as the
  provider of the API, write [feature specs]. Otherwise write [request specs].

[HTTP API Design Guide]: https://github.com/interagent/http-api-design
[oj]: https://github.com/ohler55/oj
[feature specs]: https://www.relishapp.com/rspec/rspec-rails/docs/feature-specs/feature-spec
[request specs]: https://www.relishapp.com/rspec/rspec-rails/docs/request-specs/request-spec
