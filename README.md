# Deep Learning Colab Walkthroughs

Four tutorial notebooks written for CMPE 258 (Deep Learning, SJSU, Spring 2026), each with a
recorded video walkthrough. They are committed as the `.py` files Colab produces via
**File → Download → Download .py**, so the prose lives in string literals and the outputs (plots,
training logs) are *not* included — you have to run them to see results.

Everything is PyTorch. The datasets are small and generated or downloaded inside the scripts.

## What's here

| # | File | What it does | Video |
|---|---|---|---|
| 1 | `01_gnn_fundamentals/final_gnn_fundamentals_tutorial.py` | Graph representations, the message-passing idea, and a graph convolution layer written twice — once in NumPy, once in PyTorch — then a 2-layer GCN trained on toy graphs and on Zachary's Karate Club network. | [link](https://youtu.be/7WpgMJvHVts) |
| 2 | `02_nlp_10_years/final_nlp_deep_learning_10_years_tutorial.py` | A tour from tokenization to ChatGPT: a hand-written tokenizer, embedding geometry and analogies, a NumPy RNN, LSTM/GRU gating, attention, a miniature Transformer, and a discussion of pretraining, instruction tuning and RLHF. | [link](https://youtu.be/Jrup2jDrFuo) |
| 3 | `03_rnn_lstm_gru_wavenet/final_rnn_lstm_gru_wavenet_zero_to_hero.py` | Five sequence models — RNN, LSTM, GRU, deep LSTM and a dilated-causal-convolution WaveNet — built from scratch and trained on the same inline character-level corpus, then compared on loss, parameter count and training time. | [link](https://youtu.be/aEEFHZlwRgk) |
| 4 | `04_vision_transformers/final_vision_transformers_tutorial.py` | Scaled dot-product and multi-head attention, patch embedding and a full ViT built from scratch, followed by a survey of CLIP, DINOv2 and SAM. | [link](https://youtu.be/j3Ce86Ld1ZQ) |

A few notes on what is and isn't executed, since the scripts are longer than the code that actually
runs:

- Notebook 1 trains on synthetic graphs and the Karate Club graph from `networkx`. GraphSAGE, GAT
  and GIN are named only as topics for a follow-up part, which is not in this repo.
- The embeddings in notebook 2 are constructed by hand to make the vector-arithmetic plots readable;
  nothing is trained on a real corpus there. The RNN and Transformer sections do run.
- In notebook 4, the ViT is built and run from scratch and DINOv2 is pulled from `torch.hub`. The
  CLIP section is wrapped in a `try/except ImportError` and demonstrates the API on a random tensor
  rather than a real image; SAM is shown as a printed code sample only, not executed.

## Running it

Each file is a Colab export, so the simplest path is to open a new Colab notebook and paste the file
in, or upload the `.py` and run it. Locally:

```bash
pip install torch torchvision numpy matplotlib seaborn networkx scikit-learn
python 03_rnn_lstm_gru_wavenet/final_rnn_lstm_gru_wavenet_zero_to_hero.py
```

Notebook 1 also wants `networkx`; notebook 4 pulls model weights over the network. A GPU makes
notebooks 2, 3 and 4 much faster. The original Colab URLs are in the docstring at the top of each
file.

## Attribution

The sequence-models notebook (3) follows the structure of the RNN chapters in Aurélien Géron's
*Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (O'Reilly), reworked in
PyTorch. Notebook 4 uses DINOv2 (`facebookresearch/dinov2`) via `torch.hub` and references OpenAI's
CLIP and Meta's Segment Anything.

## License

MIT. See [`LICENSE`](LICENSE).
