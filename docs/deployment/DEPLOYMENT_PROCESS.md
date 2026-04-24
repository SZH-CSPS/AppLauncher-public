# Public Deployment Process

This repository receives public-facing deployment artifacts produced from the private source repository.

## Flow

1. Build and package artifacts in the private repository.
2. Upload release assets to this public repository.
3. Update [deployment/manifest.json](../../deployment/manifest.json) with version, URL, and SHA256.
4. Push manifest update to `main`.

## Manifest Requirements

- `latest_version` must match the published release tag.
- Artifact URL must target the corresponding release asset.
- SHA256 must match the published launcher zip.

## Release Assets

Expected assets per release:

- `SZH-AppLauncher-<version>-win64.zip`
- `SZH-AppUpdater.exe`
