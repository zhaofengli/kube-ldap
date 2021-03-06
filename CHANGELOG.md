# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.3.0] - 2019-01-07
### Changed
- Failed authentication sends a WWW-Authenticate header in the HTTP response
- Default loglevel is now info (was debug)
- Update node to latest 8.x LTS in docker image

### Added
- LDAP related logging
- Configuration parameter whether to use StartTLS for LDAP or not (enabled by default).

### Fixed
- Single group memberships are returned as a string (instead of an array) by LDAP in some cases and broke the membership resolution. This is now handled correctly.
- Fixed units in README for LDAP reconnect config parameters.

## [1.2.1] - 2018-07-19
### Added
- LDAP reconnect logic (with configurable parameters)

## [1.2.0] - 2018-04-20
### Added
- Configuration parameters for LDAP connection and operation timeouts.
- Configurable mapping between LDAP and kubernetes attributes.

## [1.1.0] - 2018-03-27
### Security
- TLS (HTTPS) support (enabled by default).

### Changed
- Log error if a DN is not in a canonicalizable format.

## [1.0.0] - 2018-03-27
### Added
- Initial key functionality

[Unreleased]: https://github.com/gyselroth/kube-ldap/compare/v1.3.0...master
[1.3.0]: https://github.com/gyselroth/kube-ldap/compare/v1.2.1...v1.3.0
[1.2.1]: https://github.com/gyselroth/kube-ldap/compare/v1.2.0...v1.2.1
[1.2.0]: https://github.com/gyselroth/kube-ldap/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/gyselroth/kube-ldap/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/gyselroth/kube-ldap/tree/v1.0.0
