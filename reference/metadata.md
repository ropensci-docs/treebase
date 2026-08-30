# metadata.rda

Contains a cache of all publication metadata the search_metadata() to
pull down when run on 2012-05-12.

## Usage

``` r
metadata(phylo.md = NULL, oai.md = NULL)
```

## Arguments

- phylo.md:

  cached phyloWS (tree) metadata, (optional)

- oai.md:

  cached OAI-PMH (study) metadata (optional)

## Value

a data frame of all available metadata, (as a data.table object) columns
are: "Study.id", "Tree.id", "kind", "type", "quality", "ntaxa" "date",
"publisher", "author", "title".

## Details

recreate with: ` search_metadata() `

## Examples

``` r
if (FALSE) { # \dontrun{
meta <- metadata()
meta[publisher %in% c("Nature", "Science") & ntaxa > 50 & kind == "Species Tree",]
} # }
```
