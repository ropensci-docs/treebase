# imports phylogenetic trees from treebase. internal function

imports phylogenetic trees from treebase. internal function

## Usage

``` r
get_nex(
  query,
  max_trees = "last()",
  returns = "tree",
  curl = getCurlHandle(),
  verbose = TRUE,
  pause1 = 1,
  pause2 = 1,
  attempts = 5,
  only_metadata = FALSE
)
```

## Arguments

- query:

  : a phylows formatted search, see
  https://sourceforge.net/apps/mediawiki/treebase/index.php?title=API

- max_trees:

  limits the number of trees returned should be kept.

- returns:

  should return the tree object or the matrix (of sequences)

- curl:

  the handle to the curl

- verbose:

  a logical indicating if output should be printed to screen

- pause1:

  number of seconds to hesitate between requests

- pause2:

  number of seconds to hesitate between individual files

- attempts:

  number of attempts to access a particular resource

## Value

A list object containing all the trees matching the search (of class
phylo)
