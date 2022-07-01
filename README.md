# ACT2 (LREC2022)
This repository contains the ACT2 multi-disciplinary citation classification dataset ([paper](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.363.pdf)).

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
For descriptions of each feature, see [paper](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.363.pdf).
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
### Citation
```
@InProceedings{nambanoorkunnath-EtAl:2022:LREC,
  author    = {Nambanoor Kunnath, Suchetha  and  Stauber, Valentin  and  Wu, Ronin  and  Pride, David  and  Botev, Viktor  and  Knoth, Petr},
  title     = {ACT2: A multi-disciplinary semi-structured dataset for importance and purpose classification of citations},
  booktitle      = {Proceedings of the Language Resources and Evaluation Conference},
  month          = {June},
  year           = {2022},
  address        = {Marseille, France},
  publisher      = {European Language Resources Association},
  pages     = {3398--3406},
  abstract  = {Classifying citations according to their purpose and importance is a challenging task that has gained considerable interest in recent years. This interest has been primarily driven by the need to create more transparent, efficient, merit-based reward systems in academia; a system that goes beyond simple bibliometric measures and considers the semantics of citations. Such systems that quantify and classify the influence of citations can act as edges that link knowledge nodes to a graph and enable efficient knowledge discovery. While a number of researchers have experimented with a variety of models, these experiments are typically limited to single-domain applications and the resulting models are hardly comparable. Recently, two Citation Context Classification (3C) shared tasks (at WOSP2020 and SDP2021) created the first benchmark enabling direct comparison of citation classification approaches, revealing the crucial impact of supplementary data on the performance of models. Reflecting from the findings of these shared tasks, we are releasing a new multi-disciplinary dataset, ACT2, an extended SDP 3C shared task dataset. This modified corpus has annotations for both citation function and importance classes newly enriched with supplementary contextual and non-contextual feature sets the selection of which follows from the lists of features used by the more successful teams in these shared tasks. Additionally, we include contextual features for cited papers (e.g. Abstract of the cited paper), which most existing datasets lack, but which have a lot of potential to improve results. We describe the methodology used for feature extraction and the challenges involved in the process. The feature enriched ACT2 dataset is available at https://github.com/oacore/ACT2.},
  url       = {https://aclanthology.org/2022.lrec-1.363}
}
```
