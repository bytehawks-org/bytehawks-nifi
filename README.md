# bytehawks-nifi
Bytehawks NiFi custom container image

# Bytehawks NiFi Custom Image

[![Build Status](https://github.com/bytehawks-org/bytehawks-nifi/actions/workflows/build-nifi.yml/badge.svg)](https://github.com/bytehawks-org/bytehawks-nifi/actions)
[![Security Scan](https://github.com/bytehawks-org/bytehawks-nifi/actions/workflows/build-nifi.yml/badge.svg?branch=main&event=push)](https://github.com/bytehawks-org/bytehawks-nifi/security/code-scanning)

[![Docker Pulls](https://img.shields.io/docker/pulls/bytehawks/bytehawks-nifi?style=flat-square&logo=docker)](https://hub.docker.com/r/bytehawks/bytehawks-nifi)
[![Docker Image Size](https://img.shields.io/docker/image-size/bytehawks/bytehawks-nifi/latest?style=flat-square&logo=docker)](https://hub.docker.com/r/bytehawks/bytehawks-nifi)

![NiFi Version](https://img.shields.io/badge/NiFi-2.7.2-728e9b?style=flat-square&logo=apache)
![Python Version](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white)
[![License](https://img.shields.io/github/license/bytehawks-org/bytehawks-nifi?style=flat-square)](LICENSE)

## Overview

This repository contains the source code and configuration for a custom Apache NiFi container image, maintained by Bytehawks. The image is designed to provide a robust, extensible, and production-ready environment for running NiFi workflows.

## Features

- Based on the official Apache NiFi Docker image
- Pre-installed Python 3 most useful extensions
- Optimized for cloud and container orchestration platforms (e.g., Kubernetes)
- Secure default configuration
- Automated build and deployment pipelines

## Getting Started

### Prerequisites

- Docker or compatible container runtime
- (Optional) Kubernetes or Docker Compose for orchestration

### Building the Image

```bash
git clone https://github.com/bytehawks-org/bytehawks-nifi.git
cd bytehawks-nifi
docker build -t bytehawks-nifi:latest .
```

### Running the Container

```bash
docker run -d -p 8080:8080 --name nifi bytehawks-nifi:latest
```

Access the NiFi UI at [http://localhost:8080/nifi](http://localhost:8080/nifi).

### Configuration

You can customize NiFi properties and configuration files by mounting volumes or using environment variables. Refer to the [Apache NiFi documentation](https://nifi.apache.org/docs.html) for available options.

## Deployment

This image can be deployed on any container platform. Example Kubernetes deployment manifests and Helm charts are available in the `deploy/` directory.

## Contributing

Contributions are welcome! Please open issues or submit pull requests for bug fixes, enhancements, or new features.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact [info@bytehawks.org](mailto:info@bytehawks.org).
