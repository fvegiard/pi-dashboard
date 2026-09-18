# Security Policy

## Reporting Security Vulnerabilities

If you discover a security vulnerability in pi-dashboard, please **report it responsibly** and do not disclose it publicly until a fix is available.

### How to Report

1. **Email**: [security@your-domain.com](mailto:security@your-domain.com)
   - Send security vulnerability reports directly
   - Provide detailed information about the vulnerability
   - Include reproduction steps if possible

2. **GitHub Security Advisory**: 
   - Use GitHub's [Private Vulnerability Reporting](https://docs.github.com/en/code-security/security-advisories/private-vulnerability-reporting) feature
   - Navigate to **Security** → **Report a vulnerability** in the repository

3. **Do NOT**:
   - Create public GitHub issues for security vulnerabilities
   - Post vulnerability details on social media or public forums
   - Test exploits on production systems without permission

## Expected Response Timeline

- **Initial Response**: Within 48 hours
- **Assessment**: Within 1 week
- **Fix Development**: Depends on severity (critical: prioritized)
- **Public Disclosure**: After fix is released and sufficient time for users to update

## Supported Versions

Security updates are provided for:
- **Latest Major Release**: All minor and patch versions
- **Previous Major Release**: Critical issues only (6-month window)
- **Older Releases**: No official support (upgrade recommended)

## Security Considerations

### Network Security
- Always use HTTPS for remote connections
- Enable TLS 1.2+ for all network operations
- Validate SSL/TLS certificates
- Avoid transmitting credentials over unencrypted channels

### Application Security
- Application runs with user privileges
- No privilege escalation by default
- All system commands executed within sandbox constraints
- User input validation required for remote operations

### System Integration
- Git Bash integration allows shell command execution
- Restrict access to system operations as needed
- Monitor logs for suspicious activity
- Keep Git Bash updated with latest patches

### Data Protection
- Sensitive data should be encrypted at rest
- Configuration files should have restricted permissions (600)
- API keys and tokens should use system credential storage
- Avoid logging sensitive information

## Security Update Procedures

### For Users
1. Monitor [GitHub Releases](../../releases) for security announcements
2. Subscribe to release notifications
3. Update promptly when security fixes are released
4. Review CHANGELOG.md for security-related changes

### For Developers
1. Keep dependencies updated: `npm update`
2. Run security audit: `npm audit`
3. Use linters and static analysis tools
4. Test for common vulnerabilities (injection, XSS, etc.)
5. Review code before merging

## Known Security Limitations

1. **Unsigned Binaries**: Current distribution is not code-signed
   - Recommendation: Verify SHA256 hashes against releases page
   - Code signing planned for future releases

2. **Version Validation**: Version 43.4.1 validity needs confirmation
   - Verify against official Electron releases before deployment
   - Updated version information coming

3. **SBOM Not Available**: Software Bill of Materials not yet published
   - Dependency list available in `/docs/DEPENDENCIES.md`
   - Official SBOM planned for future release

## Third-Party Dependencies

This application includes:
- **Chromium/Electron**: Core application framework
- **FFmpeg**: Multimedia support
- **OpenGL, Vulkan, DirectX**: Graphics rendering
- **Git Bash**: System integration
- **Node.js, V8**: JavaScript runtime

See [LICENSES.chromium.html](./LICENSES.chromium.html) for complete license attributions.

## Vulnerability Disclosure Timeline

When a security vulnerability is reported:

1. **Triage** (24-48h): Assess severity and impact
2. **Fix Development** (varies): Create and test patch
3. **Release Preparation** (24h): Prepare security release
4. **Public Disclosure** (coordinated): Announce fix via release notes
5. **Archive**: Document CVE if applicable

## Security Testing

Regular security testing includes:
- Static Application Security Testing (SAST)
- Dependency vulnerability scanning (npm audit)
- Manual code review
- Fuzzing and crash testing (in CI/CD)

## CVE Disclosure

If a vulnerability is assigned a CVE:
- Full disclosure in GitHub Security Advisories
- Update CHANGELOG.md with CVE reference
- Release available immediately

## Questions?

If you have security-related questions or concerns:
- Contact: security team
- Issues: Use private vulnerability reporting
- Documentation: See [SECURITY.md](./SECURITY.md)

---

**Last Updated**: 2026-09-18  
**Policy Version**: 1.0
