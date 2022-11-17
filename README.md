# Language and Power of Workplace Conversation

An NLP analysis of Slack 

![](assets/logo.png)

# Overview

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

# LIWC Analysis

1. Make sure **LIWC-22** is installed on your computer. Make sure its desktop software is active while you run notbook #3 (this is how this program connects to the LIWC dictionary). 

2. Unzip your exported Slack data, put the folder under `/data`. Make sure the name of your Slack folder matches your configuration of "slack_dir" in `config.txt`. You may also specify cusotmized LIWC categories by modifcating `cat_all.txt`

3. Run through notebooks #1~#4. You may consult the results under `/results`. You may look under `visual` for the communication map and the file `/data/processed.csv` for the extracted messages, replies, reactions, and relevant Slack metadata.

# Exploratory Analyis

## BERT for Politeness

With notebook #5-1, you may verify the cross-domain accuracy of BERT (82.1%, trained on the SlackExchange and tested on the Wikipedia politeness datasets), and use it to make predications about Slack data. Please read the notebook's header for a more detailed guide. 

Checkpoint of the BERT model mentioned above is available at https://drive.google.com/drive/folders/17OJbUSi2KZTK_G5dyghZqfuixbpAPf7v?usp=sharing. 

Another model checkpoint (trained on Wikipedia, cross-domain accuracy of 70.1%) is available at https://drive.google.com/drive/folders/16wA3PXKbukU_UhP_EYWxsCGvQZ4uDsnt?usp=sharing.

## Weekly Sentiment and Politeness

Run notebook #5-2 (after running notebooks #1 through #4) to conduct user sentiment (politeness) analysis, along with a comparison of the weekly sentiment (politeness) scores of a user speaking to various listeners.

Consult `visual` for the results, some examples are provided here.

## Style Similarity Analysis

Following the completion of running notebooks #1 through #4, you may also run Notebook #6 to gain insights of conversational Language Style Matching (LSM) as presented in the report. Refer to the file `results/lsm results.csv` for examples of results.
