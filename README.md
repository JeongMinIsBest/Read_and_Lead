# 📚 Read & Lead
A Theme-Based Travel & Cultural Experience Platform Inspired by Literary Works
  
> Expanding the experience of reading books into the experience of walking through cities.
  
Read & Lead is a literature-based theme travel and sharing platform that connects literary works with travel destinations, travel routes, and cultural content.  
Users can directly visit places that serve as the background of books, complete missions by following AI-recommended travel plans,  
and turn their own literary travel experiences into shareable content.
  
<img width="1812" height="919" alt="image" src="https://github.com/user-attachments/assets/6e7a168c-1639-4716-88ba-d090066450bd" />
<br/>
<br/>

## 🧭 Project Overview
- **Team Name**: Oman's Insight  
- **Service Name**: Read & Lead  
- **Service Type**: Web / App Service  
  
**Key Keywords**  
Literary Travel · AI Travel Recommendation · Public Data Utilization · Cultural Tourism · Regional Branding
<br/>
<br/>

## 🎯 Background & Motivation
- Reading has expanded into a cultural trend through movements such as *Text Hip* and events like the *Seoul International Book Fair*.  
- Demand for visiting locations that serve as the background of literary works has increased.  
- Amid issues of regional decline, the limitations of existing tourism content have become apparent.
  
However, services that organically connect the background of books with real physical spaces remain insufficient.
Read & Lead proposes a new cultural tourism model that follows the flow: ```Literature → Space → Experience → Sharing```
<br/>
<br/>

## ✨ Core Features

### 1️⃣ Find Places by Book
- Enter a book title to view locations that serve as the background of the work on a map.  
- Recommendations for nearby tourist attractions, exhibitions, performances, cafés, and hot spots.  
- Filters such as distance, ratings, and operating status are provided.

<img width="1810" height="1010" alt="스크린샷 2026-01-21 002600" src="https://github.com/user-attachments/assets/68c79b48-8c9d-4659-9a41-b45e4cebb97e" />
<br/>

### 2️⃣ Find Books by Place
- Enter a place you want to visit to receive recommendations for literary works set in that location.  
- Enables exploration of literature from a place-centered perspective, even without prior literary knowledge.

<img width="1812" height="1009" alt="image" src="https://github.com/user-attachments/assets/ef3d51ba-900d-4d76-9741-bbcf6597c9a5" />
<br/>

### 3️⃣ AI Travel Questbook
- Enter the book title, number of travelers, duration, and travel theme to automatically generate a literature-based travel itinerary using AI.  
- Complete missions for each itinerary to earn badges.  
- Travel diary writing and photo-based mission verification are supported.

<img width="1813" height="985" alt="image" src="https://github.com/user-attachments/assets/35973dcd-197e-420f-bf83-2863583df4e9" />  
<br/>

### 4️⃣ Four-Cut Literary Travel
- Automatically creates four-cut photo content using travel photos.  
- Insert sentences from books, AI-recommended quotes, or user-written text.  
- Supports SNS sharing and downloads.
  
<img width="1816" height="1010" alt="스크린샷 2026-01-21 002627" src="https://github.com/user-attachments/assets/08431e88-f4f5-4d93-8c87-9b5e6b224eb5" />
<br/>

### 5️⃣ Literary Travel with Partnered Travel Agencies
- Provides literary travel packages in partnership with real travel agencies.  
- Offers detailed travel information, direct links to agency websites, and phone call connections.
<br/>

### 6️⃣ Follow Your Neighbors’ Book Travels
- View other users’ literary travel records in a blog-style format.  
- Comment and communicate with other users.  
- Follow and replicate other users’ travel routes.
<br/>
<br/>

## 🧠 Service Differentiation

- **Travel Starting from Literature**  
  - A book-centered exploration structure rather than a place-centered one.

- **AI-Based Active Travel Experience**  
  - Quest- and mission-based travel beyond simple recommendations.

- **Book–City Collection Structure**  
  - Gamification through collecting visit records as badges.

- **Transforming Travel into Content**  
  - SNS sharing based on photos, sentences, and maps.

- **Scalability**  
  - Expandable from literature to films, dramas, food, and historical content.
<br/>
<br/>

## 🗺️ Public Data & APIs Utilized

- Korea Tourism Organization TourAPI  
- National Library of Korea OPEN API (Book metadata, librarian recommendations)  
- KOPIS Performance Information API  
- Korea Culture Information Service API  
- Kakao Map API  
- Google Maps / Google Books API  
- OpenAI API (ChatGPT) → AI travel plan generation
<br/>
<br/>

## 🏗️ Project Structure
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
