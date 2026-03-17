# 📚 Read & Lead
문학 작품을 따라 떠나는 테마 여행 & 문화 체험 플랫폼
  
> 책을 읽는 경험을, 도시를 걷는 경험으로 확장하다.
  
Read & Lead는 문학 작품을 출발점으로 여행지·여행 코스·문화 콘텐츠를 연결하는 문학 기반 테마 여행 & 공유 플랫폼입니다.  
  
사용자는 책 속 배경이 된 장소를 직접 방문하고, AI가 추천한 여행 계획을 따라 미션을 수행하며,  
자신만의 문학 여행 기록을 콘텐츠로 남길 수 있습니다.
  
<img width="1812" height="919" alt="image" src="https://github.com/user-attachments/assets/6e7a168c-1639-4716-88ba-d090066450bd" />
<br/>
<br/>

## 🧭 프로젝트 개요
- **팀명**: 오만과 통찰  
- **서비스명**: Read & Lead  
- **서비스 유형**: Web / App 서비스  
- **주요 키워드**: 문학 여행 · AI 여행 추천 · 공공데이터 활용 · 문화 관광 · 지역 브랜딩
<br/>
<br/>

## 🎯 기획 배경
- ‘텍스트힙’, 서울국제도서전 등으로 독서가 하나의 문화 트렌드로 확장  
- 문학 작품을 중심으로 한 배경지 방문 수요 증가  
- 지역 소멸 문제 속에서 기존 관광 콘텐츠의 한계 대두  
  
하지만 책의 배경과 실제 공간을 유기적으로 연결하는 서비스는 부족  
**Read & Lead**는 ```문학 → 공간 → 체험 → 공유```로 이어지는 새로운 문화 관광 모델을 제안합니다.
<br/>
<br/>

## ✨ 핵심 기능

### 1️⃣ 책으로 장소 찾기
- 도서명을 입력하면 작품의 배경이 된 장소를 지도에서 확인  
- 관광지·전시·공연·카페·핫플레이스 추천  
- 거리, 평점, 운영 여부 등 필터 제공  
  
<img width="1810" height="1010" alt="스크린샷 2026-01-21 002600" src="https://github.com/user-attachments/assets/68c79b48-8c9d-4659-9a41-b45e4cebb97e" />
<br/>

### 2️⃣ 장소로 책 찾기
- 여행하고 싶은 장소를 입력하면 해당 공간을 배경으로 한 문학 작품 추천  
- 문학을 몰라도 장소 중심으로 문학 탐색 가능
  
<img width="1812" height="1009" alt="image" src="https://github.com/user-attachments/assets/ef3d51ba-900d-4d76-9741-bbcf6597c9a5" />
<br/>

### 3️⃣ AI 여행 퀘스트북
- 책 제목, 인원, 기간, 여행 테마 입력 → AI 여행 일정 자동 생성  
- 일정별 미션 수행 → 배지 획득  
- 여행 일기 작성 및 사진 인증
  
<img width="1813" height="985" alt="image" src="https://github.com/user-attachments/assets/35973dcd-197e-420f-bf83-2863583df4e9" />  
<br/>

### 4️⃣ 인생네컷 문학 여행
- 여행 사진을 인생네컷 형식으로 자동 제작  
- 책 속 문장 / AI 추천 문장 / 직접 작성 문구 삽입  
- SNS 공유 및 다운로드
  
<img width="1816" height="1010" alt="스크린샷 2026-01-21 002627" src="https://github.com/user-attachments/assets/08431e88-f4f5-4d93-8c87-9b5e6b224eb5" />
<br/>

### 5️⃣ 관광사 연계 문학 여행
- 실제 관광사 연계 문학 여행 패키지 제공  
- 여행 상세 정보, 홈페이지 바로가기, 전화 연결  
<br/>

### 6️⃣ 이웃의 책 여행 따라가기
- 다른 사용자의 문학 여행 기록 열람  
- 댓글·소통 기능  
- 다른 사용자의 여행 루트 따라가기  
<br/>
<br/>

## 🧠 서비스 차별성
- **문학을 출발점으로 한 여행**  
  - 장소 중심이 아닌 책 중심 탐색 구조  

- **AI 기반 능동적 여행 경험**  
  - 퀘스트·미션 기반 여행  

- **책–도시 수집형 구조**  
  - 방문 기록을 배지로 수집하는 게이미피케이션  

- **여행을 콘텐츠로 전환**  
  - 사진 + 문장 + 지도 기반 SNS 공유  

- **확장성**  
  - 문학 → 영화·드라마·음식·역사 콘텐츠 확장  
<br/>
<br/>

## 🗺️ 활용 공공데이터 & API
- 한국관광공사 TourAPI  
- 국립중앙도서관 OPEN API (도서 메타데이터, 사서 추천)  
- KOPIS 공연정보 API  
- 한국문화정보원 문화정보 API  
- Kakao Map API  
- Google Maps / Google Books API  
- OpenAI API (ChatGPT) → AI 여행 계획 생성  
<br/>
<br/>

