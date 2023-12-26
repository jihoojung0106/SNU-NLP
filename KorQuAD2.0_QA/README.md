# 모델 실험 결과

이 프로젝트에서는 3가지 모델을 구현하여 실험했습니다. 각 모델의 F1 score는 아래와 같습니다. F1 score는 modified DrQA 모델에서 구했습니다.

## QANet 모델
- 파일: `QANet은.ipynb`
- 설명: 해당 파일에는 모든 모듈에 대한 설명이 상세하게 기록되어 있습니다.
- 사용된 모델: QANet은 "Combining Local Convolution with Global Self-Attention for Reading Comprehension" 논문의 모델로, https://github.com/kushalj001/pytorch-question-answering의 구현을 변형하여 사용했습니다.

## DrQA 모델
- 파일: `DrQA.ipynb`
- 설명: vocab, train data 등을 직접 구현하지 않고, 이전 파일에서 저장한 데이터셋과 vocab 등을 그대로 사용했습니다.
- 사용된 모델: "Reading Wikipedia to Answer Open-Domain Questions" 논문의 모델을 변형하여 사용했습니다. 구현은 https://github.com/kushalj001/pytorch-question-answering에서 가져왔습니다.

## modifiedDrQA 모델
- 파일: `modifiedDrQA.ipynb`
- 설명: vocab, train data 등을 직접 구현하지 않고, 이전 파일에서 저장한 코드를 그대로 사용했습니다.
- 사용된 모델: DrQA와 달리 bi-directional LSTM이 아닌 RNN을 사용한 모델입니다.

### 결과 분석
모델의 inference 성능은 전반적으로 좋지 않았습니다. 이는 데이터의 일부만 사용한 메모리 이슈와 Colab GPU 성능 문제로 인해 발생했습니다. 또한, tokenize 등의 이슈도 있었습니다.

### F1 Score
전체적으로 모델 성능이 좋지 않아 F1 score가 매우 낮았습니다. 그러나 중복도가 높은 그룹에서는 상대적으로 높은 F1 score를 보였습니다. 이는 예상한 결과와 일치함을 나타냅니다.
