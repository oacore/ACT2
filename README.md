# ACT2
This repository contains the ACT2 multi-disciplinary citation classification dataset published in
(S.N. Kunnath et al., in preparation).
### Data
The released data comprises 
- the main dataset `ACT2_dataset.tsv`.
- the 229 pdfs containing the 4000 citations from the datset (`pdf` folder)
### Format
The dataset `ACT2_dataset.tsv` is stored in tab-separated value (tsv) format and contains the following columns:
```
unique_id
core_id
citation_offset
total_doc_length
section_info
citing_title
citing_author
citing_publication_info
citing_abstract
cited_title
cited_author
cited_doi
cited_publication_date
cited_publication_info
citation_context
self_citation
direct_citations
co_mentions
citation_class_label
citation_influence_label
```
For descriptions of each feature, see (S.N. Kunnath et al., in preparation).
### How to Load
#### Python
```python
import pandas
dataset = pandas.read_csv("path/to/ACT2_dataset.tsv", sep="\t", index_col="unique_id")
```
#### R
```
dataset <- read.table(file="path/to/ACT2_dataset.tsv", sep="\t", header=TRUE)
```