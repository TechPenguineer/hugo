---
title: NumberOfElements
description: Returns the number of pages in the current pager.
categories: []
keywords: []
params:
  functions_and_methods:
    returnType: int
    signatures: [PAGER.NumberOfElements]
---

```go-html-template
{{ $pages := where site.RegularPages "Type" "posts" }}
{{ $paginator := .Paginate $pages }}

{{ range $paginator.Pages }}
  <h2><a href="{{ .RelPermalink }}">{{ .LinkTitle }}</a></h2>
{{ end }}

{{ with $paginator }}
  {{ .NumberOfElements }}
{{ end }}
```
