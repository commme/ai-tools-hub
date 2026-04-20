# 매일 쓰는 AI 도구 모음

> 한국에서 실제로 많이 쓰는 AI 도구 + 직접 만든 작은 도구들. 과장 없이, 기능 그대로.

🔗 **Live**: https://commme.github.io/ai-tools-hub/
🎨 **디자인 갤러리**: https://commme.github.io/ai-tools-hub/variants/gallery.html

## 구조

```
ai-tools-hub/
├── index.html          ← 메인 (브루털리즘 톤, 옐로우 #DDFF00)
├── tools.json          ← 도구 데이터 (33개)
├── categories.json     ← 카테고리 정의 (8개)
└── variants/           ← 21개 디자인 시안 + 갤러리
    ├── gallery.html    ← 시안 비교 + 무드/뷰포트 토글
    ├── a-darkneon.html ~ t-responsive.html
```

## 카테고리

✍️ 글쓰기 · 🔍 리서치 · 🎨 이미지 · 🎬 영상 · 🎵 음성 · 💻 코딩 · ⚡ 생산성 · 🎭 디자인

## 도구 추가

`tools.json`의 `tools` 배열에 객체 하나 추가:

```json
{
  "id": "도구-아이디",
  "name": "도구 이름",
  "url": "https://...",
  "category": "writing | research | image | video | audio | coding | productivity | design",
  "tags": ["태그1", "태그2"],
  "description": "한 줄 설명.",
  "free": "완전 무료 | 제한적 | 유료",
  "by": "제조사",
  "my_note": "내 한 줄 평 (선택)",
  "is_mine": false
}
```

## 로컬 실행

```bash
py -m http.server 8765
# http://localhost:8765
```

## 배포

GitHub Pages 자동 배포. `main` 브랜치 푸시 → 1~2분 후 라이브.

---

© 2026 commme · Built with Claude Code
