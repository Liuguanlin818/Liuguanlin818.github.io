# liuguanlin818.github.io

Personal academic homepage for **Guanlin Liu**, laid out with the
[Academic Pages](https://academicpages.github.io/) design (the Minimal Mistakes
theme that academicpages is built on).

Because the site is plain static HTML, GitHub Pages serves it directly — there is
no Jekyll/Ruby build step, and no `_config.yml` to maintain.

## Structure

```
index.html               About: intro, research interests, education, selected publications
publications/index.html  all publications grouped by type
research/index.html      research statement, EHR-to-EEG comparison, current proposal
awards/index.html        grants, patents, software copyrights, competition awards
cv/index.html            full CV in HTML
404.html                 not-found page
images/profile.jpg       sidebar avatar (480 x 480)
images/favicon.svg       browser tab icon
files/Liu_Guanlin_CV.pdf printable CV, generated from cv/index.html
assets/css/              main.css + fontawesome.css (from the academicpages theme) + custom.css
assets/webfonts/         Font Awesome woff2 files
.nojekyll                tells GitHub Pages not to run Jekyll
```

All site-specific styling lives in `assets/css/custom.css`. `main.css` and
`fontawesome.css` are stock theme files — do not edit them.

## Editing content

The pages are generated from a single script so the header, sidebar and footer
stay in sync. The generator is kept outside this folder at
`E:\Program Files (x86)\海外导师采集\website_lgl_tmp\build_site.py`, and writes
into this directory. Run it with:

```
C:\Python311\python.exe "E:\Program Files (x86)\海外导师采集\website_lgl_tmp\build_site.py"
```

If you would rather hand-edit, each `index.html` is self-contained and readable —
just keep the `head`/sidebar markup identical across pages.

## Publishing

```
cd "E:\Program Files (x86)\海外导师采集\website_lgl"
git remote add origin git@github.com:Liuguanlin818/liuguanlin818.github.io.git
git push -u origin main --force
```

`--force` replaces the old Next.js export that used to be in the repository. If
you want to keep that history instead, clone the repository first, delete its old
files, copy this folder's contents in, and push normally.

After the push, GitHub Pages rebuilds within a minute or two and the site is live
at <https://liuguanlin818.github.io/>.
