# Conlangs, Programming Languages, and the Search for Semantic Primitives: A Research Report

There is no single universal "minimal word set": the pasted framing is right that the answer depends on the domain, but several of its specific claims are wrong or garbled. Human-language primitives (NSM's 65 primes, Toki Pona's ~120–137 words) and machine primitives (NAND, S and K, SUBLEQ) solve different problems. Treating them as the same thing is the main conceptual trap for anyone designing a language at this intersection.

## TL;DR

- **Conlangs and programming languages are one craft with two audiences.** Both pick primitives, a grammar and a goal. Their histories meet in specific places: Loglan/Lojban (a YACC-parsable human language), Inform 7 (English-like code), Hedy (code in local languages), esolangs (programming languages built as art) and, more recently, languages designed for LLMs to write.
- **Fact-check of the pasted text:** the NSM count of ~65 primes is correct, but the list shown is incomplete and puts some primes in the wrong groups. The Ogden "90% of everyday communication" claim is a distortion. The "top 100 words = understand 50% of a text" claim confuses token coverage with comprehension. Böhm–Jacopini and NAND/NOR are broadly correct but need caveats. The physics "four primes" is not a recognized framework.
- **Practical takeaway:** minimality and usability pull against each other in both domains. Turing tarpits like Brainfuck and Iota show that a tiny core is cheap. Toki Pona's ambiguity and Ithkuil's density show that the cost moves into the speaker's head. Design a small, well-chosen core, then build a rich layer of derived vocabulary or libraries on top of it.

## Key Findings

1. **Natural Semantic Metalanguage (NSM) does list 65 primes, and the inventory has been stable since 2014.**\[1\] It grew from 14 in Wierzbicka's 1972 *Semantic Primitives* to 60 in 2002, 63 in Goddard (2011), and 65 in Goddard & Wierzbicka (2014).\[2\] NSM is a joint program of Anna Wierzbicka and Cliff Goddard, not Wierzbicka's alone.\[3\] Its universality claim remains an empirical hypothesis, not settled fact.
2. **The pasted Ogden claim misstates the original.** The Basic English literature claims that 90% of the *concepts in the 25,000-word Oxford Pocket English Dictionary* can be expressed with 850 words.\[4\] It does not claim 850 words cover 90% of everyday communication.
3. **The "top 100 words" claim confuses frequency with understanding.** According to the Oxford English Corpus analysis (over 2 billion words), the top 100 lemmas "account for 50% of all the words" in the corpus, with the top 10 alone accounting for about 25%. They are almost all function words (the, be, to, of, and…). Knowing them does not let you understand half of a text.
4. **Computational minimal sets are real theorems, but they come with caveats.** Sequence/selection/iteration (Böhm–Jacopini 1966) needs extra boolean variables, and Böhm showed that selection itself can be removed. NAND or NOR alone is functionally complete for Boolean functions, but Boolean logic is not Turing-complete without memory and loops. S and K, the single Iota combinator, or the single SUBLEQ instruction are each computationally universal.\[5\]\[6\]\[7\]\[8\]
5. **The physics "Space / Time / Matter-Energy / Information" scheme is a pop-philosophical simplification.** No physics framework names these as "ontological primes." The genuine philosophical lineage is Aristotle's categories, Kant's table of categories and Peirce's three categories.
6. **The intersection is real, active and has a history.** Brown created Loglan explicitly to test Sapir–Whorf. Lojban's grammar is specified in YACC/EBNF. Iverson argued programming notation is a "tool of thought." Graham's "Blub paradox" is a linguistic-relativity argument about programmers.\[9\]\[10\]\[11\] In 2025, research languages such as Pel and Quasar were designed specifically for LLMs to generate.

## Details

### 1. Conlangs: history, types and design goals

**Philosophical / a priori languages (17th century).** These tried to build a language whose words *encode* a classification of reality.
- **John Wilkins, *An Essay Towards a Real Character, and a Philosophical Language* (1668).** Wilkins organized all knowledge into 40 major genera, subdivided into 251 "characteristic differences" and then species. Each word spells its own place in the taxonomy. Eco gives the example: if *De* means Element, *Deb* is the first difference (Fire) and *Debα* the first species (Flame). The tables run to roughly 270 folio pages.\[12\] Wilkins' Real Character was a written symbol system; his Philosophical Language assigned sounds to it. Borges' essay "The Analytical Language of John Wilkins" made the project famous as a cautionary tale about arbitrary taxonomy.\[13\]
- **Leibniz's *characteristica universalis*.** Leibniz imagined an "alphabet of human thought": simple concepts would be assigned primes (he experimented with number encodings), and complex concepts would be their products, so reasoning could become calculation. It is the direct ancestor of both NSM-style primitives and formal logic and programming.

