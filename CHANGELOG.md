# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [1.0.0] - 2016-10-16
### Added
- Detect old python-gitlab version and monkey-patch around it

### Changed
- Improve clarity of `-m` help output

### Fixed
- Handle non-UTC ("Z") build timestamps ([#4])



## [0.2.0] - 2016-10-02
### Added
- Show tag names for skipped builds
- Display total number and size of artifacts


## 0.1.0 - 2016-10-02
First versioned release


[Unreleased]: https://github.com/JonathonReinhart/gitlab-artifact-cleanup/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/JonathonReinhart/gitlab-artifact-cleanup/compare/v0.2.0...v1.0.0
[0.2.0]: https://github.com/JonathonReinhart/gitlab-artifact-cleanup/compare/v0.1.0...v0.2.0

[#4]: https://github.com/JonathonReinhart/gitlab-artifact-cleanup/pull/4
