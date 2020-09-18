# How to create a reproducible PDF in R markdown with APA formatting

An basic example of how to prepare an APA style PDF using <a href="https://rmarkdown.rstudio.com/">R Markdown</a> in <a href="https://rstudio.com/">RStudio</a>.


``` YAML

---
bibliography: "example.bib"
csl: "apa-single-spaced.csl"
editor_options:
  chunk_output_type: console
chunk_output_type: console
fontsize: 11pt
geometry: margin=1in
output:
  pdf_document:
    keep_tex: true
    fig_caption: yes
    includes:
      in_header: "apa.tex"
subparagraph: true 
---

```

The bibliography is a bib file, created using <a href="https://www.zotero.org/">Zotero</a> and <a href="https://github.com/retorquere/zotero-better-bibtex">Better BibTeX for Zotero</a>. This holds all of the information we need to create in-text citations and the references section at the end of the document.

CSL is a  <a href="https://github.com/citation-style-language/styles">Citation Styles Language</a> file that organises in the bibliographic information into APA-7 formatting. Many other styles are available if needed.

The `in_header` parameter allows us to run an external LaTeX file (`apa.tex`) where we can set APA formatting. 

For a published example that includes figures and tables, see <a href="https://osf.io/mjv73/">this OSF repository</a>.