**International auxiliary languages (auxlangs).** Volapük (Johann Martin Schleyer, 1879) came first. Esperanto (L. L. Zamenhof, 1887) is the most successful, partly because it was, in David Peterson's word, "open source." Ido is an Esperanto offshoot;\[14\] Occidental and Interlingua are naturalistic auxlangs. Ogden's Basic English (1930) is a different strategy: a *controlled subset* of English rather than a new language. It reduced English verbs to about 18 "operators," so "eat" becomes "have a meal" and "forget" becomes "go from memory." Critics note that Ogden himself did not write in Basic.\[15\] Its "850 words" also lean heavily on polysemy and English idiom.\[16\]

**Logical / engineered languages (engelangs, loglangs).**
- **Loglan.** James Cooke Brown began Loglan in 1955 and introduced it in *Scientific American* in 1960. He built it to test the Sapir–Whorf hypothesis: whether people speaking a "logical language" would think differently.\[17\]
- **Lojban.** Lojban was developed from 1987 by the Logical Language Group after disputes with Brown over Loglan's ownership. Its official grammar is defined in YACC, with a more readable EBNF version; in case of discrepancy, "the YACC version is official."\[9\]\[18\] It has about 1,350 root words (gismu); the official list has 1,342.\[19\]\[20\] The phonetic forms of gismu were generated algorithmically from similar words in major world languages, weighted by number of speakers.\[21\] The project describes Lojban as "machine parsable: the syntactic structure of a sentence is unambiguous and can be checked with software."\[18\]
- **Ithkuil.** John Quijada's Ithkuil is "a cross between an a priori philosophical and a logical language." Versions appeared in 2004, as Ilaksh in 2007, in 2011, and as New Ithkuil in February 2023. It is extraordinarily dense: two words, *Tram-mļöi hhâsmařpţuktôx*, translate as "On the contrary, I think it may turn out that this rugged mountain range trails off at some point."\[22\] Community documentation reports that New Ithkuil has a lexicon of several thousand consonantal roots plus hundreds of affixes.\[23\] Quijada says Ithkuil is not meant for everyday use, and he doubts claims that it would speed up thought.\[24\]

**Minimalist languages.**
- **Toki Pona.** Sonja Lang published first drafts online in 2001. *Toki Pona: The Language of Good* (2014, "pu") advertises 120 words but actually contains 123. *Toki Pona Dictionary* (2021, "ku") lists 137 "essential" words and up to 187 in total.\[25\]\[26\] Lang calls it "my attempt to understand the meaning of life in 120 words." ISO 639-3 assigned it the code *tok* in 2022.\[27\] Its trick is extreme polysemy plus compounding: each word covers a wide semantic field, and context does the rest.\[28\]

**Artistic languages (artlangs).** Hildegard von Bingen's 12th-century *Lingua Ignota* is the earliest recorded conlang.\[29\] Tolkien's Elvish languages (Quenya, Sindarin) were built with invented sound changes and histories. Victoria Fromkin's Paku was made for *Land of the Lost* in the 1970s.\[14\] Marc Okrand created Klingon for *Star Trek III* (1984), and his *Klingon Dictionary* became a bestseller.\[30\]\[31\] In 2009 HBO approached the Language Creation Society (LCS), which ran an application process involving over 30 conlangers. David J. Peterson won it; he delivered over 1,700 words of Dothraki to HBO before initial shooting, and by his own 2014 account the language had reached "thirty-eight hundred-some words."

**Experimental languages.** aUI (John Weilgart) is a "language of space" in which each phoneme carries a meaning, an a priori primitive scheme at the level of single sounds. Sylvia Sotomayor's Kēlen deliberately has no verbs, testing what language looks like without a core supposed universal.

**Design methods.** Modern conlangers, as described in Peterson's *The Art of Language Invention* and the LCS community, typically work in this order: phonology and phonotactics → morphology → syntax → lexicon → (for artlangs) a simulated diachronic history and culture. The goals differ by type:
- auxlangs aim for learnability and neutrality;
- engelangs aim for a testable property such as unambiguity or density;
- artlangs aim for naturalism and believability within a fictional world.

