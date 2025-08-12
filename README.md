# umc005-en-ur-transformer-translation
English→Urdu machine translation using UMC005 parallel corpus — custom Transformer and LSTM baselines, evaluation (BLEU/ROUGE)

```markdown
# English → Urdu Translation using LSTM Seq2Seq with Attention

##  Overview
This project implements a neural machine translation (NMT) model to translate sentences from **English** to **Urdu**.  
It uses parallel corpora from the **Quran** and **Bible** for training and evaluation.  
The model is built using **PyTorch** and follows a **Sequence-to-Sequence (Seq2Seq)** architecture with **LSTM encoders/decoders** and **Bahdanau attention**.

---

##  Features
- **Custom dataset loader** for Quran and Bible corpora.
- **Text preprocessing & tokenization** for both English and Urdu.
- **Vocabulary building** with padding & special tokens.
- **LSTM Encoder-Decoder with Attention** for better context handling.
- **BLEU & ROUGE evaluation metrics**.
- **Model checkpointing** to save the best-performing model.

---

##  Project Structure
```

project/
│── data/
│   ├── umc005-corpus/quran.txt
│   ├── umc005-corpus/bible.txt
│── best\_model.pt        # Saved best model
│── code.ipynb           # Jupyter Notebook with full implementation
│── README.md            # Project documentation

````

---

## ⚙ Installation
1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
````

2. Install dependencies:

   ```bash
   pip install torch torchvision nltk numpy matplotlib
   ```

3. Download or place your Quran and Bible parallel corpora in the `data/` folder.

---

## ▶ Usage

Run the notebook in Jupyter:

```bash
jupyter notebook code.ipynb
```

Or convert to `.py` and run:

```bash
jupyter nbconvert --to script code.ipynb
python code.py
```

---

##  Evaluation

The model is evaluated using:

* **BLEU score** – for n-gram overlap.
* **ROUGE score** – for recall-based matching.

---

##  Example Output

```
Input:   "In the beginning God created the heavens and the earth."
Target:  "شروع میں خدا نے آسمان اور زمین کو پیدا کیا۔"
Predicted: "شروع میں اللہ نے آسمان اور زمین پیدا کی۔"
```

---

##  Future Improvements

* Experiment with **Transformer architecture** for better long-range dependencies.
* Add **beam search decoding** for improved translation quality.
* Integrate a **web-based demo** for real-time translation.

---

