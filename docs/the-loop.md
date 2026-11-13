# The loop, written the long way

This note was written during a `/zen` turn on 13 November 2026. It is meant to be the next thing read. It assumes the reader remembers nothing and has only this repository.

Before writing, everything was read: the top-level `README.md` as of commit `4c4f355`, `CONTRIBUTING.md`, `CHANGELOG.md`, the code of conduct, the issue and pull request templates, the one-paragraph `README.md` in each of `spec/`, `src/`, `examples/`, `tests/` and `docs/`, and the five wiki pages (Home, Design Goals, Roadmap, FAQ, and the sidebar). There were no issues. There is no code, no specification, and no example.

Sentences in this note are one of two kinds. Where the repository says something, this note says "the README says". Everything else is a reading, and is labelled as one. Readings can be wrong and should be corrected here, in the docs, not anywhere else.

## What the README says

The README calls `/zen` a "tiny little language and tiny little loop". It defines three words and one sequence, and that is all of the design that exists today.

- `/zendoc`: read everything fresh, then write what you understand in plain English.
- `/zen`: write a thing the long way, only in the repo docs, to be read next.
- `o7`: end the session. Nothing is carried over but the docs.

The sequence is `/zendoc`, `/zen`, `/zendoc`, `/zen`, and so on, until `o7`.

## The three words, one at a time

These are readings.

**`/zendoc` is the reading half.** "Everything" means the whole repository, not the part that seems relevant. "Fresh" means reading as if for the first time, including pages you wrote yourself an hour ago, and trusting the page over your memory of it. The writing that follows is a check: if what you understood cannot be said in plain English, it was not understood, or the docs did not say it.

**`/zen` is the writing half.** "A thing" is singular: one turn, one piece of writing. "The long way" means full sentences with nothing left to be inferred: no shorthand, no "as discussed", no pointing at a conversation the reader was not in. "Only in the repo docs" means the writing goes in the repository and nowhere else, so that nothing important lives in a chat, a head, or a commit message. "To be read next" names the audience: the next `/zendoc`, which will arrive knowing nothing.

**`o7` is the ending.** It is a salute. After it, the session is gone, and the README says the only thing that survives is the docs. So anything not written down by then is lost on purpose.

Taken together, the docs are the only memory, and each half of the loop tests the other. A `/zen` is good if the following `/zendoc` can restate it correctly. A `/zendoc` is good if it finds what the last `/zen` got wrong or left out.

## Where the repository disagrees with itself

The README is the newest writing here; its three words were added on 13 November 2026, after everything else. The older pages describe something different:

- `CONTRIBUTING.md` calls `/zen` "a programming language for learning programming".
- The wiki Home page and FAQ call it "a new programming language".
- `spec/README.md` plans files for lexical structure, grammar and semantics. `src/README.md` expects a compiler or interpreter. The wiki Roadmap lists a lexer, a parser, a standard library, a formatter and a language server. The wiki Design Goals page asks about type systems and memory management.
- The README's own layout table still describes `src/` as a "compiler / interpreter" and `examples/` as "Example `/zen` programs".

Nothing in the repository says how the three words relate to a programming language with a grammar and a compiler. There are at least three ways they could:

1. **The loop is the language.** `/zen` is three words for working, and the compiler scaffolding is boilerplate left from the first commit, to be removed.
2. **The loop is the method.** `/zen` is a programming language still to be designed, and the three words are how the design gets done.
3. **Both.** A programming language for learning programming, whose own way of being built is the loop it teaches.

This note does not choose. That choice belongs to the owner of the repository.

## Questions, in the order they block other work

1. Which of the three readings above is right? Almost every other page waits on this.
2. Where does `/zendoc` write? The README says where `/zen` writes (the repo docs) but not where the plain-English understanding goes: into the docs, or only back to whoever asked.
3. What counts as "the repo docs"? The `docs/` directory only, or every Markdown file including `spec/`? The wiki is a separate git repository, so read strictly it is outside "the repo". This note took the narrowest reading and wrote only in `docs/`.
4. How big is "a thing"? One file, one decision, one section?
5. Who may say `o7`, and must anything be true first, for example that the last `/zen` has been read back once?
6. Who is a session? A person, a language model, or either. "Nothing is carried over" describes a model with no memory exactly, and a person only by discipline.

## What to write next

Answer question 1, in this directory, the long way. Once it is answered, the older pages listed above can be brought into line with the README, and either `spec/` gets its first real page or it goes away.
