---
type: jdl_writeup
description: Seth Rosen on how to build a company learning loop
tags:
  - enterprise
  - ai
  - context
  - wiki
created: 06-16-2026
updated: 06-16-2026
author: JDL
---

[Twitter link to Seth Rosen post](https://x.com/sethrosen/status/2066534763511316540?s=12)  

[Public Link to my Obsidian note re Satya Nadela's widely-discussed post](https://github.com/jlandgre/Obsidian_Resources/blob/main/JDL-Writeups/2026-0616-Satya%20Nadella-on-AI-in-workplaces.md) (link to that is in my note; Seth refers to it)

**Quote from Seth Rosen post**  
>**Please don't implement a "company brain" and expect a learning loop**
>Your long-horizon learning loop has four properties.
>1. Minimum Viable Context. Seed the system with the judgment only your company has, not everything it has ever said.
>2. Structured, introspectable, multiplayer. Everyone and every agent builds on the same shared foundation, and intermediate decisions can be traced and judged.
>3. Executable. Once the work is visible, agents can operate on it directly.
>4. Compounding. It measurably gets better the more it's used. The opposite of AI decay.

**JDL Comments**

Implementing a "company brain"** is daunting --you could, at a high price, have McKinsey or Accenture come in and interview everyone to document everything.  Besides the astronomical cost of that, the problem with it is that they are not insiders on your culture and practices. They simply have a job to do for hire and will leave afterwards without creating descriptions that have life.  For smaller companies, such an approach is simply infeasible financially.

As an aside, based on P&G Knowledge Management experience and learning about pitfalls there, don't overdo the "company brain" terminology because it suggests to employees offloading everything they know into AI thus rendering employees superfluous.  Capturing the "company soul" is a worthwhile addition to the cold, "knowledge" term. The best way to think about capturing explicit and implicit knowledge is that it's like putting an ["exoskeleton"](https://flex-lineautomation.com/product/comau-robotics/wearable-robotics-exoskeletons) on every employee that gives them superpowers (the analogy holds too in the area of needing to make sure that the exoskeleton doesn't cause their detailed knowledge (aka muscles built up by experience) to atrophy in the process. Doing that right will be a delicate balance.

Because companies can't afford to create a massive, separate "knowledge capture" effort, the best approaches are those that are easily worked into your existing processes and build things from the ground up. For example, you have people writing research summaries? Step 1: Set up a static cloud folder structure and insist that, as a manager, you will only review the posted summary --not the email attached version. Step 2: Set up consistent "frontmatter"** for the summaries that makes them open to inspection and search by AI. Step 3: Set up a wiki-like "index" that at least links to each summary but also which makes it easy for others to link to the work and write about its implications and its implementation on specific projects.  Step 4: Add agents/an AI layer (like Glean example below) to build on this and enable broad search, AI summarization and AI-driven tasks.

**A note about "frontmatter"**  
Overloading AI context is a problem that degrades its performance. The ["YAML"](https://en.wikipedia.org/wiki/YAML) formatted section at the header of this note is my "frontmatter" to create a concise, AI readable summary based on keywords. This eliminates the need for AI to pre-emptively read an entire document before discerning its relevance.  I author in Obsidian, which has a shortcut to insert this frontmatter with a single keystroke making it natural and quick to populate it for every note I author.

Both [Obsidian](https://obsidian.md) that I authored this in and Github used for sharing, render the YAML frontmatter in an readable way. Although its good to standardize, YAML uses the format of "keyword:text" where you are free to make up your own keywords based on the situation. This type of indexing enables great searching: "Give me a list of notes tagged as "enterprise" and "ai". "Show me notes created in June 2026." Etc.

**Additional Links**  
My Chat thread on software specifics (Confluence, Glean etc.):  
* https://chatgpt.com/share/6a314bc5-2db0-83ea-a309-845a3f3cc66e

Other links. 
* [Glean Software layer sits atop other knowledge sources](https://www.glean.com/blog/85-new-actions-in-agents?utm_source=chatgpt.com)
* [Confluence wiki software by Atlassian](https://www.atlassian.com/software/confluence)

Confluence has a free tier

(from chat with them) [Glean Deployment options](https://docs.glean.com/get-started/build/about-deployment)


