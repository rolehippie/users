# Changelog

## [2.0.0](https://github.com/rolehippie/users/compare/v1.3.1...v2.0.0) (2024-02-12)


### Features

* drop support for ubuntu 18.04 ([de78dee](https://github.com/rolehippie/users/commit/de78deea34f015dfa3d3d3e5037d2c4e1375c9f1))
* used full qualified collection names ([9df4557](https://github.com/rolehippie/users/commit/9df4557070a8b2b265da47c119e531c3fff7a0f5))


### Bugfixes

* remove meta requirements and document used collections ([a521512](https://github.com/rolehippie/users/commit/a5215128b6dd7e66e594bc76ad2fe36f3fe9575e))
* use right attribute for user shell ([1e9d2a9](https://github.com/rolehippie/users/commit/1e9d2a9f647e7a1803f234414330d046ff5b62e4))

## [1.3.1](https://github.com/rolehippie/users/compare/v1.3.0...v1.3.1) (2023-08-31)


### Bugfixes

* use right state attribute while removing user ([1cba3cf](https://github.com/rolehippie/users/commit/1cba3cf2a6dae007862a3de0b0d76cdd916ef435))

## [1.3.0](https://github.com/rolehippie/users/compare/v1.2.1...v1.3.0) (2023-05-23)


### Features

* make packages configurable ([ebb04be](https://github.com/rolehippie/users/commit/ebb04bea9bf66f0960e175ced9c135dc57fd36d9))

## [1.2.1](https://github.com/rolehippie/users/compare/v1.2.0...v1.2.1) (2023-05-22)


### Bugfixes

* correctly set mode for user home ([2ed8c63](https://github.com/rolehippie/users/commit/2ed8c630088b9e17fd40f402eea8d51dec9216ac))
* home dir should not be readable by others ([bfcb47a](https://github.com/rolehippie/users/commit/bfcb47a699cf452e54fd68e7d69ef451c79f6fc6))

## [1.2.0](https://github.com/rolehippie/users/compare/v1.1.1...v1.2.0) (2023-05-22)


### Features

* integrate zfs userdata ([df87a1d](https://github.com/rolehippie/users/commit/df87a1d0fd2ae80209a264c5a25eaa2822c49a06))

## [1.1.1](https://github.com/rolehippie/users/compare/v1.1.0...v1.1.1) (2023-05-03)


### Bugfixes

* write zshenv only if zsh is installed ([dfcb02c](https://github.com/rolehippie/users/commit/dfcb02c3c0bf7701c68f0fe5e19419c6fad5c917))

## [1.1.0](https://github.com/rolehippie/users/compare/v1.0.0...v1.1.0) (2023-05-03)


### Features

* add custom zshenv support ([a8117c1](https://github.com/rolehippie/users/commit/a8117c122f981e1dab6b01cb5f5c25d727cabd1f))

## 1.0.0 (2023-01-05)


### Features

* allow homeshick from other sources ([e7baf5d](https://github.com/rolehippie/users/commit/e7baf5ddea219ce7992669cd83f675e50a635f18))
* make it possible to write a private sshkey ([e922536](https://github.com/rolehippie/users/commit/e92253655bd9c5dd80cea448c589f9947c1f7fb8))
* restructure workflows and enable automated releases ([524d18e](https://github.com/rolehippie/users/commit/524d18ea9769e34dd5bd58fbf137498a6cd3f9af))


### Bugfixes

* only write ssh keys if they are present ([b3b07f8](https://github.com/rolehippie/users/commit/b3b07f802f6601800dcc50da255bef306f4e720c))
