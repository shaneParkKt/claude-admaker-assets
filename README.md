# claude-admaker-assets

admaker 스킬(비공개 저장소)이 공개 URL로 참조하는 파일만 모아 둔 공개 저장소입니다. 스킬 코드·문서는 여기에 두지 않습니다.

| 폴더 | 내용 | 참조하는 곳 |
|---|---|---|
| `fonts/` | 공개 CDN이 없는 폰트 사본 + 각 라이선스 파일 | 스킬 `references/fonts.json`의 `url` (렌더 하니스) — `https://cdn.jsdelivr.net/gh/shaneParkKt/claude-admaker-assets@main/fonts/<파일명>` |
| `gallery/previews/` | 예시 갤러리 미리보기 webp | 스킬 `gallery/data/ads.json`의 `preview_url` (앱 MCP 갤러리) — `https://raw.githubusercontent.com/shaneParkKt/claude-admaker-assets/main/gallery/previews/<slug>.webp` |
| `samples/` | 샘플 렌더 결과(gif·png·jpg) | 스킬 `gallery/prompts/*.md` 미리보기 링크 |
| `models/` | 3D 모델 GLB 20개 + `models.json` + 미리보기 | 참고·다운로드용 (스킬·앱에는 같은 파일이 들어 있음) |

## 파일 추가·갱신

스킬 저장소에서 미리보기·샘플·폰트를 새로 만들면 같은 경로로 이 저장소에도 넣습니다. 파일명은 스킬 쪽 경로와 맞춥니다(`fonts/`는 admaker 앱 `public/fonts/` 파일명과 같아야 합니다).

jsDelivr는 `@main` 브랜치를 최대 12시간 캐시합니다. 바로 반영해야 하면 `https://purge.jsdelivr.net/gh/shaneParkKt/claude-admaker-assets@main/<경로>`를 엽니다.

## 라이선스

- `fonts/`: 각 폰트의 원 라이선스를 따릅니다(같은 폴더의 `*-OFL.txt`, `*-LICENSE.txt`, `fonts/README.md`). 폰트 단독 판매는 금지입니다.
- 그 밖의 파일(미리보기·샘플 렌더·3D 모델): Copyright (c) 2026 kingsae1 (ShanePark). 보기용으로 공개합니다. 별도 허락 없이 다른 제품·서비스에 재배포할 수 없습니다.
