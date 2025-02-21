# Webhook Java 애플리케이션

이 프로젝트는 Java의 `HttpClient`를 사용하여 LLM API 및 이미지 생성 API를 호출하고, 결과를 Slack Webhook을 통해 전송하는 애플리케이션입니다.

## 🔧 기능

- LLM API를 호출하여 프롬프트 결과 생성
- LLM 결과를 사용하여 이미지 생성 API 호출
- Slack Webhook을 이용하여 메시지 전송

## 📜 코드 설명

### 1️⃣ LLM API 호출 (`useLLM` 메서드)
- 사용자 입력을 LLM API로 전달하여 응답을 받음
- 응답에서 `content` 값을 추출하여 반환

### 2️⃣ 이미지 생성 API 호출 (`useLLMForImage` 메서드)
- LLM에서 받은 결과를 기반으로 프롬프트를 생성 후 이미지 API 호출
- 응답에서 이미지 URL을 추출하여 반환

### 3️⃣ Slack 메시지 전송 (`sendSlackMessage` 메서드)
- LLM 결과와 이미지 URL을 포함한 메시지를 Slack Webhook을 통해 전송