Peterson helped organize the first Language Creation Conference at UC Berkeley in 2006 and co-founded the LCS in 2007 with nine other language creators.

### 2. Programming language creation

**Why new languages appear.** New languages appear for four main reasons:
- a new domain (APL for array mathematics, SQL for relations, Inform for interactive fiction);
- new hardware or performance needs (Mojo for AI accelerators, introduced by Modular in 2023);\[32\]
- safety or ergonomics;
- an *idea about thought*: Iverson, Lisp, Smalltalk, Forth.

**Minimal cores vs. large languages.**
- **Lambda calculus (Church, 1930s)** has three constructs: variables, abstraction (λx.M) and application (M N). Every computable function can be expressed with them.
- **Lisp.** Paul Graham's "The Roots of Lisp" shows that seven primitive operators (quote, atom, eq, car, cdr, cons, cond), plus lambda, are enough to write `eval`, a Lisp interpreter in Lisp. Graham notes that McCarthy's 1960 paper used only five primitive operators.\[33\]
- **Forth.** "Forth was invented by Charles H. (Chuck) Moore"; the first program called Forth was written around 1970.\[34\] It is a stack machine with a tiny core of words, extended by defining new words.
- **Smalltalk** is famously small syntactically. The folk claim that "Smalltalk syntax fits on a postcard" refers to a code snippet by Ralph Johnson, and only six pseudo-keywords are reserved (true, false, nil, self, super, thisContext).\[35\] This is folklore, not a formal measure.
- **APL** puts the power in a large set of symbolic primitives over arrays rather than a small syntax. It has a minimal grammar but a rich vocabulary.
- **Go** has 25 reserved keywords. Rob Pike's 2012 talk "Less is exponentially more" argues: "it would be a greater achievement to simplify the language rather than to add to it." He also claims that, despite its omissions, "Go is, I believe, more expressive than C or C++. Less can be more."\[36\]\[37\]

The lesson across these cases is that a *small grammar* (Lisp, Forth, Smalltalk) is not the same as a *small vocabulary* (APL has many primitives), and neither is the same as a *small semantic core* (lambda calculus).

**The process of building a language.**
1. Lexical grammar (tokens), usually regular expressions.
2. Syntax, usually a context-free grammar in BNF/EBNF, parsed by hand-written recursive descent or with generators (YACC/Bison, ANTLR, PEG tools).
3. Semantics: the formal definition of what programs mean, through an interpreter, an operational/denotational spec, or "the reference implementation."
4. A type system, if any: static vs. dynamic, inference, effects.
5. Runtime and compilation: interpreter, bytecode VM, or a compiler to LLVM IR or C.
6. Tooling, which now largely decides adoption: package manager, formatter, language server, debugger, documentation.

**Esoteric languages (esolangs).**
- **Brainfuck.** "Brainfuck was invented by Urban Müller in 1993, in an attempt to make a language for which he could write the smallest possible compiler for the Amiga OS."\[38\] It has eight commands (`> < + - . , [ ]`). Sources report the compiler size as either 240 or 296 bytes.\[39\]\[40\]
- **Malbolge** was invented by Ben Olmstead in 1998 to be "as difficult to program in as possible." Its first "Hello, world!" program was not written by a human. It was generated by a Lisp program using beam search, attributed to Andrew Cooke, about two years later.\[41\]
- **Piet** (David Morgan-Mar, about 2001) writes programs as abstract images in the style of Mondrian. Sources disagree on the year.\[42\]\[43\]\[44\]
- **The Shakespeare Programming Language** (Karl Wiberg, née Hasselström, and Jon Åslund, 2001) writes programs as stage plays.\[43\]
- **Chef** (Morgan-Mar, 2002) writes programs as recipes.\[45\]
- **Iota and Jot** (Chris Barker, 2001) use a single combinator, ι = λf.fSK.\[46\]\[47\]\[48\]

**Recent trends: languages for or with LLMs.**
- **Pel** (arXiv 2505.13453, 2025) is a Lisp-inspired, homoiconic language designed for LLMs to generate. It has "a minimal, easily modifiable grammar suitable for constrained LLM generation" and controls capabilities at the syntax level instead of relying on sandboxing.\[49\]
- **Quasar** (arXiv 2506.12202) is a language specialized for LLM "code actions" as an alternative to Python.\[50\]
- **LMQL** (ETH Zürich) is a Python superset that interleaves code and constrained LLM prompting.\[51\]
- Hobbyists have used LLMs themselves to design "LLM-optimized" languages, for example token-dense intermediate languages with explicit pre- and postconditions.\[52\] These are experiments, not established practice.

