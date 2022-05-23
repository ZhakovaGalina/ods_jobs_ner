# ods_jobs_ner
This is a project on extracting entities from the posts with vacancies in ODS jobs slack channel.
Detailed information can be found in the report: NER_jobs_ODS_report.pdf

Tags:
- VAC - information about the vacancy (job title and candidate level)
- LOC - location (city and metro)
- SAL - salary (including information about taxes, not including information
about bonuses)
- WST - work style (remote, partially remote, a few days in the office etc.)


Model results on test dataset:

|   | F1 |
| ------------- | ------------- |
| ner f1   | 69.12  |
| ner token f1  | 80.35  |
| VAC    | 70.73  |
| SAL  | 71.28  |
| LOC    | 70.73  |
| WST | 59.09  |


Data description:

- data/job_title_true.csv - job title true labeles
- data/level_true.csv - job level true labeles
- data/model_result.csv - result of the model
- data/train.txt - data for model train
- data/valid.txt - data for model validation
- data/test.txt - data for model test
- data/yargy_and_reg_ex_result.csv - results of other approaches (https://github.com/kuk/analyze-ods-jobs, https://github.com/egorborisov/jobs_article)


- NER_jobs_ODS_report.pdf - project report
- ner_ontonotes_bert_mult_torch.json - model config
- DeepPavlovNER_model.ipynb - model train and apply
- Metrics.ipynb - calculation of metrics



