# Straight to main

This note was written during a `/zen` turn on 13 November 2026. It records one rule about how writing gets into this repository. It assumes the reader remembers nothing and has only this repository.

## What the owner said

The owner of the repository was asked whether a new note should go in as a pull request on a branch, or directly onto the `main` branch. The answer, word for word, was:

> straight to main always less not possible
>
> /zen
>
> written so no scary
>
> easily undo
>
> ?zen

Everything below this line is a reading of those words. If the reading is wrong, correct it here.

## The rule

Every `/zen` is committed directly to the `main` branch and pushed. No branch is made and no pull request is opened. The only exception is when pushing to `main` is not possible, for example because the session has no permission to push. In that case the session says so plainly and uses the nearest thing that is possible, such as a branch.

## Why this is not scary

Going straight to `main` sounds risky. It is made safe by two habits, which are the other half of the rule.

**Each `/zen` is exactly one commit.** One thing written, one commit made. A commit never mixes two things. The commit's subject line says what the thing is in plain words.

**Each commit is easy to undo.** A `/zen` only adds or changes Markdown under `docs/`. It does not rename files, delete other people's writing, or rewrite history. So any single `/zen` can be taken back without disturbing any other.

## How to undo one

Find the commit:

```
git log --oneline -- docs/
```

Take it back, using the short code printed at the start of its line:

```
git revert <code>
git push
```

This does not erase anything. It adds a new commit that reverses the old one, so the undo can itself be undone the same way. Nothing in this repository should ever need `git push --force` or `git reset --hard`; if one of those seems necessary, stop and ask the owner.

## What this replaces

`CONTRIBUTING.md` still tells contributors to fork, branch, and open a pull request, and the pull request template has a checklist. That page was written before this rule and has not been changed. Whether the rule here applies to everyone or only to sessions working with the owner is not yet said.

## Not yet understood

The owner's message ended with `?zen`. The README defines `/zendoc`, `/zen` and `o7`, and does not define `?zen`. Two readings are possible: it is a fourth word, perhaps meaning "ask a question instead of writing", or it was simply the owner asking "is this zen?" about the rule above. This note does not choose.
