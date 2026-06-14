# Build Flow

Builds for this repo flow through the shared `cepheus-build` system and the Cepheus Linux server (`errai`).

- Use `../cepheus-build/bin/cepheus-build build -p <product> <target>` for local or release builds when this repo is modeled in `cepheus-build/products/`.
- GitHub Actions in product repos should stay thin callers into `CepheusLabs/cepheus-build` reusable workflows. Do not add repo-local build orchestration that bypasses the shared build repo.
- The default self-hosted runner path is the Linux runner on `errai`. Windows and macOS work may run in dedicated VMs or hardware, but dispatch, versioning, artifacts, signing gates, and deploy handoff still belong to `cepheus-build`.
- Library and package repos that feed products should be built through the consuming product's `cepheus-build` target, or wired into `cepheus-build/products/*.toml` before adding new CI.
- Server/container deployments should be handed off through the Linux server path documented in the relevant deployment guide, with `cepheus-build` remaining the source of truth for build inputs and artifacts.

