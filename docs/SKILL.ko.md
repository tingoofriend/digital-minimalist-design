# Digital Minimalist 디자인 가이드 (한국어판)

> 영어판 [`skills/digital-minimalist-design/SKILL.md`](../skills/digital-minimalist-design/SKILL.md)이 기준 문서이고, 이 문서는 같은 내용의 한국어판입니다. 한국어로 스킬을 쓰고 싶다면 이 파일 맨 위에 영어판과 같은 frontmatter를 붙여 `SKILL.md`로 저장하세요.

출처: Digital Minimalist 블로그(digitalminimalist.com)의 앱 큐레이션 162개 글 전체(텍스트 전수 + 이미지 약 815장 비전 분석 + 대표 화면 픽셀 실측). 해당 블로그나 여기 언급된 앱과는 제휴 관계가 없으며, 앱 이름은 스타일 참고용으로만 인용합니다.
핵심 레퍼런스 앱: Weeklist, Life Dots, Mononote, Did I Do, Thoughts, Neuecast, Clear, MinimaList, Twodos, SyncTasks, Dumb Phone, Blank Spaces, Before Launcher, Lazy Weather, The Radio, Lettera, iA Writer, Matter, Instapaper, Endel, One Sec, Onigiri, One Thing, Ice, LookAway, Fliqlo, Mudita Kompakt(e-ink).

## 1. 핵심 철학 (모든 결정의 기준)

1. **한 가지 일만 한다.** 앱 = 하나의 목적. 기능은 더하기보다 뺀다.
2. **기술은 배경에 머문다.** 주의를 끌지 않는다. 컬러, 배지, 알림 점, 추천 피드, 무한 스크롤 금지.
3. **열지 않아도 되게.** 핵심 정보는 위젯·잠금화면·Live Activity·Dynamic Island·메뉴바에서 보이고, 탭 한 번으로 끝난다.
4. **조용함 > 자극.** 색과 장식은 '자극'이다. 회색조는 의도적 선택.
5. **텍스트가 주인공.** 아이콘·썸네일·아트워크보다 텍스트 라벨이 우선.
6. **숨겨서 정리한다.** 고급 기능은 제스처·길게 누르기·`···` 메뉴 뒤로.
7. **좋은 마찰은 허용.** 중독성 행동 앞에 의도적 한 단계(대기·심호흡·확인).
8. **프라이버시·무계정.** 가입 없이 사용, 데이터는 기기에만, 광고 없음 — 문구로도 밝힌다.

## 2. 컬러 (실측 기반)

| 토큰 | Light | Dark | 근거 |
|---|---|---|---|
| bg | `#F7F7F7` (대안 `#F4F4F4`) | `#000000` | Weeklist 앱 배경 실측 L=247 / 블로그 권장 홈 배경 #F4F4F4 |
| surface | `#FFFFFF` | `#1C1C1E` | 위젯·카드 |
| text | `#000000`~`#111111` | `#FFFFFF` | |
| text-2 | `#808080` | `#8E8E93` | 날짜·메타·카운트 (실측 코어 L≈127–134) |
| text-3 | `#BBBBBB` | `#48484A` | 체크박스 테두리, "할 일 추가", 완료 항목 (실측 L≈186–193) |
| divider | `#E2E2E2` 1px | `#2C2C2E` | 실측 L=226 |
| accent | **없음** — 강조는 검정(라이트)/흰색(다크) |

- 다크 모드 기본은 **완전한 검정 #000** (잠금화면·OLED와 이어짐). 다크 카드는 #1C1C1E.
- **허용되는 예외 (앱당 하나만)**
  - *따뜻한 종이 톤*: 크림 배경 `#F2EDE3` 근처 + 세리프. 읽기·학습·단어 앱(Vocabulary, Art of Fauna, Spark).
  - *원 포인트 컬러*: 화면에 요소 하나만 컬러(Zerocam의 노란 셔터 pill, Opal의 오브). 나머지는 전부 흑백.
  - *데이터 신호색*: 아주 작은 숫자에만 녹/적(Ratio 메뉴바의 +/− 퍼센트).
