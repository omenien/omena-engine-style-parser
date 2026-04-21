# `engine-style-parser`

Rust parser crate for the parser/public-product track.

Current scope:

- style-language detection for `.module.css`, `.module.scss`, `.module.less`
- byte-span tokenization
- shallow stylesheet parsing into rule / at-rule / declaration / comment nodes
  with structured prelude / header / value payloads
- parser diagnostics for unterminated comments, strings, and blocks
- bounded Rust-vs-TS parity and CSS Modules intermediate producer binaries
- parser canonical-candidate / evaluator-candidates / canonical-producer artifacts
- parser public-product and consumer-boundary validation over those bounded outputs

Current boundary:

- standalone repo created from a history-preserving subtree split of the monorepo parser crate
- crate name stays `engine-style-parser`
- repository naming is branded separately as `omena-engine-style-parser`
- repo CI requires the `rust` status check on `main`

Non-goals in this current scaffold:

- no public package commitment
- no crates.io publish flow
- no parser runtime replacement promise outside the bounded validation surface

Standalone checks:

- `cargo test`
- `cargo fmt --all --check`
- `cargo clippy --all-targets --all-features -- -D warnings`

Repository:

- GitHub: `omenien/omena-engine-style-parser`
- CI: `.github/workflows/ci.yml`
