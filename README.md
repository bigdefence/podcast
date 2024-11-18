# AI-Search-Engine-podcast

인공지능 검색엔진 결과를 바탕으로 팟캐스트를 생성하는 도구로, OpenAI의 언어 모델과 음성 합성(TTS) 기능을 활용합니다. 이 프로젝트는 팟캐스트 스크립트를 생성하고 이를 오디오로 변환하는 과정을 하나의 흐름으로 제공합니다.

## 기능

- **동적 팟캐스트 스크립트 생성**: OpenAI의 GPT 모델을 사용하여 입력한 주제에 맞는 매력적이고 유익한 팟캐스트 스크립트를 생성합니다.
- **사용자 지정 가능한 TTS 음성**: 다양한 음성(e.g., alloy, echo, nova) 중에서 선택하여 팟캐스트에 사용할 수 있습니다.
- **검색 통합**: 검색 결과를 가져와 정확하고 문맥에 맞는 콘텐츠를 제공합니다.
- **풍부한 사용자 인터페이스**: `rich` 라이브러리를 사용하여 시각적으로 매력적인 터미널 환경을 제공합니다.
- **스크립트 및 오디오 저장**: 생성된 스크립트와 오디오 파일을 저장하여 나중에 참조할 수 있습니다.

## 설치

### 사전 요구 사항

- Python 3.7+
- OpenAI API 키 (`.env` 파일에 저장)
- 필요한 Python 패키지 (`requirements.txt`를 통해 설치)

### 설정

```bash
# 레포지토리 클론
git clone <[repository_url](https://github.com/bigdefence/AI-Search-Engine-podcast/)>
cd podcast-generator

# 종속성 설치
pip install -r requirements.txt

# 프로젝트 루트에 .env 파일을 생성하고 OpenAI API 키 추가
echo "OPENAI_API_KEY=your_openai_api_key_here" > .env
```

## 사용 방법

```bash
# 메인 스크립트 실행
python main.py
```

1. 안내에 따라 팟캐스트 주제, 원하는 길이, 음성을 입력합니다.
2. 스크립트는 다음과 같은 작업을 수행합니다:
   - 입력한 주제에 대한 검색 결과를 가져옵니다.
   - GPT를 사용하여 팟캐스트 스크립트를 생성합니다.
   - OpenAI의 TTS를 사용하여 스크립트를 오디오로 변환합니다.
   - 생성된 스크립트와 오디오를 `generated_podcasts` 디렉터리에 저장합니다.

## 인자 및 프롬프트

- **팟캐스트 주제**: 팟캐스트의 주제를 입력합니다.
- **팟캐스트 길이**: 분 단위로 길이를 지정합니다 (기본값은 5분).
- **음성 선택**: 사용 가능한 TTS 음성 중에서 선택 (`alloy`, `echo`, `fable`, `onyx`, `nova`, `shimmer`).

## 예시 출력

- 생성된 팟캐스트 스크립트는 `.txt` 파일로 저장됩니다.
- 오디오 파일은 `.mp3` 파일로 저장됩니다.
- 두 파일 모두 `generated_podcasts` 디렉터리에 저장됩니다.

## 요구 사항

- Python 라이브러리:
  - `openai`
  - `dotenv`
  - `rich`
  - `asyncio`
  - 사용자 정의 모듈 (`services.search`, `utils.text_processing`)

## 참고 사항

- 언어 및 TTS 서비스를 사용하려면 유효한 OpenAI API 키가 필요합니다.
- Windows 사용자는 생성된 팟캐스트를 기본 미디어 플레이어를 통해 직접 들을 수 있습니다.

## 기여

개선이나 새로운 기능에 대한 제안이 있으면 이슈나 풀 리퀘스트를 제출해 주세요.

## 라이선스

이 프로젝트는 MIT 라이선스 하에 오픈 소스로 제공됩니다.

## 감사의 말

- **OpenAI**: 언어 모델 및 TTS 서비스 제공에 대해 감사드립니다.
- **Rich Library**: 터미널 사용자 경험을 향상시키는 데 도움을 준 라이브러리에 감사드립니다.

