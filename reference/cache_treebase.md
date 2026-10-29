# A function to cache the phylogenies in treebase locally

A function to cache the phylogenies in treebase locally

## Usage

``` r
cache_treebase(
  file = paste("treebase-", Sys.Date(), ".rda", sep = ""),
  pause1 = 3,
  pause2 = 3,
  attempts = 10,
  max_trees = Inf,
  only_metadata = FALSE,
  save = TRUE
)
```

## Arguments

- file:

  filename for the cache, otherwise created with datestamp

- pause1:

  number of seconds to hesitate between requests

- pause2:

  number of seconds to hesitate between individual files

- attempts:

  number of attempts to access a particular resource

- max_trees:

  maximum number of trees to return (default is Inf)

- only_metadata:

  option to only return metadata about matching trees

- save:

  logical indicating whether to save a file with the resuls.

## Value

saves a cached file of treebase

## Details

it's a good idea to let this run overnight

## Examples

``` r
if (FALSE) { # \dontrun{
 treebase <- cache_treebase()
} # }
```
