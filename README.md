# currency-server-mcp

[\![Release](https://github.com/day0ops/currency-server-mcp/actions/workflows/release.yml/badge.svg)](https://github.com/day0ops/currency-server-mcp/actions/workflows/release.yml)
[\![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[\![Image](https://img.shields.io/badge/registry-GAR-4285F4?logo=google-cloud)](https://console.cloud.google.com/artifacts/docker/field-engineering-apac/australia-southeast1/kasunt)

MCP server providing live currency exchange rates, built with [FastMCP](https://github.com/jlowin/fastmcp).

## What it does

Exposes currency conversion tools over the Model Context Protocol (MCP), allowing LLM agents to fetch real-time exchange rates.

## Usage

```bash
# Build image locally
make build IMAGE_TAG=latest

# Push to registry
make push IMAGE_REPO=australia-southeast1-docker.pkg.dev/field-engineering-apac/kasunt IMAGE_TAG=<tag>

# Deploy to Kubernetes
make deploy IMAGE_REPO=australia-southeast1-docker.pkg.dev/field-engineering-apac/kasunt IMAGE_TAG=<tag>

# Tail logs
make logs
```

## Requirements

- Kubernetes cluster with agentgateway installed (`agentgateway-system` namespace)
- `kubectl` configured for the target cluster