- 그라데이션 금지. 예외: 아이콘의 은은한 흑→회, 개입 화면 하단의 회색 그라데이션 패널(One Sec).

## 3. 타이포그래피 (실측 기반, 393pt 폭 iPhone 기준)

시스템 산세리프(SF Pro / Inter / 한국어 Pretendard). 위계는 **크기와 굵기 대비만으로** 만든다.

| 역할 | 크기·굵기 | 실측 근거 |
|---|---|---|
| 디스플레이 숫자 | 56–96pt, Bold~Black 또는 Ultralight | 위젯 날짜 "07", 타이머 "24:53", 개입 화면 "4" |
| 콘텐츠 타이틀 (플레이어·읽기) | **40–44pt Bold, 행간 1.2** | Neuecast 에피소드 제목 ≈44pt, 행 피치 52pt |
| 텍스트 런처 앱 이름 | 28–34pt Regular/Medium, 행 피치 ≈1.7× | Dumb Phone 대형 ≈34pt, 피치 ≈58pt |
| Large Title | 34pt Bold | "Inbox", "Tasks", "My Lists" |
| 섹션/날짜 헤더 | **20pt Semibold** + 같은 크기 회색 보조 | Weeklist "**Mon** 5 Oct" 캡하이트 실측 → 20pt |
| 텍스트 전용 리스트 행 | 17pt Regular, 행 피치 40pt | MinimaList |
| 체크 리스트 행 제목 | **15pt Regular** | Weeklist 항목 |
| 메타 | **12pt, text-2** | Weeklist "Work · 8:00 PM" |
| 위젯 제목 / 카운트 | 15pt Bold / 15pt text-2 | Weeklist 위젯 "Monday 3" |
| 위젯 항목 | 13pt | Weeklist 위젯 |
| 위젯 큰 답 | 36–40pt Black | Did I Do "YES/NO" (158pt 위젯 기준) |

- 한 화면 굵기 2–3단계 이하. 숫자는 tabular figures.
- **개성 서체 옵션 (앱 하나에 하나만)**
  - 세리프: 읽기 본문(Instapaper·Matter), 단어 앱, 그리고 **잠금화면 시계**(New York 계열 "7:33"이 미니멀 셋업에서 자주 등장).
  - 모노스페이스: Lazy Weather, iA Writer, Ratio 메뉴바 표.
  - 픽셀: Weather Terminal.
- 텍스트 런처는 **소문자 표기**("messages photos safari")도 자주 쓰인다. 왼쪽 정렬과 가운데 정렬 모두 등장한다.

## 4. 레이아웃 & 간격 (실측 기반)

- 화면 좌우 여백: **20pt** (리스트), 22pt (읽기·플레이어), 런처 30–38pt.
- 리스트: 단일 컬럼, 좌측 정렬, 아이콘 없음.
  - 체크 행: 원형 체크박스 **20pt**(1.5pt 테두리, text-3) → 텍스트 시작 x=58pt(박스 오른쪽 14pt 간격).
  - 제목+메타 2줄 행 피치 **≈59pt**, 1줄 행 **56pt**, 텍스트 전용 행 40pt.
  - 구분선은 1px #E2E2E2, 텍스트 시작선부터 오른쪽 끝까지.
  - 완료: **취소선 + text-3**으로 남김(삭제하지 않음).
  - 섹션 끝에 회색 "Add reminder/할 일 추가" 행 하나.
  - 카운트는 행 오른쪽에 회색 숫자 + 얇은 chevron (`3 ›`).
- 상단 바: 원형 버튼 **44pt**(아이콘 하나) 좌우 + 가운데 짧은 제목. 또는 Large Title.
- 하단: 왼쪽 ← → pill, 오른쪽 원형 `+`(검정 또는 글래스) **44–56pt**. 탭바는 꼭 필요할 때만.
- 화면 대부분을 비운다. 콘텐츠는 위쪽 또는 중앙에 소수만.

