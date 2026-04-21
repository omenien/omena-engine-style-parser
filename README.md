# `engine-style-parser`

Internal Rust crate for the parser/public-product track.

Current scope:

- style-language detection for `.module.css`, `.module.scss`, `.module.less`
- byte-span tokenization
- shallow stylesheet parsing into rule / at-rule / declaration / comment nodes
  with structured prelude / header / value payloads
- parser diagnostics for unterminated comments, strings, and blocks
- bounded Rust-vs-TS parity and CSS Modules intermediate producer binaries
- parser canonical-candidate / canonical-producer artifacts over those bounded outputs

Non-goals in this first scaffold:

- no TS/runtime integration yet
- no public package commitment

Standalone checks:

- `cargo test`
- `cargo fmt --all --check`
- `cargo clippy --all-targets --all-features -- -D warnings`

Extraction note:

- this branch is a standalone scaffold prototype derived from a history-preserving subtree split
- repository branding is applied at the repo layer
- crate naming stays `engine-style-parser` for the first extraction to minimize migration noise

Current naming stance:

- keep crate name: `engine-style-parser`
- use branded repository naming separately from crate naming

Repository:

- GitHub: `omenien/omena-engine-style-parser`
- CI: `.github/workflows/ci.yml`
