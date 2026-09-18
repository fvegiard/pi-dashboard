# CHANGELOG

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [43.4.1] - 2026-09-18

### Initial Public Release

Initial release of pi-dashboard as open-source software.

#### Added
- Open-source release on GitHub
- MIT license attribution
- Security policy and vulnerability reporting guidelines
- Contributing guidelines

#### Components
- Electron-based dashboard application
- Chromium browser engine
- Graphics support (DirectX, Vulkan, OpenGL)
- FFmpeg multimedia support
- Git Bash system integration
- Localization support (ICU)

### Known Issues
- Version number validation needed (43.4.1 may not be valid Electron release)
- Executables currently unsigned (code signing recommended)
- SBOM (Software Bill of Materials) not yet published

---

## Version Format

This project follows [Semantic Versioning](https://semver.org/):
- MAJOR version for incompatible API changes
- MINOR version for new features (backwards compatible)
- PATCH version for bug fixes

---

## Release Checklist

- [ ] Version bump in `version` file
- [ ] CHANGELOG.md updated
- [ ] Code sign executables
- [ ] GitHub release created
- [ ] Security scan completed
- [ ] Binary artifacts uploaded to release page

---

For version history prior to 43.4.1, see previous release notes.
