# Prompt Template — Create Memory File

**Goal:** Generate or update a memory file inside the `memory/` folder  
to document important project context or environment information.

---

## Example Prompts

### 🧩 Example: Create Environment Audit File
Please create a new file named `memory/dev_environment.md`  
and save the full development environment audit results we just generated inside it.  
Use clear Markdown formatting with a table of tools, versions, and paths,  
and include a short **Notes** section at the end.

---

### 🧩 Example: Create Project Context File
Please create a new file named `memory/project_context.md`  
summarizing the purpose of this base project, its folder structure,  
and how it should be used as a template for future Claude Code projects.

---

## Notes
- Always run this in **Agent Mode** (so Claude can actually write the file).  
- Use consistent naming: `dev_environment.md`, `project_context.md`, `workflow_notes.md`, etc.  
- Keep prompts modular and reusable across different projects.
