# Natural Language Text to SQL Query Conversion Using NLP and Deep Learning



## Dataset:

The Dataset used in this project is a large crowd-sourced dataset for developing natural language interfaces for relational databases. This dataset consists of 80654 hand-annotated examples of questions and SQL queries distributed across 24241 tables from Wikipedia. The data files can be found in the Data folder. It is released along with the paper "Seq2SQL: Generating Structured Queries from Natural Language using Reinforcement Learning".

### Citation
```
@article{zhongSeq2SQL2017,
  author    = {Victor Zhong and
               Caiming Xiong and
               Richard Socher},
  title     = {Seq2SQL: Generating Structured Queries from Natural Language using
               Reinforcement Learning},
  journal   = {CoRR},
  volume    = {abs/1709.00103},
  year      = {2017}
}
```
### Data Content

80654 questions in the dataset is divided into three seperate files for train, validation, and test files, each consisting of 56355, 8421, 15878 natural language and SQL queries respectively.

`train.jsonl` ,`dev.jsonl` and `test.jsonl` contains the following fields:

- `table_id`: the database id to which this question is addressed.
- `question`: the natural language question
- `sql`: the SQL query corresponding to the question.
 
`train.tables.jsonl`,`dev.tables.jsonl`, `test.tables.jsonl`  contains the following information for each database:

- `id`: database id
- `header`: table header
- `types`: datatypes for header 
- `rows`: corresponding rows of the table
- `name`: original table names stored in the database.
- `page_title`: name of the page
- `section_title`: name of the section
- `caption`: table caption
- `page_id`: Page id

## Steps for execution

`preprocessing.ipynb` file helps in creating the tokenized dataset. These datasets consists of tokenized version of natural language question and SQL query. It also helps for the exploratory data analysis of the datasets.

`Encoder-Decoder-attention.ipynb` file contains seq2seq Encoder-Decoder with attention target model. Upon completion of the run, the code will generate loss graph.
