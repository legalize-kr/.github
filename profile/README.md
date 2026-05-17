### Legalize-KR: 대한민국의 법령/판례/행정규칙/자치법규를 Markdown 문서와 Git 이력으로.

법령 데이터는 "지금 무엇이 쓰여 있는가"만큼 "**언제, 어떻게 바뀌어 왔는가**"가 중요합니다. 기존 법령 포털은 특정 시점의 조문을 보여주는데 최적화되어 있지만, 변경 이력을 추적하거나 두 시점을 비교하거나 전체 내용을 다루기는 불편합니다. Legalize-KR은 [국가법령정보센터](https://www.law.go.kr) OpenAPI에서 원천 데이터를 받아 사람과 AI 모두가 읽기 편한 Markdown 형식으로 변환하고, 공포/시행/선고일자 기준의 Git commit으로 남겨 이러한 불편을 해소합니다.

### 제공 데이터셋

| 저장소 | 내용 | 사용법 |
|---|---|---|
| [`legalize-kr/legalize-kr`](https://github.com/legalize-kr/legalize-kr) | 대한민국 법령 데이터 | [소개 및 사용법](https://legalize.kr/laws.html) |
| [`legalize-kr/precedent-kr`](https://github.com/legalize-kr/precedent-kr) | 대한민국 판례 데이터 | [소개 및 사용법](https://legalize.kr/precedents.html) |
| [`legalize-kr/admrule-kr`](https://github.com/legalize-kr/admrule-kr) | 대한민국 행정규칙 데이터 | [소개 및 사용법](https://legalize.kr/admrules.html) |
| [`legalize-kr/ordinance-kr`](https://github.com/legalize-kr/ordinance-kr) | 대한민국 자치법규 데이터 | [소개 및 사용법](https://legalize.kr/ordinances.html) |

위 데이터 저장소들의 원천 데이터는 국가법령정보센터 OpenAPI로부터 가져오며, [수집/변환](https://github.com/legalize-kr/legalize-pipeline) 및 [Git 저장소로 재구성](https://github.com/legalize-kr/compiler)하는 과정을 거칩니다.

### ⚠️ Git 이력은 재구성될 수 있습니다

데이터 저장소는 일반 코드 저장소와 다르게 운영됩니다. 파싱 및 정규화 규칙이 개선되면 같은 원천에서 더 정확한 결과를 만들기 위해 저장소 전체를 재구성하고 **force-push**합니다. 따라서 **Git Commit Hash는 안정적 식별자가 아닙니다**. 
장기 참조 시에는 `법령ID`나 `판례일련번호` 같은 원천 식별자와 날짜, [law.go.kr](https://www.law.go.kr) URL을 함께 보존하고, 재현이 중요한 작업에는 release나 자체 스냅샷을 고정하세요.
