# Bio-medical-AI

## Therapeutics Data Commons

<img width="400" alt="image" src="https://user-images.githubusercontent.com/76294398/209525108-302b2057-e5e1-48ee-becb-685e2a821dc2.png">

별도의 Data curation 없이 API 형태로 데이터 이용 가능

<img width="600" alt="image" src="https://user-images.githubusercontent.com/76294398/209525424-6dce9051-672d-4610-81b0-7fd7b4f826bb.png">

**Web:** https://tdcommons.ai/

**Paper:** https://arxiv.org/abs/2102.09548

---

## Inductive Bias

**Inductive Bias**란 학습 시에는 만나보지 않았던 상황에 대하여 정확한 예측을 하기 위해 사용하는 **추가적인 가정**을 의미한다.

데이터의 특성에 맞게 적절한 Inductive Bias를 가지는 모델을 사용해야 높은 성능을 기록할 수 있고 CNN의 경우 Locality(근접 픽셀끼리 종속성), Transitional Invariance(사물 위치가 바뀌어도 동일 사물 인식)등의 특성을 가지기 때문에 이미지 데이터에 적합한 모델이 되는 것이다.

**References**

- https://re-code-cord.tistory.com/entry/Inductive-Bias%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C

- https://arxiv.org/abs/1806.01261

---

## Model Explainability

**Explainability 분석:** 만든 예측 모델이 신뢰성이 있는지 검증이 필요 (Model의 Generalization 성능 테스트)

- 결론에 대한 도메인 전문가의 이유와 모델의 이유가 비슷할수록 신뢰성이 있는 모델
- 원인 분석을 통해 특정 Biomarker를 찾기도 함

<img width="500" alt="image" src="https://user-images.githubusercontent.com/76294398/209546926-e92f0bf1-4990-4ea2-b646-3a7b7ebe09f3.png">

**대표적인 방법론:**

- **SHAP Value:** Classical ML에서 원인분석에 많이 사용되던 기법. 게임 이론에서 게임의 참여자 간 협조로 얻어진 모든 이득으로부터 참여자들의 기여분에 따라 배분되는 값을 의미하며, ML에서는 어떤 특성의 조건부 조건에서 해당 특성이 모델 예측치의 변화를 가져오는 정도를 가리킨다.

---
