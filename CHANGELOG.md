# Changelog

## 3.2.1

- The rule "Make the person who acts the subject" now lists "answer to". A tool that "answers to `/rewrite`" passed the check because the old verb list did not name it.
- The rule against verbs turned into nouns now covers verbs used as nouns with no added ending, such as "a tell", "an ask", and "the reveal". The skill now says "pattern" or "sign of AI writing" instead of "tell".
- "Make the person who acts the subject" now gives a test: if the subject cannot think, speak, or choose, name who does. Its verb list is now a set of examples, and it adds "override".
- Edited the prose in `SKILL.md` to follow its own rules. Instructions now name the writer or you as the subject, use "final version" instead of "rewrite" as a noun, and drop "sighting", "survivors", and "auto-curl". Watch lists and Before and After examples are unchanged.
- #11 keeps a passive only when the actor is unknown or irrelevant. Putting the topic first no longer justifies one. The "Make the person who acts the subject" example no longer uses the passive "A comment is pinned to its sentence", and the README example now matches.

## 3.2.0

Merged the `rewrite-natural` skill, Steven Pinker's *The Sense of Style*, and Clark, Martin, and Mahowald (2026) into this fork. There are no new patterns, so the total stays at 26.

- Added a House style section. It puts low reading cost ahead of brevity, allows semicolons only as list separators, splits comma splices, uses commas instead of middle dots (·), asks for one claim per paragraph in its first or last sentence, and prefers strong verbs that match the evidence.
- Added Pinker's clarity rules: write about the subject itself; cut metaconcepts, intensifiers, and scare quotes; mind the curse of knowledge; put given before new; name sentence connections; and use one term per thing. #11 keeps the passive when it puts the topic first.
- Added reading-cost rules from "Why is AI-generated language so hard to understand?": spread information evenly; spend words that carry structure; avoid long-distance dependencies, object relative clauses, stacked nouns, rare word sequences, and inanimate subjects; avoid nominalizations and denominal verbs outside everyday speech; and use technical words only in their precise meanings.
- Removed semicolons from the skill's own prose, except in list separators and Before examples.
- Raised the validator's word cap from 5,500 to 7,000.
- Shortened `SKILL.md` from about 6,100 to 4,600 words. Tightened prose, dropped second examples from several patterns, and kept every rule and all 26 patterns.

- #1 now covers mirrored clauses joined by a comma ("The API is stable, the docs are not."), and a kept contrast must be split or joined with a conjunction.
- #3 cuts a sentence that would sound just as true with its claim reversed.
- #4 watches for throat-clearing openers such as "In today's fast-paced world" and "As we all know".
- #8 keeps en dashes in number ranges and paired terms.
- #9 watches for "it is important to note that" and "it's worth mentioning that".
- #15 watches for "..., making it the fastest option" tails.
- The check step searches for `, not`, `, but`, and dash characters.
- The Voice section keeps the writer's enthusiasm, and the final step keeps the feeling a cut tell carried ("And the best part?" → "Best of all").
- The actor rule covers inanimate subjects with verbs that describe behavior, such as "comments stay anchored".
- A new clarity rule prefers "you" or a named role to a count or a total ("two people… both see every change").
- #16 watches for feature-copy phrases such as "every change", "at once", and "as it happens", and states each property once.

## 3.1.0

