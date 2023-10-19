[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4493224.svg)](https://doi.org/10.5281/zenodo.4493224)

# mmt_2020-11-19_11-38
Topic Model of roman18 corpus (Nov 2020)

This repository contains the results, scripts and input files for a topic modeling performed in the context of Mining and Modeling Text, a project which is located at the Trier Center for Digital Humanities (TCDH) at Trier University.

It was created on November 19, 2020.


## Parameters

* Corpus: https://github.com/MiMoText/roman18 (Status: 19.11.20, 92 texts)
* size of textchunks: 1000 words
* number of topics: 30
* iterations: 2000
* number of optimizations: 10

## Results
* document-topic-distribution in https://github.com/MiMoText/mmt_2020-11-19_11-38/blob/main/results/mmt_2020-11-19_11-38/mastermatrix.csv
* topic-word-distribution in https://github.com/MiMoText/mmt_2020-11-19_11-38/blob/main/results/mmt_2020-11-19_11-38/topicwords.csv
* pyLDAVis-visualization (https://github.com/MiMoText/mmt_2020-11-19_11-38/blob/main/results/mmt_2020-11-19_11-38/visualization.html)
* wordles of each topic (https://github.com/MiMoText/mmt_2020-11-19_11-38/tree/main/results/mmt_2020-11-19_11-38/wordles)

Example Topic 7:
![Wordle Topic 7](/results/mmt_2020-11-19_11-38/wordles/topic_007.png)

## Derivation of statements for the MiMoTextBase
* can be found here: https://github.com/MiMoText/topicmodeling/blob/master/topic%20statements/mmt_2020-11-19_11-38_statements.csv

### Explanation
The resulting Topic Model consists of a predefined number of Topics consisting of a probability distribution of the input words and a probability distribution of these Topics for each text document of the corpus.  Based on the most likely words, a label is assigned to each topic. Together with this information, topic statements are finally derived from the distribution of top topics per injected work. We consider the five most likely Topics for each novel, with prior sorting out of all Topics contained in less than 10% and in more than 80% of the corpus works.  In this way, very rare, partly work-specific, and very frequent, usually generic, topics are excluded, since they are of no use for a cross-work topic comparison. This leaves 25 topics that are included in the generation of topic statements.

It should be noted that basically every topic is present in every work. However, it only appears significantly above a certain probability, above which we speak in simplified terms of it being present in a work. The threshold value depends on the corpus size and number of topics. For the topic model described here, we have used a probability of 0.03 as the threshold value. With the help of this, we can calculate the percentage of texts in which each topic occurs.

## Licence
All texts, here used as input files, are in the public domain and can be reused without restrictions. We don’t claim any copyright or other rights on the transcription, markup, metadata or scripts. If you use our data and scripts, for example in research or teaching, please reference this collection using the citation suggestion below.

## Citation suggestion
Topic Model of roman18 corpus (Nov 2020), edited by Anne Klee and Julia Röttgermann. Release v0.1.0. Trier: TCDH, 2021. URL: https://github.com/MiMoText/mmt_2020-11-19_11-38. DOI: 10.5281/zenodo.4493224.
