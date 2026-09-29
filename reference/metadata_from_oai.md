# Internal function for OAI-MPH interface to the Dryad database

Internal function for OAI-MPH interface to the Dryad database

## Usage

``` r
metadata_from_oai(query, curl = curl)
```

## Arguments

- query:

  a properly formed url query to dryad

- curl:

  if calling in series many times, call getCurlHandle() first and then
  pass the return value in here. Avoids repeated handshakes with server.

## See also

[`dryad_metadata`](https://docs.ropensci.org/treebase/reference/dryad_metadata.md)
