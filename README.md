# ACT2
This repository contains the ACT2 multi-disciplinary citation classification dataset.

It is stored in tab-separated value (tsv) format and contains the following columns:
- unique_id
- core_id
- citation_offset
- total_doc_length
- section_info
- citing_title
- citing_author
- citing_publication_info
- citing_abstract
- cited_title
- cited_author
- cited_doi
- cited_publication_date
- cited_publication_info
- citation_context
- self_citation
- direct_citations
- co_mentions
- citation_class_label
- citation_influence_label

To load e.g. in Python:
```
import pandas
df = pandas.read_csv(path_to_act2.tsv, sep="\t", index_col="unique_id")
```