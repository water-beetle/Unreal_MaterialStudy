# ✅ 1) **Brightness (밝기)**

> **밝기 = 전체 색 값을 일정 비율로 키우거나 줄임**

📌 **수식**
$$
Color_{out} = Color_{in} \times Brightness
$$

- Brightness = 1.0 → 변화 없음
- Brightness > 1.0 → 더 밝아짐
- Brightness < 1.0 → 더 어두워짐

🔎 핵심

- RGB 전체를 동일하게 곱하므로 색상 변화 없이 “밝기”만 변화
- 값이 커질수록 흰색에 가까워지고 작아질수록 검정으로 수렴

------

# ✅ 2) **Saturation (채도)**

> **채도 = 회색(Grey)에서 원래색(Color_in) 방향으로 얼마나 이동할지**

흑백 변환 기준값을 `Luminance` 라고 하면
 (보통 `dot(Color_in, vec3(0.3, 0.59, 0.11))`)

📌 **수식**
$$
Gray = Luminance(Color_{in})
$$
또는
$$
Color_{out} = Gray \times (1 - Saturation) + Color_{in} \times Saturation
$$

- Saturation = 0 → 완전 회색
- Saturation = 1 → 원본
- Saturation > 1 → 과채도(선명함 증가)

🔎 핵심

- 색의 “진함(선명도)”만 조절
- 밝기 자체가 바뀌는 것은 아님

------

# ✅ 3) **Contrast (대비)**

> **평균(중간톤)으로부터 멀고/가깝게 색을 이동시킴**

기준을 0.5(중간값)로 잡는 경우가 일반적

📌 **수식**
$$
Color_{out} = (Color_{in} - 0.5) \times Contrast + 0.5
$$

- Contrast = 1 → 원본
- Contrast > 1 → 밝은 곳 더 밝게 / 어두운 곳 더 어둡게
- Contrast < 1 → 밝고 어두운 차이가 좁아짐 → 평탄해짐

🔎 핵심

- 명암 차이를 강조하거나 감소시킴
- 평균값에서 얼마나 멀어질지 결정

------

# ✅ 4) **Tint (색조)**

> **Tint = 특정 색을 입혀주는 과정**

📌 **수식**
$$
Color_{out} = Color_{in} \times TintColor
$$

- TintColor = (1,1,1) → 변화 없음
- TintColor = (1, 0.5, 0.5) → 붉은 계열 강조
- 특정 색 필터 씌우는 느낌

🔎 핵심

- 곱셈 기반 → 특정 채널만 강조 가능
- 전체 분위기/톤 조정에 사용

------

# ✅ 4가지 한눈 정리

| 항목           | 수식                                                    | 의미             |
| -------------- | ------------------------------------------------------- | ---------------- |
| **Brightness** | $Color_{out} = Color_{in} \times B$                     | 전체 밝기 스케일 |
| **Saturation** | $Color_{out} = Gray \times (1-S) + Color_{in} \times S$ | 선명도           |
| **Contrast**   | $Color_{out} = (Color_{in}-0.5) \times C + 0.5$         | 명암 강도        |
| **Tint**       | $Color_{out} = Color_{in} \times TintColor$             | 색조(필터)       |

------

# ✅ 관점 설명

| 이름       | 조작 방식                       |
| ---------- | ------------------------------- |
| Brightness | 원본 색을 전체적으로 곱함       |
| Saturation | 회색 → 원본 색 사이 선형 블렌딩 |
| Contrast   | 중간값 기준으로 색을 확장/압축  |
| Tint       | 색 채널별 곱으로 색 방향 변경   |

------

# ✅ 예시 시각화 (감각적)

| 항목       | 바뀌는 특징           |
| ---------- | --------------------- |
| Brightness | 밝기만 증가/감소      |
| Saturation | 색의 선명함 변화      |
| Contrast   | 밝고 어두움 차이 조절 |
| Tint       | 특정 색 기울기 부여   |

------

# ✅ 결론

- **Brightness** = 전체 밝기 스케일
- **Saturation** = 회색 ↔ 원본 사이를 섞음
- **Contrast** = 밝고 어두움의 차이를 키우거나 줄임
- **Tint** = 특정 색 필터 적용

> 네 가지 개념 모두 **수학적으로 Color_in → Color_out** 변환하는 형태로 이해하면 가장 명확함.