### 3. The intersection

**Machine-parsable human languages.** Lojban is the clearest case. It is a speakable human language whose official grammar is a YACC grammar, with an official parser (and later PEG parsers such as camxes).\[9\] Even so, "Lojban is not in itself LALR1": the official parsing pipeline needs lexer-level preprocessing before YACC can handle it.\[53\] Even a language engineered for machines needed compiler-style tricks. Loglan's founding motivations included use "as a machine-man interface" alongside the Whorf experiment.\[54\]

**Natural-language programming.** Inform 7 (Graham Nelson, 2006) lets authors write source text in a subset of English, such as "The Sheriff of Nottingham hates Robin Hood". Underneath, the semantics rest on predicate logic and binary relations. Nelson's guiding principle was that "the natural language in which to write interactive fiction is natural language." Users report the familiar problem: there are far more valid English sentences than parsable Inform sentences.\[55\]\[56\] COBOL and AppleScript tried English-like syntax earlier and ran into the same issue. English-like *surface* syntax does not give natural-language *semantics*.

**Non-English programming.** Hedy (Felienne Hermans, launched 2020) is a gradual teaching language that adds syntax level by level, from almost no syntax up to a Python subset. According to Hermans' ICPEC 2024 invited-talk abstract, Hedy "is available in 54 different languages," with localized keywords including right-to-left Arabic, which required extensive parser and transpiler changes. The same abstract reports that Hedy "now serves about 500,000 monthly users." Her research also found that learners do better in their mother tongue. Hermans points to a deeper problem: at the end of Hedy, an Arabic-speaking child faces Python, where "everything's English and left to right."\[57\]

**Linguistic relativity applied to code.**
- **Iverson.** In his 1979 Turing Award lecture "Notation as a Tool of Thought" (*CACM*, August 1980), Iverson argued that "the utility of a language as a tool of thought increases with the range of topics it can treat, but decreases with the amount of vocabulary and the complexity of grammatical rules which the user must keep in mind. Economy of notation is therefore important."\[58\] This is the best one-sentence statement of the minimality/expressiveness trade-off in either field.
- **Paul Graham's "Blub paradox"** ("Beating the Averages," 2001): a programmer fluent in a middling language, "Blub," can see that less powerful languages lack features. When looking at more powerful languages, though, they see only "weird" languages, because they think in Blub.\[11\]\[59\] It is a strong-Whorfian claim about programming languages. It is persuasive as a story but not empirically established.
- **Caution.** Mainstream linguistics accepts at most *weak* linguistic relativity for natural languages. Loglan's Whorf experiment was never carried out as a controlled study. Any claim that a language "makes you think differently" should be treated as a hypothesis to test, not a design guarantee.

**Shared machinery.** Chomsky's hierarchy of grammars (regular ⊂ context-free ⊂ context-sensitive ⊂ recursively enumerable) came from linguistics and became the backbone of compiler theory. BNF/EBNF, parser generators and type theory are now common to both communities. Montague-style formal semantics and Barker's work on continuations in natural-language semantics bring programming-language ideas back into linguistics. Barker, the inventor of Iota, is a professor of linguistics at NYU, which shows how the two communities overlap.\[46\]\[60\]

**Esolangs as conlangs.** Esolangs are to programming languages what artlangs and experimental languages are to natural languages. Their purpose is to explore the design space, not to be practical. Malbolge is the programming equivalent of Ithkuil's difficulty. Brainfuck and Iota are the equivalent of Toki Pona's minimalism. Shakespeare and Chef are artlangs with an executable semantics.

### 4. Minimal conceptual sets: verifying the pasted claims

