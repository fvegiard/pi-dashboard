# pi-dashboard

**Electron-based Raspberry Pi dashboard application**

A modern, cross-platform dashboard for monitoring and managing Raspberry Pi systems.

## Features

- Real-time system monitoring
- Cross-platform support (Windows, macOS, Linux)
- Built with Electron and Chromium
- Git Bash integration for advanced operations
- Hardware acceleration (DirectX, Vulkan, OpenGL)

## Installation

### Stable Release
Download the latest release from [GitHub Releases](../../releases)

### From Source
```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/pi-dashboard.git
cd pi-dashboard

# Build (requires Node.js and development dependencies)
npm install
npm run build
```

## System Requirements

- Windows 10 / macOS 10.15+ / Linux (Ubuntu 18.04+)
- 4GB RAM minimum
- 500MB disk space
- GPU with DirectX 11 or Vulkan support (optional, software fallback available)

## Components

### Electron Framework
- Chromium-based browser engine
- V8 JavaScript runtime
- Node.js integration

### Graphics Support
- **DirectX 11**: For Windows GPU acceleration
- **Vulkan**: Cross-platform GPU rendering
- **OpenGL**: Legacy GPU support (GLES2)
- **Software Renderer**: Vulkan SwiftShader fallback

### Multimedia
- **FFmpeg**: Audio/video processing and playback

### System Integration
- **Git Bash**: Shell operations and scripting
- **Localization**: Multi-language UI support (ICU)

## Configuration

See [CONFIGURATION.md](./docs/CONFIGURATION.md) for detailed setup instructions.

## Security

This is an Electron-based application. Security considerations:

- Application runs with user privileges
- All network operations should be encrypted (HTTPS)
- Remote operations should use secure protocols (SSH, etc.)
- See [SECURITY.md](./SECURITY.md) for security policy

## Development

### Build from Source
```bash
npm install
npm run dev      # Development mode
npm run build    # Production build
```

### Testing
```bash
npm test         # Run test suite
npm run lint     # Lint code
```

## Contributing

Contributions welcome! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

## License

Licensed under the MIT License. See [LICENSE](./LICENSE) for details.

### Third-Party Licenses
This application includes Chromium and other open-source software. See [LICENSES.chromium.html](./LICENSES.chromium.html) for complete third-party license information.

## Support

- **Issues**: [GitHub Issues](../../issues)
- **Discussions**: [GitHub Discussions](../../discussions)
- **Security**: See [SECURITY.md](./SECURITY.md) for security vulnerability reporting

## Changelog

See [CHANGELOG.md](./CHANGELOG.md) for version history and release notes.

## Roadmap

Features planned for future releases:
- [ ] Enhanced Raspberry Pi integration
- [ ] Real-time alerting system
- [ ] Cloud sync capabilities
- [ ] Mobile companion app

## Authors

- Project contributors and maintainers

## Acknowledgments

Built with:
- [Electron](https://www.electronjs.org/)
- [Chromium](https://www.chromium.org/)
- [Node.js](https://nodejs.org/)
- [Git](https://git-scm.com/)

---

**Version**: 43.4.1 (check [version](./version) file for current release)

For more information, visit the [GitHub repository](../../)
