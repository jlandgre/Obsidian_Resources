---
type: jdl_writeup
description: .code-workspace setup and path sfor Obsidian and iCloud folders
tags:
  - vscode
  - obsidian
  - icloud
  - osx
created: 05-29-2026
updated: 05-29-2026
author: JDL
---
A VS Code project can include Obsidian folders and cloud storage folders. The path to these in Mac OSX points to the Library CloudStorage and Mobile Documents folders.

## `project.code-workspace` file mockup

* substitute Obsidian vault name for "vault_name"
* substitute subfolder_path
* substitute `//Mac/Home/Library` for "xxx"
* substitute `//Mac/Home/Library/Mobile Documents/iCloud~md~obsidian/Documents` for "yyy"

```json
{
	"folders": [
		{"path": "."},
		{"path": "xxx/CloudStorage/Box-Box/subfolder_path"},
		{"path": "yyy/vault_name/subfolder_path"}
		],
	"settings": {"terminal.integrated.cwd": "."}
}
//"path": "." specifies current directory as workspace folder and includes its contents
//"terminal.integrated.cwd": "." New terminal will open in the workspace root directory
// `Mobile Documents/iCloud~md~obsidian/` = Obsidian’s iCloud container
// `.../Documents/...` = Obsidian-managed files/folders within that container
```

