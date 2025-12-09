# 🦄 유니코 AI - 농업 문서 분석 시스템

농업 PDF 문서를 AI로 스마트하게 분석하는 Streamlit 기반 애플리케이션입니다.
Google Gemini 2.0과 LangChain RAG를 활용하여 농업 관련 질문에 전문적인 답변을 제공합니다.

## 🌟 주요 기능

- **📄 PDF 자동 분석**: `fixed_pdfs` 폴더의 PDF를 자동으로 로드 및 벡터화
- **🤖 AI 농업 전문가**: Google Gemini 2.0 기반의 농업 전문 답변
- **🔍 스마트 검색**: MMR(Maximal Marginal Relevance) 검색으로 정확한 정보 제공
- **💬 대화형 인터페이스**: 채팅 형식의 직관적인 UI
- **📱 텔레그램 연동**: AI 답변을 텔레그램으로 바로 전송
- **🚀 빠른 분석**: 4가지 퀵 버튼으로 즉시 분석 가능

## 📋 분석 주제

- 🌾 작물 재배 방법 및 단계별 가이드
- 🌡️ 최적 환경 조건 (온도, 습도, 광량)
- 🐛 병충해 예방 및 방제 방법
- 💰 재배 비용 및 수익성 분석

## 🚀 설치 및 실행

### 1. 저장소 복제

```bash
git clone [이 레포지토리 주소]
cd [프로젝트 폴더]
```

### 2. 패키지 설치

```bash
pip install -r requirements.txt
```

### 3. API 키 설정

프로젝트 루트에 `.streamlit/secrets.toml` 파일 생성:

```toml
[gemini]
api_key = "your-gemini-api-key"

[telegram]
bot_token = "your-telegram-bot-token"
```

**API 키 얻는 방법:**
- [Google Gemini API 키](https://aistudio.google.com/apikey)
- Telegram 봇: @BotFather에게 `/newbot` 입력

### 4. PDF 준비

`fixed_pdfs` 디렉토리 생성하고 분석할 PDF 파일 추가:

```
프로젝트폴더/
├── app.py
├── requirements.txt
├── .streamlit/
│   └── secrets.toml
└── fixed_pdfs/
    ├── 농업_재배_가이드.pdf
    └── ...
```

### 5. 실행

```bash
streamlit run app.py
```

## 📖 사용 방법

### PDF 분석
1. 사이드바에서 PDF 선택
2. "이 PDF 로드" 클릭
3. 채팅창에 농업 관련 질문 입력
4. AI의 상세한 답변 확인

### 빠른 분석 버튼
- 🌾 **재배법 요약**: 핵심 재배 방법
- 🌡️ **환경 조건**: 온도, 습도 등 최적 조건
- 🐛 **병충해 관리**: 예방 및 방제 방법
- 💰 **수익성 분석**: 비용 및 수익 분석

### 텔레그램 연동
1. @userinfobot에서 `/start` 입력하여 Chat ID 확인
2. 사이드바 "텔레그램 설정"에서 Chat ID 입력
3. AI 답변을 텔레그램으로 전송 가능

## 🛠️ 기술 스택

- **웹 프레임워크**: Streamlit
- **LLM**: Google Gemini 2.0 Flash
- **임베딩**: Hugging Face (multilingual-MiniLM-L12-v2)
- **벡터 DB**: Chroma
- **문서 처리**: LangChain, PyPDF
- **메신저**: Telegram Bot API

## ⚠️ 주의사항

- API 키는 GitHub에 커밋하지 마세요
- `.gitignore`에 `secrets.toml` 포함 확인
- 큰 PDF는 처리 시간이 오래 걸릴 수 있습니다

## 📝 필수 요구사항

- Python 3.8 이상
- Google Gemini API 키
- (선택) Telegram 봇 토큰

## 📄 라이선스

자유롭게 사용, 수정, 배포 가능합니다.

---

**🌻 농업의 디지털 혁신을 함께합시다!**
