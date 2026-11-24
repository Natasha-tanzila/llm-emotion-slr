<h1 align="center">📏 How long is an emotion?</h1>

<p align="center">
  <em>Tiny scripts that count the words behind every emotion dataset in the review.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white" alt="Python 3.9+">
  <img src="https://img.shields.io/badge/Run%20on-Google%20Colab-F9AB00?logo=googlecolab&logoColor=white" alt="Google Colab">
  <img src="https://img.shields.io/badge/Data-Hugging%20Face-FFD21E?logo=huggingface&logoColor=black" alt="Hugging Face datasets">
  <img src="https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white" alt="pandas">
</p>

<p align="center">
  <img src="scripts/demo.gif" alt="Running a length script in the terminal" width="680">
</p>

<img src="scripts/demo.gif" alt="Running a length script in the terminal" width="680">

## 💡 Why this exists

Is *"I'm fine."* the same emotion problem as a 300-word Reddit post? Probably not. Models can behave very differently on short and long text, so the review groups benchmark datasets by how long their samples are (Table 2 and Table 3).

These scripts are where those numbers come from: each one opens a dataset, counts the words in every sample and prints the average. No magic, no hidden cleaning, just counting. 🧮

## 🔍 How the length is measured

| | |
|---|---|
| **Sample** | One text entry: a sentence, a post, an utterance or a dialogue turn, depending on the dataset |
| **Words** | Text split on whitespace (`text.split()`); one script uses `\b\w+\b`, which ignores stand-alone punctuation |
| **Average** | Total words ÷ number of samples |
| **Skipped** | Empty or missing entries |
| **Splits** | Train, validation and test are combined unless a script says otherwise |

The text is not cleaned, lower-cased or tokenised beyond this, so the values describe the raw text as it is distributed.

## ⚙️ Setup

```bash
pip install datasets pandas
```

That's it. The scripts were written in Google Colab, so file paths start with `/content/`.

## ▶️ How to run

**🤗 Datasets on the Hugging Face Hub**: these download the data themselves.

```bash
python length_1.py
```

In the notebook, just run the cells one by one. Each cell prints the number of samples and the average length.

**📁 Datasets from a local file (CSV or JSON)**

1. Download the dataset from the link in Table 2 of the review.
2. Put the file next to the script (or upload it to Colab).
3. Edit two lines at the top of the script:
   - `file_path`: where your copy of the file is
   - the column or field that holds the text, e.g. `'Text'` or `'text'`
4. Run it. 🎉

> **Tip:** not sure what the text column is called? The CSV script prints all column names before it counts anything.

## 📤 What you get

One number, rounded to two decimals:

```
Average words per entry: 14.62
```

Dialogue datasets that keep each turn in its own column print an average for each turn and for all turns together.

## 🔁 Reproducing the review

The values in Table 2 were produced with these scripts on the publicly released versions of the datasets. If a dataset is re-released with samples added or removed, expect small differences. Values in Table 2 that these scripts don't compute come from the dataset's original paper or official source.

---

<p align="center">
  Made with ☕ and a lot of <code>len(text.split())</code> by <b>N.T. Monalisa</b>
</p>