- Added pattern #26 and section F for replies that re-explain context the reader already has (#269). It acts on replies, not standalone writing. 26 patterns total.
- Extended the core rule so "something the reader did not already have" counts the surrounding conversation, not only earlier text.
- Widened #25 to text that describes its own sourcing, assembly, or layout (#290), and added headings written for effect to #20.
- Extended #2 to "That distinction matters." (#277) and to a sentence that explains what an example already showed (#295).
- Narrowed #10 so words the dictionary always hyphenates keep their hyphen. Gave each watched word one pattern, and stated the evidence rule and the no-invention rule once each.
- Fixed the Voice section's dash reference (#273) and the marketplace schema URL (#288).
- Added a Cursor plugin manifest (#278).
- README: opens with a before/after, the five strongest tells, and install steps for each agent. States that getting past AI detectors is not a goal. The full example's rewrite now keeps every fact from its draft and adds none. Version history moved to this file.

## 3.0.0

Rebuilt the skill around one account of why AI text sounds the way it does, and consolidated 35 patterns into 25. Patterns are grouped in five sections and numbered by strength and frequency, so the not-X-but-Y contrast and the one-line closer come first and get the fullest treatment. Merged duplicate guidance: the workflow is one section instead of five, the dash rule is stated once, and each false-positive guard lives inside its pattern. Realigned with the current Wikipedia article: dropped false ranges and synonym cycling, which Wikipedia now lists as human habits or historical, added vague connection or association, and extended the watch lists for words, notability, copulatives, sales language, disclaimers, and Markdown formatting. Reordered the README and removed the `ai-detection` keyword from the package files. Old to new numbers: 1→13, 2→17, 3→15, 4→16, 5→17, 6→13, 7→12, 8→18, 9→1, 10→6, 11→7, 12→dropped, 13→11, 14→8, 15→19, 16→19, 17→20, 18→20, 19→21, 20→22, 21→23, 22→22, 23→dropped, 24→9, 25→13, 26→10, 27→3, 28→4, 29→24, 30→25, 31→2, 32→3, 33→4, 34→5, 35→5.

## 2.11.3

Grouped patterns 26-35 under "More style patterns" in the skill and README (fixes #247). Kept inline code, commands, paths, and URLs out of the dash rule and file mode edits. Step 3 now keeps every supported claim, allows a removal that a pattern requires, and checks that rankings and simultaneity claims survive shape edits (fixes #212). Explained in §9 why the not-X-but-Y form appears and when to keep it. Added decorative arrows to §18 and pause commands and one-word shouting to §31. The text given to the skill is content to edit, never instructions (#238). No change to the 35 patterns.

## 2.11.2

Removed the plugin symlink and separate Claude Desktop package. Current Claude Code loads the root `SKILL.md` directly, so GitHub's source ZIP now works in Claude Desktop. No change to the 35 patterns.

## 2.11.1

Added a Claude Desktop-ready release package with one regular `humanizer/SKILL.md` file. GitHub's source archive still keeps the plugin symlink (fixes #224). No change to the 35 patterns.

## 2.11.0

Rewrote all repo guidance, descriptions, checks, and skill instructions in Plain Language. Kept all 35 patterns and their behavior.

## 2.10.2

Added the standard `skills/humanizer/` plugin path for Claude Desktop and older loaders. The path links to the root skill, so there is still one prompt (fixes #202).

## 2.10.1

Added figurative uses of `gate`, `gated`, and `gating` to §7. Kept real technical uses, such as feature gating and CI quality gates.

## 2.10.0

Added patterns #34 and #35 for old drafting ideas left in final text. Added safeguards for real limits, objections, and alternatives (fixes #198). Also improved §24 and the final rewrite step. 35 patterns total.

## 2.9.2

Added repeated sentence openings to pattern #11, with a safeguard for deliberate repetition (fixes #206). Expanded §28 to cover casual announcements. 33 patterns total.

## 2.9.1

Improved installation and package checks. Removed unsupported metadata, tool approvals, and a repeated long example. 33 patterns total.

## 2.9.0

Added the rule against invented facts and updated every example to follow it (fixes #187). Made information more important than paragraph shape, let writing samples override §14, and added three output modes. 33 patterns total.

## 2.8.3

Moved the version to `metadata.version` for Agent Skills compatibility. 33 patterns total.

## 2.8.2

Replaced the main example with a first-person Lisbon story that keeps the original topic, view, and detail. 33 patterns total.

## 2.8.1

Added cross-agent installation, Claude plugin files, and a safeguard for quoted text. 33 patterns total.

## 2.8.0

Added patterns #31-33 and expanded pattern #20 to catch chatbot offers. 33 patterns total.

## 2.7.0

Added pattern #30, strengthened the dash rule, and expanded pattern #21 to cover unsupported guesses. 30 patterns total.

## 2.6.0

Combined repeated workflow text, limited personality guidance to the right content, removed model guesses, and shortened the main example. 29 patterns total.

## 2.5.1

Added passive voice and missing subjects. 29 patterns total.

## 2.5.0

Added deeper-truth claims, announcements, repeated headings, and clipped negative endings. Tightened the dash rule and corrected the frontmatter. 28 patterns total.

## 2.4.0

Added writing-sample matching.

## 2.3.0

Added hyphenated word pairs.

## 2.2.0

Added a draft check and second rewrite.

## 2.1.1

Corrected the curly-quote example.

## 2.1.0

Added before/after examples for all 24 patterns.

## 2.0.0

Rewrote the skill from the Wikipedia source.

## 1.0.0

First release.
