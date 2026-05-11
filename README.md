# Deep Learning Colab Walkthroughs

A curated portfolio of four end-to-end Colab tutorials covering the foundations of modern deep learning, each accompanied by a code-block-by-code-block video walkthrough on YouTube.

**Author**: Nitish Chowdary

---

## Index

| # | Topic | Colab source | Video walkthrough |
|---|---|---|---|
| 1 | **GNN Fundamentals** — Graphs, message passing, GCN from scratch on Cora | [`01_gnn_fundamentals/`](01_gnn_fundamentals/final_gnn_fundamentals_tutorial.py) | [youtu.be/7WpgMJvHVts](https://youtu.be/7WpgMJvHVts) |
| 2 | **10 Years of Deep Learning in NLP** — Tokenization → embeddings → RNNs → Transformers → ChatGPT | [`02_nlp_10_years/`](02_nlp_10_years/final_nlp_deep_learning_10_years_tutorial.py) | [youtu.be/Jrup2jDrFuo](https://youtu.be/Jrup2jDrFuo) |
| 3 | **RNN, LSTM, GRU, WaveNet — Zero to Hero on Sequence Modeling** — All four architectures built from scratch and compared on the same character-level task | [`03_rnn_lstm_gru_wavenet/`](03_rnn_lstm_gru_wavenet/final_rnn_lstm_gru_wavenet_zero_to_hero.py) | [youtu.be/aEEFHZlwRgk](https://youtu.be/aEEFHZlwRgk) |
| 4 | **Vision Transformers & The Frontier of Computer Vision** — Attention → ViT → CLIP → DINOv2 → SAM | [`04_vision_transformers/`](04_vision_transformers/final_vision_transformers_tutorial.py) | [youtu.be/j3Ce86Ld1ZQ](https://youtu.be/j3Ce86Ld1ZQ) |

---

## Repository layout

```
.
├── 01_gnn_fundamentals/
│   └── final_gnn_fundamentals_tutorial.py
├── 02_nlp_10_years/
│   └── final_nlp_deep_learning_10_years_tutorial.py
├── 03_rnn_lstm_gru_wavenet/
│   └── final_rnn_lstm_gru_wavenet_zero_to_hero.py
└── 04_vision_transformers/
    └── final_vision_transformers_tutorial.py
```

Each `.py` file is a self-contained Colab notebook exported in script form. To run, either:

- **Open directly in Colab** — upload the `.py` file or paste its contents into a new Colab notebook (the cell delimiters `# %%` are preserved).
- **Run locally** — `python <file>.py` after installing the dependencies imported at the top of each script (PyTorch, torchvision, matplotlib, etc.). A GPU is strongly recommended for notebooks 2, 3, and 4.

---

## Notebook summaries

### 1. GNN Fundamentals
Builds graph neural networks from first principles. Covers graph representation, the message-passing paradigm, a hand-written graph convolution layer, and a full 2-layer GCN trained on the Cora citation network. Ends with a side-by-side comparison of GCN, GraphSAGE, and GAT.

### 2. 10 Years of Deep Learning in NLP
A guided tour from 2014-era word embeddings to 2024-era large language models. Implements character and subword tokenization, Word2Vec-style embeddings, a vanilla RNN, an LSTM, the attention mechanism, a miniature Transformer, and discusses pretraining, instruction tuning, and RLHF.

### 3. RNN, LSTM, GRU, WaveNet — Zero to Hero
Builds and trains five sequence models — vanilla RNN, LSTM, GRU, deep LSTM, and a dilated-causal-convolution WaveNet — on the *same* character-level corpus with identical hyper-parameters, then compares loss curves, parameter counts, and training time on one chart.

### 4. Vision Transformers & The Frontier of Computer Vision
Builds scaled dot-product attention, multi-head attention, patch embedding, and a complete Vision Transformer from scratch, then surveys the three foundation models defining computer vision in 2024 — **CLIP** (vision-language contrastive pretraining), **DINOv2** (self-supervised features), and **SAM** (promptable segmentation).

---

## License

MIT. See [`LICENSE`](LICENSE).
