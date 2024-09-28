# Repository Overview

This repository contains several key components essential for utilizing and understanding our dataset and the FM metric code developed for evaluating text summaries. Here's a brief overview of the contents:

## Directories

The `dataset` directory contains processed datasets supporting the research in our papers. The `evaluation_code` directory includes scripts to assess metric performance on this dataset. Central to our research is the `FM_metric_code` directory, which implements our proposed evaluation paradigm using the FM metric code. 

The `Contact Form.pdf` offers a standardized form for users to report issues or request content removal to ensure compliance with copyright laws and personal privacy. The `appendix.pdf` includes supplementary materials such as detailed tables, figures, and extensive discussions that support the data and findings from our research. 


## Data Description

This README provides a detailed overview of the `pubmed.json` file, which includes structured data in JSON format for medical articles and associated summarization content. Each line in the file represents a distinct JSON object related to a specific article, including various summaries and metrics. Below, you will find a comprehensive breakdown of the keys available in each JSON entry and their meanings.

### Data Structure

Each JSON object in contains several key-value pairs where each key indicates a specific aspect of the data related to article summaries and evaluation metrics:

- **`article`**: The original text of the article which the summaries are derived from.
- **`human`**: This key contains the human-written summary of the article for reference.
- **`bigbird_pegasus`, `longt5`,`bigbird_pegasus_block`, `longt5_block`, `gpt35`, `llama2_70b`**: These keys hold the summaries generated by different models (BigBird-Pegasus, LongT5, GPT-3.5, Llama2 70b).

#### Model Specific Keys
For each summarization model, there are several associated keys providing further detail and metrics:

- **`[model]_aspect`**: Contains decomposition results as outlined in section 3.2 of the documentation. This data is available for various models including `gpt35`, `llama2_70b`, `bigbird_pegasus`, `longt5`, `bigbird_pegasus_block`, and `longt5_block`.
- **`[model]_human`**: Scores derived from human annotations, assessing the quality of model-generated summaries.
- **`[model]_human_list`**: Provides a detailed breakdown of scores according to the Benchmarking Metric for Reference Comparison (BMRC), evaluating specific aspects of the summaries.
- **`[model]_gpt4_fm`**, **`[model]_gpt35_fm`**: Scores from evaluations conducted by GPT-4 and GPT-3.5, respectively, using our Facet-aware Metric system to assess summary quality.
- **`[model]_gpt4_fm_list`**, **`[model]_gpt35_fm_list`**: Detailed lists of FM scores, evaluating various facets of the summaries.
- **`[model]_bert`**, **`[model]_delta`**: These entries reflect BERTScore and DELTA metrics respectively, providing insights into the linguistic quality and variation of the summaries.
- **`[model]_newrouge1`**, **`[model]_newrouge2`**, **`[model]_newrougel`**: Metrics measuring the n-gram overlap between the machine-generated summaries and reference texts, using enhanced ROUGE evaluations.
- **`[model]_questeval`**: A score from QuestEval, a contemporary metric designed to assess summarization quality beyond mere lexical matching.
- **`[model]_geval`**, **`[model]_acu3`**: Scores from G-EVAL and ACU-3, metrics designed to evaluate the overall effectiveness and coherence of the summaries.
- **`[model]_gpt4`**, **`[model]_llama`**: Evaluation scores attributed to the assessments made by the GPT-4 and Llama2 70B models.




### Usage

This JSON dataset can be used for a variety of purposes, including but not limited to:

- Benchmarking and comparing different summarization models.

- Analyzing the effectiveness of different summary evaluation metrics.

