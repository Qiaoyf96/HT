# Representation Sparsification with Hybrid Thresholding for Fast SPLADE-based Document Retrieval

This repo provides the Hybrid Thresholding (HT) checkpoints and [PISA](https://github.com/pisa-engine/pisa) indexes proposed in the paper "Representation Sparsification with Hybrid Thresholding for Fast SPLADE-based Document Retrieval".

## Evaluate
```
# calculate the relevance in parallel
./evaluate_queries -e block_simdbp -i splade-ht1.index -w splade-ht1.wand -q msmarco_dev.queries -k 10 -a maxscore --weighted -s quantized --documents msmarco.lex > msmarco_dev.trec

# measure the latency in single thread
./queries -e block_simdbp -i splade-ht1.index -w splade-ht1.wand -q msmarco_dev.queries -k 10 -a maxscore --weighted -s quantized
```

## Reference

```
@inproceedings{10.1145/3539618.3592051,
author = {Qiao, Yifan and Yang, Yingrui and He, Shanxiu and Yang, Tao},
title = {Representation Sparsification with Hybrid Thresholding for Fast SPLADE-based Document Retrieval},
year = {2023},
isbn = {9781450394086},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3539618.3592051},
doi = {10.1145/3539618.3592051},
booktitle = {Proceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval},
pages = {2329–2333},
numpages = {5},
keywords = {index pruning, learned sparse representations, top-k retrieval},
location = {<conf-loc>, <city>Taipei</city>, <country>Taiwan</country>, </conf-loc>},
series = {SIGIR '23}
}
```

