# return the trees in treebase that correspond to the search results get_study is deprecated, and now can be performed more easily using phylo_metadata and oai_metadata search functions.

return the trees in treebase that correspond to the search results
get_study is deprecated, and now can be performed more easily using
phylo_metadata and oai_metadata search functions.

## Usage

``` r
get_study(search_results, curl = getCurlHandle(), ...)
```

## Arguments

- search_results:

  the output of download_metadata, or a subset thereof

- curl:

  the handle to the curl web utility for repeated calls, see the
  getCurlHandle() function in RCurl package for details.

- ...:

  additional arguments to pass to search_treebase

## Value

all corresponding phylogenies.

## Details

this function is commonly used to get trees corresponding to the
metadata search.
