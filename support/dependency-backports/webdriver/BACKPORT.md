# WebDriver 0.53.0 backport

Source: <https://crates.io/api/v1/crates/webdriver/0.53.0/download>.
The original `.crate` archive has SHA-256:

```text
91d53921e1bef27512fa358179c9a22428d55778d2c2ae3c5c37a52b82ce6e92
```

The package records upstream revision
`2c83250e67d85c2a172670b08cd88753d1552d91`, directory `testing/webdriver`:
<https://github.com/mozilla/gecko-dev/tree/2c83250e67d85c2a172670b08cd88753d1552d91/testing/webdriver>.

`Cargo.toml`, `README.md`, and `src/` come from the cached published package.
The package version remains `0.53.0`. Local changes are limited to:

- Remove the unused `cookie` dependency from `Cargo.toml`.
- Remove `extern crate cookie;` from `src/lib.rs`.
- Enable the `log` macro import only with the `server` feature, its only user,
  so path consumers without that feature also build with warnings denied.

This removes the dependency carrying RUSTSEC-2026-0594 without changing
WebDriver's protocol cookie types. All other source and manifest settings
remain unchanged. The published lockfile, original pre-normalization manifest,
and registry metadata are omitted.

The published package declares `MPL-2.0` but contains no license file.
`LICENSE` contains Mozilla's full MPL 2.0 text from
<https://www.mozilla.org/media/MPL/2.0/index.txt>.
Existing source license notices are preserved. `BACKPORT.md` and `LICENSE`
are additions to the published package.
