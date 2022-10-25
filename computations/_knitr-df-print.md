Você pode controlar como os dataframes são impressos por padrão utilizando a opção de documento `df-print`. As opções disponíveis incluem:

| Option    | Description                                                                                                                                                        |
|------------|------------------------------------------------------------|
| `default` | Use o método S3 padrão para o data frame.                                                                                                                      |
| `kable`   | Tabela Markdown usando a função  [`knitr::kable()`](https://bookdown.org/yihui/rmarkdown-cookbook/kable.html).                                                    |
| `tibble`  | Tabela de texto usando o pacote [`tibble`](https://tibble.tidyverse.org/).                                                                                      |
| `paged`   | Tabela HTML com paginação para linhas e colunas que não são apresentadas (implementado usando [`rmarkdown::paged_table()`](https://pkgs.rstudio.com/rmarkdown/reference/paged_table.html)) |

Por exemplo, aqui especificamos que queremos impressão paginada para o dataframe:

``` yaml
---
title: "Document"
format: 
   html:
     df-print: paged
---
```
