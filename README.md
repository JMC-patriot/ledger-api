# 가계부 API (ledger-api)

- GitHub: https://github.com/JMC-patriot/ledger-api
- Render: (과제 단계 5에서 채우기 — https://<서비스>.onrender.com/docs)

FastAPI + SQLAlchemy + Supabase(PostgreSQL)로 만든 계좌·거래·카테고리 API.

## 엔드포인트

| 메서드 | 경로 | 하는 일 |
|---|---|---|
| POST | /accounts | 계좌 생성 |
| GET | /accounts | 계좌 목록 |
| GET | /accounts/{account_id} | 계좌 단건 |
| POST | /transactions | 거래 생성 (계좌 없으면 404) |
| GET | /accounts/{account_id}/detail | 계좌 + 거래 목록(중첩 응답) |
| GET | /stats/by-category | 카테고리별 지출 합계 |

## 실습 기록

### ① 결과 확인
(Supabase Table Editor의 transactions 캡처를 붙인다. Render 배포 후에는 /docs의 GET /accounts 캡처도 함께.)

### ② 핵심 개념 되새김 (자기 말로 한 줄씩)
- 계좌·거래를 두 테이블로 나눈 이유(1:N 관계):
- SQLAlchemy 모델 클래스와 실제 테이블의 대응:
- 접속 문자열을 .env로 분리하는 이유:

### ③ 자유 로그
- 배운 것:
- 막힌 곳과 푼 과정:
- 아직 안 풀린 것:
- AI 활용: Claude Code로 워크북의 코드 파일을 생성하고, 단계 1 스크립트 실행 결과와 API 6개 경로의 응답(201·404·중첩·집계)이 워크북의 확인 값과 같은지 검증했다.
