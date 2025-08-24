# SLSA + SBOM Example in Go

This project demonstrates how to integrate [SLSA](https://slsa.dev) (Supply-chain Levels for Software Artifacts) provenance with an [SBOM](https://www.cisa.gov/sbom) (Software Bill of Materials) for a simple Go application. It provides a minimal working example that you can adapt to secure your own Go projects.

## Features
- **Go application** – A small sample Go program.  
- **SBOM generation** – Produces a CycloneDX or SPDX SBOM describing dependencies.  
- **SLSA provenance** – Attaches provenance metadata to the build for supply-chain integrity.  
- **Reproducible build workflow** – Example GitHub Actions pipeline included.