# Changelog
All notable changes to this project will be documented in this file.

## [v4.1] - 2023-03-27
### Added
- Description of "Okta Authentication for End-to-End Encryption", which supports Okta IDP attestations for E2EE Meetings 
- Rotatable Zero-Knowledge Set citation in "Zoom Transparency Tree" section
### Changed
- Improved E2EE meeting key rotation, leader participant list, and liveness.

## [v4.0] - 2022-11-18
### Added
- Descriptions of new features in user identity and key management:
  - New user sigchain links, Root and AddAndApprove
  - Backup keys and application to escrow
  - Sigchain fingerprints
  - Application-specific subkeys of per-user keys
- New Zoom product, Zoom Mail Service
- New Zoom Phone feature, Advanced Encryption for Voicemail
- Description of Cake-AES, encryption algorithm used for Zoom Mail and Voicemail

### Changed
- Title updated to "Zoom Cryptography Whitepaper"
- Restructured the paper to have individual sections on the background and threat model, User
  Identity and Key Management, the Zoom Transparency Tree, and Identity Provider Attestations (all
  of which can apply to multiple products), plus individual sections for each product
- Consolidated "Real-Time Security" section into User Identity and renamed it to "Compromise
  Prevention for Device Provisioning"
- Moved away from a roadmap based on "Phases" to explicitly labeling whether each feature has been
  released

## [v3.3] - 2022-07-18
### Added
- Description of E2EE Breakout Rooms in Phase I, available since 5.11.3
- An additional author: Armin Namavari
### Changed
- Separated the roles of meeting leader and meeting host

## [v3.2] - 2021-10-29
### Added
- Distinguished between hardware ids in Phase I and device ids in Phase II
- Clarified the generation of hardware ids, device ids, user ids, and account ids

## [v3.1] - 2021-10-05
### Added
- New section on Zoom Phone in Phase I
- Describe the Lock The Meeting feature, available since 5.6.
- Clarify that participants need to agree on who the leader is when checking the meeting leader
  security code.
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
- Clarify that in Phase 1 display names should not be relied upon to establish a meeting
  participant's identity
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
- "Doubling-up" of public key operations. We'll use standard
  [`libsodium`](https://github.com/jedisct1/libsodium) constructions instead.

## [v1] - 2020-05-22
### Added
- Initial draft of E2EE design.
