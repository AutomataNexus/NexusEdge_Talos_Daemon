# Contributing to NexusEdge Hailo Community Edition

Thank you for your interest in contributing to NexusEdge.

## How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## Development Setup

```bash
# Install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# Install Trunk (WASM bundler)
cargo install trunk

# Install system dependencies (Debian/Ubuntu)
sudo apt-get install -y libwebkit2gtk-4.1-dev libgtk-3-dev \
  libayatana-appindicator3-dev librsvg2-dev

# Build frontend
trunk build

# Build backend
cargo build -p nexusedge-tauri

# Run
cargo run -p nexusedge-tauri
```

## Code Style

- Run `cargo fmt` before committing
- Run `cargo clippy -- -D warnings` — zero warnings policy
- No `unsafe` without a safety comment explaining why

## What We Accept

- Bug fixes
- Documentation improvements
- New sensor signal types
- I/O board driver improvements
- Performance optimizations
- Accessibility improvements

## What Requires Discussion First

- New control algorithms (open an issue first)
- UI/UX changes (open an issue with mockups)
- New dependencies (minimize dependency count)
- Changes to the Hailo NPU integration

## License

By contributing, you agree that your contributions will be licensed under the Apache License 2.0.

## Contact

devops@automatanexus.com
