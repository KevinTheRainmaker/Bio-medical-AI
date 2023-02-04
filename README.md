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

## Model Trustworthiness & Explainability

- Machine Learning 시스템을 개발할 때 성능만큼 중요한 것은 신뢰성
- 특히 의료 모델은 의학적, 생물학적 배경지식과 일정 수준 일치하는 원인 해석이 필요

**Explainability 분석:** 만든 예측 모델이 신뢰성이 있는지 검증이 필요 (Model의 Generalization 성능 테스트)

- 결론에 대한 도메인 전문가의 이유와 모델의 이유가 비슷할수록 신뢰성이 있는 모델
- Biological Knowledge를 모델에 주입하거나, 원인 분석을 통해 특정 Biomarker를 찾기도 함
- Machine Learning의 결과를 통계적으로 해석하여 Uncertainity 수치를 계산하여 모델의 신뢰성을 높이기도 함

<img width="500" alt="image" src="https://user-images.githubusercontent.com/76294398/209546926-e92f0bf1-4990-4ea2-b646-3a7b7ebe09f3.png">

**대표적인 방법론:**

- **SHAP Value:** Classical ML에서 원인분석에 많이 사용되던 기법. 게임 이론에서 게임의 참여자 간 협조로 얻어진 모든 이득으로부터 참여자들의 기여분에 따라 배분되는 값을 의미하며, ML에서는 어떤 특성의 조건부 조건에서 해당 특성이 모델 예측치의 변화를 가져오는 정도를 가리킨다.

---

## Fairness

ML System은 데이터를 다루는 만큼, Training data의 bias에 영향을 받을 수 밖에 없다. 예를 들어, 현재 존재하는, 접근 가능한 데이터셋은 대부분 European descent 환자 데이터셋인데, 이러한 데이터셋 내 sample의 frequency 차이는 성능에 영향을 끼칠 수 밖에 없다. 또한 특정 희귀 질병 데이터의 경우 데이터 자체를 구하기가 어려운 경우가 많다.

이러한 문제를 극복하고자 하는 시도로 Meta learning과 Transfer learning 등이 연구되고 있는 추세이다.

---

## Data linking and integration

각 환자에서 얻을 수 있는 Data modality들은 다양하고 서로 영향을 주기도 하므로 Multi-modal 모델을 활용하여 다양한 input을 사용하는 연구가 중요할 수 있다. 이 뿐만 아니라 각 data modality 간의 연관성을 밝히는 연구도 중요한 연구 주제이다.

---

## Genomic data privacy

일반적으로 개인 의료 데이터는 개인의 자산으로 간주되며, 민감한 데이터로 취급 되기 때문에 쉽게 공유를 할 수 없다는 문제가 있다. 이에 개인 의료 데이터를 익명화하거나 de-identification 하여 Data sharing을 가능케 하는 것이 일반적이며, 최근에는 블록 체인 기술이나 암호화 기술을 사용하기도 한다.

또한 몇몇 의료기관들에서는 Data sharing issue가 없는 Federated learning의 도입을 시도하고 있다.

**Federated learning:** 다수의 로컬 클라이언트와 하나의 중앙 서버가 협력하여 데이터가 탈중앙화된 상황에서 글로벌 모델을 학습하는 기술

Federated learning(연합학습)은 데이터를 메인 서버가 아닌, 개개인의 로컬 클라이언트에 두고 그 로컬 클라이언트에서 학습을 수행한 후, 업데이트된 모델의 파라미터들을 중앙 서버로 보내 취합해서 하나의 모델을 업데이트 하는 것이다. 그러면 중앙 서버는 데이터를 가지지 않고 있음에도 그 데이터를 이용해 학습한 효과를 낼 수 있게 된다.
