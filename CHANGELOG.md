# Changelog
All notable changes to this project will be documented in this file.

## [v2] - 2020-06-17
### Added
- Local key storage design section.
- More detail about join/leave protocol security properties.
- An additional author: Julia Len
- Definitional footnote for "deep fakes"

### Changed
- Rename `meeting security code` to `meeting leader security code`.
- Add small clarifications about security code usage.
- Change from attached to detached signatures.
- Fix typos.

### Removed
- "Doubling-up" of public key operations. We'll use standard [`libsodium`](https://github.com/jedisct1/libsodium) constructions instead.

## [v1] - 2020-05-22
### Added
- Initial draft of E2EE design.
