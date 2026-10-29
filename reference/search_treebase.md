# A function to pull in the phyologeny/phylogenies matching a search query

A function to pull in the phyologeny/phylogenies matching a search query

## Usage

``` r
search_treebase(
  input,
  by,
  returns = c("tree", "matrix"),
  exact_match = FALSE,
  max_trees = Inf,
  branch_lengths = FALSE,
  curl = getCurlHandle(),
  verbose = TRUE,
  pause1 = 0,
  pause2 = 0,
  attempts = 3,
  only_metadata = FALSE
)
```

## Arguments

- input:

  a search query (character string)

- by:

  the kind of search; author, taxon, subject, study, etc (see list of
  possible search terms, details)

- returns:

  should the fn return the tree or the character matrix?

- exact_match:

  force exact matching for author name, taxon, etc. Otherwise does
  partial matching

- max_trees:

  Upper bound for the number of trees returned, good for keeping
  possibly large initial queries fast

- branch_lengths:

  logical indicating whether should only return trees that have branch
  lengths.

- curl:

  the handle to the curl web utility for repeated calls, see the
  getCurlHandle() function in RCurl package for details.

- verbose:

  logical indicating level of progress reporting

- pause1:

  number of seconds to hesitate between requests

- pause2:

  number of seconds to hesitate between individual files

- attempts:

  number of attempts to access a particular resource

- only_metadata:

  option to only return metadata about matching trees which lists
  study.id, tree.id, kind (gene,species,barcode) type (single,
  consensus) number of taxa, and possible quality score.

## Value

either a list of trees (multiphylo) or a list of character matrices

## Examples

``` r
if (FALSE) { # \dontrun{
## defaults to return phylogeny
Huelsenbeck <- search_treebase("Huelsenbeck", by="author")

## can ask for character matrices:
wingless <- search_treebase("2907", by="id.matrix", returns="matrix")

## Some nexus matrices don't meet read.nexus.data's strict requirements,
## these aren't returned
H_matrices <- search_treebase("Huelsenbeck", by="author", returns="matrix")

## Use Booleans in search: and, or, not
## Note that by must identify each entry type if a Boolean is given
HR_trees <- search_treebase("Ronquist or Hulesenbeck", by=c("author", "author"))

## We'll often use max_trees in the example so that they run quickly,
## notice the quotes for species.
dolphins <- search_treebase('"Delphinus"', by="taxon", max_trees=5)
## can do exact matches
humans <- search_treebase('"Homo sapiens"', by="taxon", exact_match=TRUE, max_trees=10)
## all trees with 5 taxa
five <- search_treebase(5, by="ntax", max_trees = 10)
## These are different, a tree id isn't a Study id.  we report both
studies <- search_treebase("2377", by="id.study")
tree <- search_treebase("2377", by="id.tree")
c("TreeID" = tree$Tr.id, "StudyID" = tree$S.id)
## Only results with branch lengths
## Has to grab all the trees first, then toss out ones without branch_lengths
Near <- search_treebase("Near", "author", branch_lengths=TRUE)
 } # }
```
