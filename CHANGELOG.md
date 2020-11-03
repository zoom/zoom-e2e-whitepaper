# Changelog
All notable changes to this project will be documented in this file.

## [v2.3.1] - 2020-11-03
### Changed
- Corrected release versions in Appendix A to indicate Server Key Certificate Chains is not released
  as of client version 5.4.0

## [v2.3] - 2020-10-14
### Added
- Indicate what the LPL keeps track of, per user
- Add detail about what happens when the leader drops out of the meeting
- Add protocol flow diagram for Phase 1
- Add Appendix A describing Zoom version releases and correspondence to E2EE features

### Changed
- Changed LPL broadcasts into incremental updates for efficiency
- Changed rekey interval after user join to 2 seconds
- Changed packet structure to include the full four bytes of mkSequenceNumber
- Mention ability to join meetings as guests in Phase I
- Correct CtE1's underlying AEAD to be libsodium's xchacha20poly1305_ietf in Local Key Security
- Clarified security guarantees of Phase I
- Changed context strings and minor Phase 1 protocol details

### Removed

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
