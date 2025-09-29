# Llama Stack Documentation

DONOT MAKE CHANGES TO THIS REPOSITORY DIRECTLY

This repository hosts the GitHub Pages documentation site generated from documentation in [Llama Stack](https://github.com/llamastack/llama-stack).

🔗 **Live Documentation**: https://llamastack.github.io

## Overview

This repository automatically syncs and builds documentation from the main Llama Stack repository using GitHub Actions. The documentation is built using **Docusaurus** and served as static HTML via GitHub Pages.

### Architecture

- **Current Documentation**: Built with Docusaurus from the main repository
- **Legacy Versions**: Preserved Sphinx builds (v0.2.11 - v0.2.22) available at `/legacy/vX.Y.Z/`
- **Version Management**: Uses Docusaurus native versioning with `versionsArchived.json` for legacy versions

## Updates

- Manually via GitHub Actions workflow dispatch

## Local Development

To manually build and test the documentation locally:

```bash
# Clone this repository
git clone https://github.com/llamastack/llamastack.github.io.git
cd llamastack.github.io

# Run the new Docusaurus build (requires Python 3, Node.js 20+, npm)
./local-build-test.sh

### Testing URLs After Build

- **Main site**: http://localhost:8000/docs/
- **Legacy versions**: http://localhost:8000/legacy/v0.2.22/
- **Root redirect**: http://localhost:8000/ (should redirect to `/docs/`)

The `run-docusaurus-local.py` script simulates the GitHub Actions workflow locally, providing the same build process as the CI/CD pipeline.

## Contributing

Documentation content should be contributed to the main [Llama Stack repository](https://github.com/llamastack/llama-stack/tree/main/docs). This repository only hosts the built documentation.
## License

See the [Llama Stack repository](https://github.com/llamastack/llama-stack) for license information.
