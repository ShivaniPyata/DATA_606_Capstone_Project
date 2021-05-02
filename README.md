# Natural Language Text to SQL Query Conversion Using NLP and Deep Learning



## Dataset:

The Dataset used in this project is a large-scale complex and cross-domain semantic parsing and text-to-SQL dataset annotated by Yale students. It consists of 10,181 questions and 5,693 unique complex SQL queries on 200 databases with multiple tables covering 138 different domains.

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

`train.json` and `dev.json` contain the following fields:
- `question`: the natural language question
- `question_toks`: the natural language question tokens
- `db_id`: the database id to which this question is addressed.
- `query`: the SQL query corresponding to the question.
- `query_toks`: the SQL query tokens corresponding to the question.
 
`tables.json` contains the following information for each database:
 
- `db_id`: database id
- `table_names_original`: original table names stored in the database.
- `table_names`: cleaned and normalized table names. 
- `column_names_original`: original column names stored in the database. Each column looks like: [0, "id"]. 0 is the index of table names in table_names, which is a city in this case. "id" is the column name.
- `column_names`: cleaned and normalized column names.
- `column_types`: data type of each column
- `foreign_keys`: foreign keys in the database. 
- `primary_keys`: primary keys in the database. Each number is the index of column_names.
