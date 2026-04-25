# `omena-engine-style-parser`

Parser and CSS Modules intermediate extractor for Omena CSS analysis.

Current scope:

- style-language detection for `.module.css`, `.module.scss`, `.module.less`
- byte-span tokenization
- shallow stylesheet parsing into rule / at-rule / declaration / comment nodes
  with structured prelude / header / value payloads
- parser diagnostics for unterminated comments, strings, and blocks
- bounded Rust-vs-TS parity and CSS Modules intermediate producer binaries
- parser canonical-candidate / canonical-producer artifacts over those bounded outputs
- Sass symbol seed facts in the CSS Modules intermediate producer for variables,
  mixins, functions, static `@use` / `@forward` / `@import` module edges, and
  `@use` namespace seeds
- same-file Sass resolution seeds for variables, mixin includes, and declared
  function calls
- selector attachment seeds for Sass variable refs, mixin includes, and
  declared function calls
- selector-scoped Sass symbol occurrence facts with same-file resolution status,
  byte spans, and shared-style text ranges

Non-goals in this first scaffold:

- no TS/runtime integration yet
- no provider-facing Sass symbol feature yet
- no cross-file Sass module resolution yet

Primary check:

- `cargo fmt --all --check`
- `cargo test`
- `cargo clippy --all-targets --all-features -- -D warnings`
- `cargo publish --dry-run`

Monorepo release-facing bundle:

- `pnpm check:rust-release-bundle`
