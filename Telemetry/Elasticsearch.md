# 명령어
```shell
GET /_cat/indices # 모든 인덱스 확인
GET /index/_search # Index 내의 도큐먼트 확인
PUT /index # INDEX 생성
POST /index/document/1 -d '{}' #document 생성
```

## 특이한 점
1. field Type을 number로 선언
1. 값을 "10" 입력
1. field Type 조회시 number이지만 값은 "10"으로 삽입되어 있다.
1. 이게 string인지 long인지..?

### 해결
- Elasticsearch field type -> 숫자 필드들은 기본적으로 숫자로 이해될 수 있는 값들은 숫자로 변경해서 저장.
- 예를 들어 integer 필드에 4, "4", 4.5 등을 입력하면 모두 자연수 4로 자동으로 변환되어 저장된다.
