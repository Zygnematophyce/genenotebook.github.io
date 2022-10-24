---
section: 2. Adding data
path: /documentation/adding-orthogroups
title: Orthogroup phylogenetic trees
order: 3
---
```
genenotebook add orthogroups [options] <OrthoFinder tree folder>
```

<br/>

__OrthoFinder behavior__

Orthofinder will use each proteome filename as the name for that species. However, Genotebook does not know the filename of each proteome if it is not given in the parameter. 

<br/>

_Prefixe options_

- `-pfx, --prefixe [prefixe]`  List each proteome filenames as a name for that species contained in a file or folder.

Example for a folder:

```
# Folder that contain the list of proteome filename e.g. :
#.
#├── proteomes
#│   ├── Citrus_sinensis.fasta
#│   └── Somus_speciesus.fasta
#├── newicks
#│   ├── OG0000001_tree.txt
#│   └── OG0000002_tree.txt
genenotebook add orthogroups newicks/ -pfx proteomes/
```

Example for a file:
```
# File that contain the list of proteome filename e.g. :
# cat list.txt
# Citrus_clementina.fasta, Citrus_sinensis.fasta,
genenotebook add orthogroups newicks/ -pfx list.txt
```

<br/>

or 

<br/>

- `-l, --list [prefixe]`       List of each proteome filename as the name for that species enumerated by hand.

e.g.
```
genenotebook add orthogroups newicks/ --list "Citrus_sinensis, Somus_speciesus"
```
 
<br/>

_Ignore options_

In case you want to override the behavior of OrthoFinder

- `f, --force [force]` Ignore the use of prefixes.

e.g.
```
genenotebook add orthogroups newicks/ --force
```

<br/>

_Connection options_
- `--port <port>` Port on which the GeneNoteBook daemon is serving

<br/>

_Security options_

Only admin accounts are allowed to connect to a running daemon and add data

- `-u, --username <username>` Admin username
- `-p, --password <password>` Admin password
