# SeaQuery rusqlite binder 0.8.0-rc.15 backport

Source: <https://crates.io/api/v1/crates/sea-query-rusqlite/0.8.0-rc.15/download>.
The original `.crate` archive has SHA-256:

```text
9d42855d86ace6f5d9e425b65a8035d45c64e001db87a254ecfd87f226b4b0f7
```

The package records upstream revision
`46c58fb650d5e2d3ce835c5c671b16ebbe6c145c`, directory `sea-query-rusqlite`:
<https://github.com/SeaQL/sea-query/tree/46c58fb650d5e2d3ce835c5c671b16ebbe6c145c/sea-query-rusqlite>.

`Cargo.toml` and `src/` come from the cached published package.
The package version remains `0.8.0-rc.15`. Local changes are limited to:

- Change the actual `rusqlite` requirement from `0.37` to `0.41`.
- Enable `rusqlite/fallible_uint` to preserve the binder's unsigned integer
  conversions, which rusqlite 0.41 places behind this feature.
- Raise the declared Rust minimum to 1.89, as required by rusqlite 0.41.

This allows resolution to the fixed `libsqlite3-sys` line for
RUSTSEC-2026-0459. All source, the `sea-query` requirement `1.0.0-rc.10`,
and other feature settings remain unchanged. The published lockfile,
original pre-normalization manifest, and registry metadata are omitted.

The published package declares `MIT OR Apache-2.0` but contains no license files.
`LICENSE-MIT` and `LICENSE-APACHE` are copied unchanged from the upstream
repository root at the revision above:

- <https://github.com/SeaQL/sea-query/blob/46c58fb650d5e2d3ce835c5c671b16ebbe6c145c/LICENSE-MIT>
- <https://github.com/SeaQL/sea-query/blob/46c58fb650d5e2d3ce835c5c671b16ebbe6c145c/LICENSE-APACHE>

`BACKPORT.md` and these license files are additions to the published package.
