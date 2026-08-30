#### Changing embedding from 128 to 256

# try to get best traing with epoch 1 to 10 with embedding 256 and save best epoch in best_model.pt file and load it in predict_sentiment function and show the results

## Model config (fill in once you choose values)

config = {
    "vocabulary_size": tokenizer.vocab_size,  # e.g., ~30522 for bert-base-uncased
    "num_classes": 2,                         # binary classification (pos/neg)
    "d_embed": 256,
    "context_size": MAX_LENGTH,
    "layers_num": 4,
    "heads_num": 8,
    "head_size": 32,  # 8 heads * 32 = 128 -> matches d_embed
    "dropout_rate": 0.1,
    "use_bias": True
}

result
training time: 33m 23.1s
testing and loading time: 1m 32.6s
Test Accuracy (best epoch 5): 76.52%
Text: This movie was absolutely fantastic, the acting was superb and I loved every minute.
clearly positive review
Prediction: Positive (90.67%)

Text: Terrible film. Boring plot, wooden acting, complete waste of two hours.
clearly negative review
Prediction: Negative (100.00%)

Text: The visuals were stunning but the story felt shallow and predictable.
mixed/ambiguous review
Prediction: Positive (99.61%)


```
New best model saved (epoch 1, acc 69.24%)
Epoch [2/10], Step [100/704], Loss: 0.5511
Epoch [2/10], Step [200/704], Loss: 0.5283
Epoch [2/10], Step [300/704], Loss: 0.5248
Epoch [2/10], Step [400/704], Loss: 0.5365
Epoch [2/10], Step [500/704], Loss: 0.5127
Epoch [2/10], Step [600/704], Loss: 0.5139
Epoch [2/10], Step [700/704], Loss: 0.5024
Epoch 2 - Validation Accuracy: 75.24%
New best model saved (epoch 2, acc 75.24%)
Epoch [3/10], Step [100/704], Loss: 0.4621
Epoch [3/10], Step [200/704], Loss: 0.4731
Epoch [3/10], Step [300/704], Loss: 0.4718
Epoch [3/10], Step [400/704], Loss: 0.4696
Epoch [3/10], Step [500/704], Loss: 0.4527
Epoch [3/10], Step [600/704], Loss: 0.4671
Epoch [3/10], Step [700/704], Loss: 0.4569
Epoch 3 - Validation Accuracy: 75.92%
New best model saved (epoch 3, acc 75.92%)
Epoch [4/10], Step [100/704], Loss: 0.4252
Epoch [4/10], Step [200/704], Loss: 0.4050
Epoch [4/10], Step [300/704], Loss: 0.4267
Epoch [4/10], Step [400/704], Loss: 0.4190
Epoch [4/10], Step [500/704], Loss: 0.4343
Epoch [4/10], Step [600/704], Loss: 0.4177
Epoch [4/10], Step [700/704], Loss: 0.4075
Epoch 4 - Validation Accuracy: 77.00%
New best model saved (epoch 4, acc 77.00%)
Epoch [5/10], Step [100/704], Loss: 0.3688
Epoch [5/10], Step [200/704], Loss: 0.3684
Epoch [5/10], Step [300/704], Loss: 0.3850
Epoch [5/10], Step [400/704], Loss: 0.3719
Epoch [5/10], Step [500/704], Loss: 0.3994
Epoch [5/10], Step [600/704], Loss: 0.3964
Epoch [5/10], Step [700/704], Loss: 0.3592
Epoch 5 - Validation Accuracy: 78.00%
New best model saved (epoch 5, acc 78.00%)
Epoch [6/10], Step [100/704], Loss: 0.3129
Epoch [6/10], Step [200/704], Loss: 0.3225
Epoch [6/10], Step [300/704], Loss: 0.3145
Epoch [6/10], Step [400/704], Loss: 0.3417
Epoch [6/10], Step [500/704], Loss: 0.3381
Epoch [6/10], Step [600/704], Loss: 0.3408
Epoch [6/10], Step [700/704], Loss: 0.3358
Epoch 6 - Validation Accuracy: 77.12%
Epoch [7/10], Step [100/704], Loss: 0.2757
Epoch [7/10], Step [200/704], Loss: 0.2574
Epoch [7/10], Step [300/704], Loss: 0.2784
Epoch [7/10], Step [400/704], Loss: 0.2813
Epoch [7/10], Step [500/704], Loss: 0.2925
Epoch [7/10], Step [600/704], Loss: 0.2913
Epoch [7/10], Step [700/704], Loss: 0.2942
Epoch 7 - Validation Accuracy: 78.04%
New best model saved (epoch 7, acc 78.04%)
Epoch [8/10], Step [100/704], Loss: 0.2322
Epoch [8/10], Step [200/704], Loss: 0.2192
Epoch [8/10], Step [300/704], Loss: 0.2139
Epoch [8/10], Step [400/704], Loss: 0.2434
Epoch [8/10], Step [500/704], Loss: 0.2356
Epoch [8/10], Step [600/704], Loss: 0.2612
Epoch [8/10], Step [700/704], Loss: 0.2297
Epoch 8 - Validation Accuracy: 77.32%
Epoch [9/10], Step [100/704], Loss: 0.1772
Epoch [9/10], Step [200/704], Loss: 0.1793
Epoch [9/10], Step [300/704], Loss: 0.1781
Epoch [9/10], Step [400/704], Loss: 0.1690
Epoch [9/10], Step [500/704], Loss: 0.1727
Epoch [9/10], Step [600/704], Loss: 0.2059
Epoch [9/10], Step [700/704], Loss: 0.1991
Epoch 9 - Validation Accuracy: 77.32%
Epoch [10/10], Step [100/704], Loss: 0.1138
Epoch [10/10], Step [200/704], Loss: 0.1315
Epoch [10/10], Step [300/704], Loss: 0.1426
Epoch [10/10], Step [400/704], Loss: 0.1372
Epoch [10/10], Step [500/704], Loss: 0.1588
Epoch [10/10], Step [600/704], Loss: 0.1640
Epoch [10/10], Step [700/704], Loss: 0.1360
Epoch 10 - Validation Accuracy: 76.36%

Best epoch: 7 with validation accuracy 78.04%
```