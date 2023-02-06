# Paper Starter Kit

## Usage ##

The starter kit includes a latex and markdown template with question
prompts to help fill it in. 

The file also includes project files for emacs `pandoc-mode`. If using
standalone `pandoc` use the following command to run the conversion.

``` 
/usr/local/bin/pandoc --read=markdown --write=latex --filter=pandoc-crossref --citeproc --csl=ieee.csl --standalone --include-in-header=header.tex --bibliography=ref.bib --lua-filter=scholarly-metadata.lua --lua-filter=author-info-blocks.lua article.md
```

This should update the `article.pdf` file.

If using markdown with pandoc, update the class options in the yaml
section to match formatting needs.

```
classoption:
 - 10pt #9pt, 10pt, 11pt, 12p
 - draftcls #draft, draftcls, draftclsnofoot, final
 - technote #conference, journal, technote, peerreview, peerreviewca
 - letterpaper #letterpaper, a4paper, cspaper
 - oneside #oneside, twoside
 - onecolumn #twocolumn, onecolumn
```

If using latex, update the same class options in the header to match
formatting needs.

```
\documentclass[
  10pt,
  draftcls,
  technote,
  letterpaper,
  oneside,
  onecolumn]{IEEEtran}
```

If using pandoc update glossary in `header.tex` as needed. If using
latex, update glossary in header and refer to acronyms as in text
using the `\gls` or `glspl` commands.
