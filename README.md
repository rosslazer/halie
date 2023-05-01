<div align="center">

<img src="./halie.png" width="350px"/>

**An Interactive Evaluation Framework for Human-Language Model Interaction**

</div>

## Overview

This repository contains the code for HALIE (Human-AI Language-based Interaction Evaluation), a new framework for evaluating human-LM interaction. It is designed to be flexible and extensible to support a variety of interactive tasks beyond the five tasks we considered in our paper: **social dialogue, question answering, crossword puzzles, text summarization, and metaphor generation**. All the code for the five tasks are included in this repository.

- Paper: [Evaluating Human-Language Model Interaction](https://arxiv.org/abs/2212.09746) (Mina Lee, Megha Srivastava, Amelia Hardy, John Thickstun, Esin Durmus, Ashwin Paranjape, Ines Gerard-Ursin, Xiang Lisa Li, Faisal Ladhak, Frieda Rong, Rose E. Wang, Minae Kwon, Joon Sung Park, Hancheng Cao, Tony Lee, Rishi Bommasani, Michael Bernstein, Percy Liang, 2022)

If you have any questions, please reach out to [Mina Lee](https://minalee.info/) at `minalee@stanford.edu`.

---

## Contents
- [Data](#Data)
- [Analysis](#Analysis)

---

## Data

**Standardized data.** If you simply want to take a look at our data or use it to perform your own analysis, you can find the standardized data for the five tasks in `./assets/std`. See [README](./assets/README.md) for the data format.

**Raw data.** On the other hand, if you want to standardize data from raw data we collected, you can follow the steps below to convert the raw data.

For instance, you can find the raw data for question answering in `./assets/raw/question`.

First, unzip the log files for the task you want to standardize:

```
unzip ./assets/raw/question/logs.zip
```

Run the following command to standardize the logs:

```
python3 ./src/run_question.py
```

The standardized data will be stored in `./assets/std/question`.

For the other four tasks, replace `question` with the name of the task you want to standardize in the path as well as command.

**Your data.** If you are interested in extending HALIE to support a new task, please create a PR or contact [Mina Lee](https://minalee.info/) at `minalee@stanford.edu`.

---

## Analysis

We provide Jupyter Notebook files for analyzing the data collected for HALIE. The files are stored in `./notebook`.