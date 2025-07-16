# Zig Development Container

A complete Zig development environment using VS Code Dev Containers with the Zig compiler, ZLS language server, and essential development tools pre-installed.

## Features

- **Zig Compiler**: Version 0.14.1 (configurable)
- **ZLS Language Server**: Provides intelligent code completion, error detection, and more
- **Minisign**: For signature verification of downloaded packages
- **VS Code Extensions**: Pre-configured with essential Zig development extensions
- **Secure Installation**: All downloads are cryptographically verified using minisign

## Quick Start

1. **Prerequisites**
   - [Docker](https://docs.docker.com/get-docker/)
   - [VS Code](https://code.visualstudio.com/)
   - [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

2. **Clone this repository**
   ```bash
   git clone https://github.com/omar-el-mountassir/zig-devcontainer.git
   cd zig-devcontainer
   ```

3. **Open in VS Code**
   ```bash
   code .
   ```

4. **Reopen in Container**
   - VS Code will detect the dev container configuration
   - Click "Reopen in Container" when prompted
   - Or use the Command Palette (Ctrl+Shift+P) and run "Dev Containers: Reopen in Container"

## Configuration

### Zig Version

You can customize the Zig version by modifying the build args in `.devcontainer/devcontainer.json`:

```json
"build": {
    "dockerfile": "Dockerfile",
    "args": {
        "ZIG_VERSION": "0.14.1",
        "MINISIGN_VERSION": "0.12"
    }
}
```

### VS Code Extensions

The following extensions are automatically installed:

- `ziglang.vscode-zig` - Official Zig language support
- `ianic.zig-language-extras` - Additional Zig language features
- `lorenzopirro.zig-snippets` - Useful Zig code snippets
- `vadimcn.vscode-lldb` - LLDB debugger support
- `ms-azuretools.vscode-docker` - Docker support

## What's Included

- **Zig Compiler**: Latest stable version with automatic installation and verification
- **ZLS (Zig Language Server)**: For intelligent code analysis and completion
- **Development Tools**: Essential command-line tools for Zig development
- **Secure Setup**: All downloads are verified using cryptographic signatures

## Project Structure

```
.devcontainer/
├── devcontainer.json    # Dev container configuration
├── Dockerfile          # Container image definition
└── install-zig.sh      # Zig installation script with signature verification
```

## Development

Once the container is running, you'll have:

- Zig compiler available at `/home/vscode/.local/bin/zig`
- ZLS language server available at `/home/vscode/.local/bin/zls`
- All tools available in your PATH

You can start developing Zig applications immediately with full language support, debugging capabilities, and an optimized development environment.

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
