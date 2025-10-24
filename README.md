# 🚢 타이타닉 생존자 예측 프로젝트

타이타닉 탑승객 데이터를 기반으로 생존 여부를 분류하는 머신러닝 모델을 실습합니다.

## 📂 데이터셋

  - `titanic.csv`: 탑승객의 정보와 생존 여부가 모두 포함된 통합 데이터 파일
  - **GitHub Repository**: `https://github.com/thiskorea81/titanic.git`

## 📊 속성 정보 (Attribute Information)

| 속성명 (영문) | 속성명 (한글) | 설명 |
| :--- | :--- | :--- |
| `pclass` | **객실\_등급** | 1 = 1등석, 2 = 2등석, 3 = 3등석 |
| `survived` | **생존\_여부** | 0 = 사망, 1 = 생존. **(분류 대상)** |
| `sex` | **성별** | `male`(남성), `female`(여성) |
| `age` | **나이** | 승객 나이 (세) |
| `sibsp` | **형제/배우자\_수** | 함께 탑승한 형제자매 또는 배우자의 수 |
| `parch` | **부모/자녀\_수** | 함께 탑승한 부모 또는 자녀의 수 |
| `ticket` | **티켓\_번호** | 티켓 고유 번호 |
| `fare` | **요금** | 승객이 지불한 요금 |
| `cabin` | **객실\_번호** | 승객의 객실 번호 (많은 값이 비어있음 - `NaN`) |
| `embarked` | **탑승\_항구** | C = Cherbourg, Q = Queenstown, S = Southampton |
| `boat` | **구명보트\_번호** | 생존자가 탑승한 구명보트 번호 (생존 여부 유출 가능성 있음) |

## 🚀 구글 코랩(Google Colab)에서 실행하기

구글 코랩 환경에서 아래 코드를 순서대로 실행하여 데이터를 간편하게 불러올 수 있습니다.

### 1\. GitHub 저장소 복제

`!git clone` 명령어를 사용하여 GitHub에 있는 데이터 파일을 코랩 환경으로 가져옵니다.

```python
!git clone https://github.com/thiskorea81/titanic.git
```

### 2\. Pandas로 데이터 불러오기

저장소 복제가 완료되면, `pandas` 라이브러리를 사용하여 `titanic.csv` 파일을 DataFrame으로 불러옵니다.

```python
import pandas as pd

# 복제된 폴더 안의 파일 경로를 지정합니다.
file_path = '/content/titanic/titanic.csv'

# CSV 파일을 DataFrame으로 읽어옵니다.
df = pd.read_csv(file_path)

# 데이터의 첫 5행을 출력하여 잘 불러왔는지 확인합니다.
df.head()
```
