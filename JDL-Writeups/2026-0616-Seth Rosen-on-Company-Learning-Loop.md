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

[Twitter link](https://x.com/sethrosen/status/2066534763511316540?s=12)  

**Quote from Seth Rosen post**  
>**Please don't implement a "company brain" and expect a learning loop**
>Your long-horizon learning loop has four properties.
>1. Minimum Viable Context. Seed the system with the judgment only your company has, not everything it has ever said.
>2. Structured, introspectable, multiplayer. Everyone and every agent builds on the same shared foundation, and intermediate decisions can be traced and judged.
>3. Executable. Once the work is visible, agents can operate on it directly.
>4. Compounding. It measurably gets better the more it's used. The opposite of AI decay.

**JDL Comments**

Implementing a "company brain" is daunting --you could, at a high price, have McKinsey or Accenture come in and interview everyone to document everything.  Besides the astronomical cost of that, the problem with it is that they are not insiders on your culture and practices. They simply have a job to do for hire and will leave afterwards without creating descriptions that have life.

The best approaches are those that are easily worked into your existing processes --You have people writing research summaries? Step 1: Set up a static folder structure and insist that you will only review the posted summary --not the email attached version. Step 2: Set up consistent "frontmatter"** for the summaries that makes them open to inspection by AI
Step 3: Set up a wiki-like "index" that at least links to each summary but also which makes it easy for others to link to the work and write about its implications and its implementation on specific projects

**A note about "frontmatter"**  
** The "YAML" formatted section at the header of this note is my "frontmatter" to create concise, AI readable summary based on keywords. YAML uses the format of "keyword:text". This type of indexing makes it possible to ask AI to review note content without bogging it down with the entire text of every note. It also makes searching easy: "Give me a list of notes tagged as "AI". Show me notes written in June 2026.

My Chat thread on software specifics:  
* https://chatgpt.com/share/6a314bc5-2db0-83ea-a309-845a3f3cc66e

Other links. 
* [Glean Software layer sits atop other knowledge sources](https://www.glean.com/blog/85-new-actions-in-agents?utm_source=chatgpt.com)
* [Confluence wiki software by Atlassian](https://www.atlassian.com/software/confluence)

Confluence has a free tier

(from chat with them) [Glean Deployment options](https://docs.glean.com/get-started/build/about-deployment)


