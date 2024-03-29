# Zero2Prod Coding Follow Along

## Dev Notes Re Installation
- Make sure libssl-dev is installed (WSL2)

## Commands

- Run Code Coverage Test with `cargo tarpaulin --ignore-tests`
- Run Cargo Watch with `cargo watch -x check -x test -x run`
- Run only tests with `cargo test`
- Run Linter with `cargo clipply`
- Enable CI pipeline fails when clipp emites warnings with `cargo clippy -- -D warnings`


## Formatting / rustfmt
- Install using `rustup component add rustfmt`
- Format project with `cargo fmt`
- CI pipeline step ` cargo fmt -- --check`

### Clippy

- Install using `rustup component add clippy`
- Mutes warning using the folloing attribute `#[allow(clippy::lint_name)]`
- Mute project wide by adding `#![allow(clippy::link_name)]` in cargo.toml


## Security Audit
- Install using `cargo install cargo-audit`
- Run using `cargo audit`
- 