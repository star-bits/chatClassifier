# chatClassifier

- 2022년의 데이터는 train set, 2023년 1월의 데이터는 test set으로 이용함 (각각 93만개, 5만개)
- 대화량 상위 62명의 데이터만 사용함 
- SentencePiece를 이용해 vocab size 10000으로 토큰화
- 정수변환 이후 최대 길이 25로 padding (99% 이상의 데이터가 길이 25 이하)
- Multi-Kernel 1D CNN으로 train (Epoch 6에서 early stopping)
- Validation accuracy 0.25, Test accuracy 0.29

## Inference 예시

```
존예디컵 여름 풀파티 하기 딱이긴 하겠네요
1/1 [==============================] - 0s 17ms/step
1) 爱德华/잠실르엘판매중/25: 54.91%
2) Jinyoung. woo: 7.72%
3) 정대만: 4.46%
4) 심언니: 4.13%
5) kich: 2.99%
```

```
다 없어졌.
1/1 [==============================] - 0s 16ms/step
1) 권인호: 38.04%
2) 랄프: 18.75%
3) 박찬홍/ 주생아/엉아들 잘부탁해~: 7.05%
4) Edward Jeong: 4.65%
5) 라테라테: 3.86%
```

```
ㅎㅎ
1/1 [==============================] - 0s 19ms/step
1) 김반포: 52.12%
2) Edward Jeong: 12.43%
3) 박찬홍/ 주생아/엉아들 잘부탁해~: 8.38%
4) 최재경: 6.09%
5) 리플 / 이정우: 3.36%
```
