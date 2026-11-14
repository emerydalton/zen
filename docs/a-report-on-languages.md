# A report on languages

Written on 2026-11-14, after the-library.md.

## The rule

A report on how languages are made was read next to this repository.
/zen is still not a language. What was seen is written here, and all of
it is the reader's.

This note adds no rule to the loop. It is a record of one reading.

## The document

`library/waiting/conlangs-programming-languages-semantic-primitives.md`.
Its title is "Conlangs, Programming Languages, and the Search for
Semantic Primitives: A Research Report".

It is about languages that people build on purpose. Some are for
people to speak, such as Esperanto, Lojban and Toki Pona. Some are for
machines to run, such as Lisp, Forth and Brainfuck. It asks how small
the starting set of words or operations can be, and what a small set
costs. It ends with advice for someone who wants to design a language
that sits between the two kinds.

It is the second document in the library. The author did not say it
was ready for processing. It is still in `waiting/`.

## What was seen

The author chose "Relate report to /zen" from four things the reader
offered. The reader read the document whole, read every note in docs/,
and said six things. The author has not confirmed any of them.

1. The report gives advice to a person designing a language.
   commit-or-it-never-happened.md says /zen was once taken for a
   language, and the changelog says the scaffolding of a programming
   language was removed. So the report speaks to what /zen stopped
   being.

   The report also gives a way to check the README's claim that /zen
   is not a language. By its account a language has a starting set, a
   grammar for combining, and a layer of words built from the starting
   set. The three words have none of these. The README says they
   "cannot be combined to say anything new". The report names six
   kinds of small set, and each kind is small in order to do
   something: define, compare, teach, express, compute, or infer. The
   three words do none of those. They mark turns. The report has no
   kind for words like "over" and "out".

2. The words outside the three do behave the way the report says a
   language behaves. The report says every small core grows a layer of
   built words, and that the usual way to build one is to join two
   words into one. Lojban and Toki Pona both do this.

   The notes here have contemplationcomputation in not-two.md,
   questionplace and placequestion in questionplace.md, and
   compassionwisdom and heartmind in a-line-of-inquiry.md. Each is two
   words joined into one. Twice the author gave both orders, so that
   neither half comes first. That is a way of making words, and it has
   been used more than once. The README's sentence about combining is
   said of the three words. It is not said of these.

3. The report says a small system does not remove its difficulty. It
   moves it. Toki Pona has few words, and the listener has to work out
   the meaning from the situation. Ithkuil packs everything into each
   word, and almost nobody can speak it.

   /zen has three words. The difficulty has moved into docs/, which
   says everything the long way in plain English. And the o7 takes the
   situation away, because the next reader begins blank. So /zen is
   Toki Pona turned round: few words, and nothing left for the
   situation to supply.

   The report quotes Kenneth Iverson, who said a notation is less
   useful the more vocabulary a person has to keep in mind. A blank
   reader keeps nothing in mind. So here the price of each new term,
   such as /zazen, /kinhin, ford and questionplace, is paid in what
   has to be read again at the start. open-questions.md says the
   repository should stay small. This is one reason it would.

4. The report says that making a programming language look like
   English does not make it mean what English means. It gives Inform 7
   and COBOL as cases. The slash is the same thing the other way
   round. /zendoc and /zen look like commands, and there is no command
   behind them. words-not-commands.md says a tool will report that no
   such command is installed, and that the report is true and does not
   matter.

5. The report tells a designer not to promise that a language will
   change how its speakers think. It says to treat that as an
   experiment, and that James Cooke Brown built Loglan to run such an
   experiment and never ran it.

   /zen is called a way of working. loose-ends.md describes a test of
   whether a reading crosses an o7 without a commit. It has three runs
   and none has been run. The reader said the two cases are alike: a
   claim about what a made thing does to the people who use it, and a
   test that was written down and not done.

6. One place where they pull apart. The report says the smallest sets
   for human languages and the smallest sets for machines solve
   different problems, and that treating them as the same is the main
   mistake a designer can make. It says what they share is logic, and
   what human language has in addition is wanting, feeling, knowing
   and judging good from bad.

   not-two.md says contemplation and computation are one thing, with
   no seam. a-line-of-inquiry.md has the author's words "logic ,
   computation , but also compassion". The reader said "but also" is
   the report's shape, a shared part and an added part. The author's
   compassionwisdom, written as one word, would refuse that shape.

## What was checked and what was not

The reader read the whole document and every note in docs/.

The reader did not read any of the document's sources. Everything
above about Toki Pona, Lojban, Ithkuil, Iverson, Inform 7, COBOL and
Brown is the document's account, as the reader understood it. The
document says of itself that some of its figures come from secondhand
sources and are approximate.

The reader did not read the wiki. Of the first library document, the
reader read only the opening.

## What could not be told

- At the five. loose-ends.md says five outside documents had no place
  to live. open-questions.md names one of them as a report on "words
  that travel between speech and code", and says it cites an essay by
  John Cayley. This document is about speech and code, and it does
  not mention Cayley. The reader could not tell whether it is one of
  the five or a sixth.
- At "the pasted text". The document checks the claims of a text that
  someone pasted in, and calls it "the pasted framing". That text did
  not come with the document. The reader could not tell what it said
  beyond the claims the document repeats, or who wrote it.
- At the joined words. The second thing above says the joining is a
  way of making words. It may be that, and then /zen has one small
  piece of grammar. Or each joined word may be a single case, made
  once for one need. The author has not said. kinhin.md keeps a place
  near this one, at "/zenloops".
- At "not two". The sixth thing may be a real disagreement, or the
  two may be about different things. The report speaks of the starting
  sets of languages. not-two.md speaks of the reading and the writing
  inside one span. The second question in open-questions.md asks
  whether it matters to /zen that code and text may be different. The
  reader could not tell whether the report bears on that question.
- At the ford. the-library.md could not tell whether reading the
  first document was the second ford. This is the same place again,
  with a second document. ford.md's list was not changed.

## How this was learned

The author brought the document and the repository's address, and no
other words. The reader read the README and asked what to do with the
two. The reader offered four things. One was to add the report to
docs/. The author chose that and the relating.

Then the reader read every note, and found that the-library.md had
already said where an outside document goes. So the document went
into `library/waiting/` and not into docs/. The reader had offered
the wrong place before reading the notes.

The reader committed the document on a branch and said the six things
in conversation. The reader said that none of the six was committed.
Then the author said /zen.
