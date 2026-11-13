# Changelog

All notable changes to /zen are recorded here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- Repository scaffolding: README, contributing guide, code of conduct, issue and pull request templates.
- `docs/commit-or-it-never-happened.md`: every session must commit to `docs/` before `o7`.
- `docs/words-not-commands.md`: `/zendoc`, `/zen` and `o7` are words done by hand, not commands to install.
- README: a "What this is not" section.
- README: a "The repo" section, saying that the repo's persistence is what makes the whole thing work.

### Changed

- README: /zen is described as a protocol for a way of working, not a language. The tagline is now "a tiny protocol for a way of working, held up by a repo".
- README: `/zen` now ends in a commit, and `docs/` is no longer described as empty.
- `docs/README.md`: no longer says that nothing is written.
- README: the loop is now written as … o7 … /zendoc … o7 … /zen … o7 …, with `o7` as the boundary between every stretch of work. From o7 to o7 is /zen.
- `docs/commit-or-it-never-happened.md`: the order is now given as the work, then the commit, then `o7`.

### Removed

- Programming-language scaffolding (`spec/`, `src/`, `examples/`, `tests/`, the language proposal template) and the two notes in `docs/`. The repository starts again from the README's three words.
