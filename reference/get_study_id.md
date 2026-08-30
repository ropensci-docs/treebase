# return the study.id from the search results.

get_study_id is deprecated, and now can be performed more easily using
phylo_metadata and oai_metadata search functions.

## Usage

``` r
get_study_id(search_results)
```

## Arguments

- search_results:

  the output of download_metadata, or a subset thereof

## Value

the study id

## Details

this function is commonly used to get trees corresponding to the
metadata search.
