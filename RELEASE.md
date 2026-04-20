# 매일 쓰는 AI 도구 모음 🛠️

**한국에서 실제로 많이 쓰는 AI 도구 + 직접 만든 작은 도구들. 과장 없이, 기능 그대로.**

🔗 바로 쓰기: **https://commme.github.io/ai-tools-hub/**
🎨 디자인 갤러리 (21개 시안): https://commme.github.io/ai-tools-hub/variants/gallery.html

---

## 이런 분께

- AI 도구가 너무 많아 어디부터 써야 할지 모르겠다
- "한국인이 진짜로 매일 쓰는" 도구만 압축해서 보고 싶다
- 카테고리별(글쓰기/이미지/영상/코딩…)로 비교하고 싶다
- 무료/유료 구분이 한눈에 들어오는 리스트가 필요하다
- 나만의 작은 도구도 같이 묶어서 포트폴리오로 보여주고 싶다

---

## 30초 요약

1. https://commme.github.io/ai-tools-hub/ 접속
2. 카테고리 칩 클릭 → 도구 카드 필터링
3. 카드 클릭 → 해당 도구 새 탭으로 이동

설치 ❌ 로그인 ❌ 본인 데이터 수집 ❌

---

## 무엇이 있나

### 8개 카테고리 · 33개 도구

| 카테고리 | 예시 |
|---------|------|
| ✍️ 글쓰기 | Claude, ChatGPT, Gemini |
| 🔍 리서치 | Perplexity, NotebookLM |
| 🎨 이미지 | Midjourney, Imagen, Flux |
| 🎬 영상 | Veo, Sora, Runway, Kling |
| 🎵 음성 | Suno, ElevenLabs |
| 💻 코딩 | Claude Code, Cursor |
| ⚡ 생산성 | Notion AI, ai-tools-hub |
| 🎭 디자인 | Figma AI, Canva AI |

각 카드: 도구명 / 한 줄 설명 / 무료-유료 / 제조사 / 내 한 줄 평.

---

## 직접 만든 도구도 같이

`is_mine: true`로 표시되는 카드:
- **카카오톡 채팅방 정리기** — 카톡 백업 .txt 자동 분류
- **All-to-All 변환기** — 로컬 파일 변환 올인원
- **File to PNG** — PDF/HWP → PNG
- **AI 도구 모음** — (이 사이트 자체)

---

## 도구 추가하기

`tools.json`의 `tools` 배열에 객체 추가만 하면 끝:

```json
{
  "id": "도구-아이디",
  "name": "도구 이름",
  "url": "https://...",
  "category": "writing|research|image|video|audio|coding|productivity|design",
  "tags": ["태그1", "태그2"],
  "description": "한 줄 설명.",
  "free": "완전 무료 | 제한적 | 유료",
  "by": "제조사",
  "my_note": "내 한 줄 평 (선택)",
  "is_mine": false
}
```

GitHub Pages 자동 배포 → push 후 1~2분 후 라이브.

---

## 자주 묻는 질문

**Q. 광고/제휴 링크인가요?** ❌ 전혀 없음. 순수 큐레이션.

**Q. 도구 선정 기준은?** 한국 사용자가 실제로 많이 쓰는 + 내가 직접 써본 것만.

**Q. 정기 업데이트되나요?** 새 도구 발견 시마다 수동 추가. tools.json 보면 됨.

**Q. 디자인이 왜 21개?** 브루털리즘 톤 후보 갤러리. variants/gallery.html에서 비교 가능.

**Q. 모바일에서도 봐도 돼요?** 네, 반응형.

**Q. 내 데이터 수집해요?** ❌ 정적 사이트라 수집할 게 없음. 분석 스크립트도 없음.

---

## 보안·개인정보

| 항목 | 상태 |
|------|------|
| 로그인/계정 | ❌ 없음 |
| 분석/추적 스크립트 | ❌ 없음 (Google Analytics ❌) |
| 외부 스크립트 | Google Fonts + jsdelivr Pretendard CDN만 |
| CSP | 적용 (스크립트/스타일/폰트 화이트리스트) |
| 데이터 저장 | ❌ 서버 없음, localStorage 사용 안 함 |
| 외부 링크 | 도구 카드 클릭 시 새 탭으로 해당 사이트 이동 |

순수 정적 HTML + JSON. 백엔드 없음.

---

## 디자인 컨셉

- **브루털리즘** (Brutalism) — 두꺼운 검은 테두리, 옐로우 액센트(#DDFF00)
- **타이포** Space Grotesk (헤드라인) + IBM Plex Mono (라벨) + Pretendard (본문)
- **컬러** #FAFAF7 / #0A0A0A / #DDFF00 / #666
- **모바일 대응** 카드 그리드 → 단일 칼럼 자동 전환

---

## 로컬 실행

```bash
py -m http.server 8765
# http://localhost:8765
```

`tools.json` / `categories.json`만 수정하면 즉시 반영.

---

## 만든 사람

© 2026 COMMME · Built with Claude Code

피드백/도구 추천: https://github.com/commme/ai-tools-hub/issues