### 위젯 (iOS)
- 크기는 시스템 그대로: small 158pt, 간격 20pt(393pt 폭 기준).
- 안쪽 패딩 16pt, 모서리 22pt(시스템). 제목 15pt Bold + 우측 회색 카운트, 항목 13pt, 체크박스 17pt, 항목 피치 ≈25pt.
- **위젯 배경 = 홈 배경색**으로 맞춰 "글씨만 떠 있는" 효과(SyncTasks, Dumb Phone).
- 타일형 위젯: 좌상단 작은 라인 아이콘 + 좌하단 라벨("Reading List") — Notion 페이지 위젯 스타일.

## 5. 형태·아이콘
- 카드/위젯 모서리 20–24pt(continuous), 버튼은 pill 또는 원형. 그림자는 거의 없음 — 배경색 차이로 경계를 만든다.
- 반복 모티프: **점 그리드**(Life Dots: 채움=흑/백, 남음=옅은 회색, 헤더 "Year 67%"), 얇은 원형 링 타이머, 진행 바, 눈금(The Radio).
- UI 아이콘: 1.5–2pt 라인. 텍스트로 대체 가능하면 대체한다.
- 앱 아이콘: 흰색 또는 검정 타일 + 단일 흑백 심볼(점 세 개, 접힌 종이, ↑↓, 워드마크 "Dumb Phone°"). 은은한 흑회 그라데이션·광택은 허용.
- 커스텀 아이콘 팩 스타일: **두꺼운 검정 외곽선의 둥근 글리프**(Notion-style), 다크 모드는 반전. 폴더는 옅은 회색 폴더 + 회색 라인 글리프.
- 일러스트가 필요하면: 연회색 배경 위 **둥근 단색 검정 글리프**(블로그 히어로 스타일). 사람·장면 일러스트는 피한다(예외: Clutter의 단색 라인 드로잉 하나).
- 태그/칩: 검정 둥근 사각 + 흰 텍스트(다크 칩), 또는 1px 테두리 pill.

## 6. 반복 컴포넌트 패턴
- **텍스트 런처**: 큰 텍스트 앱 이름 세로 목록, 위에 날짜(얇은 원형 시계 또는 "Tuesday / June 2"). 검정 또는 흰 배경.
- **큰 숫자 위젯**: 질문 한 줄(15pt Bold) + 답 하나(Black, 위젯 높이의 ≈25%) + 작은 타임스탬프 (Did I Do).
- **날짜 위젯**: "Thu **Nov**"(요일 검정, 월 회색) + 거대한 "07".
- **진행률 점 위젯**: "Day 46%" 헤더 + 점 그리드.
- **하나의 노트**: 화면 전체가 텍스트 영역 + 하단 검정 "Done" pill (Mononote).
- **주간 뷰**: 요일별 접히는 섹션 (Weeklist).
- **포커스 모드**: 검정 배경, 가운데 할 일 하나(Bold 흰색) + 하단 작은 타이머 (Twodos/MinimaList). 또는 얇은 링 + 큰 숫자 (Endel, ScreenFast).
- **개입(마찰) 화면**: 가운데 잠깐 멈추자는 한 문장 → 다음 화면에 큰 숫자("4번째 시도") + 흰 pill 버튼 하나 + 텍스트 링크 하나 (One Sec).
- **텍스트 우선 플레이어**: 아트워크 대신 40–44pt Bold 제목, 얇은 진행 바, 작은 컨트롤 (Neuecast).
- **읽기 화면**: 세리프 본문, 행간 1.6–1.7, 60–70자 폭. iA Writer식 포커스 모드(현재 문장 외 회색 처리)도 가능.
- **메뉴바 앱(macOS)**: 아이콘 하나 또는 짧은 텍스트("24:53"). 클릭하면 작은 흰 팝오버(큰 숫자 하나 + pill 선택지).
- **설정 화면**: 시스템 기본 그룹 리스트 그대로. 토글만, 장식 없음.

