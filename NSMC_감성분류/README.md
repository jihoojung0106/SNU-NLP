# 파일 설명

이 저장소는 4가지 모델을 비교하기 위한 파일들을 포함합니다. 각 모델에 대한 IPython 노트북 파일과 학습된 모델의 weights, 그리고 학습된 word embedding 파일을 함께 첨부했습니다. 필수 제출 파일인 IPython 노트북과 학습된 임베딩 파일을 제외한 나머지 파일들은 '기타 파일들' 폴더에 저장했습니다.

## 모델과 파일명

### Lstm with pretrained embedding
- IPython 노트북: `lstm_with_embedding.ipynb`
- 모델 weights: `lstm_with_w2v.pt`

### Lstm without pretrained embedding
- IPython 노트북: `lstm.ipynb`
- 모델 weights: `lstm_wo_w2v.pt`

### Cnn with pretrained embedding
- IPython 노트북: `cnn_with_embedding.ipynb` (동일한 파일)
- 모델 weights: `cnn_with_w2v.pt`

### Cnn without pretrained embedding
- IPython 노트북: `cnn.ipynb`
- 모델 weights: `cnn_wo_w2v.pt`

### 학습된 임베딩 파일
`w2v.model`


# 개괄

이 저장소에는 총 4가지 모델이 포함되어 있습니다. 이번 실험의 목표는 RNN과 CNN의 결과를 비교하는 것이었습니다.

전반적인 모델 및 학습, 평가 기능은 수업 자료를 참고했습니다. 각 모델은 공통적으로 10개의 epoch를 사용했으며, 아래 4가지 모델의 결과를 비교하고자 했습니다.
- Lstm with pretrained embedding
- Lstm without pretrained embedding
- Cnn with pretrained embedding
- Cnn without pretrained embedding

# Experiment Results

The models utilizing pre-trained embeddings in both LSTM and CNN showcased high accuracy, with the LSTM model outperforming the CNN model in accuracy. Surprisingly, when not using pre-trained embeddings, the expected significant drop in model accuracy was observed in the CNN model, but the difference between the two models (LSTM with and without pre-trained embeddings) was not as pronounced as anticipated.

## Lstm with pretrained embedding
- Epoch: 10 | Epoch Time: 1m 8s
- Train Loss: 0.382 | Train Acc: 82.05%
- Val. Loss: 0.373 |  Val. Acc: 83.21%
- Test Loss: 0.380 | Test Acc: 82.96%
- Inference: 9/10

## Lstm without pretrained embedding
- Epoch: 10 | Epoch Time: 2m 21s
- Train Loss: 0.267 | Train Acc: 88.99%
- Val. Loss: 0.345 |  Val. Acc: 86.62%
- Test Loss: 0.351 | Test Acc: 86.64%
- Inference: 8/10

## Cnn with pretrained embedding
- Epoch: 10 | Epoch Time: 2m 11s
- Train Loss: 0.407 | Train Acc: 81.55%
- Val. Loss: 0.427 |  Val. Acc: 80.91%
- Test Loss: 0.427 | Test Acc: 80.86%
- Inference: 9/10 

## Cnn without pretrained embedding
- Epoch: 10 | Epoch Time: 2m 5s
- Train Loss: 0.690 | Train Acc: 54.61%
- Val. Loss: 0.674 |  Val. Acc: 61.34%
- Test Loss: 0.674 | Test Acc: 61.50%
- Inference: 7/10
