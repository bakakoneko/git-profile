# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2022-02-23
### Added
- The default profile directory can be set with the `GIT_PROFILE_DIR` environment variable.

### Changed
- `git-profile` now creates a include path in the git config instead of overwriting it. This will hopefully increase compatibility with other tools that modify the git config.
