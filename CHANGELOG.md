# Changelog
All notable changes to this project will be documented in this file.

## [v3.2] - 2021-10-29
### Added
- Distinguished between hardware ids in Phase I and device ids in Phase II
- Clarified the generation of hardware ids, device ids, user ids, and account ids

## [v3.1] - 2021-10-05
### Added
- New section on Zoom Phone in Phase I
- Describe the Lock The Meeting feature, available since 5.6.
- Clarify that participants need to agree on who the leader is when checking the meeting leader security code.
- An additional author: Brian Chen

## [v3] - 2020-12-15
### Added
- Major additions to the Phase II section
- Table of Contents
- An additional author: Surya Rien
- An acknowledgements section
### Changed
- Clarify that meeting key seed boxes include mkSeqNum in addition to the key seed
- Provide more context for the choice of our authenticated encryption algorithms
- Clarify that we are considering to reintroduce a secure version of the Cloud Recording feature
- Clarify that in Phase 1 display names should not be relied upon to establish a meeting participant's identity
- Clarify the security guarantees of the feature described in the Local Key Security section
### Removed
- Multiple ZTTs in Phase III. We will use a single one (per cloud infrastructure) instead.

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
