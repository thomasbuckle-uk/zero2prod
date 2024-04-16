# Zero2Prod Coding Follow Along

## Dev Notes Re Installation
- Make sure libssl-dev is installed (WSL2)
-  `sudo apt install pkg-config`
-  `sudo apt-get install libudev-dev`

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

## Bunyan

- Used to prettify outputted logs from tests
- to install `cargo install bunyan`
- example usage: ` cargo test health_check_works | bunyan`

## Security Audit
- Install using `cargo install cargo-audit`
- Run using `cargo audit`



---

## Database

Make sure psql & sqlx are both installed, then run the bash script

```shell
./scripts/init_db.sh
```

To run migrations without having to down the postgres container each time use:
```shell
SKIP_DOCKER=true ./scripts/init_db.sh
```