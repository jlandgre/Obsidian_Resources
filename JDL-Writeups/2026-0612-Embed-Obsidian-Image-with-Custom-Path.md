---
type: jdl_writeup
description: How to embed an image in Obsidian so it renders in a Github repo
tags:
  - obsidian
  - html
  - image
created: 06-12-2026
updated: 06-12-2026
author: JDL
---

For Obsidian notes that are part of Github repo or for sub-folders where it's desirable to have a self-contained, non-default attachments subfolder that is different from the Obsidian vault's default attachments folder at the Vault's root. Loading the image with HTML renders in both Obsidian and in Github's markdown view.

Example HTML if `attachments` reside one level up from the folder with the note

`<img src="../attachments/image1.png" width="300">`

Tree structure for this:
```
root (repository folder containing .git)
   ├── attachments
   │   └── image1.png
   ├── notes-in-repo
   │   └── note-with-image.md
```

[Posted Obsidian note Github example](https://github.com/jlandgre/Obsidian_Resources/blob/main/Links/2026-0610-Matt-Pocock-Teach-Skill.md)


