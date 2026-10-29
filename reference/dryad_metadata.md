# Search the dryad metadata archive

Search the dryad metadata archive

## Usage

``` r
dryad_metadata(study.id, curl = getCurlHandle())
```

## Arguments

- study.id:

  the dryad identifier

- curl:

  if calling in series many times, call getCurlHandle() first and then
  pass the return value in here. Avoids repeated handshakes with server.

## Value

a list object containing the study metadata

## Examples

``` r
if (FALSE) { # \dontrun{
  dryad_metadata("10255/dryad.12")
} # }
```
