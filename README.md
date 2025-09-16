# Capstone-POKI💚


## 🎯 프로젝트 소개
- **프로젝트명**: PitchCoach
- **주제**: AI 기반 IR 피칭 준비 플랫폼 (PitchCoach for Startups)
- **기간**: 2025.09 ~ 2026.06

이 저장소는 **POKI** 팀이 진행하는 프로젝트의 모든 소스 코드, 문서, 그리고 관련 자료를 포함하고 있습니다. 저희 팀은 **AI 기반 IR 피칭 준비 플랫폼**을 개발하는 것을 목표로 하고 있습니다.


|팀번호|팀명|프로젝트명|
|:---|:---|:---|
|[20](#team-20-팀명20)|POKI|PitchCoach (스타트업을 위한 AI 기반 IR 피칭 준비 플랫폼)|

Team 20 POKI

| 프로젝트명 | PitchCoach (스타트업을 위한 AI 기반 IR 피칭 준비 플랫폼) |
| --- | --- |
| 프로젝트 키워드 | AI, 스타트업, IR 피칭 |
| 트랙 | 산학 |
| 프로젝트멤버 | 강민경, 김예린, 장현서 |
| 팀지도교수 | 이민수 |
| 무엇을 만들고자 하는가 | IR 피칭 준비 전 과정(공고 분석 → Deck 분석 → 리허설(음성) → AI 리포트 → 수정 가이드 → 예상 Q&A 훈련)을 지원하는 **AI 기반 통합 플랫폼** |
| 고객 | 투자와 발표를 준비하는 스타트업 대표 |
| Pain Point | 1. **IR 준비 비효율**: 공고별 요구사항에 맞춘 Deck/피칭 준비가 어려움
2. **실전 대비 부족**: 시간 관리·발화 습관·투자자 질문 대응력이 미흡
3. **정량적 지표 부족**: 발표 후 객관적인 피드백/점수가 없음
4. **투자자 관점 차이**: 창업자가 강조한 포인트와 VC가 궁금한 포인트가 불일치 |
| 사용할 소프트웨어 패키지의 명칭과 핵심기능/용도, 사용시나리오 | 1️⃣ 음성 인식 & 분석 (Speech AI)**OpenAI Whisper** → 다국어 ASR, 발표 전사**librosa / praat-parselmouth** → Prosody(억양, 속도, 발음 명료도) 분석**pyannote.audio** → 발화 구간/화자 분리**사용 시나리오**: 리허설 발표 음성 업로드 → 전사 + 억양/속도/시간 분석 → 실시간/사후 리포트 생성
2️⃣ 문서 분석 & 정보 추출 (NLP for IR Docs)**Tesseract, PDFPlumber** → Deck & PDF OCR 파싱**spaCy NER / KeyBERT / HuggingFace Transformers** → 재무 수치·단위 추출, 키워드 분석**LLM (GPT-4/5, Claude, LLaMA)** → 공고문 요약 & 평가 항목 추출**사용 시나리오**: 공고문 업로드 → 중요 평가 항목 가중치 추출 → Deck과 매칭 → 부족 섹션 강조
3️⃣ IR 루브릭 스코어링 (Evaluation AI)**ko-SBERT, sentence-transformers** → 문장 임베딩/섹션 분류**Hybrid Scoring (규칙 + LLM)** → IR 루브릭(구조/스토리/시장성/재무 등) 점수화**LIME/SHAP** → 점수 근거 문장 Highlight**사용 시나리오**: IR 발표 전체 전사·Deck → 섹션별 커버리지 평가 + 점수 대시보드 생성
4️⃣ Q&A 질문 생성 & 답변 평가 (Conversational AI)**HuggingFace QG 모델 (T5/BART)** → 질문 자동 생성**LLM Fine-tuning** → 투자자 Q&A 데이터셋 기반 학습**WebRTC + STT** → 실시간 Q&A 모드**사용 시나리오**: 예상 질문 리스트 제공 → 창업자가 음성으로 답변 → 30초 제한 평가(간결성/정확성/구조성)
5️⃣ MLOps & 운영**FastAPI/Flink** → 모델 서빙 및 API**PostgreSQL + S3** → 전사·오디오·피드백 저장**FAISS / Weaviate** → 공고문 + Deck RAG 검색**ONNX/Quantization** → 경량화 & GPU 최적화**사용 시나리오**:모델 실시간/배치 서빙발표 세션 기록 저장·비교데이터 암호화 및 만료 정책 운영 |
| 사용할 소프트웨어 패키지의 명칭과 URL | 🔗 소프트웨어 패키지와 URL
Whisper: https://github.com/openai/whisper
librosa: https://librosa.orgpyannote.audio: https://github.com/pyannote/pyannote-audio
Tesseract OCR: https://github.com/tesseract-ocr/tesseract
spaCy: https://spacy.ioHuggingFace Transformers: https://huggingface.co/transformersKeyBERT: https://github.com/MaartenGr/KeyBERT
ko-SBERT: https://github.com/UKPLab/sentence-transformers
FastAPI: https://fastapi.tiangolo.com
FAISS: https://github.com/facebookresearch/faiss |
| 팀그라운드룰 | [GroundRule](https://github.com/Capstone-POKI/POKI/blob/main/GroudRuld.MD) |
| 최종수정일 | 2025-09-16 |


## 📜 라이선스

이 프로젝트는 [라이선스 종류, 예: MIT License]에 따라 배포됩니다.
