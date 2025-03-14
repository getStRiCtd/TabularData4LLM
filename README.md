# TabularData4GigaChat
**Bench LLMs on TableQA tasks**

The repository is designed to assess the quality of GigaChat table-questions answers depending on different ways of textual representation of tables.

## Representation formats tested: [^1]
1. Pure HTML table
2. [reStructured Text](https://sublime-and-sphinx-guide.readthedocs.io/en/latest/tables.html)
[^1]: No test markdown and other tables formats that uses ascii graphic.

## Methodology
- Prompt: CoT Few-Shot prompt
- Tested on random 1000 records from each dataset


## Results:
### [Tabfact](https://huggingface.co/datasets/ibm-research/tab_fact)
Accuracy, %

| Format/Model | GigaChat-Lite | GigaChat-Pro | GigaChat-Max |
|--------------|---------------|----------|-----------|
| HTML         | 65%           | 74%      | 85.5%     |
| reST         | 63%           | 68%      | 83%       |

### [WikiTQ](https://huggingface.co/datasets/Stanford/wikitablequestions)
Accuracy (exact match), %

| Format/Model | GigaChat-Lite | GigaChat-Pro | GigaChat-Max |
|--------------|---------------|--------------|--------------|
| HTML         | 25%           | -            | -            |
| reST         | 23%           | -            | -            |


## Reproduce code
1. Add **.env** to **deployment/.env** and paste your credentials

2. Install requirements:
```bash
  pip install -r req.txt
```

3. Run **tests.ipynb**
