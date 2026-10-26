# Rewrite

Rewrite AI-generated text using Sutton and Pinker's rules for clear writing. Forked from blader/humanizer.

---

## Examples

**Before:**
> I'm thrilled to announce that shared drafts are finally here! 🚀 For months, our own team was drowning in files named final_v7.docx — and we knew there had to be a better way. Now two people can edit the same doc at once, with every change appearing live for both of them. It's not just a feature; it's a whole new way to collaborate. Comments stay anchored to the exact sentence they reference, even as the text around them evolves. And the best part? It's available today on every plan, completely free. Let that sink in.

**After (Humanizer):**
> Shared drafts are out today. For months our own team passed around files named final_v7.docx, so we built a way for two people to edit the same doc at once, with each person's changes showing up live for the other. Comments stay pinned to the sentence they're about, even when the text around them changes. It's free on every plan.

**After (Rewrite):**
> Shared drafts are finally here! For months, our own team was drowning in files named final_v7.docx, and we knew there had to be a better way. Now you and a coworker can edit the same doc and watch each other's changes appear live. A comment is pinned to its sentence, even when you edit the text around it. Best of all, shared drafts are available today on every plan, completely free.

**Before:**
> I recently spent five unforgettable days in Lisbon last October, and let me tell you — this city completely stole my heart. From the moment I checked into my charming hotel perched high in the historic Alfama district, I knew I was somewhere truly special.
>
> Yes, the famous hills are challenging — with countless stairs between my hotel and everything else, my legs certainly felt it! — but every climb rewards you with breathtaking, panoramic views that make it all worthwhile.
>
> No trip would be complete without riding the iconic Tram 28, a roughly forty-minute journey shared with plenty of fellow travelers eager to capture the magic. And the food? Simply divine. While the pastéis de nata at Pastéis de Belém are a beloved national treasure, my absolute favorite came from a hidden gem in Graça, still warm from the oven.
>
> But what truly makes Lisbon special isn't just the sights — it's the feeling. Wander just a block or two above the main squares and you'll discover a quieter, more authentic side of the city, inviting you to slow down and savor every moment.
>
> Of course, the must-see São Jorge Castle offers stunning views over the rooftops below. The queues can be long, but the experience is absolutely worth it for any history buff or curious traveler.
>
> Would I go back? Absolutely — next time in spring, and with better shoes! Lisbon isn't just a place to visit; it's a place to fall in love with, again and again. ✨

**After (Humanizer):**
> I spent five days in Lisbon last October. My hotel was up in Alfama, with a lot of stairs between it and everything else, and my legs felt every one of them. The views from the top were worth the climb.
>
> Everyone tells you to ride Tram 28, so I did. The trip took about forty minutes, and most of the car was other tourists taking pictures out the windows. The custard tarts at Pastéis de Belém are the famous ones, but my favorite came from a place in Graça, still warm from the oven.
>
> The part of Lisbon I liked best starts a block or two above the main squares, where the streets go quiet and nobody is in a hurry. São Jorge Castle has good views over the rooftops and a long queue to get them.
>
> I'd go back, in spring next time, and with better shoes.

**After (Rewrite):**
> I spent five days in Lisbon last October, and I loved it. My hotel was high up in Alfama, the old district, and I liked it from the moment I checked in.
>
> The hills are hard work. There were countless stairs between my hotel and everything else, and my legs felt it! But each climb ended with a view across the city, and the views made the stairs worth it.
>
> Of course I rode Tram 28. The trip took about forty minutes, and the car was full of other tourists trying to get the perfect photo. The food was wonderful. The pastéis de nata at Pastéis de Belém are famous across Portugal, but my favorite came from a little-known spot in Graça, still warm from the oven.
>
> What I loved most was the mood of the place. Walk a block or two above the main squares and the streets get quieter, and you want to slow down and enjoy it.
>
> São Jorge Castle has great views over the rooftops. The line can be long, but if you like history, or you're just curious, it's absolutely worth the wait.
>
> I'd go back in a heartbeat, next time in spring and with better shoes. I think I'd fall for Lisbon all over again.


## Installation

Once installed, the skill answers to `/rewrite`.

### Claude Code

```text
/plugin marketplace add asemorales/rewrite
/plugin install rewrite@rewrite
```

The plugin answers to `/rewrite:rewrite`. It needs Claude Code 2.1.142 or newer. On older versions, use `npx skills add asemorales/rewrite --global --agent claude-code`.

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

This installs Rewrite for every agent the Skills CLI supports, including Gemini CLI, GitHub Copilot, and Windsurf. Leave off `--global` in any command above to install it only in the current project. For an agent the Skills CLI does not know, copy `SKILL.md` into its skill folder.

## Usage

Call the skill directly:

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

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) maintained by [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)
- Rich Sutton, ["Advice for general technical writing"](https://docs.google.com/document/d/1EKhufclxlvF0RDA3oR0Dp02iTH5biCDguE7Ou7Sprzo/edit)
- Michael Littman, ["Stylistic comments"](https://cs.brown.edu/people/mlittman/etc/style.html)
- Steven Pinker, *The Sense of Style* (2014)
- Thomas Hikaru Clark, Matias B. Martin, and Kyle Mahowald, ["Why is AI-generated language so hard to understand?"](https://arxiv.org/abs/2610.29162) (2026)
