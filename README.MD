# whois

AI 기반 포트폴리오 챗봇 서비스

## 소개

머근이의 정보를 채용 담당자가 자연스럽게 질문하고,  
LLM이 실시간으로 응답하는 대화형 포트폴리오 서비스입니다.  
계정 없이 질문할 수 있고, 답변 불가능한 경우에는 본인에게 알림 전송 후 답변 요청이 가능합니다.

## 기술 스택

- Java 17
- Spring Boot 3.2.5
- Gradle 8.2 (Groovy DSL)
- Spring Cloud Gateway
- WebFlux, Redis
- PostgreSQL (예정)
- LLM 연동 (OpenAI, Claude 등)
- MSA + 멀티모듈 구조

## 모듈 구성

| 모듈명 | 설명 |
|--------|------|
| `gateway` | API 라우팅 |
| `auth` | 코드 인증 및 로그인 |
| `chatbot` | LLM 기반 챗 응답 처리 |
| `career` | 경력 정보 제공 |
| `profile` | 자기소개, 기본 정보 |
| `notify` | 알림 처리 (이메일, 슬랙) |
| `admin` | 관리자 전용 UI |
| `infra` | Redis, AWS 설정 |
| `clients` | 외부 API 통신 모듈 |
| `commons` | 공통 예외, 응답 객체 등 |

## 실행 방법

```bash
./gradlew build
