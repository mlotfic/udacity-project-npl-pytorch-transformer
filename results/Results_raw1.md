
# try to get best traing with epoch 1 to 10 and save best epoch in best_model.pt file and load it in predict_sentiment function and show the results

## Model config (fill in once you choose values)

config = {
    "vocabulary_size": tokenizer.vocab_size,  # e.g., ~30522 for bert-base-uncased
    "num_classes": 2,                         # binary classification (pos/neg)
    "d_embed": 128,
    "context_size": MAX_LENGTH,
    "layers_num": 4,
    "heads_num": 4,
    "head_size": 32,  # 4 heads * 32 = 128 -> matches d_embed
    "dropout_rate": 0.1,
    "use_bias": True
}

### result 
training time: 23m 56.5s
testing and loading time: 1m 26s
Test Accuracy (best epoch 5): 77.18%

Text: This movie was absolutely fantastic, the acting was superb and I loved every minute.
clearly positive review
Prediction: Positive (99.95%)

Text: Terrible film. Boring plot, wooden acting, complete waste of two hours.
clearly negative review
Prediction: Negative (99.57%)

Text: The visuals were stunning but the story felt shallow and predictable.
mixed/ambiguous review
Prediction: Negative (98.06%)

```
Epoch [1/10], Step [400/704], Loss: 0.6215
Epoch [1/10], Step [500/704], Loss: 0.5969
Epoch [1/10], Step [600/704], Loss: 0.5706
Epoch [1/10], Step [700/704], Loss: 0.5629
Epoch 1 - Validation Accuracy: 71.00%
New best model saved (epoch 1, acc 71.00%)
Epoch [2/10], Step [100/704], Loss: 0.5011
Epoch [2/10], Step [200/704], Loss: 0.5338
Epoch [2/10], Step [300/704], Loss: 0.4987
Epoch [2/10], Step [400/704], Loss: 0.4973
Epoch [2/10], Step [500/704], Loss: 0.4950
Epoch [2/10], Step [600/704], Loss: 0.5018
Epoch [2/10], Step [700/704], Loss: 0.4874
Epoch 2 - Validation Accuracy: 76.56%
New best model saved (epoch 2, acc 76.56%)
Epoch [3/10], Step [100/704], Loss: 0.4485
Epoch [3/10], Step [200/704], Loss: 0.4203
Epoch [3/10], Step [300/704], Loss: 0.4303
Epoch [3/10], Step [400/704], Loss: 0.4285
Epoch [3/10], Step [500/704], Loss: 0.4403
Epoch [3/10], Step [600/704], Loss: 0.4238
Epoch [3/10], Step [700/704], Loss: 0.4327
Epoch 3 - Validation Accuracy: 77.88%
New best model saved (epoch 3, acc 77.88%)
Epoch [4/10], Step [100/704], Loss: 0.3723
Epoch [4/10], Step [200/704], Loss: 0.3754
Epoch [4/10], Step [300/704], Loss: 0.3789
Epoch [4/10], Step [400/704], Loss: 0.3806
Epoch [4/10], Step [500/704], Loss: 0.4009
Epoch [4/10], Step [600/704], Loss: 0.3689
Epoch [4/10], Step [700/704], Loss: 0.3679
Epoch 4 - Validation Accuracy: 79.56%
New best model saved (epoch 4, acc 79.56%)
Epoch [5/10], Step [100/704], Loss: 0.3294
Epoch [5/10], Step [200/704], Loss: 0.3177
Epoch [5/10], Step [300/704], Loss: 0.3381
Epoch [5/10], Step [400/704], Loss: 0.3288
Epoch [5/10], Step [500/704], Loss: 0.3244
Epoch [5/10], Step [600/704], Loss: 0.3373
Epoch [5/10], Step [700/704], Loss: 0.3260
Epoch 5 - Validation Accuracy: 79.68%
New best model saved (epoch 5, acc 79.68%)
Epoch [6/10], Step [100/704], Loss: 0.2679
Epoch [6/10], Step [200/704], Loss: 0.2880
Epoch [6/10], Step [300/704], Loss: 0.2909
Epoch [6/10], Step [400/704], Loss: 0.2886
Epoch [6/10], Step [500/704], Loss: 0.2926
Epoch [6/10], Step [600/704], Loss: 0.2859
Epoch [6/10], Step [700/704], Loss: 0.2696
Epoch 6 - Validation Accuracy: 79.24%
Epoch [7/10], Step [100/704], Loss: 0.2251
Epoch [7/10], Step [200/704], Loss: 0.2325
Epoch [7/10], Step [300/704], Loss: 0.2414
Epoch [7/10], Step [400/704], Loss: 0.2398
Epoch [7/10], Step [500/704], Loss: 0.2562
Epoch [7/10], Step [600/704], Loss: 0.2635
Epoch [7/10], Step [700/704], Loss: 0.2444
Epoch 7 - Validation Accuracy: 80.24%
New best model saved (epoch 7, acc 80.24%)
Epoch [8/10], Step [100/704], Loss: 0.1801
Epoch [8/10], Step [200/704], Loss: 0.1930
Epoch [8/10], Step [300/704], Loss: 0.2010
Epoch [8/10], Step [400/704], Loss: 0.1931
Epoch [8/10], Step [500/704], Loss: 0.2179
Epoch [8/10], Step [600/704], Loss: 0.2090
Epoch [8/10], Step [700/704], Loss: 0.2054
Epoch 8 - Validation Accuracy: 80.12%
Epoch [9/10], Step [100/704], Loss: 0.1690
Epoch [9/10], Step [200/704], Loss: 0.1622
Epoch [9/10], Step [300/704], Loss: 0.1630
Epoch [9/10], Step [400/704], Loss: 0.1540
Epoch [9/10], Step [500/704], Loss: 0.1630
Epoch [9/10], Step [600/704], Loss: 0.1860
Epoch [9/10], Step [700/704], Loss: 0.1638
Epoch 9 - Validation Accuracy: 79.64%
Epoch [10/10], Step [100/704], Loss: 0.1186
Epoch [10/10], Step [200/704], Loss: 0.1200
Epoch [10/10], Step [300/704], Loss: 0.1242
Epoch [10/10], Step [400/704], Loss: 0.1367
Epoch [10/10], Step [500/704], Loss: 0.1269
Epoch [10/10], Step [600/704], Loss: 0.1291
Epoch [10/10], Step [700/704], Loss: 0.1319
Epoch 10 - Validation Accuracy: 79.16%

Best epoch: 7 with validation accuracy 80.24%
```