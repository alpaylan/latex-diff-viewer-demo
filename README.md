# latex-diff-viewer — live demo

A tiny multi-page LaTeX paper (`paper.tex`) wired up with
[**latex-diff-viewer**](https://github.com/alpaylan/latex-diff-viewer) so you can
see the tool end-to-end on a real repository.

## 👉 Open the viewer: https://alpaylan.github.io/latex-diff-viewer-demo/

Pick a **Base** and **Compare** commit and hit *Show diff* — added text is blue and
underlined, removed text is red and struck through. Click a page in the
**Changed pages** list to jump to it.

### What each commit changes

| Commit | Change | What the diff shows |
|--------|--------|---------------------|
| Initial draft | the whole paper | — |
| Sharpen the abstract and introduction | reworded abstract + a new intro paragraph | inline text edits on **page 1** |
| Rework the results table | extra column + row, new caption | a **float** change reported on the page it lands (float-aware index) |
| Add a limitations section | a new section | added content later in the paper |

### Try it yourself

- **On-demand diff:** [open an issue titled `latexdiff <base>..<head>`](https://github.com/alpaylan/latex-diff-viewer-demo/issues/new?title=latexdiff%20HEAD~2..HEAD)
  (any two commits, branches, or tags). A bot builds it, comments the viewer link,
  and closes the issue. The viewer's **Request diff** button does exactly this.
- **Pull request:** open a PR that edits `paper.tex` — you'll get a comment linking
  the rendered diff.

This whole setup is one workflow file (`.github/workflows/latex-diff.yml`) plus a
one-line `difftool.toml`. See the [tool README](https://github.com/alpaylan/latex-diff-viewer#readme).
