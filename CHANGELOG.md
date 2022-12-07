## v2.3.1 2022-12-07

### Changed

* Add support for namespaced auto loading paths
* Fix jruby to version 9.3.*

[Compare v2.3.0...v2.3.1](https://github.com/rom-rb/rom-rails/compare/v2.3.0...v2.3.1)

## v2.3.0 2021-03-20

### Changed

* Updated dependencies to allow Rails 6.1 (alex-lairan)

## v2.2.0 2019-09-12

### Changed

* Read new-style Rails6 configuration, inferring all defined databases (cflipse)

### Fixed

* Updated generator to produce files that are actually compatible with ROM 5.0 (cflipse)

[Compare v2.1.0...v2.2.0](https://github.com/rom-rb/rom-rails/compare/v2.1.0...v2.2.0)

## v2.1.0 2019-09-09

### Changed

* Allow rails6 (cflipse)

[Compare v2.0.0...v2.1.0](https://github.com/rom-rb/rom-rails/compare/v2.0.0...v2.1.0)

## v2.0.0 2019-04-27

### Changed

* Updated to depend on rom-* 5.0
* Repository generator creates a `by_id` method (cflipse)

[Compare v1.3.0...v2.0.0](https://github.com/rom-rb/rom-rails/compare/v1.3.0...v2.0.0)

## v1.3.0 2018-11-26

### Changed

* Rake task automatically attempts to include `rom-sql`'s tasks (cflipse)
* Escape special characters in username & password from parsed database.yml (Cervajz)

### Fixed

* do not double log when ActiveRecord is present (Cervajz)
* running the install generator no longer results in a broken app if `DATABASE_URL` is not set (cflipse)

[Compare v1.2.0...v1.3.0](https://github.com/rom-rb/rom-rails/compare/v1.2.0...v1.3.0)

## v1.2.0 2018-10-20

### Changed

* ROM output is broadcast to STDOUT during rails console (radar)
* Generators default to same adapter as the default gateway (cflipse)
* Default auto-registration path set to app (cflipse)
* Include controller extensions in API controllers (cflipse)

[Compare v1.1.1...v1.2.0](https://github.com/rom-rb/rom-rails/compare/v1.1.1...v1.2.0)

## v1.1.1 2018-04-17

### Fixedd

* Fix Rails.logger lookup bug (cflipse)

[Compare v1.1.0...v1.1.1](https://github.com/rom-rb/rom-rails/compare/v1.1.0...v1.1.1)

## v1.1.0 2018-03-18

### Added

* Add a new `rom:install` generator (cflipse)

### Changed

* Stop breaking rails loading when not yet configured. (cflipse)
* Repository generator prefers `struct_namespace` over mapper (radar, cflipse)

[Compare v1.0.1...v1.1.0](https://github.com/rom-rb/rom-rails/compare/v1.0.1...v1.1.0)

## v1.0.1  2017-12-22

### Changed

* Loosen ROM dependency

[Compare v1.0.0...v1.0.1](https://github.com/rom-rb/rom-rails/compare/v1.0.0...v1.0.1)

## v1.0.0  2017-10-18

### Changed

* Updated to work with ROM 4.0.beta (cflipse)
* Generated repositories now inherit from `ROM::Repository::Root` (cflipse)

### Removed

* remove ROM::Model::Form (cflipse)
* remove form generator (cflipse)
* remove deprecated `config.repositories` method (cflipse)
* No longer depends on `rom-model` gem (cflipse)
* No longer depends on `charlatan` gem (artofhuman)

[Compare v0.9.0...v1.0.0](https://github.com/rom-rb/rom-rails/compare/v0.9.0...v1.0.0)

## v0.9.0  2017-01-30

### Added

* Add `rom-repository` generator (fmartin91)

### Changed

* Updated to work with ROM 3.0.beta (maximderbin, cflipse)
* Command generators now produce a flat directory structure (cflipse)
* Dropped runtime dependency on `virtus` (bilby91)
* Updated generators to remove validatior hints (cflipse)
* Updated generators to provide before hook hints, rather than override `execute` (cflipse)

### Internal

* [`rom-support`](https://github.com/rom-rb/rom-support) dependency was replaced with [`dry-core`](https://github.com/dry-rb/dry-core) (solnic + flash-gordon)


[Compare v0.8.0...v0.9.0](https://github.com/rom-rb/rom-rails/compare/v0.8.0...v0.9.0)

## v0.8.0 2016-08-08
### Changed

* Updated to work with Rails 5 (cflipse)
* Form validations are now handled entirely within form (cflipse)
* [Rails5] when applicable, parmeters are converted to unsafe hash (cflipse)

### Deprecated
* Dropping support for ruby 2.1 and below

[Compare v0.7.0...v0.8.0](https://github.com/rom-rb/rom-rails/compare/v0.7.0...v0.8.0)

## v0.7.0 2016-07-27

### Changed
* Updated to work with rom 2.0
* Loosen Gem dependencies for Rails 4.2
* Allow multiple auto_registration paths (vbyno)

[Compare v0.6.0...v0.7.0](https://github.com/rom-rb/rom-rails/compare/v0.6.0...v0.7.0)

### Fixed
* Fixed generated mapper's `register_as` (duduribeiro)

## v0.6.0 2016-01-06

### Changed
* Updated to work with new ROM configuration API.

[Compare v0.5.0...v0.6.0](https://github.com/rom-rb/rom-rails/compare/v0.5.0...v0.6.0)

## v0.5.0 2015-08-19

### Changed

* Raise a helpful error when trying to use uniqueness validation without a relation (xaviershay)
* Switched to extracted rom-model (solnic)
* Updated to work with ROM 0.9.0 (solnic)

### Fixed

* Setting connectin URI for jruby that needs jdbc adapter (austinthecoder)

[Compare v0.4.0...v0.5.0](https://github.com/rom-rb/rom-rails/compare/v0.4.0...v0.5.0)

## v0.4.0 2015-06-22

### Added

* `embedded` validators allowing to nest validations for embedded values (solnic)
* Uniqueness validation supports `:scope` option (vrish88)

### Changed

* `ROM.env` is lazy-finalized on first access of any of the components (solnic)
* `db:setup` provided by the railtie now loads `:environment` (solnic)
* `repositories` in railtie configuration deprecated in favor of `gateways` (solnic)

### Fixed

* `method_missing` in validators behaves properly now (solnic)

[Compare v0.3.3...v0.4.0](https://github.com/rom-rb/rom-rails/compare/v0.3.3...v0.4.0)

## v0.3.3 2015-05-22

### Added

* `db:setup` task which works OOTB with rom-sql tasks (solnic)

### Changed

* `MissingRepositoryConfigError` is raised when repositories are not configured (solnic)

### Fixed

* The railitie no longer set `nil` as default repository when ActiveRecord is not present (solnic)

[Compare v0.3.2...v0.3.3](https://github.com/rom-rb/rom-rails/compare/v0.3.2...v0.3.3)

## v0.3.2 2015-05-17

### Fixed

* Generator uses correct directory for commands (cflipse)
* Generators can now add `register_as` and `repository` settings (cflipse)
* Database errors are now wrapped in Form objects so they can be handled gracefully (cflipse)

[Compare v0.3.1...v0.3.2](https://github.com/rom-rb/rom-rails/compare/v0.3.1...v0.3.2)

## v0.3.1 2015-04-04

### Added

* `Form.mappings` which sets up auto-mapping command results (solnic)
* Form descendants can use `input` and `validations` blocks (cflipse)
* Form generators can generate a shared base form class for new/update forms (cflipse)

[Compare v0.3.0...v0.3.1](https://github.com/rom-rb/rom-rails/compare/v0.3.0...v0.3.1)

## v0.3.0 2015-03-22

### Added

* `ROM::Model::Form` for modeling and setting up web-forms (solnic + cflipse)
* Support for timestamps attributes in Form objects (kchien)
* Allow setup using a configuration block from railtie (aflatter)

### Changed

* [BREAKING] Model::Params renamed to Model::Attributes (solnic + cflipse)
* Improved initialization process which works with AR-style configurations (aflatter)

[Compare v0.2.1...v0.3.0](https://github.com/rom-rb/rom-rails/compare/v0.2.1...v0.3.0)

## v0.2.1 2015-01-07

### Changed

* input params uses virtus' `:strict` mode by default (stevehodgkiss)

### Fixed

* `rom` extension is now mixed into ActionController::Base which addresses #12 (solnic)

[Compare v0.2.1...v0.2.0](https://github.com/rom-rb/rom-rails/compare/v0.2.0...v0.2.1)

## v0.2.0 2014-12-31

### Added

* Generators for relations, mappers and commands (solnic)
* Support for Spring and reload in development mode (solnic)

### Fixed

* Setup will be skipped when there are missing elements in the registries (solnic)

[Compare v0.1.0...v0.2.0](https://github.com/rom-rb/rom-rails/compare/v0.1.0...v0.2.0)

## v0.1.0 2014-12-06

### Added

* Support for loading commands (solnic)

[Compare v0.0.2...v0.1.0](https://github.com/rom-rb/rom-rails/compare/v0.0.2...v0.1.0)

## v0.0.2 2014-11-25

### Added

* Support for username and password in database.yml (solnic)
* Support for more db schemes (solnic)
* Missing runtime dep on rom gem (solnic)

[Compare v0.0.1...v0.0.2](https://github.com/rom-rb/rom-rails/compare/v0.0.1...v0.0.2)

## v0.0.1 2014-11-24

First public release
