# Changelog

## 2.1.0 - 2026-04-01

### Changed

- Removed the `axios` dependency in favor of an internal Node HTTP client with explicit JSON, text, binary, timeout, and redirect handling.
- Kept Deezer, Tidal, Spotify, YouTube, artwork, and Musixmatch requests on the same public library surface while making the transport layer dependency-light for publish.
- Updated the README download example and integration tests to use buffer-safe native Node networking instead of axios.

### Fixed

- Preserved binary downloads for encrypted audio, artwork, and test fixtures without relying on axios `arraybuffer` semantics.
- Preserved Deezer gateway retry behavior for auth refresh, gateway token refresh, and rate-limit backoff after the transport migration.

## 2.0.2 - 2026-03-26

### Changed

- Added an explicit npm package page link to the README for `@soulwax/d-fi-core`.
- Made the release lint scripts use the nested package's own ESLint config and plugin resolution.

### Fixed

- Published a fresh patch release so the scoped package page reflects the current package metadata and README content.

## 2.0.1 - 2026-03-26

### Changed

- Updated the npm license metadata to use a valid `SEE LICENSE IN LICENSE` expression.

### Fixed

- Corrected the README download example to use `trackData.trackUrl`.
- Aligned the README copyright and license note with the repository's current LICENSE file.
- Updated package ownership metadata to identify Christian Kling as the main developer.

## 2.0.0 - 2026-03-26

### Changed

- Renamed the npm package to `@soulwax/d-fi-core`.
- Updated package metadata to use the GitHub repository at `https://github.com/soulwax/d-fi-core`.
- Limited published npm package contents to runtime artifacts and release metadata.
- Moved the publish build hook to `prepublishOnly` so registry publishing no longer depends on install-time build behavior.

### Fixed

- Updated README and docs examples to use the scoped package name for install and import statements.
- Replaced the README FAQ link with a repository-local path so it follows the current default branch automatically.
- Allowed publish-time linting to work on Windows checkouts without normalizing the entire repository to LF first.
