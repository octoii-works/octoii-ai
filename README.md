# octoii-ai

Octoii's model vocabulary, provider drivers and transports. This Rust library has no dependency on
Siphon, Beak, the Agent host or product extensions.

The public modules cover model catalogues, requests and responses, streaming, provider protocols,
credentials interfaces and transport. Hosts supply credentials and choose providers; this repository
contains no user credentials. The sign-in fixtures under tests are test data.

## Build and test

Use the toolchain pinned in rust-toolchain.toml (Rust 1.100.0):

```sh
cargo check --locked --workspace --all-targets
cargo fmt --all --check
cargo clippy --locked --workspace --all-targets -- -D warnings
cargo test --locked --workspace
```

The live-model test is ignored by default and requires explicit configuration and invocation.
Use the public Cargo package:

```toml
[dependencies]
octoii-ai = "0.0.2"
```

Rust imports use `octoii_ai`. Source is provided under the included MIT license.

Initial extraction: octoii-works/octoii commit 057faa3, libs/octoii-ai. Source files and tests were
copied unchanged; only standalone workspace/build configuration and repository documentation were added.
