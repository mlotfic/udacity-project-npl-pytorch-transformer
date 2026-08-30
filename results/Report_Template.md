# conclusion

## 1. Project Summary

In this project, a transformer-based model (`DemoGPT`) was built from scratch and trained to classify IMDB movie reviews as positive or negative:

- The raw IMDB dataset (25,000 training reviews, 25,000 test reviews) was loaded, explored, and split into training (22,500), validation (2,500), and test (25,000) sets.
- Reviews were tokenized with the `bert-base-uncased` subword tokenizer, truncated/padded to a fixed length of 128 tokens.
- A `DemoGPT` transformer was implemented with token + positional embeddings, 4 stacked transformer blocks (each with 4-head causal self-attention and a feed-forward layer), followed by mean pooling over the sequence dimension and a linear classification head mapping to 2 output classes.
- The model was trained for 10 epochs with the AdamW optimizer and cross-entropy loss, with validation accuracy tracked after each epoch.
- Final performance was evaluated on the held-out test set using `calculate_accuracy()`, with the goal of exceeding 75% accuracy.
- We run three experiments.
1. Baseline experiment with 4 layers, 128 embedding dimension, 4 heads, 10 epochs
2. Change embedding dimension to 256, 4 layers, 8 heads, 10 epochs
3. Change embedding dimension to 256, 4 layers, 4 heads, 10 epochs

---

## 2. Experimental

### 1. Baseline

Baseline experiment with 4 layers, 128 embedding dimension, 4 heads, 10 epochs

#### Configuration

- Tokenizer: bert-base-uncased (subword tokenization)
- Max sequence length: 128
- Embedding dimension (d_embed): 128
- Number of transformer layers: 4
- Number of attention heads: 4
- Batch size: 32
- Optimizer: AdamW
- Learning rate = 3e-4
- Epochs trained: 10
- Train / Validation / Test split: 22,500 / 2,500 / 25,000 reviews

#### Results Summary

Project results have been summarized below, based on the training run logged in the notebook.

##### Overall Performance

| Metric | Value |
|---|---|
| Best epoch | [ 7 ] |
| Best validation accuracy | 80.24% |
| Final test accuracy (best checkpoint) | 78.16% |
| Total training time | 23m 56.5s |
| Testing and loading time | 2m 16.2s |
| Hardware used | GPU:RTX 1660ti with 6GB memory |

##### Per-Epoch Metrics

| Epoch | Train Loss (avg) | Val Accuracy | Best So Far? | Notes |
|---|---|---|---|---|
| 1 | [ fill in ] | [ fill in ] | [ Y/N ] | [ e.g. baseline ] |
| 2 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 3 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 4 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 5 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 6 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 7 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 8 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 9 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |
| 10 | [ fill in ] | [ fill in ] | [ Y/N ] | [ ] |

#### Training / Validation Curve

![training curve](results/1.png)

##### Qualitative Examples

Sample predictions from the `predict_sentiment()` inference examples (positive, negative, and mixed/ambiguous reviews):

- Positive example — predicted: [ fill in ], confidence: [ fill in ]%
- Negative example — predicted: [ fill in ], confidence: [ fill in ]%
- Mixed/ambiguous example — predicted: [ fill in ], confidence: [ fill in ]%

---

### 2. Change model capacity: increase embedding dimension from 128 to 256 and number of heads from 4 to 8 

....

---

### 3. Change model capacity: Increase embedding dimension from 128 to 256 and number of heads from 8 to 4

...

---

---

## 4. Key Takeaways

At least two key takeaways from this project:

- [ Takeaway 1 — e.g. how model capacity, epochs, or learning rate affected accuracy ]
- [ Takeaway 2 — e.g. what the best-epoch checkpointing revealed about overfitting ]
- [ Takeaway 3 (optional) — e.g. limitations observed, or what the qualitative examples showed ]

## 5. Conclusion

*[ Write a 2-4 sentence closing summary once results are filled in above. ]*
