# claude-admaker-assets

admaker 스킬 저장소(kingsae1/claude-admaker-skills, 비공개)에서 공개 URL로 내려줘야 하는 파일만 모아 둔 공개 저장소입니다.
여기 있는 파일은 스킬·앱이 URL로 직접 불러오므로, 파일 이름이나 경로를 바꾸면 참조하는 쪽도 함께 바꿔야 합니다.

| 경로 | 쓰는 곳 | URL |
|---|---|---|
| `fonts/` | 스킬 `references/fonts.json`, 앱 MCP `src/mcp/skill/fonts.json` (렌더 시 폰트 로드) | `https://cdn.jsdelivr.net/gh/shaneParkKt/claude-admaker-assets@main/fonts/<파일명>` |
| `gallery/previews/` | 스킬 `gallery/data/ads.json`, 앱 MCP `src/mcp/skill/gallery/ads.json`의 `preview_url` (기획 단계 예시 미리보기) | `https://raw.githubusercontent.com/shaneParkKt/claude-admaker-assets/main/gallery/previews/<slug>.webp` |
| `samples/` | 스킬 `gallery/prompts/*.md`의 미리보기 gif | `https://github.com/shaneParkKt/claude-admaker-assets/blob/main/samples/<slug>/<gif>` |

원본은 스킬 저장소의 `fonts/`, `plugin/skills/admaker/gallery/previews/`, `samples/`입니다. 원본을 바꾸면 여기에도 같은 경로로 복사합니다.
폰트 라이선스는 `fonts/README.md`와 각 라이선스 파일을 참고하세요.
