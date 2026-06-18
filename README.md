# 🧠 나만의 AI 학습 허브 — 템플릿

AI를 따라잡는 두 가지 길을 한 곳에. **코딩을 몰라도** Claude Cowork에게 시키면 됩니다.
이 저장소는 **포크해서 바로 시작하는 깨끗한 템플릿**입니다. (가득 찬 예시는 👉 [ai-newsletter 샘플](https://github.com/imakerjun/ai-newsletter) / [라이브](https://imakerjun.github.io/ai-newsletter/))

- 📰 **받아보기 (자동)** — 내 관심사 맞춤 AI 뉴스레터가 매일 아침 자동 발행됩니다.
  - 아카이브: `index.html` · 한 호: `editions/{날짜}.html`
- 📚 **깊이 읽기 (수동)** — 공부하고 싶은 어려운 문서를 **5가지 렌즈**(🔤어원·⚡한입요약·🧒비유·🧪퀴즈·📄전문번역)로 재구성.
  - 라이브러리: `learn/index.html` · 한 문서: `learn/{슬러그}.html`
- 🤖 **사양**: [`AGENT.md`](./AGENT.md) — 자동 발행 + 수동 렌즈 생성 지시서
- 🎨 Folio(Notion 스타일) 단일 HTML · 라이트/다크 자동 · GitHub Pages로 배포·누적

> 지금 들어 있는 항목은 **예시(`예시` 배지)**입니다. 첫 발행 때 에이전트가 자동으로 비우고 내 콘텐츠로 채웁니다.

---

## 따라하기 (4단계)

### 1. 이 템플릿으로 내 저장소 만들기
상단 **`Use this template` → `Create a new repository`**. 내 계정에 똑같은 구조가 생깁니다(깃 명령 불필요).

### 2. GitHub Pages 켜기
새 저장소 → `Settings → Pages → Branch: main / (root)` → 저장. 잠시 후 `https://{내아이디}.github.io/{레포}/` 로 열립니다.

### 3. Claude Cowork에 저장소 연결 + 내 관심사로 바꾸기
Cowork에 저장소를 연결하고, 아래를 붙여넣으세요.
```
이 저장소는 내 AI 학습 허브 템플릿이야. AGENT.md의 "내 설정"에서 interests를 내 관심사로 바꿔줘.
내 관심사: (예) AI 최신 소식 / 비개발자를 위한 AI 소식 / 우리 팀 업무에 쓰는 AI
persona_context에 나를 한두 문장으로 소개해줘: (예: 마케팅 담당, 신상품 기획)
그리고 오늘 날짜로 첫 호를 만들고, 예시 항목은 제거해줘.
```

### 4. 매일 자동 발행 + 슬랙 알림 걸기
```
매일 아침 8시에 AGENT.md 사양대로 새 호를 발행하고, 커밋·푸시하고,
슬랙 Incoming Webhook으로 배포 링크를 보내도록 스케줄을 등록해줘.
```

### (선택) 어려운 문서를 깊이 읽기로
```
이 링크를 '깊이 읽기' 렌즈 문서로 만들어줘 — {문서 URL}
```

---

## 구조
```
.
├── index.html               # 📰 뉴스레터 아카이브 (ARCHIVE.editions)
├── editions/2026-06-18.html  # 예시 한 호 (NEWSLETTER 데이터 객체)
├── _TEMPLATE_edition.html    # 뉴스레터 한 호의 고정 구조 템플릿
├── learn/
│   ├── index.html            # 📚 렌즈 라이브러리 (LIBRARY.docs)
│   ├── prompting-fable-5.html#   예시 렌즈 문서 (LENS_DOC 데이터 객체)
│   └── _TEMPLATE_lens.html   #   렌즈 문서의 고정 구조 템플릿
├── AGENT.md                  # 자동 발행 + 수동 렌즈 생성 사양
└── README.md
```

디자인: [Folio](https://claude.ai/design) · 깊이 읽기는 [doc-lenses](https://github.com/imakerjun/learning-templates/tree/main/doc-lenses) 각색.
