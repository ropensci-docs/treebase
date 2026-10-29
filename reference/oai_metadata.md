# Search the OAI-PMH metadata by date, publisher, or identifier

Search the OAI-PMH metadata by date, publisher, or identifier

## Usage

``` r
oai_metadata(
  x = c("date", "publisher", "author", "title", "Study.id", "attributes"),
  metadata = NULL,
  ...
)
```

## Arguments

- x:

  one of "date", "publisher", "identifier" for the study

- metadata:

  returned from `download_metadata` function. if not specified will
  download latest copy from treebase. Pass in the value during repeated
  calls to speed function runtime substantially

- ...:

  additional arguments to `download_metadata`

## Value

a list of values matching the query