## 7. 플랫폼별
- **iOS**: SwiftUI 기본 컴포넌트를 그대로 쓰고 색만 걷어낸다(`.tint(.primary)`). 위젯·Live Activity·Dynamic Island를 1급으로 설계. iOS 26+ Liquid Glass는 'Tinted/Clear' 쪽으로 절제해서 쓴다.
- **Android**: Material 3, dynamic color 끄고 모노크롬. 엘리베이션 0. 런처식 텍스트 리스트.
- **Web**: 단일 컬럼 640–720px, 시스템 폰트, 검정 pill CTA 하나. 헤더는 워드마크 + 링크 2–3개.
- **macOS**: 메뉴바 상주, 작은 플로팅 창(신호등 버튼만), 액센트 Graphite, Finder식 단순 리스트.
- **e-ink/저자극 모드**: 순수 흑백, 테두리 라인 아이콘을 둥근 사각 안에, 두꺼운 1.5–2pt 외곽선(Mudita Kompakt).

## 8. 카피 톤
- 짧은 평서문, 2인칭. 예: "이번 주를 정리하고 휴대폰은 내려놓으세요." "오늘 스트레칭 했나요?" "먼저 숨 한 번 쉬어요."
- 느낌표·이모지·과장 마케팅 문구 금지. 빈 상태는 조용한 한 문장 + 버튼 하나.

## 9. 하지 말 것
- [ ] 액센트 2개 이상, 컬러 카테고리 태그
- [ ] 빨간 배지, 스트릭 불꽃, 리더보드
- [ ] 중첩 카드, 짙은 그림자, 글래스 과용
- [ ] 아이콘+텍스트 중복 라벨, 장식 일러스트
- [ ] 화면당 주요 버튼 2개 이상
- [ ] 무한 피드, 추천, 자동 재생
- [ ] 가입 강제 온보딩, 3단계 이상 튜토리얼

## 10. 작업 절차
1. 이 앱이 하는 **단 하나의 일**을 한 문장으로 적는다.
2. 앱을 열지 않고 끝나는 표면(위젯·잠금화면·메뉴바)을 먼저 설계한다.
3. 메인 화면은 텍스트 리스트 또는 큰 숫자 하나로 시작해서 3–4장의 수치를 적용한다.
4. 색 없이 위계를 완성한 뒤, 필요할 때만 회색 단계나 예외 액센트 하나를 더한다.
5. 9장 체크리스트로 점검하고, 요소 하나를 더 뺄 수 있는지 마지막으로 묻는다.
6. 목업은 렌더링해서 **잘림·넘침·겹침을 확인**한다(컨테이너 밖으로 나간 요소, 마지막 행 잘림, 한국어 단어 중간 줄바꿈 — `word-break: keep-all`).

## 11. CSS 시작 토큰 (웹/목업)
```css
:root{
  --bg:#F7F7F7; --surface:#FFF; --text:#000; --text-2:#808080; --text-3:#BBBBBB; --line:#E2E2E2;
  --margin:20px; --row:56px; --row2:59px; --check:20px; --btn:44px; --radius-card:22px;
  --font:-apple-system,BlinkMacSystemFont,"SF Pro Text","Inter","Pretendard",system-ui,sans-serif;
  --serif:"New York","Iowan Old Style",Georgia,serif; --mono:"SF Mono",ui-monospace,Menlo,monospace;
  --t-display:64px; --t-title:34px; --t-header:20px; --t-body:17px; --t-row:15px; --t-meta:12px;
}
@media (prefers-color-scheme:dark){:root{--bg:#000;--surface:#1C1C1E;--text:#FFF;--text-2:#8E8E93;--text-3:#48484A;--line:#2C2C2E}}
body{background:var(--bg);color:var(--text);font:400 var(--t-row)/1.35 var(--font);-webkit-font-smoothing:antialiased}
.btn{background:var(--text);color:var(--bg);border-radius:999px;padding:12px 20px;font-weight:600;border:0}
.check{width:var(--check);height:var(--check);border:1.5px solid var(--text-3);border-radius:50%}
.done{color:var(--text-3);text-decoration:line-through}
```
