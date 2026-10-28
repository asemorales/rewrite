# Rewrite

Rewrite AI-generated text using Sutton and Pinker's rules for clear writing. Forked from blader/humanizer.

## Example

**Before:**
> I'm thrilled to announce that shared drafts are finally here! 🚀 For months, our own team was drowning in files named final_v7.docx — and we knew there had to be a better way. Now two people can edit the same doc at once, with every change appearing live for both of them. It's not just a feature; it's a whole new way to collaborate. Comments stay anchored to the exact sentence they reference, even as the text around them evolves. And the best part? It's available today on every plan, completely free. Let that sink in.

**After (Humanizer):**
> Shared drafts are out today. For months our own team passed around files named final_v7.docx, so we built a way for two people to edit the same doc at once, with each person's changes showing up live for the other. Comments stay pinned to the sentence they're about, even when the text around them changes. It's free on every plan.

**After, with opinionated writing principles (Rewrite):**
> Shared drafts are out today! For months, our own team passed around files named final_v7.docx, and we knew there had to be a better way. Now you and a coworker can edit the same doc at once and see each other's changes live. When you attach a comment to a sentence, it moves with that sentence as you edit the text around it. Shared drafts are free on every plan.

## Installation

After you install the skill, run it with `/rewrite`.

### Claude Code

```text
/plugin marketplace add asemorales/rewrite
/plugin install rewrite@rewrite
```

Run the plugin with `/rewrite:rewrite`. It needs Claude Code 2.1.142 or newer. On older versions, use `npx skills add asemorales/rewrite --global --agent claude-code`.

### Codex

```bash
npx skills add asemorales/rewrite --global --agent codex
```

### Claude.ai and Claude Desktop

Download this repository as a ZIP (**Code → Download ZIP**) and upload it as a skill in Settings.

### Other agents

```bash
npx skills add asemorales/rewrite --global --agent '*'
```

This installs Rewrite for every agent that the Skills CLI supports, including Gemini CLI, GitHub Copilot, and Windsurf. To install it only in the current project, leave off `--global` in any command above. If the Skills CLI does not support your agent, copy `SKILL.md` into the agent's skill folder.

## Usage

Run the skill directly:

```
/rewrite

[paste your text here]
```

Or ask in plain language:

```
Please rewrite this text: [your text]
```

To edit a file, give the skill its path:

```
Rewrite the prose in docs/launch-post.md
```

## Sources

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)
- [Wikipedia: Manual of Style](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style) and [Manual of Style/Words to watch](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style/Words_to_watch)
- Rich Sutton, ["Advice for general technical writing"](https://docs.google.com/document/d/1EKhufclxlvF0RDA3oR0Dp02iTH5biCDguE7Ou7Sprzo/edit)
- Michael Littman, ["Stylistic comments"](https://cs.brown.edu/people/mlittman/etc/style.html)
- Steven Pinker, *The Sense of Style* (2014)
- Thomas Hikaru Clark, Matias B. Martin, and Kyle Mahowald, ["Why is AI-generated language so hard to understand?"](https://arxiv.org/abs/2610.29162) (2026)