| Claim in pasted text | Verdict | Correction / context |
|---|---|---|
| NSM has "about 65" semantic primes | **Correct** | 65, stable since Goddard & Wierzbicka 2014; up from 14 (1972), 60 (2002), 63 (2011). Co-developed by Goddard. |
| The listed primes | **Incomplete; some misgrouped** | Missing: KIND, PART, LITTLE~FEW, DON'T WANT, SAY, WORDS, TRUE, BE (SOMEWHERE), THERE IS, BE (SOMEONE/SOMETHING), (IS) MINE, LIVE, DIE, FAR, NEAR, SIDE, INSIDE, A LONG TIME, A SHORT TIME, FOR SOME TIME, MOMENT, VERY, MORE, LIKE~AS~WAY. NSM uses BELOW, not UNDER. TOUCH belongs with the space primes in current tables, not with action. |
| Primes "exist in all human languages and cannot be defined" | **Hypothesis, not fact** | NSM researchers claim to have found exponents across diverse languages. Critics dispute the universality of particular primes and the method. |
| Ogden's 850 words "cover 90% of everyday communication" | **Distorted** | The original claim is that 90% of the *concepts in the Oxford Pocket English Dictionary* can be expressed with 850 words. It is not a corpus-coverage statistic. |
| Top 100 words = "understand roughly 50% of any average text" | **Misleading** | The top 100 lemmas "account for 50% of all the words" in the Oxford English Corpus (over 2 billion words). Penn Treebank WSJ: top 100 = 48.1%; Brown Corpus: 135 words make up half. These are mostly function words; Laufer (1989) put the threshold for academic reading at 95% lexical coverage and Hu & Nation (2000) at about 98% of running words for unassisted reading, though Kremmel et al. (2023) failed to replicate the 98% threshold. |
| Sequence, Selection, Iteration suffice | **Correct with caveats** | Böhm–Jacopini (1966) uses extra boolean variables, and Böhm showed selection can be eliminated (sequence + iteration). Harel (1980) notes the "folk theorem" version is often misrepresented. You also need assignment/state. |
| AND/OR/NOT, reducible to NAND or NOR alone | **Correct** | Functionally complete for Boolean functions. Boolean logic alone is not Turing-complete: it needs memory and feedback/loops. |
| Physics reduces to Space, Time, Matter/Energy, Information | **Not a recognized framework** | A popular simplification. Physics uses fields, particles, spacetime and interactions. "Information as fundamental" (Wheeler's "it from bit") is a speculative research program, not consensus. |

**Other minimal sets worth knowing:**
- **Lambda calculus:** 3 constructs (variable, abstraction, application).
- **SKI combinators:** S and K alone are universal (I = SKK). **Iota:** one combinator, ι = λf.fSK, from which I = ιι, K = ι(ι(ιι)) and S = ι(ι(ι(ιι))).\[8\]\[61\]
- **Turing machine:** a finite state table plus read, write and move left/right on an unbounded tape.
- **SUBLEQ** (one-instruction set computer): subtract the value at address A from the value at address B, store the result in B, and branch if the result is ≤ 0. It is Turing-complete if memory cells are unbounded.\[62\]\[63\]
- **Lisp:** 7 primitives (Graham), or 5 in McCarthy's 1960 paper.\[64\]
- **Brainfuck:** 8 commands.
- **Toki Pona:** 120–137 words.
- **Lojban:** about 1,350 gismu.
- **Ithkuil:** thousands of roots plus a huge morphological system. This is minimal in *word count per idea*, not in inventory.
- **Wilkins:** 40 genera, 251 differences.
- **Schank's Conceptual Dependency** (Stanford, 1969 onward) uses 11 primitive ACTs: ATRANS (transfer of possession), PTRANS (physical movement), MTRANS (information transfer), MBUILD, ATTEND, SPEAK, GRASP, MOVE, PROPEL, INGEST, EXPEL. Schank stated that they "are not mutually exclusive." Their justification was the *inferences* each one licenses: "a system of primitives is only as good as the inferences that it generates." Critics observed that "a mere eleven ACT primitives" fail to capture much of everyday meaning.\[65\]\[66\]\[67\]\[68\]
- **Philosophical categories:**
  - Aristotle's 10 categories: substance, quantity, quality, relation, place, time, position, state, action, affection.
  - Kant's 12 categories in 4 groups: quantity, quality, relation, modality.
  - Peirce's three: Firstness, Secondness, Thirdness.
- **Ontology upper levels:** WordNet's noun hierarchy bottoms out in a few "unique beginners" under *entity*. Formal upper ontologies such as BFO, DOLCE and SUMO divide reality into continuants and occurrents.
- **The Swadesh list** (100- and 207-item versions) is a list of meanings chosen for being culturally stable and resistant to borrowing, used in historical linguistics. It is a *comparison* set, not a *definitional* primitive set.

**How these sets differ.** NSM primes are *definitional*: everything else should be explicable in them. Swadesh items are *stable*. Ogden's words are *pedagogically sufficient*. Toki Pona's words are *expressively sufficient with heavy context*. Computational primitives are *extensionally complete*: they compute everything, but say nothing about meaning. Schank's ACTs are *inferentially motivated*.

### 5. Open questions for a would-be designer

**Is there a universal set shared by human and programming languages?** Not in any proven sense, but there is a suggestive overlap. NSM's logical primes (NOT, IF, BECAUSE, CAN, MAYBE, ALL, SOME, ONE, TWO, THE SAME, OTHER) correspond closely to the connectives, quantifiers, equality and modality of predicate logic. Its time and space primes (BEFORE, AFTER, WHERE, INSIDE) map to sequencing and scope. Lojban and Pel both start from predicate logic or Lisp. What programming primitives *lack* is NSM's experiential layer: I/YOU, WANT, FEEL, KNOW, GOOD/BAD, LIVE/DIE. These are exactly the primes that make human language about agents with minds. The most defensible position is that logic is the shared core and agency/evaluation is the human surplus. LLM-oriented languages such as Pel, with natural-language conditions evaluated by an LLM, are the first serious attempts to bring that surplus into executable code.

**Minimality vs. expressiveness.** Every minimal system moves its complexity somewhere else:
- Toki Pona moves it into context and pragmatics, which makes it ambiguous.
- Ithkuil moves it into morphology, which makes it dense but almost unspeakable.
- Iota and Brainfuck move it into program length. They are *Turing tarpits*, where everything is possible but nothing of interest is easy, in Alan Perlis's phrase.
- Basic English moves it into idiom and polysemy.

Iverson's formula (utility rises with range, falls with vocabulary and grammar) is the right objective function.

## Recommendations

1. **Decide which kind of "minimal" you want before choosing primitives.** Definitional (NSM), computational (lambda/SKI), learnable (Toki Pona/Basic) and inferential (Schank) are different targets. Mixing them unconsciously is the main design error in the pasted framing.
2. **Use a layered architecture.** Build a tiny semantic core (for example, lambda calculus plus a handful of NSM-like predicates) with a rich, regular derivation layer on top: compounds, macros, a standard library. Lisp, Lojban's gismu→lujvo compounding and Toki Pona's compounding all work this way.
3. **If you want human *and* machine readability, write the grammar formally from day one** (EBNF/PEG) and test it with a parser generator, as Lojban did. Expect to need lexer-level disambiguation.
4. **Don't promise Whorfian effects.** Treat "this language will change how you think" as an experiment to run with users. Brown never managed to run his.
5. **Resources:**
   - Conlangs: David J. Peterson, *The Art of Language Invention*; Mark Rosenfelder's *Language Construction Kit*; the Language Creation Society and its conferences; Arika Okrent, *In the Land of Invented Languages*.
   - Programming languages: Robert Nystrom, *Crafting Interpreters*; *Structure and Interpretation of Computer Programs*; Graham's "The Roots of Lisp"; Iverson's Turing lecture; esolangs.org for the design space.
   - Primitives: Goddard & Wierzbicka's NSM resources (nsm-approach.net, including the 150 canonical sentences for testing primes in a language); the ISKO Encyclopedia entry on semantic primitives.

## Caveats

- Some details come from secondary sources: Toki Pona word counts (community wiki plus Lang's site), New Ithkuil root counts (a fan wiki), Dothraki's word count, and the Smalltalk "postcard" claim. Treat their numbers as approximate.
- There are minor conflicts between sources: the year of Piet (2001 vs. 2003), Brainfuck's compiler size (240 vs. 296 bytes),\[39\]\[40\]\[42\]\[43\] and the exact NSM category assignments, which vary slightly between presentations.
- The LLM-oriented languages cited (Pel, Quasar, and others) are research prototypes or blog experiments, not adopted standards. Claims that they are "more robust" are their authors' arguments.
- Linguistic relativity claims about programming languages (Blub, "tool of thought") are influential essays, not experimental findings.

## Sources

1. [Semantic primitives (ISKO Encyclopedia of KO)](https://www.isko.org/cyclo/primitives.htm)
2. [Natural semantic metalanguage](https://en.wikipedia.org/wiki/Natural_semantic_metalanguage)
3. [NSM Natural Semantic Metalanguage - Language Miscellany](https://languagemiscellany.com/2026/06/nsm-natural-semantic-metalanguage/)
4. [Ogden's Basic English](https://zbenglish.net/sites/basic/basiceng.html)
5. [GitHub - ytmytm/c64-beamracer-subleq: 8-bit SUBLEQ Virtual Machine for BeamRacer · GitHub](https://github.com/ytmytm/c64-beamracer-subleq)
6. [Structured program theorem](https://en.wikipedia.org/wiki/Structured_program_theorem)
7. [P%E2%80%B2%E2%80%B2](https://en.wikipedia.org/wiki/P%E2%80%B2%E2%80%B2)
8. [Iota - Esolang](https://esolangs.org/wiki/Iota)
9. [The Complete Lojban Language (1997)/Chapter 21 - Wikisource, the free online library](<https://en.wikisource.org/wiki/The_Complete_Lojban_Language_(1997)/Chapter_21>)
10. [Paper of the Week: Notation as a Tool of Thought - Blog - Recurse Center](https://www.recurse.com/blog/58-paper-of-the-week-notation-as-a-tool-of-thought)
11. [Be Careful Of The Blub Paradox Next Time You Compare Programming Languages](https://medium.com/@badwolf256/be-careful-of-the-blub-paradox-next-time-you-compare-programming-languages-62e0cb62a0d5)
12. [Essay Towards a Real Character and a Philosophical Language](https://therealsamizdat.com/tag/essay-towards-a-real-character-and-a-philosophical-language/)
13. [An Essay Towards a Real Character, and a Philosophical Language](https://en.wikipedia.org/wiki/An_Essay_Towards_a_Real_Character,_and_a_Philosophical_Language)
14. [Speaking in tongues: the man who made a career of making up languages](https://www.irishtimes.com/culture/speaking-in-tongues-the-man-who-made-a-career-of-making-up-languages-1.1389014)
15. [Does English only need 850 words? This guy thought so.](https://theweek.com/articles/560685/does-english-only-need-850-words-guy-thought)
16. [(PDF) The application of C.K. Ogden's semiotics in Basic English.](https://www.academia.edu/17111817/The_application_of_C_K_Ogdens_semiotics_in_Basic_English)
17. [Portal:Constructed languages/Selected language/28](https://en.wikipedia.org/wiki/Portal:Constructed_languages/Selected_language/28)
18. [Lojban](https://mw.lojban.org/papri/Lojban)
19. [Semantic parsing using Lojban](https://www.inf.uni-hamburg.de/en/inst/ab/lt/teaching/theses/completed-theses/2014-ma-hinz.pdf)
20. [Lojban](https://alexburka.com/lojban/cll/lojban.html)
21. [Lojban](https://en.wikipedia.org/wiki/Lojban)
22. [graphsearch.epfl.ch](https://graphsearch.epfl.ch/concept/1683879)
23. [New Ithkuil](https://conlang.fandom.com/wiki/New_Ithkuil)
24. [Ithkuil v2](https://hybridcopynet.wordpress.com/2026/04/11/ithkuil-v2/)
25. [Toki Pona](https://en.wikipedia.org/wiki/Toki_Pona)
26. [How many words does Toki Pona have? - sona pona](https://sona.pona.la/wiki/How_many_words_does_Toki_Pona_have)
27. [Toki Pona (official site)](https://tokipona.bahaiwebsites.com/)
28. [World's simplest language with less than 150 words is enough to understand the meaning of life - Scoop Upworthy](https://scoop.upworthy.com/worlds-simplest-language-with-less-than-150-words-is-enough-to-understand-the-meaning-of-life-ex2)
29. [Conlangs, Auxlangs, and Engelangs: The Art of Language](https://keithsawyer.substack.com/p/conlangs-auxlangs-and-engelangs-the)
30. [Language Crafters](https://today.ucsd.edu/story/language_crafters)
31. [Conlangs: Languages Invented for Television and Film - U.S. Language Services](https://www.uslanguageservices.com/blog/conlangs-languages-invented-for-television-and-film/)
32. [AI Programming Languages: Python, R and What to Learn for AI in 2026](https://www.eicta.iitk.ac.in/knowledge-hub/artificial-intelligence/ai-programming-language)
33. [The Roots of Lisp - EBIN.PUB](https://ebin.pub/the-roots-of-lisp.html)
34. [Xlll Forth Session Chair: Helen Gigley THE EVOLUTION OF FORTH](https://dl.acm.org/doi/pdf/10.1145/234286.1057832)
35. [Smalltalk - CodeDocs](https://codedocs.org/what-is/smalltalk)
36. [Go Keywords: All 25 Reserved Words Explained](https://levelupgo.dev/blog/go-keywords)
37. [Less is exponentially more](https://commandcenter.blogspot.com/2012/06/less-is-exponentially-more.html)
38. [brainfuck - Esolang](https://esolangs.org/wiki/Brainfuck)
39. [Brainfuck Interpreter Online — Esolang Studio](https://funtranslations.com/esolang-studio/brainfuck)
40. [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck)
41. [Malbolge - Esolang](https://esolangs.org/wiki/Malbolge)
42. [(PDF) The Aesthetics of Multicoding Esolangs](https://www.academia.edu/143148387/The_Aesthetics_of_Multicoding_Esolangs)
43. [A Brief Introduction to Esoteric Languages](https://www.hillelwayne.com/talks/esolangs/)
44. [Piet - Esolang](https://esolangs.org/wiki/Piet)
45. [Chef - Esolang](https://esolangs.org/wiki/Chef)
46. [Chris Barker (linguist)](<https://en.wikipedia.org/wiki/Chris_Barker_(linguist)>)
47. [Mateus Jabour - Understanding how computation works part 6-1](https://mateusjabour.github.io/understanding-how-computation-works-6-1)
48. [Iota and Jot](https://static.hlt.bme.hu/semantics/external/pages/kombin%C3%A1toros_logika/en.wikipedia.org/wiki/Iota_and_Jot.html)
49. [Pel, A Programming Language for Orchestrating AI Agents](https://arxiv.org/pdf/2505.13453)
50. [\[2506.12202\] Quasar: A Programming Language Specialized for LLM Code Actions](https://arxiv.org/abs/2506.12202)
51. [GitHub - eth-sri/lmql: A language for constraint-guided and efficient LLM programming. · GitHub](https://github.com/eth-sri/lmql)
52. [imjasonh/articles/llm-programming-language.md at main · imjasonh/imjasonh · GitHub](https://github.com/ImJasonH/ImJasonH/blob/main/articles/llm-programming-language.md)
53. [Lojban Reference Grammar: Chapter 21](https://lojban.org/publications/reference_grammar/chapter21.html)
54. [LOGLAN 1: A LOGICAL LANGUAGE Revised Fourth Edition by James Cooke Brown](https://www.loglan.org/Download/Loglan1.pdf)
55. [Inform 7: A relational DSL for interactive fiction with natural language syntax](http://lambda-the-ultimate.org/node/1554)
56. [Brass Lantern: Introducing Inform 7](https://brasslantern.org/writers/howto/i7intro-b.html)
57. [Hedy: creating a gradual programming language](https://developerrelations.com/talks/hedy-creating-a-gradual-programming-language/)
58. [Kenneth E. Iverson - Wikiquote](https://en.wikiquote.org/wiki/Kenneth_E._Iverson)
59. [The Co-Blub Paradox :: Reasonably Polymorphic](https://reasonablypolymorphic.com/blog/coblub/)
60. [Iota and Jot](https://en.wikipedia.org/wiki/Iota_and_Jot)
61. [SKI combinator calculus](https://en.wikipedia.org/wiki/SKI_combinator_calculus)
62. [Subleq - Esolang](https://esolangs.org/wiki/Subleq)
63. [OISC - Esolang](https://esolangs.org/wiki/OISC)
64. [The Roots of Lisp paul graham Draft, January 18, 2002.](https://3e8.org/pub/pdf-t1/the-roots-of-lisp.pdf)
65. [Conceptual Dependency Theory (CD), Schank 1975](https://people.cs.pitt.edu/~wiebe/courses/CS3730/Spring2013/cd.pdf)
66. [and Paraphrase by Computer ROGER C. SCHANK](https://dl.acm.org/doi/pdf/10.1145/321892.321893)
67. [Conceptual dependency theory](https://en.wikipedia.org/wiki/Conceptual_dependency_theory)
68. [CHARLES E. M. DUNLOP CONCEPTUAL DEPENDENCY AS THE LANGUAGE OF THOUGHT 1](https://backend.production.deepblue-documents.lib.umich.edu/server/api/core/bitstreams/7adae908-76cb-4f81-9bc8-9ad6c8f2a871/content)
