# /zen

a tiny protocol for a way of working

Three words, said by a person and carried out by hand:

- /zendoc: read everything fresh, then write what you understand in plain English.
- /zen: write a thing the long way, only in the repo docs, and commit it, to be read next.
- o7: end the session. Nothing is carried over but the docs.

The loop: /zendoc, /zen, /zendoc, /zen … until o7.

## What this is

/zen is a way of working where nothing is remembered except what gets written down.

Every session starts blank. It has this repository and nothing else. So it reads everything, says back what it understood, writes one thing down for whoever comes next, commits it, and leaves.

```
   session one               session two
 /zendoc -> /zen   o7      /zendoc -> /zen   o7
    ^         |               ^         |
  reads     writes          reads     writes
    |         v               |         v
 +------------------------------------------+
 |                repo docs                 |
 +------------------------------------------+
```

Nothing passes directly from one session to the next. Everything goes through the docs. A session that ends without a commit leaves nothing behind, so as far as the loop is concerned it never happened.

Think of it as leaving notes for a stranger who happens to be you tomorrow. If the next /zendoc comes back wrong, the docs were unclear, and the next /zen fixes them.

## What this is not

/zen is not a language. The three words are a protocol, or a ritual. They are like "over" and "out" on a radio: they organise the talking without being the talk. They cannot be combined to say anything new, and they carry no content of their own. Everything the loop actually says is written in plain English, in the docs.

/zen is not a set of commands to install either. Each step is done by hand, in the open, so that how it works can be seen.

The substance is the practice: read fresh, write it down, commit, leave.

## Where things are

[`docs/`](docs/) is where /zen writes. Every session begins by reading all of it.

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) and the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

[MIT](LICENSE)
