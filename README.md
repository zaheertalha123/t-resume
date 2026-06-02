# t-resume

Professional CV/resume for **Muhammad Talha Zaheer**, written in LaTeX.

## Prerequisites

1. **MiKTeX** (or TeX Live) — [https://miktex.org/download](https://miktex.org/download)
2. **LaTeX Workshop** extension in Cursor/VS Code — extension ID: `James-Yu.latex-workshop`

After installing MiKTeX, restart Cursor so the extension can find `pdflatex`.

On first compile, MiKTeX may prompt to install missing packages (e.g. `geometry`, `enumitem`, `hyperref`, `titlesec`, `tabularx`). Click **Install** when asked.

## Compile in Cursor (recommended)

1. Open this folder in Cursor.
2. Open `resume.tex`.
3. Save the file (`Ctrl+S`) — LaTeX Workshop builds automatically on save.
4. View the PDF:
   - `Ctrl+Alt+V`, or
   - `Ctrl+Shift+P` → **LaTeX Workshop: View LaTeX PDF**

Other useful commands (`Ctrl+Shift+P`):

| Command | Purpose |
|---------|---------|
| LaTeX Workshop: Build LaTeX project | Build manually |
| LaTeX Workshop: View LaTeX PDF file in web browser | Open PDF in browser |

**SyncTeX:** `Ctrl+Click` in the PDF preview to jump to the matching line in `resume.tex`.

## Compile from the terminal

### PowerShell (Windows)

If `pdflatex` is not recognized, use the full MiKTeX path:

```powershell
cd e:\AstroLinx\t-resume

& "$env:LOCALAPPDATA\Programs\MiKTeX\miktex\bin\x64\pdflatex.exe" -interaction=nonstopmode resume.tex
```

Run the command twice if you add cross-references or a table of contents later.

If MiKTeX is on your PATH:

```powershell
pdflatex -interaction=nonstopmode resume.tex
```

### Output

The compiled PDF is written to:

```
resume.pdf
```

## Project files

| File | Description |
|------|-------------|
| `resume.tex` | Main LaTeX source — edit this file |
| `resume.pdf` | Generated resume (share/submit this) |
| `resume.aux`, `resume.log`, `resume.out` | Build artifacts (safe to delete; regenerated on compile) |

## Editing tips

- Update contact info, experience, and skills in `resume.tex`.
- Save and preview after each change.
- If the build fails, open **View → Output**, select **LaTeX Workshop**, and read the error log.

## Optional: ignore build artifacts in Git

Add to `.gitignore` if you use version control:

```
*.aux
*.log
*.out
*.synctex.gz
```

Keep `resume.tex` and optionally `resume.pdf` tracked in the repo.
