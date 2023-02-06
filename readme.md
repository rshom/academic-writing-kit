# Paper Starter Kit

## Usage ##

The starter kit includes a latex and markdown template with question
prompts to help fill it in. 

The file also includes project files for emacs pandoc-mode. If using
standalone pandoc use the following command to run the conversion.

``` 
/usr/local/bin/pandoc --read=markdown --write=latex --output=template.pdf --filter=pandoc-crossref --citeproc --csl=ieee.csl --standalone --include-in-header=header.tex --bibliography=ref.bib --lua-filter=scholarly-metadata.lua --lua-filter=author-info-blocks.lua
```

