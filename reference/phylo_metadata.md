# Search the PhyloWS metadata

Search the PhyloWS metadata

## Usage

``` r
phylo_metadata(
  x = c("Study.id", "Tree.id", "kind", "type", "quality", "ntaxa"),
  metadata = NULL,
  ...
)
```

## Arguments

- x:

  one of "Study.ids", "Tree.ids", "kind", "type", "quality", "ntaxa"

- metadata:

  returned from `search_treebase` function. if not specified will
  download latest copy of PhyloWS metadata from treebase. Pass in search
  results value during repeated calls to speed function runtime
  substantially

- ...:

  additional arguments to `search_treebase`

## Value

a list of the values matching the query
