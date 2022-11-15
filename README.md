# Language and Power of Workplace Conversation

An NLP analysis of Slack 

![](assets/logo.png)

## Overview

The primary goal is to investigate language power using LIWC (our source code is aligned with LIWC-22 and a license should be installed on your computer). The following exploratory analyses are also supported (see [data pipeline](https://github.com/sherl9/Language-Power-of-Workplace-Conversation/blob/main/visual/data_pipeline.pdf)):

* Sentiment analysis
* Politeness analysis
* Sytle similarity analysis

The structure of the current repository:

* `config.txt`: configuration file
* `*.ipynb`: source code
* `/data`: overall this is the folder of inputs including the Wikipedia and StackExchange politeness datasets. It is also where you will place the raw slack data (Note that we cannot disclose our dataset on GitHub for privacy issues)
* `/visual`: visualization files will be stored here
* `/results`: analysis results (in tabular format) will be stored here

Overall, the source code could be run automatically after a minimal amount of configuration, i.e., you only need to check if the required data is present and modeficate `config.txt`.

## LIWC analysis

Make sure LIWC-22 is installed on your computer and keep its desktop running while you run notbook #3. 


## Exploratory analyis