# Language and Power of Workplace Conversation

An NLP analysis of Slack 

![](assets/logo.png)

## Overview

The primary goal is to investigate language power using LIWC (our source code is aligned with LIWC-22 and a license should be installed on your computer). The following exploratory analyses are also supported (see [data pipeline](https://github.com/sherl9/Language-Power-of-Workplace-Conversation/blob/main/visual/data_pipeline.pdf)):

* Sentiment analysis
* Politeness analysis
* Sytle similarity analysis

The structure of the current repository:

* `config.txt`: the configuration file, it is where you specify the paths of input and output. The value of "slack_dir" must be the name of your own Slack directory. It is suggested to keep the other values as default.
* `cat_all.txt`: the list of LIWC categories we consider as correlated to language power; you may define new dimensiosn you want to look into.
* `*.ipynb`: notebooks #1~#6 are the source code.
* `/data`: overall this is the folder of inputs including the Wikipedia and StackExchange politeness datasets. It is also where you will place the raw slack data (Note that we cannot disclose our dataset on GitHub for privacy issues)
* `/visual`: visualization files will be stored here
* `/results`: analysis results (in tabular format) will be stored here

Overall, the source code could be run automatically after a minimal amount of configuration, i.e., you only need to check if the required data is present and modeficate `config.txt`.

## LIWC analysis

1. Make sure LIWC-22 is installed on your computer. Make sure its desktop software is active while you run notbook #3 (this is how this program connects to the LIWC dictionary). 

2. Unzip your exported Slack data, put the folder under `/data`, and make sure the name of your Slack folder matches your configuration of "slack_dir" in `config.txt`. You may also specify cusotmized LIWC categories by modifcating `cat_all.txt`

3. Run through notebooks #1~#4. 

You can look for the extracted messages, replies, reactions and pertinent Slack metada in the file `/data/processed.csv`. Look under `/visual` for the communication map described in the report (we supply the communication map of our dataaset as an example). For the user average LIWC counts and pairwise t-test results, consult `/results`. 

## Exploratory analyis