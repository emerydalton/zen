# /zen

tiny little language and tiny little loop

- /zendoc: read everything fresh, then write what you understand in plain English.
- /zen: write a thing the long way, only in the repo docs, to be read next.
- o7: end the session. Nothing is carried over but the docs.

The loop: /zendoc, /zen, /zendoc, /zen … until o7.

> **Status:** early design. Nothing here is stable yet — syntax, semantics, and tooling are all open for discussion.

## Repository layout

| Path        | Purpose                                              |
| ----------- | ---------------------------------------------------- |
| `spec/`     | Language specification (grammar, semantics)          |
| `src/`      | Reference implementation (compiler / interpreter)    |
| `examples/` | Example `/zen` programs                              |
| `tests/`    | Conformance and regression tests                     |
| `docs/`     | Guides and design notes                              |

## Getting started

There is no build yet. Once the reference implementation lands, build and run instructions will live here.

In the meantime:

- Read the [wiki](https://github.com/emerydalton/zen/wiki) for goals, roadmap, and design notes.
- Open an [issue](https://github.com/emerydalton/zen/issues) to propose or discuss a language feature.

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) and the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

[MIT](LICENSE)
