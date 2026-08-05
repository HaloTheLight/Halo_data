## 💻 Projects (주요 개발 경험)
데이터 파이프라인 구축 및 ML 모델링 핵심 프로젝트입니다.

**[Data Engineering/ML] HALO: 시공간 위험도 예측 기반 안전 보행 내비게이션 (2026) - 🏆 해커톤 대상**
* **Role:** ML Data Engineer
* **Description:** 야간 보행 안전 지수(WSI) 산출을 위한 이진 분류(대인 사건 발생 확률 추정) ML 파이프라인 뼈대 구축.
* **Key Achievements:**
  * **대규모 시공간 데이터 파이프라인:** 오픈스트리트맵(OSM)과 GeoPandas를 활용해 19.5만 개의 도로 세그먼트(Edges)를 추출하고, 5종의 이질적 공공데이터(범죄, 민원 등)를 50m 버퍼 기반으로 공간 조인(Spatial Join) 수행.
  * **6,250만 행(62.5M Rows) 패널 데이터 구축:** `(Segment × Period × DOW × Slot)` 기준으로 조합하여 시계열 예측을 위한 대규모 Base Grid 생성 및 동적/정적 피처 매핑.
  * **Target Leakage(라벨 누수) 원천 차단:** 모델이 미래 데이터를 참조하지 못하도록, 네트워크 구조 기반으로 인접 세그먼트(Adjacent)의 '과거' 사건율만 피처로 합산하는 **Time-lagged Spatial Feature** 로직 설계 및 구현.
  * **모델링 및 최적화:** LightGBM 알고리즘 적용 및 Isotonic 확률 보정 처리. 데이터 스키마 변경에 유연하게 대응할 수 있도록 Config 기반 모듈화 구조 설계.
* **Tech Stack:** Python, GeoPandas, OSMnx, NumPy, LightGBM, scikit-learn
