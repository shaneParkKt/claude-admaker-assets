# 3D 모델 에셋 (GLB)

`templates/model3d.mjs`로 만든 GLB 20개입니다. 광고에 **그대로 에셋으로** 넣거나(소품·아이콘·데모 제품), **레퍼런스·예제**로 spec을 복사해 색·라벨만 바꿔 다시 만듭니다. 목록·spec·미리보기는 `models.json`, 렌더 스틸은 `previews/<id>.jpg`.

- 그대로 쓰기 (스킬): `cp <스킬>/assets/models/star.glb assets/` 후 `{ "type": "Adapter", "adapter": "three", "src": "assets/star.glb", "params": { "scene": "model", "spin": 40 } }`. `to-admaker-import.mjs`가 앱으로 넘길 때 data URL로 담습니다.
- 그대로 쓰기 (앱 MCP): `make_model3d { asset: "star" }` (크레딧 없음).
- 바꿔 만들기: `models.json`의 `spec`을 복사해 `color`·`label`만 바꾸고 `node <스킬>/templates/make-model3d.mjs spec.json assets/<이름>.glb` (MCP는 `make_model3d`에 같은 값).
- 실제 브랜드 제품처럼 보이면 안 되는 자리(라벨 `FIZZ`, `BOX`, `P`, 화면 그림은 예시)에는 라벨을 사용자 것으로 바꿔 씁니다.

| id | 모양 | 쓰는 곳 |
|---|---|---|
| `fizz-can` | 음료 캔(라벨 그림) | 탄산·맥주·에너지 음료 히어로, 라벨 교체 예시 |
| `green-bottle` | 유리병 + 내용물 + 라벨 | 음료·소스·주류 병 |
| `cream-jar` | 뚜껑 용기 | 크림·잼·영양제 통 |
| `coffee-cup` | 테이크아웃 컵 | 커피·음료 컵(슬리브 색) |
| `pink-tube` | 원통 스틱(금 캡) | 립밤·립스틱·스틱 화장품 |
| `package-box` | 상자(앞면 그림) | 제품 상자·패키지·책 |
| `phone` | 스마트폰(화면 = screen 메시) | 앱 광고, 화면에 영상 재생(screenSlot) |
| `point-coin` | 금 동전(앞면 그림) | 포인트·적립·쿠폰 보상 |
| `blue-gem` | 보석 | 프리미엄·VIP·보상 아이콘 |
| `pill-capsule` | 알약 캡슐(두 색) | 영양제·약 |
| `candy-sphere` | 광택 공 | 버블·공·추상 오브젝트 |
| `donut` | 도넛·링 | 디저트·반지·튜브 |
| `star` | 입체 별(베벨) | 평점·혜택 강조 |
| `heart` | 입체 하트(베벨) | 좋아요·감성·선물 |
| `hex-badge` | 크롬 육각 배지 | 배지·인증 아이콘 |
| `frosted-bottle` | 젖빛 병(금 캡) | 향수·화장수·프리미엄 병 |
| `neon-bolt` | 네온 번개(직접 그린 외곽선) | 에너지·속도·번쩍 강조 |
| `glass-bottle` | 투명 유리병(밑 소재가 비침) | 음료·주스·소주 병 |
| `gold-star6` | 육각 금별 | 보상·랭킹·이벤트 |
| `black-card` | 검은 카드(직접 조립) | 카드·멤버십·결제 |

다시 만들기: 저장소 루트에서 `node samples/model3d/build.mjs` (spec은 `samples/model3d/specs.json`, 라벨 그림은 `samples/model3d/labels/`).
