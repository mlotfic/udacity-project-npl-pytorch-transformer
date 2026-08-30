# Changing number of layer to 6 with embedding 256  

## Model config (fill in once you choose values)

config = {
    "vocabulary_size": tokenizer.vocab_size,  # e.g., ~30522 for bert-base-uncased
    "num_classes": 2,                         # binary classification (pos/neg)
    "d_embed": 256,
    "context_size": MAX_LENGTH,
    "layers_num": 6,
    "heads_num": 8,
    "head_size": 32,  # 4 heads * 32 = 128 -> matches d_embed
    "dropout_rate": 0.1,
    "use_bias": True
}

## result

training time: 43m 47.2s
teesting and loading time: 1m 46.4s
Test Accuracy (best epoch 5): 77.60%

Text: This movie was absolutely fantastic, the acting was superb and I loved every minute.
clearly positive review
Prediction: Positive (99.23%)

Text: Terrible film. Boring plot, wooden acting, complete waste of two hours.
clearly negative review
Prediction: Negative (99.98%)

Text: The visuals were stunning but the story felt shallow and predictable.
mixed/ambiguous review
Prediction: Positive (96.84%)

```
Epoch [1/10], Step [100/704], Loss: 0.6944
Epoch [1/10], Step [200/704], Loss: 0.6655
Epoch [1/10], Step [300/704], Loss: 0.6364
Epoch [1/10], Step [400/704], Loss: 0.6385
Epoch [1/10], Step [500/704], Loss: 0.6151
Epoch [1/10], Step [600/704], Loss: 0.6025
Epoch [1/10], Step [700/704], Loss: 0.5822
Epoch 1 - Validation Accuracy: 69.88%
New best model saved (epoch 1, acc 69.88%)
Epoch [2/10], Step [100/704], Loss: 0.5506
Epoch [2/10], Step [200/704], Loss: 0.5502
Epoch [2/10], Step [300/704], Loss: 0.5184
Epoch [2/10], Step [400/704], Loss: 0.5249
Epoch [2/10], Step [500/704], Loss: 0.5160
Epoch [2/10], Step [600/704], Loss: 0.5136
Epoch [2/10], Step [700/704], Loss: 0.5025
Epoch 2 - Validation Accuracy: 74.08%
New best model saved (epoch 2, acc 74.08%)
Epoch [3/10], Step [100/704], Loss: 0.4882
Epoch [3/10], Step [200/704], Loss: 0.4681
Epoch [3/10], Step [300/704], Loss: 0.4557
Epoch [3/10], Step [400/704], Loss: 0.4686
Epoch [3/10], Step [500/704], Loss: 0.4615
Epoch [3/10], Step [600/704], Loss: 0.4753
Epoch [3/10], Step [700/704], Loss: 0.4396
Epoch 3 - Validation Accuracy: 74.60%
New best model saved (epoch 3, acc 74.60%)
Epoch [4/10], Step [100/704], Loss: 0.4124
Epoch [4/10], Step [200/704], Loss: 0.4188
Epoch [4/10], Step [300/704], Loss: 0.4174
Epoch [4/10], Step [400/704], Loss: 0.4055
Epoch [4/10], Step [500/704], Loss: 0.4093
Epoch [4/10], Step [600/704], Loss: 0.4043
Epoch [4/10], Step [700/704], Loss: 0.4138
Epoch 4 - Validation Accuracy: 78.08%
New best model saved (epoch 4, acc 78.08%)
Epoch [5/10], Step [100/704], Loss: 0.3672
Epoch [5/10], Step [200/704], Loss: 0.3772
Epoch [5/10], Step [300/704], Loss: 0.3733
Epoch [5/10], Step [400/704], Loss: 0.3782
Epoch [5/10], Step [500/704], Loss: 0.3799
Epoch [5/10], Step [600/704], Loss: 0.3608
Epoch [5/10], Step [700/704], Loss: 0.3695
Epoch 5 - Validation Accuracy: 78.72%
New best model saved (epoch 5, acc 78.72%)
Epoch [6/10], Step [100/704], Loss: 0.3224
Epoch [6/10], Step [200/704], Loss: 0.3303
Epoch [6/10], Step [300/704], Loss: 0.3325
Epoch [6/10], Step [400/704], Loss: 0.3155
Epoch [6/10], Step [500/704], Loss: 0.3303
Epoch [6/10], Step [600/704], Loss: 0.3435
Epoch [6/10], Step [700/704], Loss: 0.3247
Epoch 6 - Validation Accuracy: 77.64%
Epoch [7/10], Step [100/704], Loss: 0.2757
Epoch [7/10], Step [200/704], Loss: 0.2733
Epoch [7/10], Step [300/704], Loss: 0.2926
Epoch [7/10], Step [400/704], Loss: 0.2825
Epoch [7/10], Step [500/704], Loss: 0.2864
Epoch [7/10], Step [600/704], Loss: 0.2871
Epoch [7/10], Step [700/704], Loss: 0.2956
Epoch 7 - Validation Accuracy: 78.32%
Epoch [8/10], Step [100/704], Loss: 0.2194
Epoch [8/10], Step [200/704], Loss: 0.2271
Epoch [8/10], Step [300/704], Loss: 0.2280
Epoch [8/10], Step [400/704], Loss: 0.2462
Epoch [8/10], Step [500/704], Loss: 0.2426
Epoch [8/10], Step [600/704], Loss: 0.2553
Epoch [8/10], Step [700/704], Loss: 0.2505
Epoch 8 - Validation Accuracy: 77.48%
Epoch [9/10], Step [100/704], Loss: 0.1906
Epoch [9/10], Step [200/704], Loss: 0.1743
Epoch [9/10], Step [300/704], Loss: 0.1861
Epoch [9/10], Step [400/704], Loss: 0.1886
Epoch [9/10], Step [500/704], Loss: 0.1967
Epoch [9/10], Step [600/704], Loss: 0.2121
Epoch [9/10], Step [700/704], Loss: 0.2125
Epoch 9 - Validation Accuracy: 77.84%
Epoch [10/10], Step [100/704], Loss: 0.1330
Epoch [10/10], Step [200/704], Loss: 0.1288
Epoch [10/10], Step [300/704], Loss: 0.1840
Epoch [10/10], Step [400/704], Loss: 0.1449
Epoch [10/10], Step [500/704], Loss: 0.1663
Epoch [10/10], Step [600/704], Loss: 0.1594
Epoch [10/10], Step [700/704], Loss: 0.1620
Epoch 10 - Validation Accuracy: 78.16%

Best epoch: 5 with validation accuracy 78.72%
```
