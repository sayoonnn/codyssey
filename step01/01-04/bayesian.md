# 베이지안 확률 모델

- `베이지안 확률 모델`은 **사전확률(prior)**과 관측 데이터를 결합해 **사후확률(posterior)**을 추론하는 접근 방식
- 사전 지식이나 가정이 `확률 분포 형태`로 포함되며, 데이터가 관찰될 때마다 `분포가 갱신`되는 특징을 가진다.

## 핵심 개념

- **사전확률(Prior)**: 기존에 알고 있던 정보나 가정에서 비롯된 확률
- **우도(Likelihood)**: 관측 데이터가 주어졌을 때, 해당 데이터가 발생할 가능성
- **사후확률(Posterior)**: 관측 데이터와 사전확률을 결합해 갱신된 확률

## 베이지 정리

사후확률을 구하는 공식은 다음과 같다:

```
P(A|B) = (P(B|A) * P(A)) / P(B)
```

- `A|B`: `사후확률` -> `B(결과)`가 발생했다는 가정 하에 `A(원인)`가 발생하였을 확률
- `B|A`: `우도확률` -> `A(원인)`가 발생했다는 가정 하에 `B(결과)`가 발생할 확률
- `A`: `사전 확률` -> `A(원인)`가 발생할 확률

## 장점

- 불확실성을 확률 분포로 표현해 유연한 분석 가능
- 적은 표본에서도 사전 정보 활용 가능
- 점차 늘어나는 데이터에 따라 확률 분포가 갱신

## 간단 예시

1. 동전의 앞면이 나올 확률의 사전 분포를 Beta(1,1)로 설정
2. 동전을 여러 번 던져 관찰된 앞면 횟수를 기반으로 Beta 분포의 파라미터 업데이트
3. 업데이트된 분포를 통해 동전이 앞면이 나올 미래 확률을 추론

## 참고 자료

- [Bayesian Methods for Hackers](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers)
- [Wikipedia: Bayesian Probability](https://en.wikipedia.org/wiki/Bayesian_probability)
