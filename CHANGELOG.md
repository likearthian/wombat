# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Custom rendering/parsing support for Google Well Known [wrapper] Types
- Notification when a new version of Wombat is available to download
- Service and Method select dropdowns are searchable

### Fixed
- Support mac case-sensitive filesystem. Thanks to [@Azuka](https://github.com/Azuka)
- UI unresponsive when rendering empty state for repeated fields
- Fix layout of metadata for Headers and Trailers

## [v0.2.2] - 2020-11-12

### Fixed
- Windows styling issues
- WKT google.protobuf.Timestamp parsed correctly using RFC 3339
- WKT google.protobuf.Duration parsed correctly with `s` suffix (representing seconds)

## [v0.2.1] - 2020-11-11

### Removed
- Linux AppImage package due to linking errors, may be fixed in a future version

### Fixed
- UI unresponsive when request message has zero fields

## [v0.2.0] - 2020-11-10

### Added
- Input generation for oneof fields
- Input generation for map fields
- More error messages on failure
- Metadata specifically for the Reflection API
- Windows build
- CI/CD for release builds

### Changed
- Rebuilt from the ground up using Svelte frontend rather than Qt
- Updated Go Protobuf to use APIv2
- New output protobuf format based on prototext encoder
- Directly use Go gRPC invoke/stream functions rather than wrappers
- DB format (all previous saved requests will be lost)
- New looking App Icon

### Removed
- Logging to disk
- Request metadata from the workspace options (only relflection API metadata)

### Fixed
- Crash when a previous connection tries to report status changes
- Appearance of an in-flight request when application launches, when there is no request

## [v0.1.0-beta.1] - 2020-09-19

## Added
- Metadata can be added in the Workspace Options
- Metadata is added to the header of Reflection API Call
- Extra error messages
- Logger to help with providing support

## Fixed
- Crash when proto field is unknown in the resposne payload

## [v0.1.0-beta] - 2020-08-31

### Added
- Client streaming support
- Request cancellation
- Bidirectional streaming support
- Response time output
- Save metadata between requests/sessions to DB
- Save messages, fields, repeated fields on Send to DB
- Linux binary release as a tar.gz

### Changed
- - DMG background and Application shortcut for Mac OSX

## [v0.1.0-alpha.1] - 2020-08-09

### Added
- Error messages on connection errors
- Create crash log file
- Enable support for the Reflection API
- Support for client certificate/key for TLS
- Progress bar to indicate in-flight requests
- Linux AppImage build

## Changed
- Syntax highlighting on response output
- Allow nested messages to be nullable

## [v0.1.0-alpha] - 2020-07-29

### Added 
- First release with basic Unary requests
- Proto file parsing and input field generation
- Selection of services and methods
- gRPC request/response statistics
- Basic proto text output
- Output of Headers/Trailers
- Mac OS Build
