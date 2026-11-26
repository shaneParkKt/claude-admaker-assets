# 3D 모델 에셋 (GLB)

`templates/model3d.mjs`로 만든 GLB 20개와 [Poly Haven](https://polyhaven.com) 실사 스캔 모델 40개(CC0, 아래 두 번째 표)입니다. 광고에 **그대로 에셋으로** 넣거나(소품·아이콘·데모 제품), **레퍼런스·예제**로 spec을 복사해 색·라벨만 바꿔 다시 만듭니다. 목록·spec·미리보기는 `models.json`, 렌더 스틸은 `previews/<id>.jpg`.

- 그대로 쓰기 (스킬): `cp <admaker-3d 스킬>/assets/models/star.glb assets/` 후 `{ "type": "Adapter", "adapter": "three", "src": "assets/star.glb", "params": { "scene": "model", "spin": 40 } }`. `to-admaker-import.mjs`가 앱으로 넘길 때 data URL로 담습니다.
- 그대로 쓰기 (앱 MCP): `make_model3d { asset: "star" }` (크레딧 없음).
- 바꿔 만들기: `models.json`의 `spec`을 복사해 `color`·`label`만 바꾸고 `node <admaker-3d 스킬>/templates/make-model3d.mjs spec.json assets/<이름>.glb` (MCP는 `make_model3d`에 같은 값).
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

## Poly Haven 실사 모델 40종 (CC0)

[Poly Haven](https://polyhaven.com)에서 받은 사진 스캔 모델입니다. 모두 CC0라 상업 광고에 출처 표기 없이 써도 되지만, `models.json`의 `source`(URL·작가·라이선스)에 남겨 둡니다. 모양·재질은 바꾸지 않고 그대로 씁니다(라벨 교체 불가). 모든 면이 실제 스캔이라 `coverage`는 `full`입니다. 다시 받기: `node samples/model3d/external.mjs`.

| id | 모양 | 쓰는 곳 | 작가 · 주의 |
|---|---|---|---|
| `croissant` | 크루아상 | 베이커리·카페·브런치 | Greg Zaal, Dario Barresi |
| `carrot-cake` | 당근 케이크(홀) | 디저트·카페·기념일 | Greg Zaal, James Ray Cock |
| `strawberry-cake` | 딸기 초코 케이크 | 디저트·생일·시즌 메뉴 | Kuutti Siitonen |
| `apple` | 빨간 사과 | 과일·신선식품·건강 | Oliver Harries |
| `lemon` | 레몬 | 상큼함·음료·비타민 | Kuutti Siitonen |
| `avocado` | 아보카도(통) | 샐러드·건강식·식품 | Oliver Harries |
| `pomegranate` | 석류 | 과일·뷰티 성분·음료 | Oliver Harries |
| `kiwi` | 키위 | 과일·비타민·주스 | Oliver Harries |
| `cutting-board` | 나무 도마 | 요리·주방용품·푸드 받침 | Kuutti Siitonen |
| `wine-bottles` | 와인병 네 개 | 주류·레스토랑·파티 | Rico Cilliers, Jurita Burger | 주류 — 대상·매체 규정 확인
| `brass-goblets` | 황동 고블릿 잔 두 개 | 건배·축하·프리미엄 | Tina |
| `flower-jug` | 꽃무늬 도자기 주전자 | 우유·주방·홈카페 | Kuutti Siitonen |
| `film-camera` | 필름 카메라(스트랩) | 사진·여행·레트로 | Rajil Jose Macatangay |
| `retro-tv` | 브라운관 TV | 레트로·방송·화면 슬롯 | Gabriel Radić | 앞면에 실제 브랜드 글자(VTECH)가 보임 — 정면 클로즈업 피하기
| `boombox` | 붐박스 | 음악·오디오·레트로 이벤트 | Thomas Paul Mouilleron |
| `cassette-player` | 카세트 플레이어 | 레트로·녹음·추억 | Oday Abuzaeed | 앞면에 작은 제조사 글자가 보임 — 정면 클로즈업 피하기
| `video-camera` | 빈티지 영상 카메라 | 영상·촬영·영화제 | James Ray Cock, Jenelle van Heerden |
| `desk-lamp` | 주황 스탠드 | 공부·사무·조명 | Yann Kervran, Kuutti Siitonen |
| `pocket-watch` | 회중시계 | 시간·마감·클래식 | Tal Swicegood |
| `binoculars` | 쌍안경 | 탐색·발견·여행 | Derek Wight |
| `round-glasses` | 동그란 안경 | 안경·독서·지적인 느낌 | Sean Buckley |
| `rubber-duck` | 고무 오리 | 키즈·목욕·귀여운 마스코트 | Plat251 |
| `marble-bust` | 대리석 흉상 | 예술·미술관·고급스러움 | Rico Cilliers |
| `potted-plant` | 토분 화분 식물 | 인테리어·공간·친환경 | Rico Cilliers |
| `succulent` | 흰 화분 다육이 | 인테리어·책상·선물 | James Ray Cock |
| `cat-statue` | 고양이 석상 | 반려동물·장식·감성 | Rico Cilliers, Riley Queen |
| `treasure-chest` | 보물상자 | 보상·이벤트·랜덤박스 | Rico Cilliers |
| `suitcases` | 빈티지 여행가방 두 개 | 여행·휴가·이사 | Maximilian Schuster |
| `cardboard-box` | 택배 상자 | 배송·택배·언박싱 | Rahul Chaudhary |
| `lounge-chair` | 가죽 라운지 체어 | 가구·휴식·프리미엄 리빙 | Kuutti Siitonen |
| `arm-chair` | 원목 암체어 | 가구·북유럽 인테리어 | Vibrant Nordic |
| `sofa` | 클래식 소파 | 가구·거실·리빙 | Fran Calvente |
| `ukulele` | 우쿨렐레 | 음악·취미·여름 | Joseph Burgan |
| `chess-set` | 체스판 | 전략·두뇌·게임 | Riley Queen |
| `conch-shell` | 소라 껍데기 | 바다·여름·자연 소재 | Kuutti Siitonen |
| `baseball` | 야구공 | 야구·스포츠·응원 | Rico Cilliers |
| `rubber-boots` | 초록 장화 두 켤레 | 장마·아웃도어·농장 | L |
| `kr-payphone` | 한국 공중전화 | 레트로·연락·추억(한국) | UM JOORIN |
| `kr-fire-extinguisher` | 한국 소화기(받침대) | 안전·소방·캠페인(한국) | UM JOORIN |
| `garden-gnome` | 정원 난쟁이 인형 | 정원·키치·마스코트 | Bhargav Kubal |
