# Get the metadata associated with the study in which the phylogeny was published.

Get the metadata associated with the study in which the phylogeny was
published.

## Usage

``` r
show_metadata(study.id, curl = getCurlHandle())
```

## Arguments

- study.id:

  The treebase study id (numbers only, specify in quotes)

- curl:

  if calling in series many times, call getCurlHandle() first and then
  pass the return value in here. avoids repeated handshakes with server.

## Details

if the tree is imported with search_treebase, then this is in tree\$S.id
