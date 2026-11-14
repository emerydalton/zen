# What /zen is

> /zen is a language and a set of a few repeated steps, all of them really simple.

That sentence is the whole idea. This page says it the long way, so that anyone
arriving at the repository can understand what is being built before any syntax
exists. Nothing here is final. It records the idea as it stands today and marks
clearly what has not been decided.

## Two things, not one

Most programming languages describe themselves as a language and stop there: a
grammar, some rules for what the words mean, and a tool that runs the result.
/zen describes itself as two things that belong together.

**A language.** There is something you write. It has words and rules like any
other language, and a program written in it can be read by a person and run by
a machine.

**A set of steps.** There is also something you do. /zen comes with a small
routine, a handful of steps you carry out in the same order every time you sit
down to work. The steps are part of /zen in the same way the grammar is. You
have not learned /zen if you only know what to type; you have learned it when
you also know what to do.

Putting the two side by side is deliberate. /zen is a programming language for
learning programming, and what beginners usually lack is not vocabulary. It is
a way of working: knowing what to do first, what to do next, and what to do
when stuck. /zen tries to hand over that way of working along with the words.

## Few

There are only a few steps. The exact number is not settled, but the intent is
that a learner can hold all of them in their head at once, without a chart on
the wall. If the list ever grows long enough that someone has to look it up,
it has grown too long.

The same pressure applies to the language. A small language can be learned
completely. A learner who knows the whole of a small thing is in a much
stronger position than one who knows a tenth of a large thing.

## Repeated

The steps are the same every time. They do not change with the size of the
program, the experience of the person, or the kind of problem. A first program
and a hundredth program are made by going around the same loop.

Repetition is how the steps turn from instructions into habit. The first few
times, the learner follows them on purpose. After enough rounds they stop
being something to remember and become simply how the work is done. That
habit is the thing /zen most wants a learner to leave with, because it carries
over to every other language they will ever use.

## Really simple

Every part is meant to be really simple: each step, each piece of the
language, and the way the two fit together. Simple here means that each part
can be explained in a sentence or two to someone who has never programmed,
and that the explanation is the whole truth rather than a convenient
half-truth to be corrected later.

Simplicity is the rule that settles arguments. When a proposed feature or an
extra step would make /zen more capable but harder to explain, the simpler
choice wins.

## What this rules out

Taken seriously, the sentence at the top already excludes some things:

- A language that is small on the surface but needs a long list of special
  cases to explain.
- A routine with many steps, optional steps, or steps that differ by
  situation.
- Anything a learner is told to type or do "for now" without being able to
  understand why.

## The steps so far

Two steps have been named. Their place in the full set is not yet decided.

- **`/zendoc`** gathers the recent context from scratch and prints, in plain
  English, what is understood. It comes first: there is no coding in /zen
  without it.
- **`/zen`** says a thing the long way and keeps it only in the repository
  docs. This page is an example of it.

## Not yet decided

- The full list of steps, their names, and their order.
- What the language looks like: its words, its grammar, its meaning.
- How the steps and the language meet. The steps might be things a person
  does around the code, or things written in the code itself.
- Everything listed as an open question in the wiki's Design Goals page:
  compiled or interpreted, the type system, memory management, and the
  language the reference implementation is written in.