## 🏗️ 프로젝트 구조
```
Read & Lead
├─ react-frontend/                             # 프론트엔드 앱(React CRA)
│  ├─ public/
│  │  └─ index.html                            # 루트 HTML
│  ├─ src/
│  │  ├─ api/                                  # 외부 API 및 SDK 래퍼
│  │  │  ├─ config.ts                          # API 베이스/엔드포인트/공통 fetch
│  │  │  ├─ kakao.ts                           # Kakao JS SDK 로더·키워드/카테고리/지오코딩
│  │  │  ├─ googlePlaces.ts                    # (선택) 상세 보강: 사진/주소/평점
│  │  │  ├─ culture.ts                         # 문화포털 전시 프록시 클라이언트
│  │  │  ├─ kopis.ts                           # KOPIS 공연 프록시 클라이언트
│  │  │  ├─ directions.ts                      # 외부 길찾기 링크 유틸
│  │  │  ├─ auth.ts                            # 인증 API
│  │  │  ├─ neighbor.ts                        # 이웃글 API
│  │  │  ├─ diary.ts                           # 여행 일기 API
│  │  │  ├─ trips.ts                           # 여행/장소 저장·조회 API
│  │  │  ├─ stats.ts                           # 통계 API
│  │  │  └─ agency.ts                          # 제휴 여행상품 API
│  │  ├─ components/
│  │  │  ├─ common/
│  │  │  │  └─ AutocompleteInput.tsx           # 재사용 자동완성 입력
│  │  │  ├─ discovery/
│  │  │  │  ├─ DiscoveryPanelKakao.tsx         # 추천 패널
│  │  │  │  ├─ useKakaoMarkers.ts              # 카카오 마커 그룹 관리
│  │  │  │  └─ useMarkers.ts                   # 범용 마커 훅
│  │  │  ├─ map/
│  │  │  │  └─ KakaoMap.tsx                    # Kakao 지도 컨테이너
│  │  │  ├─ routes/
│  │  │  │  ├─ RoutePlannerDialog.tsx          # 경로 계획 다이얼로그
│  │  │  │  └─ RouteSidebar.tsx                # 경유지 사이드바
│  │  │  └─ diary/
│  │  │     ├─ TravelDiaryTab.tsx              # 일기 탭
│  │  │     ├─ DiaryTimeline.tsx               # 타임라인
│  │  │     ├─ DiaryComposer.tsx               # 일기 작성
│  │  │     └─ DiaryEntryCard.tsx              # 일기 카드
│  │  ├─ data/
│  │  │  ├─ book_location_event.json           # 도서 → 장소/이벤트 매핑
│  │  │  └─ neighbor_posts.json                # 이웃글 샘플
│  │  ├─ pages/
│  │  │  ├─ LocationMap.tsx                    # 책 검색 + 지도 + 패널
│  │  │  ├─ Home.tsx
│  │  │  ├─ Neighbors.tsx
│  │  │  ├─ NeighborPost.tsx
│  │  │  ├─ NeighborCompose.tsx
│  │  │  ├─ TravelDiary.tsx
│  │  │  ├─ DiaryTripPage.tsx
│  │  │  ├─ MyTrips.tsx
│  │  │  ├─ AgencyTrips.tsx
│  │  │  ├─ AgencyTripDetail.tsx
│  │  │  ├─ BookTripPage.tsx
│  │  │  ├─ BookTripDetailPage.tsx
│  │  │  ├─ PlaceToBook.tsx
│  │  │  ├─ FourCutCreator.tsx
│  │  │  └─ OAuthPopupCallback.tsx
│  │  ├─ hooks/useStops.ts
│  │  ├─ lib/utils.ts
│  │  ├─ utils/canvas.ts
│  │  ├─ types/kakao.d.ts
│  │  ├─ types/json.d.ts
│  │  ├─ styles/GlobalStyle.ts
│  │  ├─ App.tsx
│  │  ├─ index.tsx
│  │  ├─ App.css
│  │  ├─ index.css
│  │  ├─ setupTests.ts
│  │  └─ reportWebVitals.ts
│  ├─ public/manifest.json
│  ├─ package.json
│  └─ tsconfig.json
│
├─ server/                                     # 백엔드 앱(FastAPI)
│  ├─ app/
│  │  ├─ main.py
│  │  ├─ database.py
│  │  ├─ models.py
│  │  ├─ schemas.py
│  │  ├─ security.py
│  │  ├─ deps.py
│  │  ├─ db.sqlite3
│  │  ├─ routers/
│  │  │  ├─ auth.py
│  │  │  ├─ posts.py
│  │  │  ├─ stats.py
│  │  │  ├─ culture.py
│  │  │  ├─ kopis.py
│  │  │  ├─ uploads.py
│  │  │  ├─ agency_trips.py
│  │  │  └─ trips.py
│  │  └─ static/
│  ├─ requirements.txt
│  ├─ run_gunicorn.sh
│  ├─ deploy/
│  │  ├─ nginx-api.conf.example
│  │  └─ systemd/readandlead-api.service.example
│  └─ .env
│
├─ data/
│  ├─ book_location_event.json
│  └─ book_metadata_kakao.json
│
├─ scripts/
│  ├─ book_metadata_collector.py
│  └─ delete_posts_by_title.py
│
├─ docs/
│  └─ ANDROID_RELEASE.md
│
├─ .gitignore
└─ README.md
```
<br/>
<br/>
