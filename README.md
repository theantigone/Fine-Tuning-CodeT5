# GenAI for Software Development (Fine-Tuning CodeT5 for Predicting ``if`` Statements)

* [1 Introduction](#1-introduction)  
* [2 Getting Started](#2-getting-started)  
  * [2.1 Preparations](#21-preparations)  
  * [2.2 Install Packages](#22-install-packages)  
  * [2.3 Run the fine-tuning model](#23-run-the-fine-tuning-model)  
* [3 Report](#3-report)  

---

# **1. Introduction**  
This project explores **code completing suitable ``if`` statements in Python functions**, leveraging **[CodeT5 Transformer model from Hugging Face (small-sized model)](https://huggingface.co/Salesforce/codet5-small)**. CodeT5 is a pre-trained encoder-decoder Transformer model designed for code understanding and generation. It has been trained on a large corpus of code across multiple programming languages and supports a range of downstream tasks such as code completion, summarization, translation, and generation.

---

# **2. Getting Started**  

This project is implemented in **Python 3.9+** and is compatible with **macOS, Linux, and Windows**.  

## **2.1 Preparations**  

(1) Clone the repository to your workspace:  
```shell
~ $ git clone https://github.com/theantigone/Fine-Tuning-CodeT5.git
```
(2) Navigate into the repository:
```shell
~ $ cd Fine-Tuning-CodeT5
~/Fine-Tuning-CodeT5 $
```
(3) Set up a virtual environment and activate it:

For macOS/Linux:
```shell
~/Fine-Tuning-CodeT5 $ python -m venv ./venv/
~/Fine-Tuning-CodeT5 $ source venv/bin/activate
(venv) ~/Fine-Tuning-CodeT5 $ 
```

For Windows:
```shell
~/Fine-Tuning-CodeT5 $ python -m venv .\venv\
~/Fine-Tuning-CodeT5 $ .\venv\bin\Activate.ps1
(venv) ~/Fine-Tuning-CodeT5 $
```

To deactivate the virtual environment, use the command:
```shell
(venv) $ deactivate
```

## **2.2 Install Packages**

Install the required dependencies:
```shell
(venv) ~/Fine-Tuning-CodeT5 $ pip install -r requirements.txt
```
## **2.3 Run the fine-tuning model**

(1) Run Fine-Tuning Demo

This script fine-tunes a pre-trained CodeT5 model specifically for the task of predicting if
conditions. The model takes as input a function containing a special token masking a single if condition
and attempts to predict it. It masks the if conditions in a prepared dataset.
After masking, it tokenizes the input using a pre-trained tokenizer before feeding it into the
model.

Navigate to the ```src``` directory, then run:
```shell
(venv) ~/Fine-Tuning-CodeT5/src $ python fine-tuning.py
```

## 3. Report

The assignment report is available inside the ``reports`` folder named ``Assignment_Report.pdf``.



