# liuguanlin818.github.io

Personal academic homepage for **Guanlin Liu**, laid out with the
[Academic Pages](https://academicpages.github.io/) design (the Minimal Mistakes
theme that academicpages is built on).

Because the site is plain static HTML, GitHub Pages serves it directly — there is
no Jekyll/Ruby build step, and no `_config.yml` to maintain.

Live at <https://liuguanlin818.github.io/>.

## Structure

```
index.html               About: intro, research interests, education, selected publications
publications/index.html  all publications grouped by type
research/index.html      research statement, EHR-to-EEG comparison, current proposal
awards/index.html        grants, patents, software copyrights, competition awards
cv/index.html            full CV in HTML
404.html                 not-found page
images/profile.jpg       sidebar avatar
images/favicon.svg       browser tab icon
files/Liu_Guanlin_CV.pdf printable CV
assets/css/main.css      Minimal Mistakes theme stylesheet (do not edit)
assets/css/fontawesome.css  icon font stylesheet (do not edit)
assets/css/custom.css    all site-specific styling lives here
assets/webfonts/         Font Awesome woff2 files
.nojekyll                tells GitHub Pages not to run Jekyll
```

## Editing content

The pages are generated from a single script, `tools/build_site.py`, so the
header, sidebar and footer stay in sync across all five pages. `tools/` is
listed in `.gitignore`, so the tooling stays local and never reaches the
published site — the repository itself holds only the 19 files above.

```
C:\Python311\python.exe tools\build_site.py      # regenerate the pages
C:\Python311\python.exe tools\preview.py         # regenerate + serve + open a browser
C:\Python311\python.exe tools\publish.py -m "msg"  # regenerate + commit + push
C:\Python311\python.exe tools\make_avatar.py "photo.jpg" --mode half  # 3:4 avatar
```

`tools\维护手册.md` documents the whole workflow, including the VS Code tasks in
`.vscode\tasks.json` (build / preview / publish / avatar).

All text content lives in `tools/build_site.py`; all styling in
`assets/css/custom.css`. Do not hand-edit the generated `index.html` files —
they are overwritten on the next build.

## Publishing

```
C:\Python311\python.exe tools\publish.py -m "Describe the change"
```

or, from the repository root:

```
git add -A && git commit -m "Describe the change" && git push
```

GitHub Pages picks the change up within a minute or two; press `Ctrl+F5` to
bypass the browser cache.
