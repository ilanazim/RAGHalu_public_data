# RAGHalu Public Data

This repo contains the public data used to train RAGHalu (Two-tiered Encoder-based Hallucination Detection for
Retrieval-Augmented Generation in the Wild), comprising of modified data from [FactScore](https://github.com/shmsw25/FActScore), [HaluEval](https://github.com/RUCAIBox/HaluEval), [Dolly Databricks](https://huggingface.co/datasets/databricks/databricks-dolly-15k), and [TruthfulQA](https://huggingface.co/datasets/truthfulqa/truthful_qa). Data from the aforementioned data sets were modified and aggregated as descibed in Appendix A.1 of RAGHalu.

The data is released both [here](RAGHalu_public) and [on HuggingFace Datasets](https://huggingface.co/datasets/liveperson/raghalu-open)

## Data Organization

Data organization is as described below. The json lines files can be read with the Python pandas package as follows `pd.read_json(<data_path>, lines=True)`.
RAGHalu1 contains the data used to train, validate and test the VERIFIABLE (label 1), NO-INFO (label 0) stage one model described in the paper, and RAGHalu2 contains the data used to train the SUPPORTED (label 1) and UNSUPPORTED (label 0) tier-2 model described in the paper.

```
RAGHalu_public
    - RAGHalu1
      - train.jsonl
      - test.jsonl
    - RAGHalu2
      - train.jsonl
      - test.jsonl
```

## License

This project is licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
