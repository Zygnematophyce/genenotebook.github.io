---
section: 2. Adding data
path: /documentation/adding-similar-sequences
title: Sequence aligner
order: 5
---

__BLAST__
```
genenotebook add blast [options] <Blast output formats .XML, .TXT file>
```

or 


__Diamond__
```
genenotebook add diamond [options] <Diamond output formats .XML, .TXT file>
```

<br/>

_Aligner options_

- `-alg, --algorithm <algorithm>` The algorithm used to compare the sequences to a database (e.g: **blastx**, **blastp**).
- `-db,  --database  <database>`  The database used to compare the sequences (e.g: **Non-redundant protein sequences** (nr)).
- `-mtx, --matrix    <matrix>`    The matrix of substitution used for sequence alignment (e.g: **BLOSUM90, BLOSUM80, PAM100 ...**).

e.g.
```
genenotebook add diamond --algorithm blastp pairwise.txt --database "Non-redundant protein sequences" --matrix "BLOSUM90"
```

<br/>

_Format option_
- `-fmt, --format <parser>` Choose a parser for the blast output format.

<br/>

_Connection options_
- `--port <port>` Port on which the GeneNoteBook daemon is serving

<br/>

_Security options_

Only admin accounts are allowed to connect to a running daemon and add data

- `-u, --username <username>` Admin username
- `-p, --password <password>` Admin password
