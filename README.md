# AI 도구 모음 · ai-tools-hub

매일 쓰는 AI 도구 큐레이션 + 직접 만든 작은 도구 모음.
정적 HTML 한 장 + JSON 두 개. 빌드 없음, 서버 없음.

## 구조

```
ai-tools-hub/
├── index.html          ← 전체 앱 (B-2 Claude-toned aurora 디자인)
├── tools.json          ← 도구 목록 (여기만 편집)
├── categories.json     ← 카테고리 목록
└── README.md
```

## 도구 추가하는 법

`tools.json`의 `tools` 배열에 객체 하나 추가하면 끝.

```json
{
  "id": "unique-id",
  "name": "도구 이름",
  "url": "https://...",
  "category": "writing",
  "tags": ["태그1", "태그2"],
  "description": "한 줄 설명",
  "free": "완전 무료",
  "by": "제작자",
  "my_note": "(선택) 내가 쓰는 이유 한 줄",
  "is_mine": false
}
```

| 필드 | 필수 | 설명 |
|------|------|------|
| `id` | ✅ | 고유 식별자 (영문 소문자 + 하이픈) |
| `name` | ✅ | 표시 이름 |
| `url` | ✅ | 도구 링크 |
| `category` | ✅ | `categories.json`의 id 중 하나 |
| `tags` | ✅ | 검색용 태그 배열 |
| `description` | ✅ | 한 줄 설명 |
| `free` | ✅ | "완전 무료" / "제한적" / "유료" 등 |
| `by` | ✅ | 제작사 / 제작자 |
| `my_note` | ⬜ | 내가 쓰는 이유 (있으면 카드에 인용구로 표시) |
| `is_mine` | ⬜ | `true`면 "내가 만든 도구" 섹션에 노출 |

## 카테고리 추가하는 법

`categories.json`의 `categories` 배열에 추가:

```json
{ "id": "newcat", "name": "새 카테고리", "emoji": "🆕" }
```

## 로컬 실행

`file://`로 열면 `fetch` 차단됨. 정적 서버 띄워서 확인:

```bash
py -m http.server 8765
# → http://localhost:8765
```

## 배포

GitHub Pages 정적 호스팅. `commme/ai-tools-hub` 레포에 푸시 후 Pages 활성화.

## 디자인

Anthropic Claude 톤:
- 워밍 크림 (`#F5F1E8`) + Book Cloth 오렌지 (`#CC785C`)
- Source Serif 4 + Pretendard + JetBrains Mono
- 드리프팅 오로라 라디얼 그라디언트 3개
- SVG fractal noise 그레인 오버레이
- 마그네틱 호버 카드 (커서 추적 translate3d + 라디얼 글로우)
