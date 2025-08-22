[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/tyler36/ddev-netdata/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/tyler36/ddev-netdata/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/tyler36/ddev-netdata)](https://github.com/tyler36/ddev-netdata/commits)
[![release](https://img.shields.io/github/v/release/tyler36/ddev-netdata)](https://github.com/tyler36/ddev-netdata/releases/latest)

# DDEV Netdata

## Overview

This add-on integrates Netdata into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get tyler36/ddev-netdata
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Netdata |
| `ddev netdata` | Launch local Netdata UI |
| `ddev logs -s netdata` | Check Netdata logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.netdata --netdata-docker-image="ddev/ddev-utilities:latest"
ddev add-on get tyler36/ddev-netdata
ddev restart
```

Make sure to commit the `.ddev/.env.netdata` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `NETDATA_DOCKER_IMAGE` | `--netdata-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
