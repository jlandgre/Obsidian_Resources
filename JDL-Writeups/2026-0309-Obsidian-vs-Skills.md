---
type: jdl_writeup #jdl_writeup, web link, xxx
description: AI context via Obsidian vs Skills vs copilot-instructions.md
tags: 
- obsidian
- context
- skills
- copilot-instructions
created: 3/9/26
updated: 5/29/26
author: JDL
---
## AI Chat re VBA ExcelSteps project

**JDL**
I am writing up a system for making code changes where The workspace landscape for the project and change descriptions is comprised of a `ProjectName` folder and an Obsidian `Graph_ProjectName` folder containing notes with context. Is there anything special about storing skills \*.md files in the .Github/Skills folder, or could they just be Obsidian notes that I ask AI to use as a "skill" for doing a task?

**AI**
The [skills](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) folder has special functionality for automatic discovery and invocation by GitHub Copilot, but Obsidian notes can work as manual reference documentation. Here are the key differences:
## [skills](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) Advantages

**Automatic Discovery:**
- Copilot automatically indexes skills in [skills](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) at workspace load. It loads the YAML frontmatter without pre-loading entire skill text into context
- Skills appear in the skills list shown in the agent customization system
- Can be automatically suggested based on context patterns

**Structured Metadata (YAML frontmatter):**
```
---
description: When to use this skill and what it covers
applyTo: ["**/*.bas", "**/*.cls"]  # Auto-invoke for these file patterns
---
```

**Referenced in copilot-instructions.md:**
- The `<skills>` section lists available skills
- Copilot knows to use them for specific domains

## Obsidian Notes Approach

**Works fine if you:**
- Manually tell AI: "Read `Graph_ProjectName/change_workflow.md` and follow that process"
- Use `read_file` tool to load context when needed
- Don't need automatic context-based invocation

**Advantages:**
- Keep all project knowledge in one place (Obsidian)
- More flexible organization (tags, backlinks, graphs)
- No need to duplicate content between systems

## Recommended Hybrid Approach

1. **Core coding patterns** → [skills](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) (e.g., VBA_Arrays.md, testing patterns)
    
    - Things AI should always know when writing code
2. **Project/workflow context** → Obsidian notes
    
    - Change processes, project history, decision logs
    - Manually reference when needed: "Read the change workflow from Graph_ProjectName/workflows.md"
3. **Architecture/conventions** → [copilot-instructions.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) or [copilot-instructions.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html)
    
    - Core patterns AI must always follow

The [skills](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) structure adds convenience but isn't required. If you prefer keeping everything in Obsidian and manually referencing files, that works perfectly fine—you just lose automatic invocation.

Can you comment on the current copilot-instructions.md? Is it at an appropriate level of detaiL.   
Assessment of [copilot-instructions.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html)

**Overall: Excellent level of detail** - this is well-suited for AI-assisted VBA development. Here's my breakdown:

### ✅ Strengths

**1. Right Balance of Specificity**

- Concrete code examples for every pattern
- Shows both correct and incorrect approaches (e.g., cross-workbook instantiation)
- Includes the "why" behind patterns (e.g., xlwings sync requirement)

**2. Comprehensive Coverage**

- Architecture → Data patterns → Error handling → Testing → Integration
- Covers the full development lifecycle
- Domain-specific (VBA + ExcelSteps) not generic advice

**3. Actionable Examples**

- Every section has copy-pasteable code templates
- Shows complete function/sub structures with proper error handling
- Includes docstring requirements and formatting rules

**4. Well-Organized Hierarchy**

- Critical patterns (function architecture, error handling) prominently placed
- Testing framework thoroughly documented
- Quick reference sections (naming, file org) at end

### 📝 Minor Suggestions

**1. Consider Moving to Skills:**  
These sections could be extracted to separate skill files if the main file gets longer:

- [VBA_Arrays.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) ✅ already done
- [vs_code_setup.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) ✅ already done
- Potentially: "ExcelSteps Integration Patterns" → `excelsteps_patterns.md`
- Potentially: "Testing Framework" → `testing_patterns.md`

**2. Add Navigation Hints (Optional):**  
At the top, add a quick "when to read which section":

**3. Consolidate Cross-References:**  
The file mentions [vs_code_setup.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) skill—consider adding forward references to other skills like [VBA_Arrays.md](vscode-file://vscode-app/c:/Users/j.d.landgrebe/AppData/Local/Programs/Microsoft%20VS%20Code/61b3d0ab13/resources/app/out/vs/code/electron-browser/workbench/workbench.html) where relevant.

### copilot-instructions.md Length Assessment

**Current: ~385 lines - APPROPRIATE**
- Short enough to load into context efficiently
- Long enough to be comprehensive
- Good ratio of explanation to code examples

**If it grows beyond ~500 lines**, consider:
- Moving testing framework to separate skill
- Moving ExcelSteps integration patterns to separate skill
- Keep core architecture and function patterns in main file

### 🎯 Bottom Line

**This is at the right level of detail.** It's:
- Specific enough to generate correct code patterns
- Comprehensive enough to cover the full workflow
- Concise enough to be maintainable
- Well-balanced between rules and examples

The file effectively serves as both a **reference manual** and a **code template library**, which is exactly what AI needs for consistent code generation in a specialized domain like VBA+ExcelSteps.

**Recommendation: Keep as-is.** Only split into additional skills if you find yourself adding significant new domains (e.g., if you add web API integration, reporting templates, etc.).