---
section: 2. Adding data
path: /documentation/adding-interproscan
title: Protein domain predictions
order: 4
---
```
genenotebook add interproscan [options] <InterProScan GFF3 or TSV output file>
```

<br/>

_Format option_

- `--format [parser] ` Choose a parser for the interproscan output files.

Example:

```
genenotebook add interproscan testdata_iprscan.tabular --format tsv
```

<br/>

_Connection options_
- `--port <port>` Port on which the GeneNoteBook daemon is serving

<br/>

_Security options_

Only admin accounts are allowed to connect to a running daemon and add data

- `-u, --username <username>` Admin username
- `-p, --password <password>` Admin password
