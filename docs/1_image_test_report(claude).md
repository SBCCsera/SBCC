Autopsy- MCP-Claude 기반 AI 디지털 포렌식 질의응답 성능 평가  
Magnet AXIOM CTF 이미지 기반

1. **실험 개요**  
   **1.1 실험 목적**  
   Autopsy에 적재한 Magnet AXIOM CTF 이미지를 MCP를 통해 Claude Desktop에 연결하고, Claude가 Autopsy의 포렌식 데이터를 바탕으로 CTF 질문에 정확하게 답변할 수 있는지 평가한다.   
     
   **1.2 실험 환경**

| 분석 도구 | Autopsy 4.23.1 |
| :---: | :---: |
| AI Agent | Claude Desktop 2.16120.0 / Opus5.5 |
| 연결 방식 | MCP |
| 이미지 출처 | Magnet Forensics AXIOM CTF |

   

   **1.3 실험 절차**

   ① Magnet AXIOM CTF 이미지를 다운받아 Autopsy에 적재한다. 

   ② Autopsy에서 분석 가능한 아티팩트와 데이터가 정상적으로 표시되는지 확인한다. 

   ③ Autopsy MCP 서버를 활성화하고 Claude Desktop과 연결한다. 

   ④ 공개된 CTF 질문을 선정해 Claude에 입력한다. 

   ⑤ 동일한 이미지와 동일한 문항을 실행자 3명이 각각 수행한다. 

   ⑥ Claude의 답변과 Autopsy에서 확인한 실제 정답을 비교한다. 

   ⑦ 오답이 발생한 경우 각 실행자가 독립적으로 오답 유형을 라벨링한다. 

   ⑧ 전체 실험 후 개별 라벨을 비교하고, 오류 발생 원인을 기준으로 최종 오답 유형을 통합한다. 

   

   **1.4 정답 판정 기준**

   CTF에서 제시된 공식 정답 또는 Autopsy의 원본 데이터에서 직접 확인 가능한 값을 정답으로 판정한다. 

**1.5 CTF 이미지 목록**

| 2026 |  |  |
| :---: | :---: | :---: |
| **이미지 명** | **이미지 다운 링크** | **문제 링크** |
| Android | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFAndroid | https\://www\.hexordia.com/blog/magnet-virtual-summit-2026-ctf-android-questions |
| iOS | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFiOS | https\://www\.hexordia.com/blog/magnet-virtual-summit-2026-ctf-ios-questions |
| macOS | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFMac | https\://www\.hexordia.com/blog/magnet-virtual-summit-2026-ctf-mac-questions |
| **2025** |  |  |
| **이미지 명** | **이미지 다운 링크** | **문제 링크** |
| WIndows | https\://drive.google.com/drive/u/0/mobile/folders/1gHQsfx1hqCv-V4Anm2eYukB4jPtraNBH?usp=drive\_link  | https\://www\.hexordia.com/blog/ctf-windows |
| Chromebook |  | https\://www\.hexordia.com/blog/ctf-chromebook |
| iOS |  | https\://www\.hexordia.com/blog/ctf-ios |
| Android |  | https\://www\.hexordia.com/blog/ctf-android |

**2\. 2026 CTF 이미지\_SamsungA53**

**이미지 기본 정보**

| 이미지명 | SamsungA53 |
| :---: | :---: |
| 연도 | 2026 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 36.4GB |
| 출처 | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFAndroid |
| Autopsy Case명 | 26\_samsungA53 |
| 대상 OS | Window 11 |
| 문항 수  | 14 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 001 | 99 Restaurant | 99 Restaurants | 99 Restaurant | T |
| 002 | 2025-12-15 18:07:05 | 2025-12-15 18:07:01 | 2025-12-15 18:07:01 UTC | F(0%) |
| 003 | Saudi Arabia | Saudi Arabia | Saudi Arabia | T |
| 004 | IP67 | \- | \- | F(0%) |
| 005 | COLIC | COLIC | CIGAR | F(66%) |
| 006 | Hidden Gems | \- | Alex Maurie  | F(33%) |
| 007 | 13 (OTHER KILLS BY SYSTEM) | 13(“other”, a kill by the system) | 13, “Other kills by system”  | T |
| 008 | com.ss.android.ugc.aweme.splash.SplashActivity | com.ss.android.ugc.aweme.splash.SplashActivity | com.ss.android.ugc.aweme.splash.SplashActivity  | T |
| 009 | MOCKS | MOCKS | MOCKS | T |
| 010 | 83 | 83 | 83 | F(66%) |
| 011 | \#262626 | \- | \#262626 | F(66%) |
| 012 | 5254 | \- | \- | F(33%) |
| 013 | 2025-11-10 18:11:26 **OR** 2025-11-10 18:11:25 | 2025-11-10 18:11:14 | 2025-11-10 18:11:14 | F(33%) |
| 014 | com.google.android.youtube | com.google.android.youtube | com.google.android.youtube | T |

| NO | Question |
| :---: | ----- |
| 001 | What is the name of the establishment the user took a screenshot of? |
| 002 | What was the last time in UTC Clash Of Clans was closed? (Format: YYYY-MM-DD HH:MM:SS |
| 003 | What country was the other party from for a rejected/declined call? |
| 004 | What is the Ingress rating of the security camera that supports night vision? |
| 005 | What was the answer to the first Wordle puzzle solved? |
| 006 | What is the name of the client the user was most recently working on? |
| 007 | What was the reason the Nike app was last exited? |
| 008 | What class had the most badges? |
| 009 | What was the second guess on the first Wordle the user played? |
| 010 | How many emails were automatically labeled as notifications? |
| 011 | What is the hex code of the content color for the entry that expires on 2025-12-01 15:06:45? |
| 012 | What was the PID of the app that was in focus at 2025-12-15 17:48:09? |
| 013 | When in UTC was the timezone set? (YYYY-MM-DD HH:MM:SS) |
| 014 | What was the top package name in a splitscreen shortcut? |

**2.1 2026 CTF 이미지\_SamsungA53**

**이미지 기본 정보**

| 이미지명 | SamsungA53 |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_samsungA53 |
| 문항 수  | 14 |
| 실험자 | 박제윤 |
| 정답률 | 8/14(57%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 DB/아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 001 | 99 Restaurant | 99 Restaurants | T | /data/media/0/DCIM/Screenshots/Screenshot\_20251209\_153814\_Chrome.jpg,TSK\_WEB\_HISTORY  |
| **002** | **2025-12-15 18:07:05** | **2025-12-15 18:07:01** | **F(3)** | **shared\_prefs/appsflyer-data.xml** |
| 003 | Saudi Arabia | Saudi Arabia | T | calllog.db-wal, Android geocoded\_location |
| **004** | **IP67** | **\-** | **F(3)** | **Chrome History** |
| 005 | COLIC | COLIC | T | app\_webview/Default/Local Storage/leveldb, 000017.ldb |
| **006** | **Hidden Gems** | **\-** | **F(3)** | **files/stashes/1a1869603c5aae099881926a44fc747e/DB** |
| 007 | 13 (OTHER KILLS BY SYSTEM) | 13 (“other”, a kill by the system) | T | /data/system/procexitstore/procexitinfo |
| **008** | **com.ss.android.ugc.aweme.splash.SplashActivity** | **com.ss.android.ugc.aweme.splash.SplashActivity** | **T(2)** | **badge.db-wal** |
| 009 | MOCKS | MOCKS | T | app\_webview/Default/Local Storage/leveldb, 000005.ldb |
| 010 | 83 | 83 | T | bigTopDataDB, ^smartlabel\_notification |
| **011** | **\#262626** | **\-** | **F(3)** | **local\_layer\_config.xml, media\_content\_card.db, googlequicksearchbox** |
| **012** | **5254** | **\-** | **F(3)** | **ssrm\_heating\_13.log, /data/system/procexitstore/procexitinfo** |
| **013** | **2025-11-10 18:11:26 OR 2025-11-10 18:11:25** | **2025-11-10 18:11:14** | **F(3)** | **DB\_SET\_TIMEZONE.xml, /data/property/persistent\_properties**   |
| 014 | com.google.android.youtube | com.google.android.youtube | T | /data/data/com.sec.android.app.launcher/databases/appsedge.db-wal |

**AI 답변 및 실행 근거 상세 기록**  
**001**  
질문: What is the name of the establishment the user took a screenshot of?

정답: 99 Restaurants

⬥ Samsung A53의 /data/media/0/DCIM/Screenshots/ 경로에서 스크린샷 파일 Screenshot\_20251209\_153814\_Chrome.jpg (object 51721)를 확인함.  
⬥ Chrome 방문 기록 아티팩트(TSK\_WEB\_HISTORY)를 조회하여 스크린샷 촬영 직전(2025-12-09 15:38:14 로컬 시간)에 열려 있던 페이지 목록을 분석함.  
⬥ 스크린샷 촬영 직전 방문한 마지막 웹페이지가 "Bar Restaurant in Williston, VT \| 99 Restaurants" (\[99restaurants.com/locations/vermont/williston/\](https\://99restaurants.com/locations/vermont/williston/))임을 확인하여 매장명을 추출함.

**002**  
질문: What was the last time in UTC Clash Of Clans was closed? (Format: YYYY-MM-DD HH:MM:SS)

오답1: 2025-12-15 18:07:01

⬥ Clash of Clans 앱의 Firebase Analytics 설정 파일 /data/data/com.supercell.clashofclans/shared\_prefs/com.google.android.gms.measurement.prefs.xml에 접근함.  
⬥ 앱이 백그라운드로 전환될 때 기록되는 last\_pause\_time 키의 밀리초 타임스탬프 값 1765822021957을 확인함.  
⬥ 해당 타임스탬프를 변환하여 게임이 마지막으로 종료된 시각인 2025-12-15 18:07:01 UTC (18:07:01.957)를 확인하여 답을 추출함.

오답2: 2025-12-15 18:07:01

⬥ 안드로이드 시스템의 최근 실행 태스크 기록 파일인 /data/system\_ce/0/recent\_tasks/129\_task.xml에 접근함.  
⬥ Firebase Analytics의 last\_pause\_time (1765822021957) 기록과 함께 18:07:01 직후 다른 앱(Threads: 71\_task.xml, Gmail: 151\_task.xml)으로 포커스가 전환된 타임라인을 교차 확인함.  
⬥ 2025-12-16 09:32의 단순 백그라운드 프로세스 시작을 제외하고, 포그라운드에서 실행된 게임의 마지막 종료 시각이 2025-12-15 18:07:01 UTC임을 재확인하여 답을 추출함.

오답3: 2025-12-15 18:07:01

⬥ Clash of Clans 앱의 AppsFlyer 분석 설정 파일인 shared\_prefs/appsflyer-data.xml에 접근함.  
⬥ 세션 실행 시각 1765820944147 (17:49:04 UTC)에 세션 지속 시간 prev\_session\_dur (1078초)를 더해 계산된 세션 종료 시각(18:07:02)과 해당 xml 파일 수정 시각(18:07:03)을 확인함.  
⬥ Firebase, AppsFlyer 및 태스크 로그 3개 출처 교차 검증을 통해 최우선 정밀 타임스탬프 시각인 2025-12-15 18:07:01 UTC를 확인하여 최종 답을 추출함.

003  
질문: What country was the other party from for a rejected/declined call?

정답: Saudi Arabia

⬥ Samsung A53의 통화 기록 DB 파일인 calllog.db-wal에 접근함.  
⬥ 통화 거절/거부(rejected/declined)를 의미하는 type 컬럼값 5로 기록된 행을 조회함.  
⬥ 수신 거절된 전화번호 \+966 50 444 9263의 국가 코드(\+966) 및 안드로이드 위치 조회 필드(geocoded\_location)를 분석하여 상대방 국가가 Saudi Arabia임을 확인함.

**004**  
질문: What is the Ingress rating of the security camera that supports night vision?

오답1: \-

⬥ Samsung A53의 Chrome 방문 기록에서 나이트 비전을 지원하는 2MP HD Vandalproof Dome Camera with 100-foot night vision (cctvsecuritypros.com) 웹페이지 방문 내역(2025-12-10 08:04:19 UTC)을 확인함.  
⬥ 브라우저 방문 기록에는 Ingress Protection(IP) 등급 정보가 포함되어 있지 않음을 확인함.  
⬥ 정확한 IP 등급을 도출하기 위해 Chrome 캐시 데이터 및 ALEAPP 보고서 조회가 필요함을 파악함.

오답2: \-

⬥ Chrome 캐시(17:04:20\~17:04:22) 내 제품 이미지(SV-ED2-N...png) 및 스크립트 파일만 존재하고 HTML 본문 데이터는 저장되지 않음을 확인함.  
⬥ Chrome 저장 오프라인 페이지 4건 중 해당 카메라 제품 페이지가 포함되어 있지 않음을 확인함.  
⬥ Chrome 탭 썸네일 이미지 파일 data/data/com.android.chrome/app\_textures/21.jpeg (object ID 6651)의 뷰어를 통한 직접 확인이 필요함을 파악함.

오답3: \-

⬥ 기기 내 방문 기록, Chrome 캐시, 오프라인 페이지, 키워드 검색 결과 전체를 재검증했으나 IP 등급 상세 사양이 확인되지 않음.  
⬥ exact IP 등급 확인을 위해 Autopsy에서 탭 썸네일(app\_textures/21.jpeg) 열람, "IP66" 또는 "IP67" 키워드 검색, 혹은 ALEAPP "Chrome Browser Cache" 보고서 첨부가 필요함을 파악함.

**005**  
질문: What was the answer to the first Wordle puzzle solved?

정답: COLIC

⬥ Samsung A53의 NYT Games 앱 내 웹뷰 로컬 스토리지 파일인 app\_webview/Default/Local Storage/leveldb에 접근함.  
⬥ 스토리지 파일 중 000017.ldb 내 6번째 시도(Row 6)에서 상태값 WIN으로 기록된 "COLIC" 정답을 확인함.  
⬥ 또 다른 저장 기록(2025-12-04 기록, 정답 TULIP)과 비교하여 2025-11-28 19:53 UTC경 해결된 COLIC이 가장 먼저 풀린 문제임을 검증하여 답을 추출함.

**006**  
질문: What is the name of the client the user was most recently working on?

오답1: \-

⬥ Samsung A53에서 최근 작업한 Google Docs 문서 CLIENT Security Recommendations (doc ID: 1b62HtfpeE\_F8wY7hwvSfixz1sIIPgXoY0e0AldvdIg, 비즈니스 계정: djones.iss.secure@gmail.com)에 접근함.  
⬥ 오프라인 문서 파일 files/stashes/1a1869603c5aae099881926a44fc747e/DB (objectId 14567\) 본문을 조회했으나 클라이언트 실명 대신 "the customer", "CLIENT" 표기만 존재함.  
⬥ 클라이언트 실명 확인을 위해 비즈니스 계정 드라이브 캐시 DB cello.db-wal (objectId 13681)의 items 테이블 조회가 필요함을 파악함.

오답2: \-

⬥ 두 번째 오프라인 문서(stashes/2ec36817.../DB, objectId 14574\) 및 검색 기록, 알림, 캘린더 아티팩트를 추가 조사했으나 클라이언트명을 확인하지 못함.  
⬥ Google Chat 알림 DB(1\_room\_notifications.db-wal)에서 워크스페이스 스페이스 ID spaces/yfhJFiAAAAE를 발견함.  
⬥ 구체적 메시지 및 클라이언트 확인을 위해 Google Chat DB인 dynamite.db (objectId 14665\) 및 \-wal (objectId 14667\) 파일의 별도 추출 및 디코딩이 필요함을 파악함.

오답3: CLIENT (또는 \-)

⬥ Google Chat 비즈니스 계정 DB dynamite.db-wal (objectId 14667\) 및 개인 계정 문서 stashes/2ec36817.../DB (objectId 14574)를 추가 검증함.  
⬥ 최근 작업 문서 내 본문 및 제목 전체에서 실제 고객 실명이 명시되지 않고 대체문구인 CLIENT로만 기록되어 있음을 최종 확인함.  
⬥ 질문이 문서에 쓰인 표기 자체를 뜻할 경우 CLIENT가 정답이며, 실제 특정 클라이언트 사명을 구하기 위해서는 dynamite.db 내 메시지 텍스트 파싱 또는 Gmail DB(bigTopDataDB.\*) 조회가 필요함을 확인함.

**007**  
질문: What was the reason the Nike app was last exited?

정답: 13 (“other”, a kill by the system)

⬥ Samsung A53의 프로세스 종료 로그 파일인 /data/system/procexitstore/procexitinfo에 접근함.  
⬥ Nike Run Club 앱(패키지명: com.nike.plusgps)의 종료 기록을 조회함.  
⬥ 이유 코드가 13으로 기록되어 있으며, 해당 코드가 'other' (a kill by the system that isn't a crash or a user action)를 나타내는 것을 확인하여 답을 추출함.

**008**  
질문: What class had the most badges?

오답: com.bytedance.nproject.app.MainActivity

⬥ Samsung A53의 앱 아이콘 뱃지 DB인 com.sec.android.provider.badge/databases/badge.db 및 WAL 로그 파일 badge.db-wal에 접근함.  
⬥ DB 로그 전체 이력을 조회하여 각 앱의 활동 클래스(Activity Class)별 최대 뱃지 수량을 확인함.  
⬥ Lemon8 앱의 클래스인 com.bytedance.nproject.app.MainActivity가 최대 99개로 전체 앱 중 가장 많은 뱃지 수를 기록했음을 확인하여 답을 추출함.

정답: [com.ss](http://com.ss).android.ugc.aweme.splash.SplashActivity

⬥ Samsung A53의 badge.db-wal 로그 파일에서 가장 마지막으로 기록된 최신 상태의 뱃지 테이블을 조회함.  
⬥ 기기 추출 시점에 Lemon8 뱃지 수는 8개로 감소해 있었음을 확인함.  
⬥ 최종 상태 기준 TikTok 앱의 클래스인 com.ss.android.ugc.aweme.splash.SplashActivity가 15개로 가장 많은 뱃지를 보유하고 있음을 확인하여 답을 추출함.

**009**  
질문: What was the second guess on the first Wordle the user played?

정답: MOCKS

⬥ Samsung A53의 NYT Games 앱 내 웹뷰 로컬 스토리지 경로 app\_webview/Default/Local Storage/leveldb에 접근함.  
⬥ 스토리지 파일 중 가장 오래된 게임 기록 파일인 000005.ldb (2025-11-28 19:50\~19:53 UTC 저장)를 조회함.  
⬥ 해당 파일의 시도 단어 리스트 \["acorn", "mocks", "coupe", "coyly", "third"\]에서 두 번째 추측 단어가 MOCKS임을 확인하여 답을 추출함.

**010**  
질문: How many emails were automatically labeled as notifications?

정답: 83

⬥ Samsung A53에 등록된 2개 Gmail 계정의 앱 DB 파일인 bigTopDataDB에 접근함.  
자동 알림 카테고리 태그인 ^smartlabel\_notification 카운터를 조회함.  
⬥ 개인 계정(danieljonesonline55@gmail.com) 73개 및 업무 계정(djones.iss.secure@gmail.com) 10개를 합산하여 총 83개임을 확인하여 답을 추출함.

**011**  
질문: What is the hex code of the content color for the entry that expires on 2025-12-01 15:06:45?

오답1: \-

⬥ Autopsy 아티팩트, 쿠키, 틱톡 및 Lemon8(local\_layer\_config.xml) 설정 파일 등을 수색했으나 해당 만료 시각의 레코드가 존재하지 않음을 확인함.  
⬥ 정확한 파일 추적을 위해 대상 앱 종류, 아티팩트 범주, 기준 타임존(UTC, 동부 표준시, KST 등) 확인이 필요함을 명시함.

오답2: \-

⬥ Firebase In-App Messaging 캠페인 파일, Lemon8 팝업 설정, 틱톡 자산, Chrome 탭 그룹, 삼성 클라우드 DB(media\_content\_card.db) 등을 추가 분석했으나 일치 항목이 없음.  
⬥ 구체적인 앱 명칭이나 "content color"가 표기된 위치(ALEAPP 리포트 또는 Autopsy 뷰) 정보 제공이 필요함을 파악함.

오답3: \-

⬥ Google 앱(googlequicksearchbox) 이미지 캐시 및 2025-11-30 15:06 UTC 전후 생성 파일까지 조사 범위를 넓혔으나 만료 시각과 색상이 기록된 엔트리가 없음.  
⬥ 정답 확인을 위해 Autopsy에서 content\_color, contentColor 키워드 검색(Keyword Search)을 실행하여 해당 파일 및 Hex 값을 직접 파싱해야 함을 최종 파악함.

**012**  
질문: What was the PID of the app that was in focus at 2025-12-15 17:48:09?

오답1: \-

⬥ Samsung A53의 디바이스 케어 히팅 로그 파일인 ssrm\_heating\_13.log (object 37502)에 접근함.  
⬥ 로그 시각(UTC-5 기준 12:48:09)을 분석하여 2025-12-15 17:48:09 UTC에 포커스된 앱이 com.google.android.permissioncontroller임을 확인함.  
⬥ 해당 포커스 로그에는 PID 필드가 없으며, 프로세스 종료 기록 파일인 /data/system/procexitstore/procexitinfo (object 54599)가 텍스트 변환 과정에서 바이너리 바이트 손상을 입어 해당 시점의 PID를 추출하지 못함.

오답2: \-

⬥ ssrm\_heating\_13.log에서 17:48:07 UTC부터 포커스된 앱이 com.google.android.permissioncontroller임을 재검증함.  
⬥ iPhone/Mac 포커스 기록(App.InFocus), 히팅 로그, 디바이스 품질 DB, 오디오 서비스 DB 등 8개 출처를 모두 확인했으나 포커스 앱의 PID 정보가 존재하지 않음을 확인함.  
⬥ procexitinfo 바이너리 파일의 직접 추출 및 ALEAPP/protobuf 파서를 통한 디코딩 작업이 필요함을 확인함.

오답3: \-

⬥ ssrm\_heating\_13.log (UTC-5 기준 12:48:07\~12:49:04)를 통해 해당 시점 실행 앱이 com.google.android.permissioncontroller임을 최종 확인함.  
⬥ 17:48:09 UTC 주변의 복원된 타임스탬프 바이트를 밀리초 단위로 대조했으나, 복원된 PID는 삼성 백그라운드 서비스(cmh, faceservice 등)의 수치이며 permissioncontroller 항목의 PID와 시간 데이터는 완전히 손실되었음을 확인함.  
⬥ 정확한 PID 산출을 위해 procexitinfo (object 54599\) 원본 파일 직접 추출이 필수적임을 확인함.

**013**  
질문: When in UTC was the timezone set? (YYYY-MM-DD HH:MM:SS)

오답1: 2025-11-10 18:11:14

⬥ 삼성 시계 앱의 설정 파일인 DB\_SET\_TIMEZONE.xml (/SamsungA53/.../com.sec.android.app.clockpackage/shared\_prefs/)에 접근함.  
⬥ 해당 파일 내에 저장된 오프셋 값 \-18000000 (UTC-5, 동부 표준시)과 수정 시각 타임스탬프인 2025-11-10 18:11:14Z를 확인함.  
⬥ 3개 사본(data/data, data/user/0, data\_mirror) 모두 동일한 수정 시각을 유지하고 있어 타임존 설정/변경 시점으로 도출함.

오답2: 2025-11-10 18:11:14

⬥ DB\_SET\_TIMEZONE.xml 파일의 최신 수정 시각이 2025-11-10 18:11:14Z임을 재검증함.  
⬥ 주변 설정 파일들(Settings Intelligence, Play Store, Google Messages 등)이 \~18:08, Gmail tz-database 파일이 18:09:00에 작성된 정황과 부합하여 최초 부팅/설정 과정에서 적용된 타임존 변경 시점으로 확정함.

오답3: 2025-11-10 18:11:14 

⬥ /data/property/persistent\_properties 내 persist.sys.timezone \= America/New\_York 및 persist.sys.timezone\_confidence \= 100 속성을 확인하여 UTC-5 타임존 값을 재확인함.  
⬥ persistent\_properties 파일 자체 수정 시각(2025-12-22)은 속성 변경에 따른 수치라 쓸 수 없으며, 초기 설정 구역(18:07\~18:21) 내 타임존을 저장한 가장 이른 파일인 DB\_SET\_TIMEZONE.xml 기록 시각 2025-11-10 18:11:14를 최종 답으로 도출함.

**014**  
질문: What was the top package name in a splitscreen shortcut?

정답: com.google.android.youtube

⬥ Samsung A53의 엣지 패널 DB 로그 파일인 /data/data/com.sec.android.app.launcher/databases/appsedge.db-wal (object 36819)에 접근함.  
⬥ item 테이블 내 분할 화면(splitscreen/app pair) 바로가기 문자열 레코드를 조회함.  
⬥ 문자열 구조 상 첫 번째(상단) 앱 패키지명인 com.google.android.youtube (YouTube)를 확인하여 답을 추출함. 

**2.3 2026 CTF 이미지\_SamsungA53**

**이미지 기본 정보**

| 이미지명 | SamsungA53 |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_samsungA53 |
| 문항 수  | 14 |
| 실험자 | 진세라 |
| 정답률 | 9/14(64%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 001 | 99 Restaurant | 99 Restaurant | T | screenshot image file, Chrome History |
| 002 | 2025-12-15 18:07:05 | 2025-12-15 18:07:01 UTC | F(3) | /data/data/com.supercell.clashofclans/shared\_prefs/com.google.android.gms.measurement.prefs.xml,game analytics settings file |
| 003 | Saudi Arabia | Saudi Arabia | T | com.samsung.android.providers.contacts/databases/calllog.db-wal  |
| 004 | IP67 | \- | F(3) | Chrome History([cctysecuritypros.com](http://cctysecuritypros.com)), 야간 시야 기능 정보 포함된 제품 페이지 url |
| 005 | COLIC | CIGAR | F(3) | data/data/com.nytimes.crossword/app\_webview/Default/Local Storage/leveldb/  |
| 006 | Hidden Gems | Alex Maurie  | F(3) | google chat app db, DM, Chat Message, File modified time |
| 007 | 13 (OTHER KILLS BY SYSTEM) | 13, “Other kills by system”  | T | .../com.nike.plusgps/cache/newrelic/applicationExitInfo/  |
| 008 | com.ss.android.ugc.aweme.splash.SplashActivity | com.ss.android.ugc.aweme.splash.SplashActivity  | T | [badge.db](http://badge.db)\-wal, badge table |
| 009 | MOCKS | MOCKS | T | New York Times Games 앱 로컬 스토리지 키, LevelDB로 저장되고 Snappy로 압축된 스냅샷  |
| 010 | 83 | 83 | T | bigTopDataDB.-1378477988 : gmail계정1의 DB, bigTopDataDB.-257370584 : gmail계정2의 DB label\_counts 확인 |
| 011 | \#262626 | \#262626 | T | /data/data/com.google.android.gms/ → FCM queued messages → 000053.ldb → Lemon8 notification → content\_color\_s |
| 012 | 5254 | \- | F(3) | Recent Tasks \- /data/system\_ce/0/recent\_tasks/129\_task.xml   Process Exit Info \- /data/system/procexitstore/procexitinfo |
| 013 | 2025-11-10 18:11:26 or 2025-11-10 18:11:25 | 2025-11-10 18:11:14 | F(3) | com.sec.android.app.clockpackage/shared\_prefs/DB\_SET\_TIMEZONE.xml |
| 014 | com.google.android.youtube | com.google.android.youtube | T | Apps Edge DB WAL (com.sec.android.app.launcher/databases/appsedge.db-wal) appsedge.db-wal 내부 레코드 (2;3;0.5;0.5;com.google.android.youtube/.app.honeycomb.Shell\$HomeActivity:0;com.sec.android.app.sbrowser/.SBrowserMainActivity:0) |

**AI 답변 및 실행 근거 상세 기록**

001  
질문: What is the name of the establishment the user took a screenshot of?  
정답: 99 Restaurant

1차:

* Autopsy 도구에서 JPEG 이미지 직접 렌더링 불가로 장소명 미확정.  
* Chrome 검색 및 스크린샷 직전 방문 기록(\[99restaurants.com/\](https\://99restaurants.com/)..., 2025-12-09 20:32:33 UTC) 분석 결과 99 Restaurants in Williston, Vermont로 추정.  
* 스크린샷(Screenshot\_20251209\_153814\_Chrome.jpg, 20:38:15 UTC) 및 클립보드 복사 기록 확인.  
* 정확한 확인을 위해 Autopsy Media Viewer(Object ID 51721)로 실제 이미지 열람 필요.

2차:

* 1차와 동일하게 이미지 직접 확인 불가하여 Chrome 기록 기반 추정.  
* EXIF 촬영 시간(20:38:14 UTC) 및 스크린샷 직전 접속 페이지("Bar Restaurant in Williston, VT \| 99 Restaurants") 확인.  
* 정확한 확인을 위해 Autopsy Viewer로 실제 이미지 내 상호명 검증 필요.

002  
질문: What was the last time in UTC Clash Of Clans was closed? (Format: YYYY-MM-DD HH:MM:SS)  
정답: 오답(2025-12-15 18:07:01 UTC)

1차:

* aLEAPP 보고서 접근 미승인으로 분석 중단.  
* 앱 설치(12-09 20:49 UTC) 및 첫 실행(21:11 UTC) 시간만 확인 가능.  
* 종료 시간 확인을 위해 aLEAPP 보고서(Digital Wellbeing / usage stats) 또는 /data/system\_ce/0/usagestats/ 파일 필요.

2차:

* Firebase 설정 파일(com.google.android.gms.measurement.prefs.xml) 분석으로 종료 시간 도출.  
* last\_pause\_time \= 1765822021957 (Epoch ms) \-\> 2025-12-15 18:07:01.957 UTC 확인.  
* 세션 시작(17:46:11 UTC) 및 관련 설정 파일 수정 시각(18:07:03 UTC) 일치 확인.  
* OS 차원의 최종 확인을 위해 aLEAPP Digital Wellbeing 페이지 검증 필요.

003\.   
질문 : What country was the other party from for a rejected/declined call?  
정답 : Saudi Arabia

1차:

* Autopsy의 call-type 필드(수신, 부재중, 거절 등) 텍스트 변환 제한으로 거절(declined) 플래그를 직접 확정하지는 못함.  
* 삼성 통화 기록 DB WAL 파일(`calllog.db-wal`) 수동 검증 진행:  
  * 통화 기록 내 미국 국가번호(`+1`) 외 유일한 해외 전화번호: **`+966 50 444 9263`**.  
  * 국가코드 `+966` 및 해당 레코드의 라벨인 **Saudi Arabia** 확인.  
* 정확한 거절 플래그(`type = 5`) 검증을 위해 SQLite viewer에서 `calllog.db` 및 `-wal` 파일 직접 확인 또는 aLEAPP 통화 기록 페이지 조회 필요 명시.

004

질문: What is the Ingress rating of the security camera that supports night vision?

정답: \-

1차:

* 케이스 내 제품 목록/파일 미확인으로 정확한 카메라 모델 및 IP 등급 답변 불가.  
* 일반적인 야간 비전 지원 야외 카메라 등급(IP65, IP66/IP67) 안내 및 제품명/스펙시트 확인 필요 명시.

005\.   
질문 : What was the answer to the first Wordle puzzle solved?  
정답 : 오답(CIGAR)  
1차:

* 최초 Wordle 퍼즐(\#0, 2021-06-19) 공식 정답인 CIGAR로 응답.

2차 :

* 공식 정답리스트 상의 첫 번째 퍼즐(\#0) 정답은 CIGAR, 그다음 퍼즐(\#1) 정답은 REBUT임을 보완 설명.  
* 최초 일반 공개 시점(2021년 10월) 차이로 실제 플레이어가 최초로 푼 퍼즐에 대한 부연설명 제공.

006\.   
질문 : What is the name of the client the user was most recently working on?  
정답 : 오답(Alex Maurie)  
1차:

* SMS/MMS 메시지, 이메일, 검색 기록, 사용자 저장소 파일명 분석 결과 클라이언트명 발견 불가.  
* Autopsy 연결 오류로 최근 열어본 항목 일부 조회 실패.  
* 추가 검증을 위해 Google Chat, OneDrive, Signal, 메모 앱 등 파싱되지 않은 DB 검토 필요성 명시.

2차:

* Google Chat 앱 데이터(djones.iss.secure@gmail.com 계정) 대화 기록에서 Alex Maurie 확인.  
* 대화 내역: "The doc looks great, thanks for your help" 메시지 존재 (2025-12-15 최종 수정).  
* 텍스트 덤프 방식 판독 한계로 다른 대화 상대 존재 가능성 존재하여 Autopsy에서 Chat DB 직접 열람 권장.

007\.   
질문 : What was the reason the Nike app was last exited?  
정답 : 13, “Other kills by system” 

008\.  
질문 : What class had the most badges?  
정답 : com.ss.android.ugc.aweme.splash.SplashActivity   
1차:

* badge.db 본체(4 KB)가 비어 있고 WAL 로그 파일(badge.db-wal)만 존재하여 텍스트 판독만으로는 정확한 순위 확정 불가.  
* 정확한 분석을 위해 badge.db, \-wal, \-shm 파일을 추출하여 DB Browser for SQLite로 조회 필요 명시.

2차:

* badge.db-wal 파일의 커밋 프레임 내 배지 테이블 페이지를 직접 해석하여 배지 수 확인.  
* TikTok (com.zhilioapp.musically)의 com.ss.android.ugc.aweme.splash.SplashActivity 클래스가 배지 수 15개로 가장 많음 확인.

009\.   
질문 : What was the second guess on the first Wordle the user played?  
정답 : MOCKS  
1차:

* NYT Games 앱(com.nytimes.crossword)의 LevelDB 파일(000005.ldb) 분석 시도.  
* Snappy 압축으로 인해 단어의 마지막 글자가 깨져 보여 "MOCK?" (MOCKS, MOCHA 등)으로만 확인되고 마지막 5번째 글자 판독 불가.

2차:

* 이후 스냅샷 파일(000017.ldb) 분석을 통해 두 번째 추측 단어가 MOCKS임을 최종 확정.  
* 첫 번째 스냅샷(000005.ldb)에서는 "mock" \+ 은닉 문자 형태였으나, 두 번째 스냅샷에서 완전한 "mocks" 텍스트 복원 성공.

010\.   
질문 : How many emails were automatically labeled as notifications?  
정답 : 83  
1차:

* 대화 내 공유된 이메일 데이터 또는 연동된 메일함 미존재로 개수 확인 불가.

2차:

* Autopsy 분석 중 이메일 아티팩트(TSK\_EMAIL\_MSG) 및 알림 아티팩트(TSK\_PROG\_NOTIFICATIONS) 미발견.  
* Gmail 앱 데이터베이스(bigTopDataDB.-1378477988, bigTopDataDB.-257370584) 파일 존재 파악 및 SQL 미지원으로 인해 DB Browser for SQLite 활용 필요성 안내.

3차:

* Gmail 앱 DB 내 label\_counts 캐시 및 WAL 파일 수동 분석을 진행함.  
* ^smartlabel\_notification 라벨 기준 총 83개 (계정1: 73개, 계정2: 10개) 확인. (참고: 엄격한 기준인 ^smartlabel\_pure\_notif 라벨 기준은 총 80개)

011\.   
질문 : What is the hex code of the content color for the entry that expires on 2025-12-01 15:06:45?  
정답 : \#262626  
1차:

* 해당 만료 시각(2025-12-01 15:06:45)을 가지는 타임라인 이벤트 및 아티팩트를 발견하지 못함.  
* 파일 경로, FCM 덤프, 앱 명칭 등 구체적인 세부 출처 확인 필요성 명시.

2차:

* 기기의 푸시 메시지 큐 파일(/data/data/com.google.android.gms/files/fcm\_queued\_messages.ldb/000053.ldb, Object ID 23354\) 분석 완료.  
* Lemon8 (com.bd.nproject) 알림 메시지 큐 저장 시각: 2025-11-30 19:06:45 UTC (만료 시각인 2025-12-01 15:06:45와 정확히 20시간 차이).  
* 해당 알림 메시지의 설정 내 "content\_color\_s": "\#262626" 확인 (bg\_color\_s: \#FFFFFF).

012\.   
질문 : What was the PID of the app that was in focus at 2025-12-15 17:48:09?  
정답 : \-   
1차:

* 17:48:09 UTC 기준 포커스된 앱은 Clash of Clans (com.supercell.clashofclans)로 강력 추정되나, PID를 직접 입증할 수 있는 데이터 미발견.  
* Thermal log (ssrm\_heating\_13.log), GOS 로그 (ipm\_ringlog), Process exit history (procexitinfo) 분석 시도 중 바이너리/프로토버프 데이터 판독 한계 발생.  
* 정확한 PID 도출을 위해 Hex dump, protobuf 데코더, logcat 또는 dumpsys 데이터 필요.

2차 :

* 17:00\~19:00 UTC 타임라인 및 data artifacts/tags, logcat/bugreport 재검증했으나 PID 미확정 유지.  
* usagestats 바이너리 프로토버프 파일 분석 결과 포커스 및 백그라운드 이벤트 기록은 존재하나 PID 필드 없음 확인.  
* flight\_records 내 프로세스 시작 기록(Google Restore: 7697, Google Photos: 7736 등)은 존재하나 해당 시점 포커스 앱의 PID는 아님.

013\.   
질문 : When in UTC was the timezone set? (YYYY-MM-DD HH:MM:SS)  
정답 : 오답(2025-11-10 18:11:14)  
1차:

* 삼성 시계(Clock) 앱 설정 파일(DB\_SET\_TIMEZONE.xml) 분석.  
* 설정값: DB\_SET\_TIMEZONE \= \-18000000 (UTC-5시간), 최종 수정 시각: 2025-11-10 18:11:14 UTC.  
* 이는 시계 앱에 저장된 타임존 값의 수정 시각이며, 시스템 수준 타임존 설정(persist.sys.timezone)은 발견하지 못했음을 명시.

2차 :

* 시스템 속성 persist.sys.timezone \= America/New\_York (UTC-5) 및 신뢰도 100 확인.  
* 단, 해당 시스템 속성이 담긴 persistent\_properties 파일의 최종 수정 시각(2025-12-22 17:01:26 UTC)은 상한선일 뿐이며, 2025-11-10 18:11:14 UTC가 타임존 설정에 대한 가장 직접적이고 최선의 기록임을 유지.

3차 :

* 시스템 타임존 파일(persistent\_properties)의 마지막 기록 시각인 2025-12-22 17:01:26 UTC로 수정 제시.  
* 네트워크 기반 자동 타임존 설정 (auto\_time\_zone \= 1 in settings\_global.xml) 상태 확인.  
* 이전 2025-11-10 시각은 시계 앱 자체 저장 기록 시각임을 보완 설명.

014\. 

질문 : What was the top package name in a splitscreen shortcut?  
정답 : com.google.android.youtube  
1차:

* Apps Edge 데이터베이스 WAL 로그(appsedge.db-wal) 내 App Pair 기록 분석.  
* 레코드: 2;3;0.5;0.5;com.google.android.youtube/.app.honeycomb.Shell\$HomeActivity:0;com.sec.android.app.sbrowser/.SBrowserMainActivity:0

* Top app: com.google.android.youtube (YouTube)  
* Bottom app: com.sec.android.app.sbrowser (Samsung Internet)  
* Split 비율: 0.5:0.5 (동일 분할)

**3\. 2026 CTF 이미지\_iPhone14Plus**

**이미지 기본 정보**

| 이미지명 | iPhone14Plus |
| :---: | :---: |
| 연도 | 2026 |
| 이미지 형식 | zip |
| 이미지 용량 | 18GB |
| 출처 | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFiOS |
| Autopsy Case명 | 26\_iPhone14Plus |
| 대상 OS | iOS |
| 문항 수  | 16 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 015 | @mrbeast **OR** mrbeast | @mrbeast | @mrbeast | T |
| 016 | headphones | Headphones | headphones | T |
| 017 | 2025-12-12 18:00:10 | 2025-12-12 18:00:10 | 2025-12-12 18:00:10 | T |
| 018 | 472.01 | \- | 1,968.54 | F |
| 019 | 3 | \- | \- | F |
| 020 | Social Networking | Social Networking | Social Networking | T |
| 021 | McLaren Senna | McLaren Senna | McLaren Senna | T |
| 022 | Long Island MacArthur Airport | Long Island MacArthur Airport | Long Island MacArthur Airport | T |
| 023 | how-a-turbo-works.gif | how-a-turbo-works.gif | how-a-turbo-works.gif | T |
| 024 | fun festive sweater | fun festive sweater | fun festive sweater | T |
| 025 | “The Panda” **OR** “Panda” | panda | \- | T(50%) |
| 026 | 44.4758453, \-73.2134094 | 44.4758453, \-73.2134094 | latitude 44.4758453, longitude \-73.2134094 | T |
| 027 | 49354 | 49354 | 49354 | T |
| 028 | sipposed | sipposed | \- | T(50%) |
| 029 | 7FF3F4981C033CB5B10251CC57580B9C | 5AB9FEDB-537F-37F0-85FE-01D07D00A86F | 5AB9FEDB-537F-37F0-85FE-01D07D00A86F | F |
| 030 | 00:02:32.077  | 00:02:32.077 | \- | T(50%) |

| NO | Question |
| :---: | ----- |
| 015 | What Instagram handle does User ID 2278169415 belong to? |
| 016 | What item does the user need to buy for Christmas? |
| 017 | In UTC when was the last iCloud backup? (YYYY-MM-DD HH:MM:SS) |
| 018 | What was the farthest distance the user logged in meters? (Round to the nearest hundredth) |
| 019 | How many people did the user message expressing concern about Daniel? |
| 020 | What genre of app did the user download the most of? |
| 021 | What is the make and model of the car that was photographed without an iPhone? |
| 022 | What airport was the phone near when it pinged off of a cell tower on 2025-12-16 22:47:24 (UTC)? |
| 023 | What is the name including extension of the purple tagged file? |
| 024 | What secondhand item was the user searching for? |
| 025 | What is the mascot of the frozen dessert shop that the user visits a lot? |
| 026 | What are the recorded coordinates of the place the user went to comment about a certain adult beverage? |
| 027 | What port was the host directed through for a sign-in? |
| 028 | What word did the user misspell, then correct before sending over text on a Friday? (Format: type the misspelled word as-is) |
| 029 | What is the UUID of the process that is related to an initiated shutdown? |
| 030 | How much time elapsed between Tom reading a phone number and sending their first message on a different platform? (Format: HH:MM:SS.sss) |

**3.1 2026 CTF 이미지\_iPhone14Plus**

**이미지 기본 정보**

| 이미지명 | iPhone174Plus |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_iPhone14Plus |
| 문항 수  | 16 |
| 실험자 | 박제윤 |
| 정답률 | 12/16(75%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 DB/아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| **015** | **@mrbeast OR mrbeast** | **@mrbeast** | **T(3)** | **79726424276/user\_bootstrap/shared\_bootstraps.plist** |
| 016 | headphones | Headphones | T | Calendar Entry (Artifact ID: 666792\) |
| 017 | 2025-12-12 18:00:10 | 2025-12-12 18:00:10 | T | /private/var/mobile/Library/Preferences/com.apple.mobile.ldbackup.plist |
| **018** | **472.01** | **\-** | **F(3)** | **\-** |
| **019** | **3** | **\-** | **F(3)** | **signal.sqlite, Session.sqlite, 00008110-0008196A2299401E\_keychain.plist** |
| 020 | Social Networking | Social Networking | T | iTunesMetadata.plist |
| **021** | **McLaren Senna** | **McLaren Senna** | **T(2)** | **Photos.sqlite, psi.sqlite, DCIM/100APPLE/IMG\_0001.WEBP** |
| 022 | Long Island MacArthur Airport | Long Island MacArthur Airport | T | private/var/root/Library/Caches/locationd/cache\_encryptedB.db |
| 023 | how-a-turbo-works.gif | how-a-turbo-works.gif | T | CloudDocs/session/db/client.db |
| 024 | fun festive sweater | fun festive sweater | T | Documents/atevents.sqlite-wal |
| 025 | “The Panda” **OR** “Panda” | panda | T | /private/var/mobile/Library/Caches/com.apple.routined/Cloud-V2.sqlite |
| **026** | **44.4758453, \-73.2134094** | **44.4758453, \-73.2134094** | **T(2)** | **fsCachedData/9426920C-3F46-4D40-B096-E006A23F9440** |
| 027 | 49354 | 49354 | T | \[http\://127.0.0.1:49354/\](http\://127.0.0.1:49354/) |
| 028 | sipposed | sipposed | T | /private/var/mobile/Library/Biome/streams/restricted/Keyboard.TokenFrequency/local/785347902592136, zangidb\_9193129592.sqlite |
| **029** | **7FF3F4981C033CB5B10251CC57580B9C** | **5AB9FEDB-537F-37F0-85FE-01D07D00A86F** | **F(3)** | **/private/var/db/diagnostics/shutdown.log** |
| **030** | **00:02:32.077** | **00:02:32.077** | **T(2)** | [**1998824521952800768-dmv2.db**](http://1998824521952800768-dmv2.db)**\-wal, NSELogs/org.whispersystems.signal.SignalNSE 2025-12-12--00-43-26-938.log** |

**AI 답변 및 실행 근거 상세 기록**  
**015**  
질문: What Instagram handle does User ID 2278169415 belong to?

오답1: \-

⬥ iPhone 14 Plus (case 26\_iOS) 내 기존 파싱 결과, 파일 경로, 파싱된 인스타그램 계정 목록에서 사용자 ID 2278169415를 찾지 못함.  
⬥ 인스타그램 메시지 DB(DirectSQLiteDatabase/79726424276.db) 및 설정 plist 파일(hazyalex2002)을 확인하였으나 해당 ID의 핸들명을 발견하지 못함.  
⬥ 데이터가 존재할 가능성이 높은 ig-msys-1784226378065627773.db 파일에 대한 파일 추출 및 키워드 검색 등 추가 작업이 필요함을 파악함.

오답2: \-

⬥ iPhone14Plus 다운로드 폴더 접근 권한이 거부되어 추가 파일 열람 조치가 중단됨.  
⬥ 인스타그램 메시지 DB 파일인 ig-msys-1784226378065627773.db (object ID 129762)를 직접 열어보지 못해 사용자 ID 2278169415에 대한 핸들명을 추출하지 못함.

정답: @mrbeast

⬥ iPhone 14 Plus의 인스타그램 공유 앱 그룹 폴더 내 79726424276/user\_bootstrap/shared\_bootstraps.plist 설정 캐시 파일(object ID: 129639)에 접근함.  
⬥ 해당 plist 파일 내 상호작용 계정 목록 데이터를 조회함.  
⬥ 사용자 ID 2278169415에 매핑된 인스타그램 핸들명(username)이 mrbeast (표시 이름: MrBeast)임을 확인하여 답을 추출함.

**016**  
질문: What item does the user need to buy for Christmas?

정답: Headphones

⬥ iPhone 14 Plus의 LogicalFileSet2에 접근함.  
⬥ 캘린더(Calendar) 아티팩트 DB(ID: 666792)를 조회하여 "Buy headphones for Christmas"라는 사용자 생성 일정을 확인함.  
⬥ DB 내 저장된 UTC 시간(2025-12-21 15:00 \~ 2025-12-22 14:59:59 UTC)을 분석하여 작성 당시 타임존이 UTC+9였음을 파악함.  
⬥ 전체 대상 "Christmas" 키워드 검색을 통해 기본 공휴일 3건을 제외한 유일한 사용자 작성 항목임을 검증하여 답을 추출함.

**017**  
질문: In UTC when was the last iCloud backup? (YYYY-MM-DD HH:MM:SS)

정답: 2025-12-12 18:00:10 UTC

⬥ iPhone 14 Plus의 /private/var/mobile/Library/Preferences/com.apple.mobile.ldbackup.plist 설정 파일(아티팩트 ID: 324445)에 접근함.  
⬥ 해당 plist 파일 내 LastCloudBackupDate 키값인 787255210 (Apple 절대 시간 타임스탬프)을 확인함.  
⬥ Apple 타임스탬프(787255210)에 2001년 이전 초값(978307200)을 더해 Unix 타임스탬프(1765562410)로 변환 및 계산하여 최종 UTC 시간을 추출함

**018**  
질문: What was the farthest distance the user logged in meters? (Round to the nearest hundredth)

오답1: \-

⬥ Apple Health DB인 healthdb\_secure.sqlite (object ID 137123\) 및 WAL 파일에 저장된 이동 거리가 8바이트 바이너리 형태라 일반 텍스트 리더로 파싱되지 않음.  
⬥ iLEAPP 보고서 파싱 시 모듈 에러(no such column: workouts.activity\_type)가 발생하여 운동 및 이동 거리 데이터를 자동 추출하지 못함.  
⬥ 정답 도출을 위해 해당 Health DB 파일 직접 추출 및 SQLite 쿼리 조회가 필요함을 파악함.

오답2: \- 

⬥ Health DB 파일(healthdb\_secure.sqlite)의 바이너리 데이터를 일반 텍스트 변환 시 데이터 훼손이 발생하여 정확한 소수점 두 자리 거리 수치를 산출할 수 없음.  
⬥ 폴더 접근 권한 및 컴퓨터 제어 요청이 거부되어 Autopsy 내장 SQLite 뷰어를 통한 DB 열람이 중단됨.  
⬥ 정확한 답을 구하려면 healthdb\_secure.sqlite 파일 내 workouts 또는 workout\_activities 테이블 조회가 필요함을 확인함.

오답3: \-

⬥ Health 폴더 접근 권한이 재차 거부되어 가장 먼 이동 거리 값 도출 작업이 최종 중단됨.  
⬥ 파일 직접 추출(Extract File(s)) 또는 Autopsy의 SQLite Viewer(Application 탭)를 사용하여 healthdb\_secure.sqlite 내 workouts 및 workout\_activities 테이블을 직접 조회해야 함을 명시함.

**019**  
질문: How many people did the user message expressing concern about Daniel?

오답1: \-

⬥ iPhone의 읽기 가능한 메세지 저장소(SMS/iMessage, Gmail, Zangi, Instagram, Twitter/Threads)를 조사했으나 Daniel에 대한 우려를 표현한 메시지가 발견되지 않음.  
⬥ 주요 메세지 전송 대상인 Signal(T Blizzard) 및 Session(Clay M)의 DB가 암호화되어 있어 메세지 본문 읽기가 불가능함을 확인함.  
⬥ 해당 메세지 DB 복호화를 위해 키체인 덤프(Keychain dump) 복호화 키 조회가 필요함을 확인함.

오답2: \-

⬥ iOS 메세지 수집 저장소, 키보드 학습 캐시, SimpleX 앱 등을 추가 조사했으나 우려 메시지 수신자를 특정하지 못함.  
⬥ Session 알림 캐시에서 1:1 대화 3건을 확인했으나 본문 텍스트 없이 메시지 해시만 저장되어 있음을 파악함.  
⬥ signal.sqlite 및 Session.sqlite DB를 복호화하기 위한 추출 키체인 키가 필요함을 확인함.

오답3: \-

⬥ 복호화된 키체인 덤프 파일(keychain.plist)을 확보하여 Signal(signal.sqlite) 및 Session(Session.sqlite)의 SQLCipher 복호화 키를 추출하는 데 성공함.  
⬥ Autopsy의 텍스트 리더 특성상 암호화 데이터 복호화에 필요한 원본 바이너리 바이트가 손상되어 직접 복호화가 진행되지 않음.  
⬥ 정확한 인원수를 도출하기 위해 해당 앱 그룹 DB 파일(signal.sqlite, Session.sqlite)의 직접 추출 및 원본 파일 접근 권한 부여가 필요함을 파악함.

**020**  
질문: What genre of app did the user download the most of?

정답: Social Networking

⬥ iPhone 14 Plus에 설치된 각 앱의 메타데이터 파일인 iTunesMetadata.plist에 접근함.  
⬥ App Store에서 다운로드한 총 17개 앱의 장르별 개수를 분석함.  
⬥ Social Networking 장르가 총 7개(Signal, Session, Telegram, SimpleX, Zangi, Threads, Letterboxd)로 가장 많은 비중을 차지함을 확인하여 답을 추출함.

**021**  
질문: What is the make and model of the car that was photographed without an iPhone?

오답: Nissan GT-R (R35)

⬥ iPhone 14 Plus의 카메라 롤(DCIM/100APPLE) 내 iPhone 카메라 메타데이터가 없는 유일한 비(non)-iPhone 사진 파일 IMG\_0001.WEBP (object 141903)를 확인함.  
⬥ 사진 검색 인덱스 DB(psi.sqlite, object 142000)를 조회하여 해당 사진에 Sports Car, Supercar 등의 태그가 지정된 것을 확인함.  
⬥ 웹 방문 기록 분석 시 MotorWorld.net 포럼 내 GT-R 관련 게시글("2011 Nissan GT-R" 등)을 열람한 내역을 근거로 답을 추론함.

정답: McLaren Senna

⬥ Photos.sqlite DB 분석을 통해 IMG\_0001.WEBP 파일이 Safari(com.apple.mobilesafari)를 통해 저장되었고 카메라 메타데이터가 없음을 확인함.  
⬥ 사진 검색 인덱스 DB(psi.sqlite) 내 해당 이미지에 Hypercar, Megacar 등 McLaren Senna급 차종에 부여되는 태그를 확인함.  
⬥ 이미지 저장 당일(2025-12-11) Safari 검색 기록에서 "maclaren senna" 검색 내역을 교차 검증하여 기존 GT-R 추론을 대체하고 최종 답을 추출함.

**022**  
질문: What airport was the phone near when it pinged off of a cell tower on 2025-12-16 22:47:24 (UTC)?

정답: Long Island MacArthur Airport 

⬥ iPhone 14 Plus의 /private/var/root/Library/Caches/locationd/cache\_encryptedB.db 위치 캐시 DB(objectId: 335268)에 접근함.  
⬥ Apple 시간 타임스탬프 787618044 (2025-12-16 22:47:24 UTC) 기록에서 기지국 좌표 범위(약 40.81°N, 73.05–73.10°W)를 추출함.  
⬥ 해당 좌표에서 약 1\~2km 거리에 위치한 가장 가까운 공항인 Long Island MacArthur Airport를 확인함.

**023**  
질문: What is the name including extension of the purple tagged file?

정답: how-a-turbo-works.gif

⬥ iCloud Drive DB 파일인 CloudDocs/session/db/client.db (object 131336\) 및 해당 \-wal 파일(131338)에 접근함.  
⬥ client\_items 테이블을 조회하여 item\_finder\_tags 필드가 "Purple"로 설정된 행을 확인함.  
⬥ 해당 행의 item\_filename 필드값인 how-a-turbo-works.gif를 확인하여 확장자가 포함된 파일명을 추출함.

**024**  
질문: What secondhand item was the user searching for?

정답: fun festive sweater

⬥ iPhone 14 Plus에 설치된 Depop 앱(번들 ID: com.garageitaly.garage)의 로그 파일 Documents/atevents.sqlite-wal (objectId: 297447)에 접근함.  
⬥ 2025-12-11 UTC 이벤트 로그 내역을 조회함.  
⬥ 검색 및 상품 조회 활동 로그에서 사용자가 찾은 중고 의류 키워드가 "fun festive sweater"임을 추출함.

**025**  
질문: What is the mascot of the frozen dessert shop that the user visits a lot?

정답: panda

⬥ iPhone 14 Plus의 자주 방문한 장소 DB인 /private/var/mobile/Library/Caches/com.apple.routined/Cloud-V2.sqlite 및 WAL 파일을 조회함.  
⬥ 사용자가 5회 이상 자주 방문한 디저트 가게가 "Shy Guy Gelato"(198 St Paul St)임을 확인함.  
⬥ 해당 디저트 가게의 웹사이트 정보를 참조하여 마스코트/대표 캐릭터가 panda(팬더)임을 추출함.

**026**  
질문: What are the recorded coordinates of the place the user went to comment about a certain adult beverage?

오답: 44.47385397387211, \-73.21355093019157

⬥ iPhone의 Untappd 앱 캐시 DB인 Library/Caches/\[com.untappdllc.com/Cache.db-wal\](https\://com.untappdllc.com/Cache.db-wal) (object 116223)에 접근함.  
⬥ 2025-12-11 19:25경 전송된 체크인 요청 API (\[api.untappd.com/v4/checkin/add\](https\://api.untappd.com/v4/checkin/add)) 파라미터를 분석함.  
⬥ 체크인 시 기기에서 전송된 위도 및 경도 값(geolat=44.47385397387211, geolng=-73.21355093019157)을 확인하여 답을 추출함.

정답: 44.4758453, \-73.2134094

⬥ Untappd 캐시 내 서버 응답 데이터 파일 fsCachedData/9426920C-3F46-4D40-B096-E006A23F9440 (object 116319)에 접근함.  
⬥ 체크인 장소인 JP's Pub (Foursquare ID: 4b13066bf964a520de9223e3)의 실제 등록 위치 정보를 확인함.  
⬥ 장소의 서버 등록 좌표 필드값인 "lat":44.4758453, "lng":-73.2134094를 확인하여 기존 기기 위치 수치를 교정하고 최종 답을 추출함.

**027**  
질문: What port was the host directed through for a sign-in?

정답: 49354

⬥ 2025-12-09 12:45 UTC경 Safari 브라우저에서 진행된 Google 로그인 과정의 방문 기록(Browser history)에 접근함.  
⬥ OAuth2 인증 요청 및 리다이렉트 URL (redirect\_uri=\[http\://127.0.0.1:49354\](http\://127.0.0.1:49354)&...) 내 로컬호스트 주소를 확인함.  
⬥ 인증 완료 후 "Authentication Status" 페이지로 돌아갈 때 사용된 로컬호스트 포트 번호가 49354임을 확인하여 답을 추출함.

**028**  
질문: What word did the user misspell, then correct before sending over text on a Friday? (Format: type the misspelled word as-is)

정답: sipposed

⬥ iPhone 14 Plus의 키보드 입력 로그 파일 /private/var/mobile/Library/Biome/streams/restricted/Keyboard.TokenFrequency/local/785347902592136에 접근함.  
⬥ 입력 로그에서 오타인 "sipposed"와 올바른 단어인 "supposed"가 각각 1회씩 기록된 내역을 확인함.  
⬥ Zangi 메신저 앱 DB(zangidb\_9193129592.sqlite)의 메시지(msgId1765569453404)를 조회하여 2025-12-12 금요일 19:57:33 UTC에 "supposed"로 수정되어 전송된 내역을 교차 검증함.

**029**  
질문: What is the UUID of the process that is related to an initiated shutdown?

오답1: 359DB623-5C72-3BF3-B5D2-785FB581FFF7

⬥ iPhone의 종료 로그 파일인 /private/var/db/diagnostics/shutdown.log (object 108187)에 접근함.  
⬥ 기록된 5회의 종료 기록 중 항상 마지막까지 실행 중인 kernel 프로세스(pid: 0)를 조회함.  
⬥ 모든 종료 과정에서 최종적으로 대기하는 kernel 프로세스의 UUID인 359DB623-5C72-3BF3-B5D2-785FB581FFF7을 확인하여 답을 추출함.

오답2: 359DB623-5C72-3BF3-B5D2-785FB581FFF7

⬥ /private/var/db/diagnostics/shutdown.log 내 전체 프로세스 UUID 및 등장 횟수 테이블을 재분석함.  
⬥ 통합 로그(diagnostics/\*.tracev3) 손상 및 설치 로그 내 프로세스명 부재로 인해 특정 종료 시발 프로세스를 명시적으로 확인하지 못함.  
⬥ 5회 종료 전체에 공통으로 나타나며 항상 마지막까지 유지되는 kernel 프로세스의 UUID 359DB623-5C72-3BF3-B5D2-785FB581FFF7을 최종 유지함.

오답3: 5AB9FEDB-537F-37F0-85FE-01D07D00A86F

⬥ /private/var/db/diagnostics/shutdown.log 내 2025-12-22 15:42:56 UTC 종료 기록(SIGTERM: \[1766418176\])의 최상단 레코드를 분석함.  
⬥ 연결된 컴퓨터의 외부 명령을 처리하는 원격 서비스 프로세스 /usr/libexec/remoted (pid: 1925)의 생성을 확인함.  
⬥ 외부 원격 연결에 의한 시스템 종료 시작을 유발한 해당 remoted 프로세스의 UUID인 5AB9FEDB-537F-37F0-85FE-01D07D00A86F를 추출함.

**030**  
질문: How much time elapsed between Tom reading a phone number and sending their first message on a different platform? (Format: HH:MM:SS.sss)

오답: 00:01:32.548 

⬥ iPhone의 X 앱 그룹 DB 파일 1998824521952800768-dmv2.db-wal에 접근함.  
⬥ 전화번호가 적힌 X DM 메시지를 Tom이 읽은 시간(Read receipt) 2025-12-12 00:41:54.019 UTC를 확인함.  
⬥ Signal 앱 로그 파일 NSELogs/org.whispersystems.signal.SignalNSE 2025-12-12--00-43-26-938.log를 조회하여 Tom이 첫 메시지를 전송한 시간 2025-12-12 00:43:26.567 UTC를 확인함.  
⬥ 두 시간의 차이(00:43:26.567 \- 00:41:54.019)를 계산하여 경과 시간인 00:01:32.548을 추출함.

정답: 00:02:32.077

⬥ iPhone의 X DM 이벤트 시퀀스를 이벤트 서명 키(ID: 1999278251005403136\) 기준으로 재분석하여 Tom이 전화번호 메시지를 실제로 읽은 정밀 시간 2025-12-12 00:40:54.490 UTC를 교차 확인함.  
⬥ Signal 알림 로그를 통해 Tom의 첫 텍스트 메시지 전송 시간 2025-12-12 00:43:26.567 UTC를 확인함.  
⬥ 정확한 읽은 시간과의 차이(00:43:26.567 \- 00:40:54.490)를 재계산하여 최종 경과 시간인 00:02:32.077을 추출함.  
**3.3 2026 CTF 이미지\_iPhone14Plus**

**이미지 기본 정보**

| 이미지명 | iPhone14Plus |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_iPhone14Plus |
| 문항 수  | 16 |
| 실험자 | 진세라 |
| 정답률 | 10/16(62%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 015 | @mrbeast or mrbeast | @mrbeast | T(3) | instagram cache file의 user id 확인 |
| 016 | headphones | headphones | T | Autopsy calender entry object ID : 481014 |
| 017 | 2025-12-12 18:00:10 | 2025-12-12 18:00:10 | T(2) | `com.apple.mobile.ldbackup.plist`에서 `lastCloudBackupDate`, `CloudBackupEnabled`, `lastCloudBackupTZ` 필드를 확인. `com.apple.MobileBackup.plist`의 백업 성공 기록과 관련 캐시 및 스냅샷 데이터베이스의 수정 시각을 교차 검증  |
| 018 | 472.01 | 1,968.54 | F(3) | Apple Health의 healthdb\_secure.sqlite-wal에서 일별 걷기 달리기 기록 |
| 019 | 3 | \- | F(3) | iMessage/SMS, Gmail, X, DM, Zangi, Instagram DM, 휴대폰 검색 인덱스, signal 및 session(암호화) 대화 기록 조회 |
| 020 | Social Networking | Social Networking | T(2) | iTunesMetadata.plist에서 App Store 장르 정보 조회 |
| 021 | McLaren Senna | McLaren Senna | T | DCIM/100APPLE/IMG\_0001.WEBP (Object 141903), Safari 방문 기록(maclaren senna 검색기록), Photos.sqlite(사진출처, 메타데이터) |
| 022 | Long Island MacArthur Airport | Long Island MacArthur Airport | T(2) | `cache_encryptedB.db`의 `LteCellLocation` 테이블에서 특정 시각의 LTE 기지국 위치 기록을 조회  |
| 023 | how-a-turbo-works.gif | how-a-turbo-works.gif | T | iCloud Drive DB 조회해 파일별 태그 정보 확인 후 purple태그 파일 확인 |
| 024 | fun festive sweater | fun festive sweater | T | Depop활동로그(atevents.sqlite-wal)에서 ‘Fun Festive sweater’검색 결과 열람 |
| 025 | “The Panda” or “Panda” | \- | F |  |
| 026 | 44.4758453, \-73.2134094 | latitude 44.4758453, longitude \-73.2134094 | T | untapped cache에서 맥주 체크인 기록 등 확인 |
| 027 | 49354 | 49354 | T | safari history에서 google oauth인증 과정 확인 |
| 028 | sipposed | \- | F | [sms.db](http://sms.db)의 iMessage/SMS 메시지 조회 |
|  029 | 7FF3F4981CB5B10251CC57580B9C | 5AB9FEDB-537F-37F0-85FE-01D07D00A86F | F(3) | `shutdown.log`에서 마지막 종료 기록의 프로세스 `remoted`(PID 1925)를 확인  |
| 030 | 00:02:32.077 | \- | F | Zangi 데이터베이스(`zangidb_9193129592.sqlite`)에서 Tom의 첫 메시지 “this Alex?”와 전송 시각(2025-12-12 17:09:15.925 UTC)을 확인  |

**AI 답변 및 실행 근거 상세 기록**  
015  
질문 : What Instagram handle does User ID 2278169415 belong to?  
정답 : @mrbeast  
1차:

* Autopsy 분석 결과 및 Instagram/Threads 앱 캐시, DB에서 해당 ID(2278169415) 미발견.  
* 기기 계정은 hazyalex2002 (Alex Maurie, ID: 79726424276)만 확인됨.  
* 바이너리 판독 한계로 인해 ig-msys-...db SQLite 직접 열람 및 Autopsy 임시 폴더 접근 필요성 명시.

2차 :

* 케이스 재검증 및 iLEAPP 보고서, Instagram 앱 캐시 재확인했으나 ID 미발견 상태 유지.  
* 바이너리 형태 데이터 판독을 위한 원본 파일 접근 권한 요청.

3차:

* Instagram 앱 캐시 파일(ig-ranking-data-ig-ranking-entity-ids-to-entities-and-additional-user-info.plist, Object ID 112429)에서 데이터 발견 성공.  
* User ID 2278169415는 Instagram 핸들 **@mrbeast** (표시 이름: MrBeast)에 해당함.  
* share\_extension, ig\_share\_sheet, call\_recipients 등의 추천 연락처 목록에 포함되어 있음 확인.

016  
질문 : What item does the user need to buy for Christmas?  
정답 : headphones  
1차:

* 캘린더 일정(Object ID 481014)에서 **"Buy headphones for Christmas"** 기록 확인.  
* 2025년 12월 22일 종일 일정 (시작 시각: 2025-12-21 15:00 UTC \= 한국 시간 22일 00:00).

017  
질문 : In UTC when was the last iCloud backup? (YYYY-MM-DD HH:MM:SS)  
정답 : 2025-12-12 18:00:10  
1차:

* /private/var/mobile/Library/Preferences/com.apple.MobileBackup.plist 파일 분석.  
* 백업 성공 시각 바이너리 8바이트 중 일부 텍스트 손상으로 **2025-12-12 17:53:04 \~ 18:01:36 UTC** 범주만 추정.  
* 정확한 초 단위 확인을 위해 plist viewer로 BackupStateInfo 확인 또는 iLEAPP HTML 보고서 검증 필요 명시.

2차 :

* /private/var/mobile/Library/Preferences/com.apple.mobile.ldbackup.plist (Object ID 138667\) 파일 분석 완료.  
* LastCloudBackupDate \= 787,255,210 (Mac Absolute Time: 2001-01-01 기준 초) \-\> **2025-12-12 18:00:10 UTC** (기기 타임존 GMT-5 기준 13:00:10) 도출.  
* cloudkit\_cache.db-wal (18:00:10 UTC) 및 백업 스냅샷 DB 수정 시각(18:00:11 UTC)과 일치 확인.

018  
질문 : What was the farthest distance the user logged in meters? (Round to the nearest hundredth)  
정답 : 1,968.54  
1차:

* healthdb\_secure.sqlite DB 내 8바이트 부동소수점 데이터가 Autopsy 텍스트 변환 시 누락되어 소수점 둘째 자리까지의 정확한 거리 산출 불가.  
* 수동 검증 결과 가장 큰 수치는 0x405F로 시작하는 약 124\~128m 범주로 추정되나 확정 불가.  
* 정확한 값 도출을 위해 원본 DB 파일(healthdb\_secure.sqlite 및 \-wal) 추출 후 SQLite 쿼리(SELECT ROUND(MAX(q.quantity),2) FROM samples s JOIN quantity\_samples q ON q.data\_id \= s.data\_id WHERE s.data\_type \= 8;) 실행 필요 명시.

019  
질문 : How many people did the user message expressing concern about Daniel?  
정답 : \-  
1차:

* Autopsy 내 파싱된 iMessage(13건 중 "STOP" 제외 본문 공란) 및 메시지/연락처 키워드 검색("Daniel") 결과 미발견.  
* 원본 메시지 DB (sms.db) 및 sms.db-wal 미해독으로 메시지 내용 확인 불가.  
* 정확한 메시지 확인을 위해 iLEAPP 보고서 폴더 (ModuleOutput\\iLEAPP) 접근 승인 또는 sms.db, sms.db-wal 파일 디코딩 필요 명시.

2차:

* 다니엘(Daniel Jones, djones.iss.secure@gmail.com)에 관해 우려(concern)를 표현한 메시지가 확인 가능한 메시징 앱상에서 발견되지 않아 인원수 확정 불가.  
* 앱별 검토 결과:  
  * **iMessage/SMS**: 인증번호 및 통신사 공지 외 내용 없음.  
  * **Gmail**: 다니엘 본인에게 보낸 이메일 2건만 존재 (우려 표현 없음).  
  * **X (Twitter) DM**: Tom Blizzard와의 대화 중 Signal 번호 전달 내역만 존재.  
  * **Zangi / Instagram DM**: 관련 내용 없음.  
* 열람 불가 앱 (Signal, Session): 키체인이 포함되지 않아 데이터베이스가 암호화되어 있음.  
* 우려 메시지는 암호화된 Signal 또는 Session 앱 내에 존재할 가능성이 높으며, 해독을 위해서는 복호화된 키체인 또는 분석 보고서가 필요함을 파악함.


020  
질문 : What genre of app did the user download the most of?  
정답 : Social Networking  
1차:

* 자의적 인앱 기능 분류 기준 분석 시 Messaging / chat 장르가 5개(Gmail 포함 6개)로 가장 많은 것으로 판단.

2차 :

* 앱스토어 공식 메타데이터(iTunesMetadata.plist) 기준 재분석 실행.  
* **Social Networking** 장르가 총 7개(Telegram, Signal, Session, SimpleX Chat, Zangi, Threads, Letterboxd)로 가장 많이 설치됨 확인.

021  
질문 : What is the make and model of the car that was photographed without an iPhone?  
정답 : McLaren Senna  
1차:

* iPhone이 아닌 Mac 웹캠(Photo Booth)으로 촬영된 사진(Object ID 142033\) 메타데이터 발견.  
* 텍스트 판독 한계로 차종 확정이 불가하여 이미지 파일 추출 열람 권장.

2차 :

* 외부 다운로드 이미지 IMG\_0001.WEBP (Safari 저장, 2025-12-11) 및 검색 기록 분석.  
* 검색 기록 내 **"maclaren senna"** (2025-12-11 15:25 UTC) 및 이미지 검색 태그(Hypercar/Supercar/Coupe)를 종합하여 **McLaren Senna**로 강력 추정.

022  
질문 : What airport was the phone near when it pinged off of a cell tower on 2025-12-16 22:47:24 (UTC)?  
정답 : Long Island MacArthur Airport  
1차:

* 기기 위상 위치 캐시 DB (/private/var/root/Library/Caches/locationd/cache\_encryptedB.db, LteCellLocation 테이블) 분석.  
* 타임스탬프 787618044.995 (Apple time) \= **2025-12-16 22:47:24.995 UTC**.  
* 해당 시각 접속 기지국 좌표 클러스터 중심: 위도 **40.82° N**, 경도 **73.03° W**.  
* 해당 좌표 주변 인근 공항: **Long Island MacArthur Airport (ISP)** (New York).

023  
질문 : What is the name including extension of the purple tagged file?  
정답 : how-a-turbo-works.gif  
1차:

* Autopsy 분석 결과 태그가 없어 파일 앱(Files app) 내 태그 정보 검색 필요성 명시.  
* CloudDocs/session/db/client.db 데이터베이스 검색 진행 권장.

2차:

* iCloud Drive 데이터베이스 (CloudDocs/session/db/client.db) 수동 분석 완료.  
* Purple 태그가 저장된 유일한 레코드의 파일명: **how-a-turbo-works.gif**.

024  
질문 : What secondhand item was the user searching for?  
정답 : fun festive sweater  
1차:

* 중고 의류 거래 앱 Depop의 활동 로그 (Documents/atevents.sqlite-wal) 분석.  
* 2025-12-11 18:43:26 \~ 18:56:06 UTC 간 검색 및 상품 보기 기록 확인.  
* 검색/추천 키워드: **fun festive sweater**.

025   
질문 : What is the mascot of the frozen dessert shop that the user visits a lot?  
정답 : \-  
1차:

* Apple Maps 장소 캐시 DB (com.apple.geod/Vault/PDPlaceCache.db-wal) 분석 결과 자주 찾은 디저트 가게는 버몬트주 벌링턴의 **Shy Guy Gelato** (198 St Paul St)로 확인.  
* 캐시 내 디저트 가게 웹사이트 및 로고 이미지 열람 불가로 마스코트 미확정.

2차:

* 웹 검색 및 로고 사진 검토 진행.  
* 로고 이미지 상에서 **판다(Panda)** 마스코트가 시각적으로 노출되나, 텍스트상으로 마스코트명이 서술된 기록은 기기 데이터 및 관련 기사/블로그 리뷰에서 발견되지 않음.

3차:

* 웹사이트(shyguygelato.com) 및 Yelp 페이지 차단, 기기 내 마스코트 관련 텍스트 부재로 최종 미확정 유지.  
* 로고 내 그림(판다) 직접 검증 또는 매장 공식 웹사이트 조회가 필요함을 명시.

026  
질문 : What are the recorded coordinates of the place the user went to comment about a certain adult beverage?  
정답 : latitude 44.4758453, longitude \-73.2134094  
1차:

* 맥주 체크인 앱 Untappd 캐시 데이터 (\[com.untappdllc.com/fsCachedData/\](https\://com.untappdllc.com/fsCachedData/)) 분석.  
* 2025-12-11 19:25:52 UTC 시점 **JP's Pub** (139 Main St, Burlington, VT)에서 Budweiser 체크인 및 별점 1.5점 남김 확인.  
* 장소에 기록된 좌표: **latitude 44.4758453, longitude \-73.2134094**. *(참고: 기기 검색 시점 실제 측정 좌표: 44.47385397, \-73.21355093)*

027  
질문 : What port was the host directed through for a sign-in?  
정답 : 49354  
1차:

* Safari 방문 기록 (2025-12-09 12:45 UTC) 내 Google 로그인 리다이렉션 경로 분석.  
* OAuth 인가 요청 리다이렉트 URI: \[http\://127.0.0.1:49354\](http\://127.0.0.1:49354).  
* 최종 로그인 완료 후 이동된 로컬 포트: **49354**.

028  
질문 : What word did the user misspell, then correct before sending over text on a Friday? (Format: type the misspelled word as-is)  
정답 : \-  
1차:

* Autopsy의 iOS 메시지 데이터 파싱 한계로 attributedBody 및 message\_summary\_info 원본 열람 불가.  
* sms.db, sms.db-wal, sms.db-shm 원본 추출 후 수동 디코딩 필요 명시.

029  
질문 : What is the UUID of the process that is related to an initiated shutdown?  
정답 : 오답(5AB9FEDB-537F-37F0-85FE-01D07D00A86F)  
1차:

* 종료 진단 로그 (/private/var/db/diagnostics/shutdown.log) 분석.  
* 모든 종료 시점마다 공통으로 존재하는 커널 프로세스 kernel (pid 0\) UUID: **359DB623-5C72-3BF3-B5D2-785FB581FFF7**.  
* 개별 종료 시점별 잔여 프로세스:  
  * 가장 최근 종료 시 프로세스 remoted (pid 1925\) UUID: 5AB9FEDB-537F-37F0-85FE-01D07D00A86F

  * 가장 자주 출현한 프로세스 CommCenter UUID: C4F3503B-A47B-3FF8-AF3F-29A9C8C35318

030  
질문 : How much time elapsed between Tom reading a phone number and sending their first message on a different platform? (Format: HH:MM:SS.sss)  
정답 : \-  
1차:

* 다른 플랫폼(Zangi 앱, zangidb\_9193129592.sqlite)에서의 첫 번째 메시지 전송 시각은 확인됨.  
  * 메시지: **"this Alex?"**

  * 전송 시각: **2025-12-12 17:09:15.925 UTC** (Message ID: msgId1765559355925 기반 ms 타임스탬프)  
* 그러나 전화번호를 읽은(Read) 시점의 타임스탬프를 발견하지 못하여 경과 시간 산출 불가.  
  * Session, Signal, Telegram, SimpleX 등의 암호화 메시징 앱 데이터 직접 판독 불가.  
  * iMessage (sms.db) 내 해당 기록 없음.  
* 정확한 시간 차 계산을 위해 iLEAPP 리포트 폴더(ModuleOutput\\iLEAPP) 접근 또는 해당 메신저의 읽은 시각 타임스탬프 보완 필요 명시.

**4\. 2026 CTF 이미지\_MacBookPro**

**이미지 기본 정보**

| 이미지명 | MacBookPro |
| :---: | :---: |
| 연도 | 2026 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 81.6GB |
| 출처 | https\://cfreds.nist.gov/all/Hexordia/2026MVSCTFMac |
| Autopsy Case명 | 26\_MacBookPro |
| 대상 OS | iOS |
| 문항 수  | 17 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 031 | SALTED-SHA512-PBKDF2 | SALTED-SHA512-PBKDF2 | SALTED-SHA512-PBKDF2 | T |
| 032 | 2025-12-10 18:53:49 **OR** 2025-12-10 18:53:50 (round or chop off decimals) | \- | 2025-12-10 18:53:50  | T(50%) |
| 033 | 39.0 **OR** 39 | 39 | 42 | T(50%) |
| 034 | Asphalt 9 **OR** Asphalt Legends: Racing Game **OR** Asphalt Legends | Asphalt (또는 Asphalt 9\) | Asphalt 9 | T |
| 035 | 4 | 4 | 4 | T |
| 036 | 351906515098518 | 351906515098518 | 351906515098518 | T |
| 037 | 68DC219D-1135-49E2-8D1C-542BEBAC903A | 68DC219D-1135-49E2-8D1C-542BEBAC903A | 68DC219D-1135-49E2-8D1C-542BEBAC903A | T |
| 038 | 2025-12-01  | 2025-12-01 | 2025-12-01  | T |
| 039 | 3.9.6 | 3.9.6 | 3.9.6 | T |
| 040 | 04:BC:6D:D2:0D:90 | 04:BC:6D:D2:0D:90 | 04:BC:6D:D2:0D:90  | T |
| 041 | C4:04:15:8B:A5:8F | C4:04:15:8B:A5:8F | C4:04:15:8B:A5:8F  | T |
| 042 | 10.32 | 10.32 | 10.32 | T |
| 043 | 7506837257 **OR** 9251250272 | 약 9.84 GB (또는 6.4\~8.6 GB) | 9,251,225,696 to 9,251,258,208 bytes  | F |
| 044 | 52733820-0C3F-4E07-934B-E31167E9490A | 1094.329 | 7Ef5Jz6oCy1O0Qxs2/5gjkj5rd/A8AtGYt45dCaz358=  | F |
| 045 | 6 | 6 | 6 | T |
| 046 | b399473d58a8d601369be898a30ada8b000248d7 | b399473d58a8d601369be898a30ada8b000248d7 | b399473d58a8d601369be898a30ada8b000248d7 | T |
| 047 | 20:45 | 20:43 | 20:42 | F |

| NO | Question |
| :---: | ----- |
| 031 | What is the password hashing algorithm for the "alexmaurie" user? |
| 032 | At what time did the user last access a URL using Siri in UTC? (Format: YYYY-MM-DD HH:MM:SS) |
| 033 | What was the lowest battery level the device reached? |
| 034 | What was the name of the racing game the user installed? |
| 035 | How many tasks did the user have on 2025-12-10? |
| 036 | What is the IMEI of the connected iPhone? |
| 037 | What is the UUID of the ZSH terminal session restored on 2025-11-20 19:31:51 (UTC)? |
| 038 | What date did Alex become eligible to work at ISS? (Format: YYYY-MM-DD) |
| 039 | What version of Python did the user have installed? |
| 040 | What is the Bluetooth address of Alex's iPhone? |
| 041 | What's the MAC address of the router that the user was leased on 2025-12-24 09:48:49 (UTC)? |
| 042 | How many seconds did it take for the system to totally install a 3rd-party cloud storage app? (Format: xx.xx) |
| 043 | What was the logical size of the second most recent backup? |
| 044 | What was the value associated with the most recent iCloud operation? |
| 045 | How many total knight moves were played? |
| 046 | What is the exec\_cdhash of the event that occurred at 2025-12-01 09:23:52 PM? |
| 047 | At what time (UTC 24hr time, format HH:MM) did the user join the network of a cafe on the first day of the month? |

**4.1 2026 CTF 이미지\_MacBookPro**

**이미지 기본 정보**

| 이미지명 | MacBookPro |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_MacBookPro |
| 문항 수  | 17 |
| 실험자 | 박제윤 |
| 정답률 | 13/17(76%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 DB/아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 031 | SALTED-SHA512-PBKDF2 | SALTED-SHA512-PBKDF2 | T | /private/var/db/dslocal/nodes/Default/users/alexmaurie.plist |
| **032** | **2025-12-10 18:53:49 OR 2025-12-10 18:53:50 (round or chop off decimals)** | **\-** | **F(3)** | **Web History, Cookies, Timeline, HashtagImages app snapshots** |
| **033** | **39.0 OR 39** | **39** | **T(2)** | **/private/var/log/powermanagement/\*.asl** |
| 034 | Asphalt 9 **OR** Asphalt Legends: Racing Game **OR** Asphalt Legends | Asphalt (또는 Asphalt 9\) | T | /Library/Receipts/InstallHistory.plist |
| **035** | **4** | **4** | **T(3)** | **Apple Notes database, Tasks for today** |
| 036 | 351906515098518 | 351906515098518 | T | /private/var/wireless/Library/Preferences/com.apple.commcenter.device\_specific\_nobackup.plist |
| 037 | 68DC219D-1135-49E2-8D1C-542BEBAC903A | 68DC219D-1135-49E2-8D1C-542BEBAC903A | T | /Users/alexmaurie/.zsh\_sessions/, 68DC219D-1135-49E2-8D1C-542BEBAC903A.session |
| 038 | 2025-12-01 | 2025-12-01 | T | /Users/alexmaurie/Documents/i-9\_template.pdf |
| 039 | 3.9.6 | 3.9.6 | T | /Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/3.9/, Resources/Info.plist |
| 040 | 04:BC:6D:D2:0D:90 | 04:BC:6D:D2:0D:90 | T | /Library/Bluetooth/com.apple.MobileBluetooth.ledevices.paired.db-wal |
| 041 | C4:04:15:8B:A5:8F | C4:04:15:8B:A5:8F | T | /private/var/db/dhcpclient/leases/en0.plist |
| 042 | 10.32 | 10.32 | T | /private/var/log/install.log |
| **043** | **7506837257 OR 9251250272** | **약 9.84 GB (또는 6.4\~8.6 GB)** | **F(3)** | **.../2025-11-26-105508.backup/backup\_manifest.plist, .com.apple.timemachine.checkpoint, com.apple.MobileBackup.plist** |
| **044** | **52733820-0C3F-4E07-934B-E31167E9490A** | **1094.329** | **F(3)** | **/private/var/mobile/Library/Preferences/com.apple.MobileBackup.plist** |
| 045 | 6 | 6 | T | i am terrible at chess.game |
| 046 | b399473d58a8d601369be898a30ada8b000248d7 | b399473d58a8d601369be898a30ada8b000248d7 | T | /private/var/protected/xprotect/db/XPdb, events |
| **047** | **20:45** | **20:43** | **F(3)** | **Biome/streams/restricted/Device.Wireless.WiFi**  |

**AI 답변 및 실행 근거 상세 기록**  
**031**  
질문: What is the password hashing algorithm for the "alexmaurie" user?

정답: SALTED-SHA512-PBKDF2

⬥ MacBook Pro (LogicalFileSet3)의 계정 Directory Services 레코드 파일인 /private/var/db/dslocal/nodes/Default/users/alexmaurie.plist에 접근함.  
⬥ 해당 plist 파일 내 authentication\_authority 및 ShadowHashData 필드를 분석함.  
⬥ 로컬 로그인 인증용 패스워드 해시 알고리즘으로 SALTED-SHA512-PBKDF2 (HMAC-SHA512 및 솔트 기반 PBKDF2)가 사용되었음을 확인하여 답을 추출함.

**032**  
질문: At what time did the user last access a URL using Siri in UTC? (Format: YYYY-MM-DD HH:MM:SS)

오답1: \-

⬥ Autopsy MCP 툴 기본 기능만으로는 Siri의 URL 접근 아티팩트가 추출되지 않음.  
⬥ 해당 데이터는 Mac(/Users/alexmaurie/Library/Application Support/Knowledge/knowledgeC.db) 또는 iPhone(/private/var/mobile/Library/CoreDuet/Knowledge/knowledgeC.db)의 원본 knowledgeC.db 파일에 수록되어 있음.  
⬥ 텍스트 파싱 시 바이너리 타임스탬프 바이트가 손상(?로 변환)되므로, 해당 DB 파일들에 대한 직접 SQLite 쿼리 조회가 필요함을 확인함.

오답2: \-

⬥ Autopsy 파일 리더의 바이너리 파싱 한계로 knowledgeC.db 열람을 위해 폴더 접근 권한을 요청했으나 거부됨.  
⬥ 정확한 타임스탬프 산출을 위해 Mac 및 iPhone의 knowledgeC.db, \-wal, \-shm 파일들을 직접 추출하여 첨부하거나 폴더 접근 권한 부여가 필요함을 명시함.

오답3: \-

⬥ 폴더 접근 요청이 재차 거부되어 Siri URL 접근 시각에 대한 추가 검색이 최종 중단됨.  
⬥ 정답 확인을 위해서는 Autopsy에서 knowledgeC.db (및 WAL, SHM) 파일들을 Extract File(s)로 추출한 후 직접 쿼리를 수행해야 함을 최종 파악함.

**033**  
질문: What was the lowest battery level the device reached?

오답: \-

⬥ macOS의 Powerlog DB 파일인 CurrentPowerlog.PLSQL 및 아카이브 파일들(.../Library/BatteryLife/Archives/powerlog\_\*.PLSQL)에 접근함.  
⬥ 배터리 기록 테이블인 PLBatteryAgent\_EventBackward\_Battery 조회가 필요하나, 텍스트 검색 툴의 한계로 바이너리 데이터 수치를 파싱하지 못함.  
⬥ 정답 추출을 위해 해당 .PLSQL 파일들을 추출하여 SELECT MIN(Level), timestamp FROM PLBatteryAgent\_EventBackward\_Battery; 쿼리를 실행해야 함을 명시함.

정답: 39

⬥ macOS 전원 관리 로그 파일인 /private/var/log/powermanagement/\*.asl을 부분 조회함.  
⬥ 2025년 12월 24일 21:45 UTC경 충전기(AC) 연결 직전 기록된 최저 배터리 수치가 39%임을 확인하여 답을 도출함.  
⬥ 다만 수면/깨어남 이벤트 시점에만 기록되는 ASL 로그의 특성과 일부 미확인 구간이 존재하므로, 정밀 최저 수치 확인에는 Powerlog DB 전체 쿼리가 필요함을 명시함.

**034**  
질문: What was the name of the racing game the user installed?

정답: Asphalt (또는 Asphalt 9\)

⬥ MacBook Pro의 설치 이력 로그 파일인 /Library/Receipts/InstallHistory.plist에 접근함.  
⬥ 설치 로그 테이블의 packageIdentifiers 필드가 com.gameloft.asphalt9mac이고 displayName 필드가 Asphalt인 레코드를 확인함.  
⬥ 해당 앱이 Mac App Store(appstoreagent)를 통해 2025-11-26 19:42:09 UTC에 설치된 Gameloft의 Asphalt 9 레이싱 게임임을 확인하여 답을 추출함.

**035**  
질문: How many tasks did the user have on 2025-12-10?

오답1: 37

⬥ iPhone 및 MacBook의 Apple Reminders(미리알림) 앱 데이터를 확인한 결과 총 37개의 할 일 항목을 확인함.  
⬥ 36개는 식재료 품목("1 cup chicken broth" 등)이고, 1개는 크리스마스 헤드폰 구매 항목("Buy headphones for Christmas", 마감일 12월 21\~22일)임.  
⬥ 모두 2025년 11월 25\~27일 사이에 생성되었으므로 12월 10일 기준 열려있는 총 항목 수는 37개로 추산함.

오답2: 37

⬥ Reminders DB의 동기화 이력 및 미완료 상태를 재검증하여 37개의 할 일(식재료 36개 \+ 헤드폰 구매 1개)이 12월 10일 시점에도 완료 처리되지 않고 유지되었음을 확인함.  
⬥ 단, 12월 10일 당일이 마감일(Due date)로 지정된 항목은 존재하지 않아 마감일 기준 시 0개임을 명시함.

정답: 4

⬥ MacBook의 Apple Notes 앱에서 Tasks for today라는 제목의 메모를 발굴하여 기존 Reminders 기반 추론을 수정함.  
⬥ 해당 메모는 2025년 12월 10일에 수정된 기록이 있으며, 아래 4가지 체크리스트 항목이 수록되어 있음을 확인함:

1. Look for an ID scanner  
2. Look for alarm system  
3. Find out what camera client wants to pick  
4. What is a mantrap? And look for one.

⬥ 당일 웹 검색 기록(CCTV 보안 카메라 사이트 접속)과의 정황상 일치 여부를 교차 확인하여 최종 답을 4개로 도출함. 

**036**  
질문: What is the IMEI of the connected iPhone?

정답: 351906515098518

⬥ iPhone의 셀룰러 설정 파일인 /private/var/wireless/Library/Preferences/com.apple.commcenter.device\_specific\_nobackup.plist에 접근함.  
⬥ imeis 키 아래 저장된 슬롯 1(primary)의 IMEI 주소인 351906515098518을 확인하여 답을 추출함.

**037**  
질문: What is the UUID of the ZSH terminal session restored on 2025-11-20 19:31:51 (UTC)?

정답: 68DC219D-1135-49E2-8D1C-542BEBAC903A

⬥ MacBook의 ZSH 세션 저장 경로인 /Users/alexmaurie/.zsh\_sessions/에 접근함.  
⬥ 68DC219D-1135-49E2-8D1C-542BEBAC903A.session 파일 내 복원 시각 타임스탬프(1763667111)가 2025-11-20 19:31:51 UTC와 정확히 일치함을 확인하여 해당 UUID를 추출함.

**038**  
질문: What date did Alex become eligible to work at ISS? (Format: YYYY-MM-DD)

정답: 2025-12-01

⬥ MacBook의 양식 파일인 /Users/alexmaurie/Documents/i-9\_template.pdf (Form I-9)에 접근함.  
⬥ 근로 자격 검증 섹션의 서명 날짜 필드인 Today's Date (Section 1\)에 기록된 12/1/2025를 확인하고 요청된 포맷(YYYY-MM-DD)으로 변환하여 답을 추출함.

**039**  
질문: What version of Python did the user have installed?

정답: 3.9.6

⬥ MacBook의 Xcode Command Line Tools 경로인 /Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/3.9/에 접근함.  
⬥ 프레임워크 내 Resources/Info.plist 파일의 CFBundleShortVersionString 필드값이 3.9.6으로 지정되어 있음을 확인하여 답을 추출함.

**040**  
질문: What is the Bluetooth address of Alex's iPhone?

정답: 04:BC:6D:D2:0D:90

⬥ MacBook의 블루투스 페어링 DB 로그 파일인 /Library/Bluetooth/com.apple.MobileBluetooth.ledevices.paired.db-wal에 접근함.  
⬥ "Alex's iPhone" 기기 레코드의 고정 하드웨어 주소 필드인 Address / Resolved address 값 04:BC:6D:D2:0D:90을 확인하여 답을 추출함.

**041**  
질문: What's the MAC address of the router that the user was leased on 2025-12-24 09:48:49 (UTC)?

정답: C4:04:15:8B:A5:8F

⬥ MacBook의 Wi-Fi DHCP 임대 저장 파일인 /private/var/db/dhcpclient/leases/en0.plist에 접근함.  
⬥ 2025-12-24 21:48:49 UTC(12시간제 표현 시 09:48:49 PM)의 Router hardware address Base64 값(xAQVi6WP)을 디코딩하여 라우터 MAC 주소인 C4:04:15:8B:A5:8F를 추출함.

**042**  
질문: How many seconds did it take for the system to totally install a 3rd-party cloud storage app? (Format: [xx.xx](http://xx.xx))

정답: 10.32

⬥ macOS 설치 로그 파일인 /private/var/log/install.log에 접근함.  
⬥ 2025-12-09 Google Drive (GoogleDrive.pkg) 첫 설치 기록의 최종 요약 정보(\-total-)에 기록된 시간인 10.32초를 확인하여 답을 추출함.

**043**  
질문: What was the logical size of the second most recent backup?

오답1: 약 9.84GB(9,839,861,120 \~ 9,848,184,319 bytes)

⬥ Time Machine 설정 파일(/Library/Preferences/com.apple.TimeMachine.plist)을 확인하여 두 번째로 최신 백업이 2025-11-26 15:55 UTC (2025-11-26-105508) 백업임을 확인함.  
⬥ 해당 백업 폴더의 요약 파일 backup\_manifest.plist 내 logicalSize 바이너리 바이트(02 4A ?? 5D ??)를 확인했으나, 손상된 바이트로 인해 정확한 정수 대신 약 9.84 GB 범위를 추출함.

오답2: 약 6.45 \~ 8.58 GB (6,449,872,649 \~ 8,580,579,081 bytes)

⬥ 2025-12-12 백업 폴더 내 backup\_manifest.plist에 기록된 2025-11-26 백업 레코드의 'Changed(새로 복사된)' 데이터 크기를 재분석함.  
⬥ 원본 바이트 01 ?? 71 3F 09를 해독하여 2025-11-26 백업의 실제 로지컬 크기 범위를 6.45 \~ 8.58 GB로 교정함.

오답3: 약 9.84 GB (또는 6.4\~8.6 GB)

⬥ Time Machine의 backup\_manifest.plist 바이너리 데이터 손상 문제로 인해 해석 방식에 따른 두 가지 수치 범위를 비교 요약함:

1. 해석 A (의도된 기본값): 2025-11-26 백업 자체 요약 파일의 레코드 (0x024A??5D??) $\rightarrow$ 9,839,861,120 \~ 9,848,184,319 bytes (약 9.84 GB)  
2. 해석 B (후속 백업 기록): 2025-12-12 요약 파일에 명시된 11-26 백업 엔트리 (0x01??713F09) $\rightarrow$ 6,449,872,649 \~ 8,580,579,081 bytes (약 6.4 \~ 8.6 GB)

⬥ 정확한 byte 단위 정답 입력을 위해서는 plutil \-p 명령어를 사용해 stats $\rightarrow$ changed $\rightarrow$ logicalSize 원본 값을 직접 디코딩해야 함을 밝힘.

**044**  
질문: What was the value associated with the most recent iCloud operation?

오답1: SHA256:7Ef5Jz6oCy100Qxs2/5gjkj5rd/A8AtGYt45dCaz358=

⬥ MacBook의 Apple iCloud 에스크로(계정 복구) 로그 파일인 sbd-operation-log.plist에 접근함.  
⬥ 2025-11-26 20:23:50 UTC에 수행된 가장 최근의 작업 레코드를 확인함.  
⬥ 해당 에스크로 작업의 Record ID (value) 필드값인 SHA256:7Ef5Jz6oCy100Qxs2/5gjkj5rd/A8AtGYt45dCaz358=을 추출함.

오답2: SHA256:7Ef5Jz6oCy100Qxs2/5gjkj5rd/A8AtGYt45dCaz358= 또는 100

⬥ /Library/Daemon Containers/.../Data/sbd-operation-log.plist 파일을 재검증함.  
⬥ 가장 최근 에스크로 작업의 recordId는 SHA256:7Ef5Jz6oCy100Qxs2/5gjkj5rd/A8AtGYt45dCaz358=이며, 해당 액티비티의 수치형 타입 코드는 100임을 교차 확인하여 명시함.

오답3: 1094.329

⬥ iPhone의 iCloud 백업 상태 파일인 /private/var/mobile/Library/Preferences/com.apple.MobileBackup.plist 내 LastOnConditionEvents 로그를 검증하여 이전 에스크로 로그 기반 정답을 수정함.  
⬥ 가장 최근 백업 이벤트인 2025-12-12 12:31:19 EST (17:31:19 UTC)의 로그 라인 2025-12-12T12:31:19.351-05:00\|1094.329\|1\|1\|0\|1\|1\|0\|1398\|0\|86095\|0\|0\|2\|1\|1\|1\|0을 확인함.  
⬥ 타임스탬프 바로 뒤에 기록된 작업 소요 시간(초) 값인 1094.329를 추출함.

**045**  
질문: How many total knight moves were played?

정답: 6

⬥ iCloud Drive Documents 폴더 내 저장된 Apple 체스 게임 파일 i am terrible at chess.game에 접근함.  
⬥ 체스 기보를 재생하여 나이트(Knight) 이동 기보(\#3 Ng1-h3, \#12 Nb1-c3, \#17 Nb8-c6, \#18 Nc6-a5, \#19 Ng8-f6, \#21 Nf6-e4)를 분석함.  
⬥ 백(White) 2회, 흑(Black) 4회로 수행된 전체 나이트 이동 횟수가 총 6회임을 확인하여 답을 추출함.

**046**  
질문: What is the exec\_cdhash of the event that occurred at 2025-12-01 09:23:52 PM?

정답: b399473d58a8d601369be898a30ada8b000248d7

⬥ MacBook의 XProtect 행위 DB인 /private/var/protected/xprotect/db/XPdb 파일 내 events 테이블에 접근함.  
⬥ 2025-12-01 21:23:52 UTC (9:23:52 PM UTC) 시각에 기록된 Chrome 이벤트 행(id: 27)을 조회함.  
⬥ 해당 레코드의 exec\_cdhash 필드값인 b399473d58a8d601369be898a30ada8b000248d7을 확인하여 답을 추출함.

**047**  
질문: At what time (UTC 24hr time, format HH:MM) did the user join the network of a cafe on the first day of the month?

오답1: 20:42

⬥ MacBook Wi-Fi 로그(\~/Library/Biome/streams/restricted/Device.Wireless.WiFi/...)를 확인하여 2025년 12월 1일 접속한 카페 네트워크가 uncommonqburyguest임을 밝혀냄.  
⬥ 타임스탬프 바이트 손상으로 접속 시각 범위가 20:41:37 \~ 20:45:51로 파악되었으나, 접속 후 첫 웹 검색(20:44:35 UTC) 시각을 교차 분석하여 20:42로 추정함.

오답2: 20:42

⬥ Wi-Fi 로그 인덱스 레코드(\#3)를 확인하여 2025-12-01 카페 네트워크 접속 시각 범위(20:41:37 \~ 20:45:51)를 재검증함.  
⬥ XProtect 로그 내 Chrome 이벤트 시각(20:42:56 UTC)과 교차 분석하여 유력한 분 단위 시각을 20:42로 제시함.

오답3: 20:43

⬥ XProtect 이벤트 DB(XPdb) 분석 결과, 맥북이 활성화된 시각(runningboardd, Safari widget, Finder 작동)이 20:42:56임을 확인함.  
다른 날짜의 깨어남 직후 Wi-Fi 연결 소요 시간 패턴과 첫 웹 검색 시각(20:44:35)을 종합하여 접속 구간을 20:42:56 \~ 20:44:35 사이로 좁히고 가장 유력한 시각으로 20:43을 도출함.  
**4.3 2026 CTF 이미지\_MacBookPro**

**이미지 기본 정보**

| 이미지명 | MacBookPro |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_MacBookPro |
| 문항 수  | 17 |
| 실험자 | 진세라 |
| 정답률 | 13/17(76%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 031 | SALTED-SHA512-PBKDF2 | SALTED-SHA512-PBKDF2 | Ｔ | alexmaurie 사용자 계정 레코드의 ShadowHashData plist (시스템 볼륨 및 Data 볼륨의 APFS 사본)  |
| 032 | 2025-12-10 18:53:49 **OR** 2025-12-10 18:53:50 (round or chop off decimals) | 2025-12-10 18:53:50  | Ｔ | macOS Biome `App.Intent` 스트림 파일 (`com.apple.parsecd` 서비스 기록) 및 Safari 방문 기록 DB (`History.db`)  |
| 033 | 39.0 **OR** 39 | 42 | Ｆ | Powerlog DB (private/var/db/powerlog/Library/BatteryLife/CurrentPowerlog.PLSQL 및 \-wal, Archives/ 파일) 및 전원 관리 로그 (private/var/log/powermanagement/ 내 .asl 파일)  |
| 034 | Asphalt 9 **OR** Asphalt Legends: Racing Game **OR** Asphalt Legends | Asphalt 9 | Ｔ | 쓰레기통 경로(/Users/alexmaurie/.Trash/Asphalt.app)에 위치한 번들 내 Info.plist 파일 및 앱 번들 속성 정보 |
| 035 | 4 | 4 | T | Apple Notes 데이터베이스인 /Users/alexmaurie/Library/Group Containers/group.com.apple.notes/NoteStore.sqlite 및 해당 \-wal 파일  |
| 036 | 351906515098518 | 351906515098518 | T(3) | Apple ID 계정 기기 목록 DB인 /Users/alexmaurie/Library/Application Support/com.apple.akd/devicelist.db의 device\_list 테이블 (additional\_info 필드)  |
| 037 | 68DC219D-1135-49E2-8D1C-542BEBAC903A | 68DC219D-1135-49E2-8D1C-542BEBAC903A | Ｔ | 사용자 홈 디렉터리의 \~/.zsh\_sessions/ 폴더 내 .session 파일 및 동일 세션의 .history 파일  |
| 038 | 2025-12-01 | 2025-12-01  | Ｔ | 사용자 Documents 폴더 내 서명된 Form I-9 PDF 파일인 Documents/i-9\_template.pdf |
| 039 | 3.9.6 | 3.9.6 | Ｔ | Xcode Command Line Tools 내 `/Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/3.9/Resources/Info.plist` 및 실행 파일 `bin/python3.9`  |
| 040 | 04:BC:6D:D2:0D:90 | 04:BC:6D:D2:0D:90  | Ｔ | 페어링된 블루투스 LE 기기 DB 로그 파일인 `/Library/Bluetooth/com.apple.MobileBluetooth.ledevices.paired.db-wal`의 `PairedDevices` 테이블  |
| 041 | C4:04:15:8B:A5:8F | C4:04:15:8B:A5:8F  | Ｔ | Wi-Fi 인터페이스의 DHCP 대여 정보 파일인 /private/var/db/dhcpclient/leases/en0.plist (및 /System/Volumes/Data/ 하위 사본)  |
| 042 | 10.32 | 10.32 | T | mac installer log records(/private/var/log/install.log) |
| 043 | 7506837257 **OR** 9251250272 | 9,251,225,696 to 9,251,258,208 bytes  | F | Time Machine 백업 폴더 내부의 백업 매니페스트 파일인 backup\_manifest.plist |
| 044 | 52733820-0C3F-4E07-934B-E31167E9490A | 7Ef5Jz6oCy1O0Qxs2/5gjkj5rd/A8AtGYt45dCaz358=  | F | iCloud 키체인 백업 로그 파일인 sbd-operation-log.plist (/Users/alexmaurie/Library/Daemon Containers/741BDBD8-DF2A-481F-8041-F8EBDF63C0A8/Data/sbd-operation-log.plist 및 /System/Volumes/Data 사본)  |
| 045 | 6 | 6 | T | 사용자 iCloud Documents 내 macOS Chess 저장 파일인 i am terrible at chess.game |
| 046 | b399473d58a8d601369be898a30ada8b000248d7 | b399473d58a8d601369be898a30ada8b000248d7 | T | XProtect Behavior Service DB인 /private/var/protected/xprotect/db/XPdb 의 events 테이블  |
| 047 | 20:45 | 20:42 | F | 저장된 Wi-Fi 목록 plist (/Library/Preferences/com.apple.wifi.known-networks.plist) 및 macOS Biome Wi-Fi 스트림 로그 (/Users/alexmaurie/Library/Biome/streams/restricted/Device.Wireless.WiFi/local/785865828566727)  |

**AI 답변 및 실행 근거 상세 기록**  
031  
질문 : What is the password hashing algorithm for the "alexmaurie" user?  
정답 : SALTED-SHA512-PBKDF2  
1차:

* Autopsy 계정 테이블 미인덱싱으로 shadow 파일 분석 진행.  
* alexmaurie 계정의 ShadowHashData 내 비밀번호 해싱 알고리즘 확인.  
* 기본 대화형 로그인 알고리즘: SALTED-SHA512-PBKDF2 (HMAC-SHA512 기반 PBKDF2). *(참고: 원격/네트워크 인증용으로는 SRP-RFC5054-4096-SHA512-PBKDF2 함께 저장됨)*

032  
질문 : At what time did the user last access a URL using Siri in UTC? (Format: YYYY-MM-DD HH:MM:SS)  
정답 : 2025-12-10 18:53:50   
1차:

* macOS Biome App.Intent 스트림 및 Safari 방문 기록 분석.  
* Siri를 통해 연 최신 URL: \[https\://x.com/\](https\://x.com/).  
* Safari 방문 타임라인 분석:  
  * \[x.com/\](https\://x.com/) 접속: 18:53:50 UTC  
  * 로그인 페이지: 18:54:16 UTC  
  * 로그인 후 리다이렉트(\[x.com/\](https\://x.com/), /home): 18:56:12 UTC  
* 이벤트 순서상 최초 사이트 열람을 유도한 Siri 실행 시각: 2025-12-10 18:53:50 (UTC).

033  
질문 : What was the lowest battery level the device reached?  
정답 : 오답(42)  
1차:

* Autopsy 내 배터리 관련 데이터 직접 파싱 불가.  
* CurrentPowerlog.PLSQL DB 및 powermanagement/\*.asl 로그 파일 분석 필요성 명시.  
* 샘플 텍스트 확인 중 12월 24일 DarkWake 기록에서 42%가 포착되었으나 전체 최저 수치는 아니며, 원본 파일 직접 쿼리 필요함을 파악함.

2차 :

* 12월 24일 자 로그 일부(\~31 KB)에서 단편적으로 읽힌 값: 42% (DarkWake), 48% (Sleep/Wake), 43% (DarkWake).  
* 전체 .asl 로그(약 3.8 MB) 검색 한계로 확정 수치 제출 불가.

3차 :

* Powerlog DB 및 systemstats/\*.battery\_charge.stats, powermanagement/\*.asl 전수 검토.  
* 단편적 판독 최저치(42%) 외 전체 최저 배터리 잔량을 확정하려면 Autopsy 내 키워드 검색(Charge:) 재실행 또는 원본 DB 파일 추출 후 MIN(Level) 쿼리 조회가 필수임을 재확인.

034  
질문 : What was the name of the racing game the user installed?  
정답 : Asphalt 9  
1차:

* 위치: /Users/alexmaurie/.Trash/Asphalt.app (휴지통 이동 확인).  
* Bundle ID: com.gameloft.asphalt9mac.  
* App category: public.app-category.racing-games.  
* Facebook display name / 제품명: Gameloft의 Asphalt 9 (Display name: Asphalt).  
* Info.plist 생성/수정 시각: 2025-10-21 17:23 UTC.

035  
질문 : How many tasks did the user have on 2025-12-10?  
정답 : 4  
1차:

* Apple Notes 노트명 "Tasks for today" (NoteStore.sqlite, Note ID: 5CFBF8D5-77FF-461C-BA07-6A21E4A638C4) 분석.  
* 2025-12-10 날짜로 생성 및 편집된 작업 목록 총 4개 확인:  
  1. Find out what camera client wants to pick  
  2. Look for alarm system  
  3. Look for an ID scanner  
  4. What is a mantrap? And look for one.  
* Reminders 및 Calendar 앱에는 해당 날짜의 작업 기록 없음 확인.

036  
질문 : What is the IMEI of the connected iPhone?  
정답 : 351906515098518  
1차:

* 계정 신뢰 기기 DB (/Users/alexmaurie/Library/Application Support/com.apple.akd/devicelist.db, device\_list 테이블) 분석.  
* 연동 기기: Alex's iPhone (iPhone14,8 / iPhone 14 Plus, Serial: FH49Q1TVX6).  
* IMEI (SIM slot 1): 351906515098518 (Luhn 검증 통과).

037  
질문 : What is the UUID of the ZSH terminal session restored on 2025-11-20 19:31:51 (UTC)?  
정답 : 68DC219D-1135-49E2-8D1C-542BEBAC903A  
1차:

* \~/.zsh\_sessions/ 폴더 내 세션 파일 분석.  
* 세션 파일명: 68DC219D-1135-49E2-8D1C-542BEBAC903A.session.  
* 내부 복원 스크립트 epoch 타임스탬프 (1763667111) \= 2025-11-20 19:31:51 UTC 일치 확인.

038  
질문 : What date did Alex become eligible to work at ISS? (Format: YYYY-MM-DD)  
정답 : 2025-12-01   
1차:

* Documents/i-9\_template.pdf (Form I-9) 서류 분석.  
* Section 1 근로 자격 확인란 서명 날짜: 2025-12-01 (생성 시각: 2025-12-01 21:33 UTC).  
* Section 2 (고용주 작성란)의 "First Day of Employment" 항목은 비어 있음 명시.

039  
질문 : What version of Python did the user have installed?  
정답 : 3.9.6  
1차:

* Xcode Command Line Tools 번들 Python 경로 (/Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/3.9/) 분석.  
* Resources/Info.plist 기준 버전: 3.9.6.  
* Homebrew 설치 버전(Cellar/python)은 없음 확인.

040  
질문 : What is the Bluetooth address of Alex's iPhone?  
정답 : 04:BC:6D:D2:0D:90   
1차:

* 페어링된 Bluetooth LE DB WAL 파일 (/Library/Bluetooth/com.apple.MobileBluetooth.ledevices.paired.db-wal) 분석.  
* Alex's iPhone 주소: 04:BC:6D:D2:0D:90 (Public address).

041  
질문 : What's the MAC address of the router that the user was leased on 2025-12-24 09:48:49 (UTC)?  
정답 : C4:04:15:8B:A5:8F   
1차:

* Wi-Fi DHCP 임대 설정 파일 (/private/var/db/dhcpclient/leases/en0.plist) 분석.  
* LeaseStartDate: 2025-12-24T21:48:49Z (12시간 표기 시 09:48:49 PM에 해당).  
* RouterHardwareAddress Base64 값 (xAQVi6WP) 디코딩 결과: C4:04:15:8B:A5:8F.

042  
질문 : How many seconds did it take for the system to totally install a 3rd-party cloud storage app? (Format: xx.xx)  
정답 : 오답(10.32)  
1차:

* macOS 설치 로그 (/private/var/log/install.log) 분석.  
* 대상 앱: Google Drive (GoogleDrive.dmg, 2025-12-09 설치).  
* Summary Information 내 \-total- 경과 시간: 10.32 초 (install: 10.31 초, PackageKit 패키지 작성 시간: 7.8 초).


043  
질문 : What was the logical size of the second most recent backup?  
정답 : 오답(9,251,225,696 to 9,251,258,208 bytes )  
1차:

* Time Machine 백업 3건 중 두 번째 최신 백업(2025-11-26 10:55:08) 확인.  
* 바이너리 backup\_manifest.plist 파일 판독 제한으로 원본 파일 직접 열람 필요성 안내.

2차 :

* 2025-12-12-162727.backup/backup\_manifest.plist 내부 기록 분석.  
* logicalSize, changed data: 6.45 GB \~ 8.58 GB 범위 추정 (바이너리 바이트 손상).  
* logicalSize, propagated data: 약 9.25 GB (9,251,225,696 \~ 9,251,258,208 bytes).

3차 :

* changed 영역의 logicalSize 필드 Raw value(0x0001 ?? 71 3F 09\) 내 누락 바이트(??)로 인해 6.45 GB \~ 8.58 GB 사이의 exact byte 수치를 추정 없이 확정할 수 없음을 밝힘.  
* 정확한 값 확인을 위해 Autopsy의 Plist viewer에서 stats \-\> changed \-\> logicalSize 트리 직접 확인 권장.

044  
질문 : What was the value associated with the most recent iCloud operation?  
정답 : 오답(7Ef5Jz6oCy1O0Qxs2/5gjkj5rd/A8AtGYt45dCaz358=)  
1차:

* iCloud Keychain 보안 백업 로그 (/Users/alexmaurie/Library/Daemon Containers/.../sbd-operation-log.plist) 분석 (2025-11-26 20:23:50 UTC 작성).  
* 가장 최근 작업: cdpd: type=SignIn; endpoint=HandleCloudDataProtectionState; backupActivity=CheckAndRemoveExistingThenEnableSecureBackupRecord

* 연관 레코드 ID 값: SHA256:7Ef5Jz6oCy1O0Qxs2/5gjkj5rd/A8AtGYt45dCaz358=

2차 :

* 로그 전체 및 기타 iCloud 소스(CloudKit, Notes sync 등) 재검증 진행.  
* 해당 로그 내 최신 작업의 recordId 값인 SHA256:7Ef5Jz6oCy1O0Qxs2/5gjkj5rd/A8AtGYt45dCaz358= 상태 유지 보완.

045  
질문 : How many total knight moves were played?  
정답 : 6  
1차:

* iCloud Documents 내 macOS Chess 저장 파일 i am terrible at chess.game 분석 (2025-11-26 대국).  
* 총 나이트(Knight) 이동 횟수: 6회

  * 백(White) 2회: Move 3 (g1-h3), Move 12 (b1-c3)  
  * 흑(Black) 4회: Move 17 (b8-c6), Move 18 (c6-a5), Move 19 (g8-f6), Move 21 (f6-e4)

046  
질문 : What is the exec\_cdhash of the event that occurred at 2025-12-01 09:23:52 PM?  
정답 : b399473d58a8d601369be898a30ada8b000248d7  
1차:

* XProtect Behavior Service DB (/private/var/protected/xprotect/db/XPdb, events 테이블) 분석.  
* 2025-12-01 21:23:52 (UTC 기준 09:23:52 PM) 이벤트 행 조회.  
* violated\_rule: macOS.QntDb.Generic (Google Chrome 실행 관련).  
* exec\_cdhash: b399473d58a8d601369be898a30ada8b000248d7.

047  
질문 : At what time (UTC 24hr time, format HH:MM) did the user join the network of a cafe on the first day of the month?  
정답 : 오답(20:42)  
1차:

* 저장된 Wi-Fi 목록 (com.apple.wifi.known-networks.plist) 분석.  
* 카페 네트워크 PANERA 접속 기록은 12월 10일(19:31 UTC)로, 매월 1일 접속 건이 아니어서 정확한 시각을 도출하지 못함.

2차 :

* Biome Wi-Fi 스트림 DB (.../Biome/streams/restricted/Device.Wireless.WiFi/...) 수동 해석 진행.  
* 2025-12-01 날짜의 카페 네트워크: Uncommon Grounds (uncommonqburyguest).  
* 접속 시간 범위: 20:41:36 \~ 20:45:52 UTC 사이.  
* 재부팅 시각(20:42:05) 및 첫 Google 검색 시각(20:44:35)을 종합하여 부팅 직후 자동 접속 시각인 20:42로 강력 추정하나, 바이트 손상으로 분 단위 확정을 위해 Hex view 추가 검증 필요 명시.

**6\. 2025 CTF 이미지\_Windows 11**

**이미지 기본 정보**

| 이미지명 | Windows 11 |
| :---: | :---: |
| 연도 | 2025 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 123GB |
| 출처 | [2025CTF](https://drive.google.com/drive/folders/1gHQsfx1hqCv-V4Anm2eYukB4jPtraNBH) |
| Autopsy Case명 | 25\_Windows11 |
| 대상 OS | Windows 11 |
| 문항 수  | 19 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 048 | S-1-5-21-493923485-410185161-2094537482-1001 | S-1-5-21-493923485-410185161-2094537482-1001 | S-1-5-21-493923485-410185161-2094537482-1001 | T |
| 049 | 2024-11-24 17:36:55 | 2024-11-23 05:01:26 | 2024-11-23 05:01:26 UTC | F |
| 050 | https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg | https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg | https\://www\.treehugger.com | T |
| 051 | Candy Crush Saga | Candy Crush Saga | Candy Crush Saga | T |
| 052 | X | X | X | T |
| 053 | Reddit | Reddit | Reddit | T |
| 054 | Python | Python | Python | T |
| 055 | 2024-09-24 15:11:51 | 2024-09-24 15:11:51 | 2024-09-24 15:11:51 | T |
| 056 | Something’s Fishy | Something’s Fishy | Something’s Fishy | T |
| 057 | sucess.txt.txt | sucess.txt.txt | SDelete | T(50%) |
| 058 | Proton Mail | Proton Mail | Proton Mail | T |
| 059 | Edge | Microsoft Edge | Microsoft Edge | T |
| 060 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 UTC | T |
| 061 | 12-6 | 12-6 | 12 | T |
| 062 | geomaryr | geomaryr | geomaryr | T |
| 063 | fRlLkVPTrliLVAGhQRWjQd.kKDyvvjO4OaDd5zoJRt4 | \- | \- | F |
| 064 | wandering4cache | \- | wandering4cache | T(50%) |
| 065 | steghide |  | SDelete | F |
| 066 | marywuzhere | \- | \- | F |

| NO | Question |
| :---: | ----- |
| 048 | What is the SID for the user “chick”? |
| 049 | When was the last logoff time for the user “chick”? (YYYY-MM-DD HH:MM:SS) |
| 050 | What is the host URL that crow.jpg was downloaded from? |
| 051 | What popular game was installed on the computer?  |
| 052 | On what social media platform did Mary look at a Burlington news account?  |
| 053 | Where did Mary look for help with her coding questions?  |
| 054 | What language was Mary's first program written in?  |
| 055 | What is the creation date for Mary’s user account? (YYYY-MM-DD HH:MM:SS) |
| 056 | What was the name of the geocache that was completed?  |
| 057 | What file was an anti-forensics tool used on?  |
| 058 | What email service is Mary using other than gmail?  |
| 059 | What is the default browser set as?  |
| 060 | What time was the tiktok that Mary watched posted? (YYYY-MM-DD HH:MM:SS UTC) |
| 061 | What was the suggestion count when Mary was going to play a popular word-based browser game?  |
| 062 | What is Mary’s username on geocaching.com? |
| 063 | What is the hashed password for the user “chick”?  |
| 064 | What was the username of the person who saw the clouds coming in at 6:30 while doing a geocache? |
| 065 | What suspicious command line tool was installed on Mary’s system?  |
| 066 | What does the file sucess.txt.txt contain?  |

**6.1 2025 CTF 이미지\_Windows 11**

**이미지 기본 정보**

| 이미지명 | Windows 11 |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 25\_Windows11 |
| 문항 수  | 19 |
| 실험자 | 박제윤 |
| 정답률 | 14/19(73%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 048 | S-1-5-21-493923485-410185161-2094537482-1001 | S-1-5-21-493923485-410185161-2094537482-1001 | T | C:\\Users\\chick\\NTUSER.DAT |
| **049** | **2024-11-24 17:36:55** | **2024-11-23 05:01:26** | **F(3)** | **NTUSER.DAT** |
| 050 | https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg | https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg | T | Microsoft Edge History DB |
| 051 | Candy Crush Saga | Candy Crush Saga | T | C:\\Program Files\\WindowsApps\\[king.com](http://king.com).CandyCrushSaga\_1.2901.2.0\_x64\_\_kgqvnymyfvs32 |
| 052 | X | X | T | Microsoft Edge History DB |
| 053 | Reddit | Reddit | T | Microsoft Edge History DB |
| 054 | Python | Python | T | AppData\\Roaming\\Code\\User\\History\\4f2e0e45\\sAGV.py |
| **055** | **2024-09-24 15:11:51** | **2024-09-24 15:11:51** | **T(2)** | **SAM\\Domains\\Account\\Users\\Names\\chick** |
| 056 | Something’s Fishy | Something’s Fishy | T | Microsoft Edge History DB |
| 057 | sucess.txt.txt | sucess.txt.txt | T | ConsoleHost\_history.txt, SDELETE.EXE |
| 058 | Proton Mail | Proton Mail | T | Microsoft Edge History DB |
| 059 | Edge | Microsoft Edge | T | NTUSER.DAT, Software\\Microsoft\\Windows\\Shell\\Associations\\UrlAssociations |
| 060 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 | T | Microsoft Edge History DB |
| 061 | 12-6 | 12-6 | T | Microsoft Edge History DB |
| 062 | geomaryr | geomaryr | T | Microsoft Edge History DB |
| **063** | **fRlLkVPTrliLVAGhQRWjQd.kKDyvvjO4OaDd5zoJRt4** | **\-** | **F(3)** | **\-** |
| **064** | **wandering4cache** | **geomaryr** | **F(3)** | **Cache\_Data, Microsoft Edge History** |
| **065** | **steghide** | **Kali Linux** | **F(3)** | **C:\\Program Files\\WindowsApps\\KaliLinux.54290C8133FEE\_1.2024.3.0\_x64\_\_...\\kali.exe, AppRepository, C:\\Users\\chick\\AppData\\Local\\Packages\\KaliLinux.54290C8133FEE\_ey8k8hqnwqnmg\\LocalState\\ext4.vhdx, Installed Programs List** |
| **066** | **marywuzhere** | **\-** | **F(3)** | **LNK, [Windows.db](http://Windows.db), ...Microsoft.WindowsNotepad\_8wekyb3d8bbwe\\LocalState\\TabState\\, ConsoleHost\_history.txt, MFT** |

**AI 답변 및 실행 근거 상세 기록**  
**048**  
질문: What is the SID for the user “chick”?

정답: S-1-5-21-493923485-410185161-2094537482-1001

⬥ Autopsy의 OS 계정 정보 분석 결과(Autopsy: Get os accounts)를 확인함.  
⬥ 사용자 계정 chick에 할당된 보안 식별자(SID) 필드값이 S-1-5-21-493923485-410185161-2094537482-1001로 명시되어 있음을 확인하여 정답을 도출함.  
⬥ RID가 1001인 것으로 보아 시스템에서 생성된 첫 번째 로컬 사용자 계정이며, 홈 디렉터리는 C:/Users/chick임.

**049**  
질문: When was the last logoff time for the user “chick”? (YYYY-MM-DD HH:MM:SS)

오답1: \-

⬥ 사용자 로그오프 이벤트(Event ID 4634 또는 4647)가 기록되는 Security.evtx 파일이 파싱되지 않음.  
⬥ 외부 폴더 접근 거부로 인해 직접 로그오프 이벤트를 읽지 못하여 정답을 추출하지 못함.

오답2: \-

⬥ 폴더 접근 요청이 거부되어 chick 계정(SID 끝자리 \-1001)의 로그오프 시각을 계속 산출하지 못함.  
⬥ Autopsy 서버를 통한 Security.evtx 파싱 또는 파일 직접 첨부 필요성을 안내함.

오답3: 2024-11-23 05:01:26

⬥ chick 계정의 레지스트리 프로필 파일인 NTUSER.DAT의 최종 수정 시각인 2024-11-23 05:01:26 UTC (한국 시간 14:01:26)를 확인함.  
⬥ Windows 시스템은 로그오프 시 해당 사용자 프로필(NTUSER.DAT)을 디스크에 기록하므로, 해당 시각을 로그오프 시점으로 추론함.  
⬥ 동일 시각 SAM 파일 수정 및 약 1분 뒤(05:02:48) SMB 클라이언트 로그 작성 정황이 이를 뒷받침함.

**050**  
질문: What is the host URL that crow.jpg was downloaded from?

정답: [https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg](https://www.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill\(auto,1\)/__opt__aboutcom__coeus__resources__content_migration__mnn__images__2019__10__american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg)

⬥ chick 계정의 Microsoft Edge 다운로드 기록 DB(History)를 파싱함.  
⬥ crow.jpg 파일의 다운로드 URL \[https\://www\.treehugger.com/thmb/EmZ0vx28sGNqCtDqQQBMGv-aezM=/4288x2848/\](https\://www\.treehugger.com/thmb/EmZ0vx28sGNqCtDqQQBMGv-aezM=/4288x2848/)...을 확인함.  
⬥ 호스트 URL이 \[www\.treehugger.com\](https\://www\.treehugger.com)임을 추출함.

**051**  
질문: What popular game was installed on the computer?

정답: Candy Crush Saga

⬥ 파일 시스템 내 Microsoft Store 앱 설치 경로인 C:\\Program Files\\WindowsApps\\king.com.CandyCrushSaga\_1.2901.2.0\_x64\_\_kgqvnymyfvs32를 확인 함.  
⬥ 설치된 실행 파일 candycrushsaga.exe 및 chick 계정의 AppData 경로 내 관련 데이터가 2024-11-15에 생성된 정황을 확인하여 인기 게임인 Candy Crush Saga를 정답으로 도출함.

**052**  
질문: On what social media platform did Mary look at a Burlington news account?

정답: X

⬥ Edge 방문 기록에서 Burlington 지역 언론사 계정인 @bfp\_news (Burlington Free Press) 접속 기록 \[https\://x.com/bfp\_news\](https\://x.com/bfp\_news)를 확인함.  
⬥ 해당 방문이 소셜 미디어 플랫폼 X (구 Twitter)에서 이루어졌음을 확인하여 정답을 추출함.

**053**  
질문: Where did Mary look for help with her coding questions?

정답: Reddit

⬥ Edge 방문 기록에서 "coding" 검색 후 접속한 서브레딧 페이지 \[reddit.com/search/?q=coding\](https\://reddit.com/search/?q=coding) 및 r/coding 내 게시물 방문 이력을 확인함.  
⬥ 코딩 질문에 대한 도움을 찾은 사이트가 Reddit임을 도출함.

**054**  
질문: What language was Mary's first program written in?

정답: Python

⬥ VS Code의 로컬 편집 이력 내 소스 파일 경로 C:\\Users\\chick\\import random.py (AppData\\Roaming\\Code\\User\\History\\...)를 파싱함.  
⬥ 2024-11-12 16:10:13 UTC에 처음 작성된 숫자 맞추기 게임 코드가 Python 언어로 작성되었음을 확인하여 정답을 추출함.

**055**  
질문: What is the creation date for Mary’s user account? (YYYY-MM-DD HH:MM:SS)

오답: 2024-09-24 15:11:52

⬥ Mary(계정명 chick)의 최초 로그인 시 생성된 프로필 폴더(C:\\Users\\chick), 레지스트리 파일(NTUSER.DAT, UsrClass.dat) 및 기본 시작 메뉴 바로가기 파일들의 타임스탬프인 2024-09-24 15:11:52 UTC를 확인함.  
⬥ SAM 레지스트리 파일(C:\\Windows\\System32\\config\\SAM) 바이너리 데이터 손상으로 인해 프로필 최초 생성 시각을 계정 생성 시점의 대체값(stand-in)으로 도출함.

정답: 2024-09-24 15:11:51

⬥ SAM 레지스트리 파일 내 사용자 계정 엔트리 경로 SAM\\Domains\\Account\\Users\\Names\\chick 및 RID 레코드(Users\\000003E9)에 접근함.  
⬥ 손상된 8바이트 타임스탬프(41 7D 21 15 ?? 0E ?? 01) 중 2024년 날짜 구조 및 프로필 생성 시각(15:11:52)과의 선후 관계를 재구성하여 2024-09-24 15:11:51 UTC (한국 시각 2024-09-25 00:11:51)을 정밀 계산해 정답을 도출함.

**056**  
질문: What was the name of the geocache that was completed?

정답: Something’s Fishy

⬥ chick(Mary) 계정의 Edge 방문 기록에서 Geocaching 페이지 \[geocaching.com/geocache/GCM70J\](https\://geocaching.com/geocache/GCM70J)를 확인함.  
⬥ 해당 캐시의 웹페이지 제목이 GCM70J Something’s Fishy (Traditional Cache)...이며, 로그 작성 페이지(/live/geocache/gcm70j/log) 접속 이력을 확인하여 정답을 Something’s Fishy로 도출함.

**057**  
질문: What file was an anti-forensics tool used on?

정답: success.txt.txt

⬥ 안티포렌식 도구인 SDelete(Sysinternals 보안 삭제 유틸리티) 사용 이력을 PowerShell 명령어 기록(ConsoleHost\_history.txt) 및 Prefetch 로그에서 확인함.  
⬥ 바탕화면 경로의 특정 파일 C:\\Users\\chick\\Desktop\\sucess.txt.txt에 대해 SDelete 명령어가 실행되어 파일명이 ZZZZZZ.ZZZ.ZZZ로 변경 후 완전 삭제된 정황을 확인하여 정답을 추출함.

**058**  
질문: What email service is Mary using other than gmail?

정답: Proton Mail

⬥ Edge 방문 기록에서 Proton Mail 수신함 페이지 (7) Inbox \| hackergotyou@proton.me \| Proton Mail 및 가입 접속 페이지(account.proton.me/mail/signup) 이력을 확인함.  
⬥ Gmail 외에 사용 중인 이메일 서비스가 Proton Mail임을 도출함.

**059**  
질문: What is the default browser set as?

정답: Microsoft Edge

⬥ 사용자 레지스트리 NTUSER.DAT 내 기본 앱 설정 경로(Software\\Microsoft\\Windows\\Shell\\Associations\\UrlAssociations)의 http 및 https 프로토콜 연결 프로그램이 MSEdgeHTM으로 지정되어 있음을 확인함.  
⬥ 시스템 기본 브라우저가 Microsoft Edge로 설정되어 있음을 확인하여 정답을 도출함.

**060**  
질문: What time was the tiktok that Mary watched posted? (YYYY-MM-DD HH:MM:SS UTC)

정답: 2024-11-12 22:11:09

⬥ Edge 방문 기록의 TikTok 동영상 URL \[https\://www\.tiktok.com/@dochristmass/video/7436518844501347616\](https\://www\.tiktok.com/@dochristmass/video/7436518844501347616)을 파싱함.  
⬥ TikTok 비디오 ID 7436518844501347616의 상위 32비트 Unix 타임스탬프(7436518844501347616 \>\> 32 \= 1731449469)를 디코딩하여 게시 시각이 2024-11-12 22:11:09 UTC임을 정확히 산출함.

**061**  
질문: What was the suggestion count when Mary was going to play a popular word-based browser game?

정답: 12-6

⬥ Wordle 게임 플레이를 위해 Bing 검색창에 "wordle"을 입력할 당시의 검색 링크 URL ...\&pq=wordle\&sc=12-6...을 분석함.  
⬥ Bing 검색 URL 파라미터 sc=12-6에서 sc는 자동완성 제안 수(12) \- 검색어 길이(6)를 의미하므로 자동완성 추천 개수가 12개임을 도출함.

**062**  
질문: What is Mary’s username on [geocaching.com](http://geocaching.com)?

정답: geomaryr

⬥ Gmail 가입 확인 메일을 통해 클릭한 geocaching.com 계정 인증 URL \[https\://www\.geocaching.com/account/join/validateaccount?code=...\&username=geomaryr\](https\://www\.geocaching.com/account/join/validateaccount?code=...\&username=geomaryr)을 확인함.  
⬥ URL 파라미터 username에 명시된 사용자명이 geomaryr임을 확인하여 정답을 도출함.

**063**  
질문: What is the hashed password for the user “chick”?

오답1: \-

⬥ Windows SAM 하이브에서 사용자 계정(chick)의 NT/LM 비밀번호 해시 추출을 요청했으나, 자격 증명 탈취 및 크래킹/패스 더 해시 공격 위험으로 인해 출력이 거부됨.  
⬥ 분석 대상 파일이 포렌식 증거일지라도 해시 추출은 수행되지 않음을 명시함.

오답2: \-

⬥ SAM 비밀번호 해시(NT/LM 해시)가 암호 크래커 입력 또는 Pass-the-Hash 인증에 직접 악용될 수 있는 자격 증명 데이터이므로 요청을 재차 거부함.  
⬥ 계정 메타데이터(SID, 풀네임, 생성 시각), 타임라인, SDelete 이력 등 다른 포렌식 항목 분석으로 대안을 제시함.

오답3: \-

⬥ 연속된 재요청에도 불구하고 SAM 비밀번호 해시 파싱/추출 거부 정책을 최종 유지함.  
⬥ 계정 속성 정보 및 RegRipper 보고서 재검증 등 안전한 아티팩트 분석 진행을 안내함.

**064**  
질문: What was the username of the person who saw the clouds coming in at 6:30 while doing a geocache?

오답1: \-

⬥ 지오캐싱 로그("clouds coming in at 6:30")는 "Something’s Fishy" (GCM70J) 캐시 페이지에 존재함.  
⬥ Mary의 Edge 캐시 파일(data\_1 \~ data\_3) 내 해당 응답 데이터가 압축 처리되어 있어 Autopsy 텍스트 리더로 압축 해제하지 못함.  
⬥ 교차 검증 정보로 Mary의 지오캐싱 계정명이 geomaryr임은 확인했으나, 해당 로그 작성자임을 압축 해제 전까지 확정할 수 없음.

오답2: geomaryr

⬥ data\_1 및 data\_2 캐시 블록 수색 결과 원본 텍스트는 압축 상태(content-encoding:gzip)로 존재함.  
⬥ 시스템 내 유일하게 등록 및 사용된 geocaching.com 계정이 Mary의 geomaryr임.  
⬥ "Something’s Fishy" (GCM70J) 캐시 페이지 및 작성 페이지(/log) 방문 기록과 현장 정황 기록(6:30 구름 유입)을 작성한 탐색자(finder) 본인이 Mary임을 정황상 확인하여 답을 도출함.

오답3: geomaryr

⬥ 3개 캐시 블록 파일(data\_1, data\_2, data\_3) 전체를 조회하였으나 압축 해제 한계로 문자 단위 직저 파싱은 불가능함을 재확인함.  
⬥ 증거 데이터상 존재하는 유일한 지오캐싱 계정이며, "Something’s Fishy" (GCM70J) 캐시의 탐색자 노트를 작성한 사용자가 Mary(geomaryr)임을 교차 분석을 통해 최종 확정함.

**065**  
질문: What suspicious command line tool was installed on Mary’s system?

오답1: Kali Linux

⬥ Microsoft Store 패키지 경로 C:\\Program Files\\WindowsApps\\ 내에 설치된 침투 테스트/오펜시브 보안용 Linux 배포판 패키지 KaliLinux.54290C8133FEE\_1.2024.3.0\_x64\_\_... 및 실행 파일 kali.exe를 확인함.  
⬥ 2024-11-11 20:38:30 UTC에 kali.exe가 생성되었으며, 동일 날짜에 설치된 Windows Subsystem for Linux (WSL v2.3.24.0) 기반으로 실행되는 의심스러운 커맨드라인 도구임을 확인함.

오답2: Kali Linux

⬥ Mary의 사용자 프로필 경로 C:\\Users\\chick\\AppData\\Local\\Packages\\KaliLinux...\\LocalState\\ext4.vhdx (약 1.15 GB) 가상 디스크 이미지 파일 존재를 확인함.  
⬥ 2024-11-11 20:51 UTC에 최초 생성(초기 세팅)된 이후 2024-11-15 15:51 UTC까지 지속적으로 수정 및 용량이 증가하여 단순 설치를 넘어 실제 환경에서 커맨드라인 도구로 활용되었음을 재확인함.

오답3: Kali Linux

⬥ Windows AppRepository 등록 정보, 패키지 파일, WSL 가상 디스크 이미지(ext4.vhdx)의 교차 검증을 완료함.  
⬥ 시스템 내 설치된 커맨드라인 성격의 도구(OpenSSH, SDelete, FTK Imager 등) 중 가장 명확하게 의심스러운 오펜시브 보안 커맨드라인 환경인 Kali Linux를 최종 정답으로 확정함.

**066**  
질문: What does the file sucess.txt.txt contain?

오답1: \-

⬥ 해당 파일(C:\\Users\\chick\\Desktop\\sucess.txt.txt)은 안티포렌식 도구인 SDelete를 통해 데이터 덮어쓰기가 완료되어 디스크 내 원본 텍스트가 삭제됨.  
⬥ LNK 바로가기 파일 및 파일명 변경 잔재(ZZZZZZ.ZZZ.ZZZ) 등 메타데이터 정황만 존재할 뿐, 실제 내용 텍스트는 복구 불가능함을 확인함.

오답2: \-

⬥ 파일 시스템의 할당/비할당 영역, OneDrive 캐시, Windows Search 인덱스 DB(Windows.db)를 전수 조사함.  
⬥ SDelete로 파일이 완전히 와이핑되어 디스크 이미지 내에 내용 텍스트가 전혀 남아있지 않음을 재확인함.

오답3: \-

⬥ Windows 11 메모장(Notepad)의 탭 상태 캐시(.../LocalState/TabState) 파일 .bin을 파싱함.  
⬥ 2024-11-11경 메모장에서 열린 이력이 확인되었으나, 저장된 상태 데이터 커서/길이 마커(0B 0B, 약 11글자 추정)만 남았을 뿐 본문 텍스트 캐시(...1.bin)는 0바이트로 존재하지 않음.  
⬥ 이에 따라 디스크 이미지상 파일 내용을 직접 복구할 수 없음(Unrecoverable)을 최종 확정함.

**6.3 2025 CTF 이미지\_Windows 11**

**이미지 기본 정보**

| 이미지명 | Windows 11 |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 26\_Windows11 |
| 문항 수  | 19 |
| 실험자 | 진세라 |
| 정답률 | 14/19(73%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 048 | S-1-5-21-493923485-410185161-2094537482-1001 | S-1-5-21-493923485-410185161-2094537482-1001 | T | C:/Users/chick chick 계정 SID |
| **049** | **2024-11-24 17:36:55** | **2024-11-23 05:01:26 UTC** | **F(3)** | **E:\\Windows\\System32\\winevt\\Logs\\Security.evtx, NTUSER.DAT 최종수정시각** |
| 050 | https\://www\.treehugger.com/thmb/EmZOvx28sGNqCtDqQQBMGv-aezM=/4288x2848/filters:fill(auto,1)/\_\_opt\_\_aboutcom\_\_coeus\_\_resources\_\_content\_migration\_\_mnn\_\_images\_\_2019\_\_10\_\_american-crow-portrait-01-b3f0cfbdbf164de59831c9725bfdbf67.jpg | https\://www\.treehugger.com | T | Bing검색(crow bird), Edge History,  C:\\Users\\chick\\Downloads\\crow.jpg  |
| 051 | Candy Crush Saga | Candy Crush Saga | T | C:\\Program Files\\WindowsApps\\king.com.CandyCrushSaga\_1.2901.2.0\_x64\_\_kgqvnymyfvs32  |
| 052 | X | X | T | Edge History, https\://x.com/bfp\_news  |
| 053 | Reddit | Reddit | T | Edge History, Reddit 검색어(coding)  |
| 054 | Python | Python | T | C:Users\\chick\\import [random.py](http://random.py), Python 3.11설치 기록 |
| 055 | 2024-09-24 15:11:51 | 2024-09-24 15:11:51 | T | 사용자 계정명, 계정 생성시각, Autopsy의 RegRipper SAM 리포트  |
| 056 | Something’s Fishy | Something’s Fishy | T | Geocaching 로그 및 방문 기록, Edge History, geocaching.com/live/geocaching/gcm70j/log  |
| **057** | **sucess.txt.txt** | **SDelete** | **F(3)** | **C:\\Users\\chick\\Desktop\\sucess.txt.txt, Recent Files ShortCut기록** |
| 058 | Proton Mail | Proton Mail | T | Edge History(회원가입 및 받은편지함 접속 url, Bing 검색어 기록) |
| 059 | Edge | Microsoft Edge | T | NTUSER.DAT(Software\\Microsoft\\Windows\\Shell\\Associations\\UrlAssociations\\) |
| 060 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 UTC | T | Edge History 내 Tiktok 열람기록(https\://www\.tiktok.com/@dochristmass/video/7436518844501347616)  |
| **061** | **12-6** | **12** | **T(3)** | **Address Bar Shortcuts DB(Users/chick/AppData/Local/Microsoft/Edge/User Data/Default/Shortcuts), Bing검색URL 매개변수, Edge History** |
| 062 | geomaryr | geomaryr | T | 수신 이메일, Edge History |
| **063** | **fRlLkVPTrliLVAGhQRWjQd.kKDyvvjO4OaDd5zoJRt4** | **\-** | **F** | **SAM레지스트리(SAM\\Domains\\Account\\Users\\000003E9), 연동 Microsoft 계정** |
| 064 | wandering4cache | wandering4cache | T | 지오캐싱 GPX 데이터 파일(C:\\Users\\chick\\Downloads\\GC365HN.gpx), GPX log data |
| **065** | **steghide** | **SDelete** | **F(3)** | **Edge 검색 이력, Jump List LNK파일, PowerSHell실행기록** |
| **066** | **marywuzhere** | **\-** | **F(3)** | **LNK, Jumplist record, 메모장 탭 캐시, C:\\Users\\chick\\Desktop\\sucess.txt.txt**  |

**AI 답변 및 실행 근거 상세 기록**

### **048**

**질문: What is the Security Identifier (SID) of the chick user account?**  
정답 : S-1-5-21-493923485-410185161-2094537482-1001

* 실행 근거:  
  * Windows 시스템 레지스트리 및 계정 설정 정보 분석 결과, chick 계정의 RID는 1001임.  
  * 홈 디렉터리 경로(C:/Users/chick) 및 Autopsy 데이터 소스("25\_Windows11") 분석을 통해 해당 계정의 완전한 SID가 S-1-5-21-493923485-410185161-2094537482-1001임을 확인 함.

### **049**

**질문: What timestamp was the user chick logged out of the system?**  
오답1 : \-

* 실행 근거:  
  * Security.evtx 이벤트 로그의 4634, 4647 레코드를 확인하려 하였으나 레지스트리 하이브 카운터 미갱신 문제로 정확한 시각 도출에 실패함.

오답2 : \-

* 실행 근거:  
  * E:\\Windows\\System32\\winevt\\Logs\\Security.evtx 이벤트 로그 파일 분석 중 파싱 상태 불량 및 바이너리 손상을 확인하여 로그아웃 시각을 특정하지 못함.

정답 : 2024-11-23 05:01:26 UTC

* 실행 근거:  
  * SYSTEM 레지스트리 하이브의 ShutdownTime 값이 2024-11-23 05:01:26Z로 기록되어 있음을 도출함.  
  * chick 계정의 NTUSER.DAT 파일 최종 수정 시각(2024-11-23 05:01:26Z)과 일치하여 시스템 종료 및 로그아웃 타임스탬프를 확정함.  
      
    

### **050**

**질문: What was the website hostname used to download crow.jpg?**  
정답 : [www\.treehugger.com](https://www.google.com/search?q=https%3A%2F%2Fwww.treehugger.com)

* 실행 근거:  
  * Microsoft Edge History 원본 데이터베이스 분석 결과, C:\\Users\\chick\\Downloads\\crow.jpg 파일의 다운로드 URL이 \[https\://www\.treehugger.com/thmb/.../american-crow-portrait-...jpg\](https\://www\.treehugger.com/thmb/.../american-crow-portrait-...jpg)임을 확인 함.  
  * 해당 다운로드 링크의 호스트네임(Hostname)을 \[www\.treehugger.com\](https\://www\.treehugger.com)으로 확인함.

### **051**

**질문: What is the full name of the popular game installed on the system from the Microsoft Store?**  
정답 : Candy Crush Saga

* 실행 근거:  
  * Microsoft Store를 통해 설치된 앱 데이터베이스 및 C:\\Program Files\\WindowsApps 경로 탐색 결과 king.com.CandyCrushSaga\_1.2901.2.0\_x64\_\_kgqvnymyfvs32 확인.  
  * 제작사 King에서 제공하는 해당 인기도 높고 유명한 게임의 정식 명칭이 Candy Crush Saga임을 입증 함.

### **052**

**질문: What account/handle on Twitter (X) did the user visit?**  
정답 : Burlington Free Press (@bfp\_news)

* 실행 근거:  
  * Microsoft Edge 브라우저 방문 기록(History DB) 검색 결과 \[https\://x.com/bfp\_news\](https\://x.com/bfp\_news) 페이지 접속 기록을 확인함.  
  * 해당 페이지의 타이틀 "BurlingtonFreePress (@bfp\_news) / X" 및 Bing 검색을 통한 유입 경로를 확인함.

### **053**

**질문: What was the name of the Reddit community searched for?**  
정답 : r/coding

* 실행 근거:  
  * Microsoft Edge History DB에서 Reddit 검색 URL \[https\://www\.reddit.com/r/coding/\](https\://www\.reddit.com/r/coding/) 접속 레코드 확인.  
  * "coding" 키워드 검색을 통해 방문한 커뮤니티가 r/coding임을 확인함.

### **054**

**질문 : What was the name of the Python script written by the user?**  
정답 : import random.py

* 실행 근거:  
  * VS Code 로컬 저장 히스토리 분석 결과 C:\\Users\\chick\\import random.py 파일 생성 기록 확인.  
  * 사용자가 작성한 코드가 1\~100 사이 숫자를 맞추는 파이썬 게임 프로그램이며, 첫 줄의 import random 코드가 그대로 파일명으로 저장된 사실을 입증함.

### **055**

**질문 : What timestamp was the chick user account created?**  
정답 : 2024-09-24 15:11:51 UTC

* 실행 근거:  
  * SAM 레지스트리 하이브 및 Autopsy의 RegRipper SAM 리포트 파싱 결과 확인.  
  * chick (Mary Jones, RID 1001\) 계정의 Account Created 원본 타임스탬프가 2024-09-24 15:11:51Z (Raw: 1727190711)로 기록되어 있음을 도출함.

### **056**

**질문: What was the name and cache code of the completed geocache?**  
정답 : Something's Fishy (GCM70J)

* 실행 근거:  
  * Edge History DB 조회 결과 \[geocaching.com/live/geocaching/gcm70j/log\](https\://geocaching.com/live/geocaching/gcm70j/log) 접속 및 로그 제출 완료 기록(luid 파라미터) 확인.  
  * 해당 지오캐시의 공식 이름이 "Something's Fishy"이고 Cache Code가 GCM70J임을 도출함.

### **057**

**질문: What anti-forensics tool was used to delete a file on the desktop and what exact time was it deleted?**  
오답1 : \-

* 실행 근거:  
  * SDelete 도구 다운로드(SDelete.zip) 및 PowerShell 실행 이력(.\\sdelete C:\\Users\\chick\\Desktop\\sucess.txt.txt)을 파악했으나, 최종 확정 답변 정리 단계 미완료.  
    

오답2 : \-

* 실행 근거:  
  * SDELETE.EXE Prefetch 생성 시각(20:12:24 UTC) 및 최종 삭제 시각(20:13:05 UTC)의 정밀 분석 결과를 정리하였으나 최종 답변 형식을 작성하지 않음.  
    

정답 : SDelete / 2024-11-12 20:13:05 UTC

* 실행 근거:  
  * Microsoft Sysinternals의 SDelete 유틸리티 사용 확인.  
  * PowerShell Console History, Prefetch 파일(SDELETE.EXE-29E0DCB3.pf), Desktop 폴더 인덱스 수정 타임스탬프를 교차 검증하여 삭제 실행 시각이 2024-11-12 20:13:05 UTC임을 확정함.

### **058**

**질문: What email address was used for the secondary email account created by the user?**  
정답 : hackergotyou@proton.me

* 실행 근거:  
  * Edge History DB 내 Proton Mail 회원가입 및 Inbox 접속 URL 분석.  
  * 페이지 타이틀 Inbox \| hackergotyou@proton.me \| Proton Mail 레코드를 통해 보조 이메일 주소가 hackergotyou@proton.me임을 확인함.

### **059**

**질문: What was the name of the default browser set on the system?**  
정답 : Microsoft Edge

* 실행 근거:  
  * NTUSER.DAT 하이브 내 Software\\Microsoft\\Windows\\Shell\\Associations\\UrlAssociations 레지스트리 키 검사.  
  * http, https, .htm, .html 관련 ProgId 값이 모두 MSEdgeHTM으로 설정되어 있어 기본 브라우저가 Microsoft Edge임을 입증함.  
      
    

### **060**

**질문: What timestamp was the TikTok video posted according to the URL?**  
정답 : 2024-11-12 22:11:09 UTC

* 실행 근거:  
  * Edge History 내 TikTok URL \[https\://www\.tiktok.com/@dochristmass/video/7436518844501347616\](https\://www\.tiktok.com/@dochristmass/video/7436518844501347616) 확인.  
  * 비디오 ID (7436518844501347616)의 상위 32비트를 Unix 타임스탬프(1731449469)로 비트 shift 디코딩하여 정확한 게시 시각이 2024-11-12 22:11:09 UTC임을 정밀 도출함.

### **061**

**질문: How many suggestions were given by Bing when searching for Wordle?**  
오답1 : 1

* 실행 근거:  
  * Edge 주소창 Shortcuts DB(Users/chick/AppData/Local/Microsoft/Edge/User Data/Default/Shortcuts)의 hit count 값(1)을 제안 수로 잘못 해석함.  
    

오답2 : \-

* 실행 근거:  
  * Bing 검색 URL 매개변수 sc=12-6을 파싱하여 제안 수가 12개임을 분석했으나 종합 정리 미완료.  
    

정답: 12

* 실행 근거:  
  * Edge 히스토리에 기록된 Bing 검색 URL \[https\://www\.bing.com/search?q=wordle&...\&sc=12-6\](https\://www\.bing.com/search?q=wordle&...\&sc=12-6)의 매개변수 디코딩 완료.  
  * sc=12-6 규격에 따라 "wordle" 6글자 입력 시 Bing이 제시한 제안(Suggestions) 개수가 12개임을 확정함.  
      
    

### **062**

**질문: What was the username chosen for the geocaching account created?**  
정답 : geomaryr

* 실행 근거:  
  * Gmail로 수신된 계정 인증 메일 "Validate your Geocaching account" 분석.  
  * Edge History DB 내 계정 인증 완료 URL (\[https\://www\.geocaching.com/account/join/validateaccount?...\&username=geomaryr\](https\://www\.geocaching.com/account/join/validateaccount?...\&username=geomaryr))을 확인하여 사용자명이 geomaryr임을 확정함.  
      
    

### **063**

**질문: What is the password hash of the chick user account?**  
오답1 : \-

* 실행 근거:  
  * SAM 레지스트리 키(SAM\\Domains\\Account\\Users\\000003E9)를 확인하였으나 NTLM 해시 복구 단계를 진행 중임.  
    

오답2 : \-

* 실행 근거:  
  * RegRipper samparse 리포트를 검토했으나 SAM V 구조체의 암호화 해제를 위한 SYSTEM bootkey/secretsdump 적용 절차를 설명함.  
    

오답3 : \-

* 실행 근거:  
  * Autopsy 도구의 바이너리 레지스트리 수집 과정에서 바이트 손상이 발생하여 NTLM 해시값을 텍스트로 바로 추출할 수 없음을 안내함.

### **064**

**질문: Who was the finder of the GC365HN micro cache according to the GPX file?**  
정답 : wandering4cache

* 실행 근거:  
  * C:\\Users\\chick\\Downloads\\GC365HN.gpx 파일 내부 XML 구조 파싱.  
  * 해당 지오캐시 로그 데이터 내 발견자 사용자명 태그 \<groundspeak:finder id="68063"\>wandering4cache\</groundspeak:finder\> 레코드를 확인 함.

### 

### **065**

**질문: What suspicious anti-forensic tool was found on the system?**  
오답1 : \-

* 실행 근거:  
  * SDelete 도구의 다운로드 파일(SDelete.zip) 및 Prefetch 항목(SDELETE.EXE-29E0DCB3.pf)을 식별했으나 정답 작성 미완료.

오답2 : \-

* 실행 근거:  
  * SDelete 외에 FTK Imager 도구과의 차이점을 검토하여 안티포렌식 도구로서의 SDelete 특성을 정리함.

정답: SDelete

* 실행 근거:  
  * Bing 검색어("sdelete download"), 다운로드 및 압축 해제 경로(Downloads\\SDelete\\), PowerShell을 통한 파일 파괴 실행 이력을 통해 시스템에서 사용된 안티포렌식 도구가 SDelete임을 입증함.  
      
    

### **066**

**질문: What file was wiped using SDelete on the desktop?**  
오답1 : \-

* 실행 근거:  
  * C:\\Users\\chick\\Desktop\\sucess.txt.txt 파일이 SDelete로 삭제되었음을 파악하고 바탕화면의 ZZZZZZ.ZZZ.ZZZ 0바이트 아티팩트를 분석함.  
    

오답2 : \-

* 실행 근거:  
  * SDelete 동작으로 인해 비할당 공간 카빙이 불가능함을 설명하고 LNK/Jump List 파일의 삭제 파일 참조 흔적을 정리함.

정답 : sucess.txt.txt (또나 C:\\Users\\chick\\Desktop\\sucess.txt.txt)

* 실행 근거:  
  * 메모장 탭 상태 캐시(TabState\\e87d7267-...bin) 및 LNK/Jump List 기록을 통해 원본 파일명이 sucess.txt.txt임을 확인함.  
  * SDelete의 파일명 변경 및 축소 동작 시그니처인 C:\\Users\\chick\\Desktop\\ZZZZZZ.ZZZ.ZZZ (크기: 0 bytes) 흔적과 PowerShell 삭제 명령어를 종합 교차 검증하여 삭제된 파일명을 확정함.

**7\. 2025 CTF 이미지\_Chromebook**

**이미지 기본 정보**

| 이미지명 | Chromebook |
| :---: | :---: |
| 연도 | 2025 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 7.66GB |
| 출처 | [2025CTF](https://drive.google.com/drive/folders/1gHQsfx1hqCv-V4Anm2eYukB4jPtraNBH) |
| Autopsy Case명 | 25\_Chromebook |
| 대상 OS | Chrome OS |
| 문항 수  | 16 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 067 | 87 | 87 | 87 | T |
| 068 | 1267  | 0x04F3(1267) | 0x04F3(=1267) | T |
| 069 | 172.19.70.25 | 172.19.70.25 | 172.19.70.25 | T |
| 070 | \+1 (802) 829-2741  | \+1 (802) 829-2741 | \+1 (802) 829-2741 | T |
| 071 | Power Button  | Lid Open | Power Button | T(50%) |
| 072 | 21 **OR** 22 | 21 | \- | T(50%) |
| 073 | 2024-11-06 01:09:41 | 2024-11-06 01:08:11 | 2024-11-06 01:08:11 | F |
| 074 | ruthonthego98@gmail.com | ruthonthego98@gmail.com | ruthonthego98@gmail.com | T |
| 075 | 373,228 | 373,228 | 373,228 | T |
| 076 | Pretty Little Liars | Pretty Little Liars | Pretty Little Liars | T |
| 077 | 253018 | 253018 | 253018 | T |
| 078 | 2024-11-16 | 2024-11-16 | 2024-11-16 | T |
| 079 | 472a3434-8989-4133-b94a-5151333e6743 | 472a3434-8989-4133-b94a-5151333e6743 | 472a3434-8989-4133-b94a-5151333e6743 | T |
| 080 | Yang Jiayu | María Pérez | María Pérez | F |
| 081 | newark | newark | Newark | T |
| 082 | 8 | \- | \- | F |

| NO | Question |
| :---: | ----- |
| 067 | What was the most recent battery level recorded by the Chromebook? |
| 068 | What is the vendor ID for the touchpad? |
| 069 | What was the ip address of the Chromebook?  |
| 070 | What number is stored in contacts? Format: \+X (XXX) XXX-XXXX |
| 071 | How was the device most commonly woken up?  |
| 072 | How many months was Mary employed with her company?  |
| 073 | When did the user first interact with a fanfiction website? (UTC) Format: YYYY-MM-DD HH:MM:SS  |
| 074 | What string was autofilled the most? |
| 075 | What is the size of Ruth’s advertisement in bytes?  |
| 076 | What TV show does Ruth have an interest in?  |
| 077 | What is the version of the noise suppression software? |
| 078 | What date was the game installed on the system? YYYY-MM-DD |
| 079 | What is the ID of the URL with the most number of hits?  |
| 080 | What is the name of the current champion of the sport Ruth was trying to learn? |
| 081 | What region had the lowest latency for Discord?  |
| 082 | How many shirts are in the ad?  |

**7.1 2025 CTF 이미지\_Chromebook**

**이미지 기본 정보**

| 이미지명 | Android |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 25\_Chromebook |
| 문항 수  | 16 |
| 실험자 | 박제윤 |
| 정답률 | 12/16(75%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| **067** | **87** | **87** | **T(2)** | **/var/log/power\_manager/powerd.20240101-200042** |
| 068 | 1267 | 0x04F3(1267) | T | /var/log/messages.1 |
| 069 | 172.19.70.25 | 172.19.70.25 | T | /var/log/net.1.log |
| 070 | \+1 (802) 829-2741 | \+1 (802) 829-2741 | T | .shadow/.../mount/ 및 home/root/ 경로 내 Android contacts DB |
| **071** | **Power Button** | **Lid Open** | **F(3)** | **/var/log/eventlog.txt** |
| **072** | **21 OR 22** | **21** | **T(3)** | **marysresume.pdf, Takeout/Mail/All mail Including Spam and Trash.mbox** |
| **073** | **2024-11-06 01:09:41** | **2024-11-06 01:08:11** | **F(3)** | **Takeout/Chrome/History.json, /home/chronos/u-2bf8.../History** |
| 074 | ruthonthego98@gmail.com | ruthonthego98@gmail.com | T | /home/chronos/u-2bf8.../Web Data |
| **075** | **373,228** | **373,228** | **T(2)** | **MyFiles/Downloads/New Marketing Folder/Flopper Advertisement.jpeg** |
| 076 | Pretty Little Liars | Pretty Little Liars | T | Chrome browsing history |
| 077 | 253018 | 253018 | T | /home/.shadow/2bf8.../mount/root/android-data/data/data/com.discord/files/assetpacks/krisp/253018/253018/\_metadata/properties.dat |
| 078 | 2024-11-16 | 2024-11-16 | T | Takeout/Google Play Store/Installs.json, com.supercell.clashroyale |
| **079** | **472a3434-8989-4133-b94a-5151333e6743** | **472a3434-8989-4133-b94a-5151333e6743** | **T(2)** | **/home/chronos/u-2bf8.../Network Action Predictor** |
| **080** | **Yang Jiayu** | **María Pérez** | **F(3)** | **Takeout Chrome history, Gemini activity, Google Image Search activity, Takeout Mail / Mailbox** |
| 081 | newark | newark | T | /data/data/com.discord/cache/http-cache/42b1fce53aa9609fb137f9378bdeb394 |
| **082** | **8** | **\-** | **F(3)** | **MyFiles/Downloads/New Marketing Folder/Flopper Advertisement.jpeg, TypeShirt\_Ad.jpeg** |

**AI 답변 및 실행 근거 상세 기록**  
**067**  
질문: What was the most recent battery level recorded by the Chromebook?

오답: 61

⬥ Chromebook의 powerd 로그 파일 /var/log/power\_manager/powerd.20241104-151846 (object ID 59893)을 확인함.  
⬥ 2024-12-11 01:44:05 UTC (KST 10:44:05)에 기록된 로그 엔트리 On battery at 61% (displayed as 62%)를 확인하여 배터리 잔량을 61%로 도출함.

정답:87

⬥ 2024-12-11 01:48 UTC경 재부팅 후 새로 작성된 powerd 로그 파일 /var/log/power\_manager/powerd.20240101-200042 (object ID 59892)의 마지막 라인을 확인함.  
⬥ 2024-12-11 02:30:28 UTC (KST 11:30:28)에 충전기(AC) 연결 상태에서 기록된 최신 잔량 엔트리 On AC ... with battery at 87% (displayed as 89%)를 확인하여 최종 정답을 87%로 수정/확정함.

**068**  
질문: What is the vendor ID for the touchpad?

정답: 0x04F3(1267)

⬥ 커널 부트 로그(var/log/messages.1) 및 udev 레코드 분석 결과, 터치패드 제조사가 ELAN Microelectronics Corporation (터치패드 장치 input4, i2c-ELAN0000:00)으로 명시되어 있음을 확인함.  
⬥ 커널 udev 드라이버(elan\_i2c) 레벨에서 등록된 ELAN Microelectronics의 표준 벤더 ID 수치 0x04F3을 정답으로 도출함.

**069**  
질문: What was the ip address of the Chromebook?

정답: 172.19.70.25

⬥ 네트워크 로그 파일 /var/log/net.1.log (object 59882\) 내 2024-12-11 01:44:04 UTC에 할당된 DHCP 임대 기록을 확인함.  
⬥ Wi-Fi 인터페이스 wlan0에 할당된 IPv4 주소가 172.19.70.25 (/19 서브넷)임을 확인하여 정답을 도출함.

**070**  
질문: What number is stored in contacts? Format: \+X (XXX) XXX-XXXX

정답: \+1 (802) 829-2741

⬥ .shadow/.../mount/ 및 home/root/ 경로 내 Android 연락처 DB 파일(소스 파일 480 및 42116)을 파싱함.  
⬥ Mary라는 이름 아래 저장된 전화번호 정보가 \+1 (802) 829-2741 규격으로 저장되어 있음을 확인하여 정답을 추출함.

**071**  
질문: How was the device most commonly woken up?

오답1: Lid Open

⬥ 펌웨어 이벤트 로그(/var/log/eventlog.txt, object 59808)의 절전 모드(S3 suspend) 해제 이력을 분석함.  
⬥ 총 47회의 절전 해제 중 Lid Open(덮개 열기)이 35회(약 74%)로 가장 높은 비중을 차지함을 확인함.  
⬥ 참고로 콜드 부팅(cold boot) 시 기록되는 Wake Source 필드 기준으로는 Power Button(26회)이 가장 많으나, 실제 수면 상태 해제 기준은 Lid Open임.

오답2: Lid Open

⬥ eventlog.txt 내 ACPI Wake \| S3 항목 라인 번호를 전수 재검증함.  
⬥ Lid Open: 35회 (라인 107, 110, 125 등), AC adapter only: 7회, Power Button: 3회, RTC Alarm: 2회 총 47회 중 Lid Open이 35회로 가장 높은 빈도를 유지함을 재확인함.

오답3: Lid Open

⬥ 절전 모드 해제(Wake up from sleep)의 가장 주된 원인은 Lid Open (35/47회)임.  
⬥ 로그의 특정 텍스트 필드명인 Wake Source 값 자체를 묻는 경우라면 Power Button (26회)이 해당됨.

**072**  
질문: How many months was Mary employed with her company?

오답1: \-

⬥ Downloads 폴더의 이력서 파일 marysresume.pdf (object ID 15562\) 내부 텍스트가 압축되어 있어 Autopsy 텍스트 파서로 즉시 해독하지 못함. 

오답2: \-

⬥ Downloads 폴더의 이력서 파일 marysresume.pdf (object ID 15562\) 내부 텍스트가 압축되어 있어 Autopsy 텍스트 파서로 즉시 해독하지 못함. 

정답: 21

⬥ Google Takeout의 이메일 백업 파일(Takeout/Mail/All mail...mbox) 내 첨부파일 marysresume.pdf를 복원하여 분석함.  
⬥ 이력서의 경력 항목에 Senior Marketing Associate, 02/2023 \- 11/2024 (GFields Marketing Solutions Inc)로 기재되어 있음을 확인함.  
⬥ 2023년 2월부터 2024년 11월까지 계산하여 총 21개월을 정답으로 도출함. 

**073**  
질문: When did the user first interact with a fanfiction website? (UTC) Format: YYYY-MM-DD HH:MM:SS

오답1: 2024-11-06 01:08:11

⬥ Google Takeout의 크롬 방문 기록(Takeout/Chrome/History.json, object 61292)을 분석함.  
⬥ 2024-11-06 01:07:30 UTC에 구글 검색 후, 2024-11-06 01:08:11 UTC에 FanFiction.net 페이지(/tv/Pretty-Little-Liars/)에 최초 접속했음을 확인함.

오답2: 2024-11-06 01:08:11

⬥ 기기 로컬 Chrome DB(/home/chronos/u-2bf8.../History, object 27724)와 Cloudflare 토큰 타임스탬프(1730855382)를 교차 검증하여 동일한 최초 접속 시각 2024-11-06 01:08:11 (상세 01:08:11.029)을 확인함.

오답3: 2024-11-06 01:08:11

⬥ 기기 내 타 팬픽션 사이트(AO3, Wattpad 등) 및 안드로이드 앱 데이터 전체를 전수 조사했으나 다른 팬픽션 활동이 없음을 확인함.  
⬥ 따라서 FanFiction.net에 최초 접속한 2024-11-06 01:08:11 UTC를 최종 정답으로 확정함.

**074**  
질문: What string was autofilled the most?

정답: [ruthonthego98@gmail.com](mailto:ruthonthego98@gmail.com)

⬥ Chrome 브라우저 DB /home/chronos/u-2bf8.../Web Data (object 29931\) 내 autofill 테이블 레코드를 확인함.  
⬥ email 필드 2회, EMAI 필드 1회로 총 3회 자동완성되어 가장 높은 사용 횟수(Count)를 기록한 문자열 ruthonthego98@gmail.com을 추출함.

**075**  
질문: What is the size of Ruth’s advertisement in bytes?

오답: \-

⬥ Marketing Advertisements.7z 파일 내 Sleeper\_Sock\_Ad.jpeg 파일의 바이트 수치를 읽고자 했으나, LZMA 압축 인덱스로 인해 정밀 수치를 추출하지 못함. 

정답: 373,228

⬥ MyFiles/Downloads/New Marketing Folder/ 경로의 Gemini 생성 이미지 파일 Flopper Advertisement.jpeg (object 15564)를 파싱함.  
⬥ 2024-11-16 21:54:38 UTC 수정 기록 및 정확한 파일 크기인 373,228 bytes (Hex 0x05B1EC)를 도출함.

**076**  
질문: What TV show does Ruth have an interest in?

정답: Pretty Little Liars

⬥ 2024-11-06 및 11-08 접속 웹 방문 기록을 파싱함.  
⬥ Google 검색어 pretty little liars fanfiction 및 FanFiction.net 내 Pretty Little Liars 팬픽션 아카이브 페이지(/tv/Pretty-Little-Liars/), 소설 2건(*Get Out*, *Out of Reach*) 방문 이력을 확인하여 관심 있는 TV 프로그램을 도출함.

**077**  
질문: What is the version of the noise suppression software?

정답: 253018

⬥ Discord 안드로이드 앱에 번들된 소음 억제 소프트웨어 Krisp의 메타데이터 파일 /home/.shadow/2bf8.../mount/root/android-data/data/data/com.discord/files/assetpacks/krisp/253018/253018/\_metadata/properties.dat (object 1209)을 확인함.  
⬥ 해당 파일 내 명시된 모듈 버전 태그 moduleVersionTag=253018 및 자산 폴더명(krisp/253018/253018/)을 통해 버전 253018을 도출함.

**078**  
질문: What date was the game installed on the system? YYYY-MM-DD

정답: 2024-11-16

⬥ Google Takeout 백업 내 Google Play 설치 이력 파일 Takeout/Google Play Store/Installs.json (object 61323)을 파싱함.  
⬥ 설치된 게임 Clash Royale (com.supercell.clashroyale)의 최초 설치 타임스탬프 "firstInstallationTime": "2024-11-16T21:25:01.965902Z"를 확인하여 날짜 2024-11-16을 도출함.

**079**  
질문: What is the ID of the URL with the most number of hits?

오답: 11

⬥ Chrome 브라우저의 History DB 내 urls 테이블을 단순 방문 수(visit\_count) 기준으로 조회함.   
⬥\[https\://mail.google.com/mail/u/0/\#inbox\](https\://mail.google.com/mail/u/0/\#inbox)가 5회 방문으로 1위이며 ID는 11로 도출됨.

정답: 472a3434-8989-4133-b94a-5151333e6743

⬥ 질문의 "hits"는 Chrome의 Network Action Predictor DB(network\_action\_predictor 테이블, object 27918\) 내 number\_of\_hits 컬럼을 의미함을 파악함.  
⬥ 주소창에 takeout.google.com을 입력하여 예측 성공(hit) 2회를 기록한 레코드의 GUID ID인 472a3434-8989-4133-b94a-5151333e6743을 최종 정답으로 확정함. 

**080**  
질문: What is the name of the current champion of the sport Ruth was trying to learn?

오답1: María Pérez

⬥ Ruth가 배우려 했던 스포츠 종목은 Race walking(경보 / 속도 보행)임.  
⬥ (2024-11-16 21:24:54 UTC에 Google에서 how to improve speed walking technique를 검색함)  
⬥ 2025년 도쿄 세계육상선수권대회(World Athletics Championships in Tokyo) 기준 세계 챔피언 목록:

* 여성 20km & 35km: María Pérez (스페인, 가장 유력함)  
* 남성 20km: Caio Bonfim (브라질)  
* 남성 35km: Evan Dunfee (캐나다)

⬥ 올림픽(2024 파리 올림픽 20km) 챔피언 기준일 경우:

* 남성: Brian Daniel Pintado (에콰도르)  
* 여성: Yang Jiayu (중국)

오답2: María Pérez

⬥ Ruth가 배우려 한 스포츠 종목은 Race walking(경보 / 속도 보행)임. (2024-11-16 4:24 PM EST에 how to improve speed walking technique 검색)  
⬥ 대표/일반적 권장 정답: María Pérez (스페인)

* 2025년 도쿄 세계육상선수권대회(World Championships in Tokyo) 여성 20km 및 35km 통합 세계 챔피언으로 가장 보편적으로 언급됨.

⬥ 2026년 4월 12일 브라질리아 세계 경보 팀 선수권(World Athletics Race Walking Team Championships in Brasília) 기준 챔피언:

* 여성 하프마라톤: Kimberly García (페루)  
* 여성 마라톤: Paula Milena Torres (에콰도르)  
* 남성 하프마라톤: Francesco Fortunato (이탈리아)  
* 남성 마라톤: Hayato Katsuki (일본)

오답3: María Pérez

⬥ 종목 확정: Ruth의 전체 활동(Chrome 106개, Gemini 프롬프트 13개, 이메일 등) 분석 결과, 2024-11-16 4:24 PM EST에 how to improve speed walking technique를 검색하고 속보 관련 기사를 읽은 내역만 존재하여 대상 스포츠는 Race walking(경보 / 속도 보행)으로 확정됩니다.  
⬥ 기준에 따른 정답 후보군:

* María Pérez (스페인): 2025 도쿄 세계선수권 여성 부문 통합 챔피언으로, 여성 학습자인 Ruth의 관점에서 가장 대표적인 권장 정답임.  
* Álvaro Martín (스페인): 2023 부다페스트 세계선수권 남성 20km/35km 챔피언입니다. 2024년 말 문제 출제 당시 기준 정답키로 설정되었을 가능성이 높음.  
* Kimberly García (페루): 2026년 4월 세계 경보 팀 선수권 여성 하프마라톤 우승자로 가장 최신 국제 타이틀 보유자임.  
* Caio Bonfim / Evan Dunfee: 2025 도쿄 세계선수권 남성 20km / 35km 챔피언임.

**081**  
질문: What region had the lowest latency for Discord?

정답: newark

⬥ Discord 안드로이드 앱 캐시 파일 /data/data/com.discord/cache/http-cache/42b1fce53aa9609fb137f9378bdeb394 (.1 응답 바디 파일, obj 62101\) 내의 \[https\://latency.discord.media/rtc\](https\://latency.discord.media/rtc) 응답 결과를 분석함.  
⬥ Discord Latency 서비스 응답 데이터는 레이턴시(지연 시간)가 낮은 순서부터 정렬되어 있으며, 캐시 목록의 1순위 항목이 newark (66.22.212.70)로 기록되어 있음을 확인하여 정답을 도출함.

**082**  
질문: How many shirts are in the ad?

오답1: \-

⬥ Autopsy 서버 연결 특성상 이미지 데이터가 텍스트 형태로 수신되어 실제 광고 이미지를 시각적으로 확인할 수 없음.  
⬥ 관련 광고 파일 상태:

* Flopper Advertisement.jpeg: 파일 자체는 온전하나(373,228 bytes) 시각적 렌더링이 불가능함.  
* TypeShirt\_Ad.jpeg: 손상된 Marketing Advertisements.7z 압축 파일 내에 존재하여 0바이트 항목으로 표시됨.  
* Gemini 내역: 2024-11-04 20:50 EST에 생성된 이미지 링크만 존재하며 다운로드가 차단됨.

⬥ 추측을 배제하고 정확한 셔츠 개수를 파악하려면 Autopsy에서 해당 이미지를 직접 추출(Extract File(s))하여 첨부하거나 Application 탭에서 직접 확인해야 함을 명시하고 있음.

오답2: \-

⬥ Autopsy 분석 특성상 이미지 파일 데이터가 깨진 텍스트 형태로 수신되어 시각적 확인이 불가능하며, OCR이나 EXIF 메타데이터 분석 결과에도 개수 정보가 없음.  
⬥ 관련 파일 및 활동 데이터 상태:

* TypeShirt\_Ad.jpeg: 손상된 Marketing Advertisements.7z 압축 파일 내에만 존재하여 0바이트로 표시되며, Downloads, 이메일 첨부파일, Takeout 백업 등 어디에도 다른 복사본이 없음.  
* Discord 메시지 및 이메일: AI로 광고를 생성한다는 정황만 언급될 뿐 셔츠에 대한 구체적인 묘사가 없음.  
* Gemini 히스토리: 2024-11-04에 생성된 구글 서버 링크만 존재하며, 다운로드 차단 및 브라우저 열기 미진행으로 접근이 정지됨.

⬥ 정확한 개수 산출을 위해서는 Autopsy에서 Flopper Advertisement.jpeg (object 39573\) 또는 복구된 TypeShirt\_Ad.jpeg 파일을 직접 추출(Extract File(s))하여 전달해야 함.

오답3: \-

⬥ 케이스 전체 대상 재수색 결과, 광고 복사본 미존재: shirt 및 \_Ad 키워드 검색 시 손상된 Marketing Advertisements.7z 내 0바이트 TypeShirt\_Ad.jpeg 파일만 조회됨.  
⬥ Autopsy 분석 결과 부재: 개체 탐지(Object Detection), OCR, EXIF 메타데이터 및 키워드 탐지 결과가 없으며, 유일한 보고서인 Android 보고서에도 해당 이미지가 포함되어 있지 않음.  
⬥ 메시지 및 이메일 상 묘사 부재: Ruth의 Discord 메시지 및 이메일 내역에 AI 광고 제작 언급만 있을 뿐, TypeShirt 광고 내용에 대한 구체적 설명이 없음.  
⬥ 이미지 데이터 파싱 한계: Flopper Advertisement.jpeg (object 39573\) 및 Takeout 내 Gemini PNG 파일들이 텍스트로 읽혀 시각화되지 않으며, 온라인 Gemini 링크 접속도 차단된 상태임.  
⬥ 명확한 셔츠 개수 확인을 위해서는 Autopsy에서 파일을 직접 추출(Extract File(s))하여 전달하거나 Application 탭에서 직접 확인해야 함.  
**7.2 2025 CTF 이미지\_Chromebook**

**이미지 기본 정보**

| 이미지명 | Android |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 25\_Chromebook |
| 문항 수  | 16 |
| 실험자 | 진세라 |
| 정답률 | 12/16(75%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| **067** | **87** | **87** | **T(3)** | 전력 관리자 로그 파일 및 경로(/var/log/power\_manager/powerd.20240101-200042), 배터리 상태 기록 로그 |
| 068 | 1267  | 0x04F3(=1267) | T | 터치패드 벤더/기기 식별정보, 펌웨어 업데이트 로그 |
| 069 | 172.19.70.25 | 172.19.70.25 | T | 네트워크 로그 파일, DHCP할당 및 네트워크 설정 아티팩트 |
| 070 | \+1 (802) 829-2741  | \+1 (802) 829-2741 | T | 연락처 |
| 071 | Power Button  | Power Button | T(3) | 펌웨어 이벤트 로그 파일, Wake Source" 필드 기준 집계  |
| **072** | **21 OR 22** | **\-** | **F(3)** | **download 내 marysresume.pdf(MyFiles/Downloads/marysresume.pdf)** |
| **073** | **2024-11-06 01:09:41** | **2024-11-06 01:08:11** | **F(3)** | chrome History DB, Cloudflare 챌린지 토큰 unix timestamp |
| 074 | ruthonthego98@gmail.com | ruthonthego98@gmail.com | T | Chrome Web Data DB, Autofill record\&count |
| 075 | 373,228 | 373,228 | T | 광고이미지파일, 계정 trello 보드 정보 |
| 076 | Pretty Little Liars | Pretty Little Liars | T | Chrome History DB, Google search suggestions 저장내역 |
| **077** | **253018** | **253018** | **T(2)** | **Discord Krisp 에셋 팩 경로(/android-data/data/data/com.discord/files/assetpacks/krisp/253018/253018/)** |
| 078 | 2024-11-16 | 2024-11-16 | T | Autopsy Android 패키지 데이터, aLEAPP리포트 |
| **079** | **472a3434-8989-4133-b94a-5151333e6743** | **472a3434-8989-4133-b94a-5151333e6743** | **T(3)** | **Network Action Predictor DB, number of hits** |
| **080** | **Yang Jiayu** | **María Pérez** | **F(3)** | **Google 검색어, Times of India 기사, 웹 검색** |
| 081 | newark | Newark | T | Discord Android 앱 공유 설정 파일 및 키(shared\_prefs/CacheStore.xml 내 RTCRegionStore) |
| **082** | **8** | **\-** | **F(3)** | **/home/chronos/user/MyFiles/Downloads/New Marketing Folder/Flopper Advertisement.jpeg, Autopsy text 출력 데이터(확인못함)**  |

**AI 답변 및 실행 근거 상세 기록**

##### **067**

**질문: What power manager log file records battery status information?**  
오답1 : \-

* 실행 근거:  
  * /image4/var/log/power\_manager/ 경로 내 로그 파일 목록(powerd.20241104-151846, powerd.20240101-200042 등) 및 심볼릭 링크를 도출했으나 특정 세부 기록 로그를 지정하지 않음. 정답 (25\_ch\_067\_1): powerd.20240101-200042 (또는 /var/log/power\_manager/powerd.20240101-200042)

* 실행 근거:  
  * /var/log/power\_manager/powerd.20240101-200042 파일 내부에서 2024-12-11T02:30:28.136611Z 시점의 배터리 상태 기록(실제 87%, 표시 89%, USB\_PD 충전 데이터)을 정밀 도출함.  
      
    

##### **068**

**질문: What is the Vendor ID and Product ID of the Elan Touchpad?**   
정답: 04f3:00cd (Vendor ID: 0x04F3, Product ID: 0x00CD)

* 실행 근거:  
  * /var/log/messages.1 커널 로그 및 chromeos-elan-touch-firmware-update-legacy 로그 분석.  
  * Elan Microelectronics 터치패드(ACPI ID: ELAN0000)의 USB/HID Vendor ID 0x04F3 및 Product ID 0x00CD (Product ID 205.0)를 도출함.

##### **069**

**질문: What was the assigned IPv4 address during the DHCP lease in net.7.log?**   
정답 : 172.19.70.25

* 실행 근거:  
  * /var/log/net.7.log 네트워크 로그 파일 분석.  
  * 2024-11-16 21:18:41 UTC에 wlan0 인터페이스에 할당된 DHCP IPv4 주소가 172.19.70.25/19 (Gateway: 172.19.64.1)임을 도출함.

##### **070**

**질문: What is the saved contact name and phone number?**   
정답 (25\_ch\_070): Mary / \+18028292741

* 실행 근거:  
  * 탐색된 연락처 DB 파일(Source ID: 477, 42113\) 내부 저장 레코드 파싱.  
  * 이름 Mary 및 전화번호 \+18028292741 (표시 형식: \+1 (802) 829-2741) 아티팩트를 확정함.  
      
    

##### **071**

**질문: How was the device most commonly woken up?**   
오답1 : Lid opened

* 실행 근거:  
  * /var/log/eventlog.txt 펌웨어 이벤트 로그에서 S3 절전 모드 깨어남 원인 중 "Lid opened" 통계를 35회로 1차 집계함.


오답2: Lid opened

* 실행 근거:  
  * /var/log/eventlog.txt 내 EC Event \| Lid Open 태그 항목을 기준으로 엄격하게 전수 카운트하여 총 40회임을 도출함.

오답3 : Power Button

* 실행 근거:  
  * Wake Source 필드에 기록된 Power Button (26회) 및 RTC Alarm (12회) 통계에 집중하여 Lid Open 카운트를 누락함.  
      
    

##### **072**

**질문: What is the filename and path of Mary's resume PDF file?**  
오답1 : marysresume.pdf

* 실행 근거:  
  * 외부 호스트 참조 케이스 폴더(C:\\2025\\Chromebook) 경로를 혼동하여 표기함.


오답2 : MyFiles/Downloads/marysresume.pdf

* 실행 근거:  
  * Chromebook 내부 저장소 경로 MyFiles/Downloads/marysresume.pdf (파일 크기: 237 KB, 생성 시각: 2024-11-11 16:54:56 UTC)를 확정함.  
      
    

##### **073**

**질문: What exact timestamp was the Pretty Little Liars FanFiction archive URL first visited?**  
오답1 : 2024-11-06 01:08:11 UTC

* 실행 근거:  
  * Chrome History DB 분석을 통해 URL (\[https\://www\.fanfiction.net/tv/Pretty-Little-Liars/\](https\://www\.fanfiction.net/tv/Pretty-Little-Liars/))의 첫 방문 시각이 2024-11-06 01:08:11 UTC임을 도출함.

오답2 : 2024-11-06 01:08:11.011 UTC (또는 01:08:11.011 \~ 01:08:11.043 UTC)

* 실행 근거:  
    
  * Chrome History DB (URL ID 67\) 밀리초 단위 복원 타임스탬프(01:08:11.011 UTC)를 정밀 도출함.

오답3 : 2024-11-06 01:08:11.011 UTC

* 실행 근거:  
  * 전체 URL ID(66\~80) 디코딩 및 Cloudflare 토큰 타임스탬프(1730855382) 교차 검증으로 01:08:11.011 UTC를 재확정함.  
      
    

##### **074**

**질문: What string was autofilled the most?**  
정답 : ruthonthego98@gmail.com (Count: 2\)

* 실행 근거:  
  * /home/chronos/user/Web Data 내 autofill 테이블 레코드 분석.  
  * email \| ruthonthego98@gmail.com (Count: 2\) 및 EMAI \| chickadeemary2000@gmail.com (Count: 1\) 항목을 도출함.

##### **075**

**질문: What is the size of Ruth’s advertisement in bytes?**   
정답 : 373,228 bytes

* 실행 근거:  
  * /home/chronos/user/MyFiles/Downloads/New Marketing Folder/Flopper Advertisement.jpeg 파일 메타데이터 분석.  
  * 파일 크기 373,228 bytes 및 MD5 해시 577492da3b00ff9bb9ef89712b83be00을 도출함.

##### **076**

**질문: What TV show does Ruth have an interest in?**   
정답 : Pretty Little Liars

* 실행 근거:  
  * Chrome History DB 내 Google 검색어 "pretty little liars fanfiction" 및 FanFiction.net 접근 경로(/tv/Pretty-Little-Liars/) 분석을 통해 대상 TV 쇼를 도출함.  
      
    

##### **077**

**질문: What noise cancellation component was requested and what was its requested version/download URL?**  
오답1 : nc-ap-dlc / R129-16002.60.0

* 실행 근거:  
  * /var/log/update\_engine/ 로그 분석을 통해 ChromeOS 노이즈 억제 DLC 컴포넌트(nc-ap-dlc) 및 URL 요청을 도출했으나 디스크 내 dlc.img 파일이 0으로 채워진 미설치 상태임을 밝힘.  
    

정답 : Krisp / version 253018

* 실행 근거:

  * Discord Android 앱 경로(/android-data/data/data/com.discord/files/assetpacks/krisp/253018/253018/) 내부 메타데이터(metadata/properties.dat) 파싱.  
  * checkpoint.dat (fileStatus=4) 분석을 통해 실제 정상 설치된 노이즈 억제 엔진이 Krisp (버전: 253018)임을 확정함.  
      
    

##### **078**

**질문: What game app was installed on 2024-11-16 and at what exact UTC time?**  
정답 : Clash Royale (com.supercell.clashroyale) / 2024-11-16 21:22:30 UTC

* 실행 근거:  
  * Autopsy Android 패키지 데이터 및 aLEAPP 리포트 교차 검증.  
  * com.supercell.clashroyale 패키지의 정확한 설치 타임스탬프가 2024-11-16 21:22:30 UTC임을 도출함.  
      
    

##### **079**

**질문: Which URL had the highest visit count in Chrome History?**  
오답1 : [https\://mail.google.com/mail/u/0/\#inbox](https://www.google.com/search?q=https://mail.google.com/mail/u/0/%23inbox) (Visits: 5\)

* 실행 근거:  
  * Chrome History DB (/home/chronos/user/History) urls 테이블 파싱.  
  * URL ID 11 (Inbox (18) \- ruthonthego98@gmail.com \- Gmail)의 방문 횟수가 5회로 가장 높음을 도출함.  
    

오답2 : [https\://mail.google.com/mail/u/0/\#inbox](https://www.google.com/search?q=https://mail.google.com/mail/u/0/%23inbox) (Visits: 5\)

* 실행 근거:  
  * 전체 URL ID 레코드 전수 검수 결과 5회 방문 기록을 가진 URL ID 11 항목을 재확인함.


오답3 : takeout.google.com (Hits: 2\)

* 실행 근거:  
  * Chrome History DB가 아닌 Network Action Predictor DB를 조회하여 잘못된 테이블 결과를 도출함.  
    

##### **080**

**질문: According to search results, who were the 2025 World Athletics Championships race walking champions?**  
오답1 : María Pérez (여자) / Caio Bonfim (남자)

* 실행 근거:  
  * 경보 학습 관련 검색어 분석 후 2025 도쿄 세계 선수권 예상 챔피언 데이터 도출 시도.

오답2 : Brian Pintado (2024 파리 올림픽 남자 20km)

* 실행 근거:  
  * 2024 파리 올림픽 데이터와 혼동하여 잘못 정리함.

오답3 : María Pérez (여자 20km/35km) / Caio Bonfim (남자 20km)

* 실행 근거:  
  * Chrome History 내 종목 학습 방문 기록("how to improve speed walking technique", Times of India 기사)과 연관된 2025 도쿄 세계 선수권 대표 챔피언 데이터를 정밀 정리함.

##### **081**

**질문: Which Discord voice region had the lowest latency (fastest preference) in settings?**  
정답 : newark

* 실행 근거:  
  * Discord Android 앱 설정 파일 shared\_prefs/CacheStore.xml 내 RTCRegionStore 키 파싱.  
  * preferredRegions 배열 및 lastGeoRankedOrder 필드 순서 \["newark", "us-east", "atlanta", ...\] 분석을 통해 newark가 최저 지연 시간 지역임을 확인함.  
    

##### **082**

**질문: What watermark/metadata note was present on Flopper Advertisement.jpeg?**  
오답1 : \-

* 실행 근거:  
  * Autopsy 텍스트 변환 시 바이너리가 손상되어 내용 파악이 제한적이었으나 IPTC 태그 존재를 파악함.

오답2 : Made with Google AI

* 실행 근거:  
  * JPEG 파일 내 IPTC 메타데이터 태그 분석을 통해 "Made with Google AI" 표기를 정밀 도출함.  
    

오답3 : Made with Google AI

* 실행 근거:  
  * Autopsy 케이스 내 Flopper Advertisement.jpeg 메타데이터 속성 파싱을 통해 재확인함.

**8\. 2025 CTF 이미지\_iPhone**

**이미지 기본 정보**

| 이미지명 | iPhone |
| :---: | :---: |
| 연도 | 2025 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 10.5GB |
| 출처 | [2025CTF](https://drive.google.com/drive/folders/1gHQsfx1hqCv-V4Anm2eYukB4jPtraNBH) |
| Autopsy Case명 | 26\_iPhone |
| 대상 OS | iOS |
| 문항 수  | 20 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 083 | 18.0 | 18.0 | 18.0 | T |
| 084 | 18024959063 | \+1 (802) 495-9063 | \+1 (802) 495-9063 | T |
| 085 | Mary | Mary | Mary | T |
| 086 | 0 | 0 | 0 | T |
| 087 | 51 | 51 | 48 | T(50%) |
| 088 | 2:15 | 2:15 | 2:15 | T |
| 089 | blonde | \- | \- | F |
| 090 | Canva: AI Photo & Video Editor | Canva: AI Photo & Video Editor | Canva | T |
| 091 | 184.171.159.153 | \- | 66.22.212.147 | F |
| 092 | 36.1660667 | 36.1660667 | 36.1660667 | T |
| 093 | 432 | 432 | 432 | T |
| 094 | com.toyopagroup.picaboo | Snapchat (com.toyopagroup.picaboo) | com.toyopagroup.picaboo | T |
| 095 | EARLYBF24  | EARLYBF24 | EARLYBF24  | T |
| 096 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09  | T |
| 097 | North Beach Park | North Beach Park | North Beach Park  | T |
| 098 | 2022-12 | 2024-09 | 2024-06 | F |
| 099 | nicole vranjican | nicole vranjican | nicole vranjican | T |
| 100 | Dunkin’ | Dunkin’ | Dunkin’  | T |
| 101 | https\://delivr.com/2fsmr-qr | \- | \- | F |
| 102 | 2024-11-20 20:02:02 | 2024-11-13 18:04:13 | 2024-11-13 13:00:49  | F |

| NO | Question |
| :---: | ----- |
| 083 | What version of iOS? |
| 084 | What is the device’s phone number? |
| 085 | What was the contact name stored on 2024-11-13 5:45:05.000 PM |
| 086 | Out of all the incoming calls, how many were answered? |
| 087 | How many words typed were autocorrected? |
| 088 | What time did Ruth plan to meet Mary at Black Cap? |
| 089 | What color hair does Ruth’s Bitmoji have? |
| 090 | What was the first AI tool installed on the device? |
| 091 | What was the IP address logged from Discord? |
| 092 | What is the Latitude of Nashville in the Weather App? Format: xx.xxxxxxx |
| 093 | What is the answer to second the equation in notes? |
| 094 | What app was denied permission to use Microphone? |
| 095 | If Ruth bought an item for \$40 or more, she gets her second one 40% off with what code? |
| 096 | In YYYY-MM-DD HH:MM:SS format, when was the tiktok video posted? |
| 097 | What beach was searched for? |
| 098 | Using format YYYY-MM, When was this device purchased? |
| 099 | Who is the author of the October 2023 wallpaper? |
| 100 | What popular coffee company did Ruth get coffee from? |
| 101 | What link redirects you to apply for a job? |
| 102 | When was the last written record created? (format YYYY-MM-DD HH:MM:SS) |

**8.1 2025 CTF 이미지\_iPhone**

**이미지 기본 정보**

| 이미지명 | iPhone |
| :---: | :---: |
| 이미지 형식 | zip |
| Autopsy Case명 | 25\_iPhone14Plus |
| 문항 수  | 20 |
| 실험자 | 박제윤 |
| 정답률 | 15/20(75%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 083 | 18.0 | 18.0 | T | /System/Library/CoreServices/SystemVersion.plist |
| 084 | 18024959063 | \+1 (802) 495-9063 | T | /private/var/wireless/Library/Preferences/com.apple.commcenter.plist |
| 085 | Mary | Mary | T | /private/var/mobile/Library/AddressBook/AddressBook.sqlitedb-wal |
| 086 | 0 | 0 | T | CallHistory.storedata |
| 087 | 51 | 51 | T | /private/var/mobile/Library/Keyboard/user\_model\_database.sqlite |
| 088 | 2:15 | 2:15 | T | Library/Caches/com.hammerandchisel.discord/Cache.db-wal |
| **089** | **blonde** | **\-** | **F(3)** | **Documents/Composer/824aa24e-f3ec-4b10-ac32-abd1ef6c919c/PersistentStores/avatar\_data, Library/Caches/bitmojiNotif/870a5b8a-f92b-4b63-889e-81cf00cfa6ee\_bigquery** |
| **090** | **Canva: AI Photo & Video Editor** | **Canva: AI Photo & Video Editor** | **T(2)** | **iTunesMetadata.plist** |
| **091** | **184.171.159.153** | **\-** | **F(3)** | **com.hammerandchisel.discord, auth/location-metadata, latency.discord.media/rtc** |
| 092 | 36.1660667 | 36.1660667 | T | /private/var/mobile/Containers/Shared/AppGroup/5A25F7AB-6542-44BF-BFF0-3A1B6E0EC1F1/Library/Preferences/group.com.apple.weather.plist |
| 093 | 432 | 432 | T | NoteStore.sqlite |
| 094 | com.toyopagroup.picaboo | Snapchat (com.toyopagroup.picaboo) | T | /private/var/mobile/Library/TCC/TCC.db |
| 095 | EARLYBF24 | EARLYBF24 | T | SMS / Messages Database |
| 096 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09 | T | Messages Chat History |
| 097 | North Beach Park | North Beach Park | T | /private/var/mobile/Containers/Shared/AppGroup/680BC20F-.../Maps/MapsSync\_0.0.1 |
| **098** | **2022-12** | **2024-09** | **F(3)** | **com.apple.purplebuddy.notbackedup.plist, /Library/activation\_records/activation\_record.plist** |
| 099 | nicole vranjican | nicole vranjican | T | October-2023-iphone-wallpaper-1170-x-2436-px-1.pdf |
| 100 | Dunkin’ | Dunkin’ | T | MapsSync\_0.0.1 |
| **101** | **https\://delivr.com/2fsmr-qr** | **\-** | **F(3)** | **psi.sqlite, /private/var/mobile/Media/DCIM/100APPLE/IMG\_0004.JPG, /tmp/WKFileUploadPanel-.../IMG\_0004.jpeg, Photos.sqlite, Mail app** |
| **102** | **2024-11-20 20:02:02** | **2024-11-13 18:04:13** | **F(3)** | **NoteStore.sqlite, NoteStore.sqlite-wal, Notes search-index log, Notes handwriting cache** |

**AI 답변 및 실행 근거 상세 기록**  
**083**  
질문: What version of iOS?

정답: 18.0

⬥ 시스템 버전 설정 파일인 /System/Library/CoreServices/SystemVersion.plist 경로의 plist 데이터를 확인하여 운영체제 버전 iOS 18.0 및 빌드 번호 22A3354를 도출함. 

**084**  
질문: What is the device’s phone number?

정답: \+1 (802) 495-9063

⬥ 환경설정 파일 경로 /private/var/wireless/Library/Preferences/com.apple.commcenter.plist 내 PhoneNumber, CopiedSIMPhoneNumber, PNRPhoneNumber, kActiveSimIdPhNumKey 필드를 분석함.  
⬥ 활성화된 SIM (ICCID 89012803331553629756)에 연결된 디바이스 전화번호가 \+1 (802) 495-9063 (또는 18024959063)임을 확인함.

**085**  
질문: What was the contact name stored on 2024-11-13 5:45:05.000 PM

정답: Mary

⬥ 연락처 데이터베이스 WAL 파일 /private/var/mobile/Library/AddressBook/AddressBook.sqlitedb-wal 로그를 파싱함.  
⬥ 수정 시각 타임스탬프 753,212,705 (UTC 기준 2024-11-13 17:45:05 UTC)에 정확히 일치하는 연락처 이름이 Mary (ruthonthego98@gmail.com 구글 계정 동기화, 전화번호 \+1 (802) 829-2741)임을 도출함.

**086**  
질문: Out of all the incoming calls, how many were answered?

정답: 0

⬥ 통화 기록 DB 파일 CallHistory.storedata 및 WAL 로그의 13건의 통화 내역을 확인함.  
⬥ 13건 전체가 수신 통화(ZORIGINATED \= 0)이나, 모든 통화 기록의 수신 플래그가 ZANSWERED \= 0이며 통화 시간(Duration) 역시 0초로 기록되어 응답한 통화가 0건임을 확정함.

**087**  
질문: How many words typed were autocorrected?

정답: 51

⬥ 키보드 데이터 DB /private/var/mobile/Library/Keyboard/user\_model\_database.sqlite 및 WAL 로그의 usermodeldurablerecords 테이블을 분석함.  
⬥ 키보드 누적 카운터 키 tium.totalWordsAutocorrected의 최신 값이 51로 기록되어 있음을 도출함.

**088**  
질문: What time did Ruth plan to meet Mary at Black Cap?

정답: 2:15

⬥ Discord 캐시 DB /Library/Caches/com.hammerandchisel.discord/Cache.db-wal 내 2024년 11월 5일 자 다이렉트 메시지(DM) 내역을 확인함.  
⬥ Ruth(ruthonthego\_18865)가 작성한 메시지 \*"Ofc\! It'd be great to catch up. How does Black Cap around 2:15 sound?"\*를 분석하여 약속 시간이 2:15 PM (Eastern Time 기준 14:15, UTC 기준 19:15)임을 도출함.

**089**  
질문: What color hair does Ruth’s Bitmoji have?

오답1: \-

⬥ Autopsy 텍스트 리더 특성상 압축 데이터 및 이미지 바이트가 깨져 수신되어 Bitmoji 데이터 파싱에 실패함.  
⬥ 추후 분석이 가능한 대상 파일 2건 식별 완료:

* .../Documents/Composer/.../PersistentStores/avatar\_data (1,376 bytes, 압축된 아바타 설정 데이터)  
* .../Library/Caches/bitmojiNotif/870a5b8a-f92b-4b63-889e-81cf00cfa6ee\_bigquery (58 KB PNG, 캐시된 Bitmoji 이미지, object ID 107394\)

⬥ 정확한 색상 확인을 위해 Autopsy에서 PNG 파일을 직접 열거나, Downloads\\00008110-0008196A2299401E\_files\_full-001 추출 폴더에 대한 접근 권한 부여가 필요함을 제시함.

오답2: \-

⬥ 폴더 접근 요청이 다시 거부되어 Autopsy 파일 리더 외에는 파일 접근 경로가 차단됨.  
⬥ 해결 방법으로 3가지 대안을 제시함:

* 해당 추출 폴더에 대한 접근 허용  
* Snapchat 컨테이너(CA6618F8-E002-4DE8-91EF-2097D7407250) 내 avatar\_data 및 PNG 이미지 파일 2건을 직접 첨부  
* Autopsy 파일 뷰어에서 object ID 107394(캐시된 Bitmoji PNG)를 직접 확인

오답3: \-

⬥ 동일 폴더(Downloads\\00008110-0008196A2299401E\_files\_full-001)에 대한 접근 권한 요청이 3번째 거절되어 추가 요청을 중단함.  
⬥ Claude 데스크톱 앱 내 권한 승인 팝업 확인 방법 또는 직접 폴더 추가(\+ \-\> Add folder) 절차를 안내하고, 미승인 시 두 핵심 파일(avatar\_data, 캐시 PNG)을 직접 업로드할 것을 최종 요청함.

**090**  
질문: What was the first AI tool installed on the device?

오답: ChatGPT

⬥ 2024년 9월 26일 기기 초기 설정 이후의 앱 설치 로그를 확인한 결과, 11월 13일 이전에는 SNS 및 게임 앱만 설치되었음을 확인함.  
⬥ 2024-11-13 설치 타임라인:

* 14:45:34: Canva (AI 기능이 내장된 디자인 앱)  
* 14:48:18: ChatGPT (com.openai.chat, 순수 AI 툴 앱 중 최초 설치)  
* 14:52:14: PictureThis (AI 식물 식별 앱)  
* 14:53:15: Adobe Express (AI 기능 디자인 앱)

⬥ 독립된 전용 AI 툴 기준으로는 ChatGPT가 최초 설치 앱으로 산출됨.

정답: Canva: AI Photo & Video Editor

⬥ App Store 구매 기록 파일 iTunesMetadata.plist 및 설치 로그를 교차 재검증함.  
⬥ 2024-11-13 19:45:32 UTC (로컬 14:45:34)에 설치된 앱의 정식 App Store 타이틀이 Canva: AI Photo & Video Editor로 명시되어 있어 앱 자체가 AI 툴로 분류됨을 파악함.  
⬥ 따라서 전체 AI 툴 기준 최초 설치 앱은 Canva로 수정/확정되며, AI 챗봇 전용 앱으로 특정하는 질문일 경우 약 3분 뒤 설치된 ChatGPT가 정답임.

**091**  
질문: What was the IP address logged from Discord?

오답1: \-

⬥ Discord 관련 캐시 DB, 웹 요청, 키-값 저장소, Adjust 분석 파일 등을 전체 검색했으나 기기 본래의 IP 주소 아티팩트는 존재하지 않음.  
⬥ 발견된 IP 항목:

* Discord 음성 서버 IP: Newark 지역 서버 IP 목록(66.22.214.44, 66.22.214.16, 66.22.214.51, 66.22.214.87, 66.22.214.59), US-East 서버(66.22.231.203) 등 앱 자체의 서버 IP만 저장되어 있음.  
* IPv6 연결 지표: Firebase 링크 트래킹 응답에 "requestIpVersion": "IP\_V6" 지표만 존재할 뿐 실제 IP 주소는 기록되어 있지 않음.

⬥ 화면에 표시되었을 가능성이 있는 Discord 앱 스크린샷 이미지(objects 176462-176469)에 대한 추가 시각 검증이 제안됨.

오답2: \-  
⬥ IPv6 및 캐시된 약 40개 웹 요청 전체를 재검색했으나, 위치 메타데이터 응답에는 "country\_code": "US" 정보만 있을 뿐 기기 IP는 기록되어 있지 않음.  
⬥ Discord 서버 속도 테스트(latency.discord.media/rtc) 결과 중 2024년 9월 28일 첫 세션의 Newark 서버 IP(66.22.214.44 등) 및 최신 메인 캐시의 66.22.214.80 등 음성 서버 IP만 확인됨.

오답3: \-

⬥ 3차에 걸친 분석 결과, 기기나 Ruth의 계정에 할당된 실제 IP 기록은 존재하지 않는 것으로 최종 확정됨.  
⬥ 확인된 데이터는 Discord 자체 음성 서버 IP(66.22.214.44 등) 및 주소 값이 없는 "requestIpVersion": "IP\_V6" 지표가 전부임.  
⬥ IP 확인을 위해서는 원본 바이너리 파일 바이패스 파싱, 세부 타임라인 타겟팅, 또는 Autopsy 내 스크린샷 아티팩트(objects 176462-176469)의 시각적 확인이 필요함.

**092**  
질문: What is the Latitude of Nashville in the Weather App? Format: xx.xxxxxxx

정답: 36.1660667

⬥ 날씨 앱 환경설정 파일 /private/var/mobile/Containers/Shared/AppGroup/5A25F7AB-6542-44BF-BFF0-3A1B6E0EC1F1/Library/Preferences/group.com.apple.weather.plist 내 저장된 도시 목록을 파싱함.  
⬥ Nashville 항목의 LocationID: LocationID:36.1660667:-86.777802 필드에서 위도 수치 36.1660667을 도출함.

**093**  
질문: What is the answer to second the equation in notes?

정답: 432

⬥ 메모 앱 DB NoteStore.sqlite (노트 ID 34796591-0283-4420-BC80-E723A5E227C8) 내 손글씨 인식 텍스트를 파싱함.  
⬥ 첫 번째 수식 12 × 18 \= 216에 이어, 두 번째 수식 216 × 2 \= 432를 확인하여 정답 432를 도출함.

**094**  
질문: What app was denied permission to use Microphone?

정답: Snapchat (com.toyopagroup.picaboo)

⬥ iOS 권한 설정 DB /private/var/mobile/Library/TCC/TCC.db 내 kTCCServiceMicrophone 서비스 항목을 분석함.  
⬥ Snapchat 앱(com.toyopagroup.picaboo)의 마이크 권한 상태값이 auth\_value \= 0 (Denied, 거부됨)으로 기록되어 있음을 확인함.

**095**  
질문: If Ruth bought an item for \$40 or more, she gets her second one 40% off with what code?

정답: EARLYBF24

⬥ 2024년 11월 20일 08:55:26 UTC에 Zenni Optical로부터 수신된 문자 메시지 본문을 파싱함.  
⬥ *"Zenni: Early Black Friday \| Buy One Pair for \$40+, Get Your Second Pair 40% off* with code: EARLYBF24."\* 메시지에서 프로모션 코드 EARLYBF24를 추출함.

**096**  
질문: In YYYY-MM-DD HH:MM:SS format, when was the tiktok video posted?

정답: 2024-11-12 22:11:09

⬥ Mary와의 메시지 채팅에서 공유된 TikTok 비디오 URL (\[https\://www\.tiktok.com/@dochristmass/video/7436518844501347616\](https\://www\.tiktok.com/@dochristmass/video/7436518844501347616))의 ID 수치를 파싱함.  
⬥ 비디오 ID 상위 32비트 비트연산(7436518844501347616 \>\> 32 \= 1731449469)을 통해 추출한 Unix 타임스탬프를 UTC 변환하여 게시 시각 2024-11-12 22:11:09를 도출함.

**097**  
질문: What beach was searched for?

정답: North Beach Park

⬥ Apple Maps 검색 이력 DB /private/var/mobile/Containers/Shared/AppGroup/680BC20F-.../Maps/MapsSync\_0.0.1를 파싱함.  
⬥ 2024-11-03 09:47:45 UTC에 검색된 장소가 버몬트주 버링턴에 위치한 North Beach Park (60 Institute Rd, New North End, Burlington, VT)임을 도출함.

**098**  
질문: Using format YYYY-MM, When was this device purchased?

오답1: 2024-09

⬥ 기기 내부 파일 분석 결과 구매 날짜 직접 기록은 존재하지 않으나, 최초 설정 및 활성화 기록을 분석함.  
⬥ Setup Assistant: com.apple.purplebuddy.notbackedup.plist 파일에 iOS 17.4.1 기반 기기 최초 설정 기록(2024년 9월 22\~23일 추정)이 존재함.  
⬥ Activation Record: activation\_record.plist 파일 최종 수정 시각이 2024-09-23 16:43:07 UTC로 기록되어 있어 해당 시점에 기기가 활성화되었음을 확인함.  
⬥ 보증 파일(...\_Warranty.plist) 기준 1년 보증 만료 상태(Coverage Expired)이므로, 현 사용자의 중고/리퍼비시 구매 또는 재설정 시점인 2024-09를 정답으로 도출함.

오답2: 2024-09

⬥ 활성화 기록 파일(/Library/activation\_records/activation\_record.plist)을 추가 분석하여 타임라인을 정밀 재구성함.

* 2022-10: 기기 제조 일자 "manufacturingDate":"2022-10-18T16:14:31Z" (China).  
* 2023-11 이전: 최초 리테일 판매 추정 시점 (2024년 11월 기준 1년 보증 만료 상태).  
* 2024-09: Ruth 계정으로의 기기 활성화 및 최초 설정 시점 (2024년 9월 22\~23일, 활성화 증명서 발급 2024-09-23 16:43:20 UTC).

⬥ Ruth가 기기를 입수/활성화하여 사용하기 시작한 시점인 2024-09를 정답으로 확정함.

오답3: 2024-09

⬥ 보증 캐시, 활성화 기록, 설정 기록, Safari 이력, 메시지, 메모 등 전체 파일 수색 결과 실제 '구매 영수증/구매일' 데이터는 기기 내에 미보존 상태임.  
⬥ 기기 시리얼 번호(FH49Q1TVX6, iPhone 14 Plus) 및 2024-09-23 활성화 타임스탬프를 종합하여 Ruth의 입수/활성화 시점인 2024-09를 최종 정답으로 도출함.

**099**  
질문: Who is the author of the October 2023 wallpaper?

정답: nicole vranjican

⬥ Ruth의 iCloud Drive Downloads 폴더에 저장된 배경화면 PDF 파일 October-2023-iphone-wallpaper-1170-x-2436-px-1.pdf의 문서 속성(Document Properties)을 파싱함.  
⬥ 해당 파일의 Author 메타데이터 필드에 명시된 작성자 이름 nicole vranjican을 도출함.

**100**  
질문: What popular coffee company did Ruth get coffee from?

정답: Dunkin’

⬥ Apple Maps 이력 DB(MapsSync\_0.0.1)를 파싱함.  
⬥ 2024-11-01 01:36:08 UTC에 검색된 매장 정보 Dunkin', 1220 Williston Rd, South Burlington, VT 05403를 확인함.  
⬥ Starbucks 등 타 브랜드 검색 기록이 없으며, 대형 커피 프랜차이즈 브랜드로서 Dunkin' (Dunkin' Donuts)을 정답으로 도출함.

**101**  
질문: What link redirects you to apply for a job?

오답1: \-

⬥ Safari, SMS/iMessage, Discord, Mail(43개 중 주요 이메일 30개), Pinterest, Trello, Adobe Express 등 텍스트 데이터 전수 조사 결과 링크 미발견됨.  
⬥ iOS 사진 검색 색인(psi.sqlite)에서 Pinterest로부터 저장된 이미지의 OCR 텍스트 "we're hiring", "much", "fun", "it's", "scary", "grow"가 감지됨.  
⬥ 대상 이미지: /private/var/mobile/Media/DCIM/100APPLE/IMG\_0004.JPG (object ID 143195, 2024-11-13 19:58:12 UTC 저장, 716,876 bytes).  
⬥ 해당 이미지에 구인 링크나 QR 코드가 인쇄되어 있을 것으로 판단되며, Autopsy의 미디어 뷰어를 통한 시각적 확인이 필요함.  
⬥ *(참고 \- 하단 이전 질문 보충)*: 2024-11-05 00:18 UTC 수신된 Discord 로그인 이메일에서 Discord 로그인 IP 184.171.159.153 (Burlington, Vermont) 확인됨.

오답2: \-

⬥ apply, job, career, hiring, recruit, forms, bit.ly, linktr, lever, greenhouse, workday, indeed 키워드를 포함한 URL 전수 검색 결과 일치 항목 없음.  
⬥ 2024-11-13 19:58 UTC 저장 이미지 IMG\_0004.JPG (object 143195\) 내 인쇄된 URL/QR 코드 확인이 필요하며, 1분 뒤 저장된 IMG\_0005.JPG도 확인 대상으로 제시됨.

오답3: \-

⬥ Instagram 활동 로그, 브라우저 캐시, 메시지, Discord, Pinterest, TikTok, Trello, Photos 라이브러리 전체 수색 결과 텍스트 형태의 링크는 미존재함.  
⬥ 가장 유력한 소스는 Pinterest에서 저장된 DCIM/100APPLE/IMG\_0004.JPG (object 143195\) 및 IMG\_0005.JPG (object 143196\) 이미지임.  
⬥ Autopsy 뷰어로 해당 이미지를 열어 인쇄된 URL을 읽거나 QR 코드를 스캔해야 정확한 채용 지원 링크 도출이 가능함.

**102**  
질문: When was the last written record created? (format YYYY-MM-DD HH:MM:SS)

오답1: 2024-11-13 17:53:05 \~ 17:57:19

⬥ Apple Notes DB (NoteStore.sqlite 및 WAL 로그) 분석 결과, 마지막 작성 메모는 손글씨 그림 노트(New Note, 노트 ID BC2C2DD6-3A5B-4DF5-ACC4-D1F98ED79C70)임.  
⬥ 바이트 훼손으로 정확한 초 단위 측정에 한계가 있어 타임라인 추정 범위(17:53:05 \~ 17:57:19 UTC)를 산출함.  
⬥ 정확한 타임스탬프 계산을 위해 ZICCLOUDSYNCINGOBJECT 테이블 내 ZCREATIONDATE1 수치 파싱이 제안됨.

오답2: 2024-11-13 18:04:13

⬥ Notes용 검색 색인 로그(Search-index log)에서 손상되지 않은 생성 시각 바이트를 발견하여 교차 파싱을 진행함.  
⬥ Apple 타임스탬프 수치 753213853.536483 (2001-01-01 기준 초)를 변환하여 정확한 생성 시각 2024-11-13 18:04:13.536 (UTC)를 도출함.  
⬥ 해당 메모는 DB 저장 시각(18:00:57) 이후 변경 로그에 기록된 최신 작성 메모임.

오답3: 2024-11-13 18:04:13

⬥ 기기 내 존재 하는 전체 3건의 메모 타임라인 전수 재검증:

1. To do list for 10/4: 2024-09-27 생성  
2. 12×18=216: 2024-11-13 약 17:52\~17:53 생성  
3. 43 (내용: *every 2 Weeks for 432 / 12 hours of work*): 2024-11-13 18:04:13.536 (UTC) 생성

⬥ 작성 메모 중 가장 마지막으로 생성된 데이터가 노트 43이며, 정식 포맷에 맞춘 최종 생성 시각은 2024-11-13 18:04:13 (UTC)임.  
**8.3 2025 CTF 이미지\_iPhone**

**이미지 기본 정보**

| 이미지명 | iPhone |
| :---: | :---: |
| 이미지 형식 | zip |
| Autopsy Case명 | 25\_iPhone14Plus |
| 문항 수  | 20 |
| 실험자 | 진세라 |
| 정답률 | 14/20(70%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 083 | 18.0 | 18.0 | T | 시스템 버전 파일 경로 및 속성(/System/Library/CoreServices/SystemVersion.plist), 디바이스 식별자 |
| 084 | 18024959063 | \+1 (802) 495-9063 | T | com.apple.commcenter.plist(기기 전화번호 설정 파일) |
| 085 | Mary | Mary | T | 연락처 DB, DB WAL(/private/var/mobile/Library/AddressBook/) |
| 086 | 0 | 0 | T | CallHistory.storedata, CallHistory.storedata-wal |
| **087** | **51** | **48** | **F(3)** | **user\_model\_database.sqlite, tium.totalWordsAutocorrected**  |
| 088 | 2:15 | 2:15 | T | /Library/Caches/com.hammerandchisel.discord/fsCachedData/70B7CE99-8702-484B-BE16-42566F47035F, chat timestamp data, Discord Accounts |
| **089** | **blonde** | **\-** | **F(3)** | **avatar\_data, builder\_section\_persistence\_v2\_store, Library/Caches/bitmojiNotif/870a5b8a-f92b-4b63-889e-81cf00cfa6ee\_bigquery**  |
| 090 | Canva: AI Photo & Video Editor | Canva | T | App Store 구매 기록 데이터, App Store Metadata(/private/var/containers/Bundle/Application/D2C87DAC-F3D4-4036-A7D5-B0BFB878EF7A/iTunesMetadata.plist) |
| **091** | **184.171.159.153** | **66.22.212.147** | **F(3)** | **Library/Caches/com.hammerandchisel.discord/Cache.db 및 [Cache.db](http://Cache.db)\-wal, mmkv.default,**  |
| 092 | 36.1660667 | 36.1660667 | T | /private/var/mobile/Containers/Shared/AppGroup/5A25F7AB-6542-44BF-BFF0-3A1B6E0EC1F1/Library/Preferences/group.com.apple.weather.plist  |
| 093 | 432 | 432 | T | /private/var/mobile/Containers/Shared/AppGroup/48006795-907F-4242-865D-11B66F78AC1E/NoteStore.sqlite |
| 094 | com.toyopagroup.picaboo | com.toyopagroup.picaboo | T | /private/var/mobile/Library/TCC/TCC.db |
| 095 | EARLYBF24 | EARLYBF24  | T | SMS 내역 데이터 |
| 096 | 2024-11-12 22:11:09 | 2024-11-12 22:11:09  | T | /Library/AWEStorage/UnifyStorage.sqlite  |
| 097 | North Beach Park | North Beach Park  | T | /private/var/mobile/Containers/Shared/AppGroup/680BC20F-C78B-4F5E-B1EB-25679152C374/Maps/MapsSync\_0.0.1, 지도 검색 기록 |
| **098** | **2022-12** | **2024-06** | **F(3)** | **/private/var/mobile/Library/Preferences/com.apple.NewDeviceOutreach.plist, mobileactivationd cache and DB** |
| 099 | nicole vranjican | nicole vranjican | T | /private/var/mobile/Library/Mobile Documents/com\~apple\~CloudDocs/Downloads/October-2023-iphone-wallpaper-1170-x-2436-px-1.pdf  |
| 100 | Dunkin’ | Dunkin’  | T | /private/var/mobile/Containers/Shared/AppGroup/680BC20F-C78B-4F5E-B1EB-25679152C374/Maps/MapsSync\_0.0.1 |
| **101** | **https\://delivr.com/2fsmr-qr** | **\-** | **F(3)** | /private/var/mobile/Library/Mail/MessageData/24/full.emlx |
| **102** | **2024-11-20 20:02:02** | **2024-11-13 13:00:49**  | **F(3)** | Apple Notes DB, NoteStore.sqlite-wal |

**AI 답변 및 실행 근거 상세 기록**

##### **083**

**질문: What is the system version and build number of the iOS device?**  
정답 : iOS 18.0 / 22A3354

* 실행 근거:  
  * /System/Library/CoreServices/SystemVersion.plist (Object ID: 148236\) 분석.  
  * ProductName: "iPhone OS", ProductVersion: 18.0, ProductBuildVersion: 22A3354 파싱 및 확인.  
      
    

##### **084**

**질문: What is the device's phone number and SMS center number (smsc)?**  
정답 : \+18024959063

* 실행 근거:  
  * /private/var/wireless/Library/Preferences/com.apple.commcenter.plist (Object ID: 148188)에서 전화번호 \+18024959063 추출.  
  * com.apple.commcenter.device\_specific\_nobackup.plist (Object ID: 148187)의 smsc 키값에서 SMS 센터 번호 \+13123149810 도출.  
      
    

##### **085**

**질문: What is the contact name associated with the contact photo updated on 2024-11-13?**  
오답1: \-

* 실행 근거:  
    
  * AddressBookImages.sqlitedb-wal (Object ID: 130532, 수정 시각: 2024-11-13 17:45:05 UTC)을 통해 사진 변경 시각은 확인했으나 연락처 이름을 특정하지 못함. 

오답2 : \-

* 실행 근거:  
  * /private/var/mobile/Library/AddressBook/ 경로 내 AddressBook.sqlitedb DB 및 WAL 파일을 검토했으나 이름 매칭 실패.   
    

정답 : Mary

* 실행 근거:  
  * /private/var/mobile/Library/PersonalizationPortrait/Contacts/name\_records/1.pb (Object ID: 139385\) 프로토콜 버퍼 파일 분석.  
  * Contact ID (1411E2DB-1775-4518-8E56-BBD7304FDD36:ABPerson)와 연결된 연락처 이름 Mary 도출.  
      
    

##### **086**

**질문: How many incoming calls were answered according to the call log database?**  
오답1 : \-

* 실행 근거:  
  * Autopsy 내 13개의 Call-log 항목을 도출했으나, 수신 여부 및 응답 플래그 디코딩 미완료.   
    

오답2 : \-

* 실행 근거:  
  * iLEAPP 리포트(Call History.html) 및 ZCALLRECORD 테이블 조건(ZORIGINATED \= 0, ZANSWERED \= 1)을 파악했으나 정답 수치 제시 미완료.

오답3 : \-

* 실행 근거:  
  * CallHistory.storedata-wal 내 재시도 통화 패턴 분석을 진행했으나 최종 집계 결과 정리 미완료.

정답 : 0 (None)

* 실행 근거:  
  * CallHistory.storedata-wal (Object ID: 137237\) 내 총 13건의 수신 기록 전수 디코딩.  
  * 모든 통화의 Answered flag가 0, Call duration이 0으로 부재중 처리되어 응답 통화 수 0 확인.

##### **087**

**질문: How many total words were autocorrected according to the keyboard learning database?**  
오답1 : \-

* 실행 근거:

  * user\_model\_database.sqlite (Object ID: 139004\) 내 usermodeldurablerecords 테이블 분석 진행.

오답2 : \-

* 실행 근거:  
  * WAL 카운터 참조 필드(tium.wordsAutocorrected 등)를 교차 검증 중 정답 미확정.

정답 : 48

* 실행 근거:  
  * /private/var/mobile/Library/Keyboard/user\_model\_database.sqlite 내 usermodeldurablerecords 테이블 조회.  
  * tium.totalWordsAutocorrected 키값의 48을 확인.

##### **088**

**질문: What time was the meeting scheduled for in the Discord chat cache?**  
정답 : 2:15 PM (US Eastern)

* 실행 근거:  
  * /Library/Caches/com.hammerandchisel.discord/fsCachedData/70B7CE99-8702-484B-BE16-42566F47035F 디스코드 캐시 파싱.  
  * Ruth와 Mary의 대화 중 2024-11-05 17:30:30 UTC 메시지 *"How does Black Cap around 2:15 sound?"* 레코드에서 약속 시각 2:15 PM 도출.

##### **089**

**질문: What is the filename and path of the Bitmoji notification cache image?**  
오답1: \-

* 실행 근거:  
  * Snapchat 컨테이너 내 avatar\_data 및 cronet/disk\_cache/ 내 타 후보 이미지 분석.

오답2 : \-

* 실행 근거:  
  * Library/Caches/bitmojiNotif/ 경로 내 PNG 파일 탐색 및 검토.

정답 : 870a5b8a-f92b-4b63-889e-81cf00cfa6ee\_bigquery (경로: Library/Caches/bitmojiNotif/)

* 실행 근거:  
  * Snapchat 비트모지 렌더링 캐시 경로 Library/Caches/bitmojiNotif/870a5b8a-f92b-4b63-889e-81cf00cfa6ee\_bigquery (Object ID: 107395\) 확정  
      
      
    

##### **090**

**질문: What AI application was installed on 2024-11-13 at 19:45:32 UTC?**  
오답1 : \-

* 실행 근거:  
  * iTunesMetadata.plist 내 여러 앱(Canva, Fishdom, ChatGPT 등)의 purchaseDate 타임스탬프 나열.

오답2 (25\_ios\_090\_1): \-

* 실행 근거:  
  * ChatGPT (19:48:17 UTC)와 Canva (19:45:32 UTC) 비교 검토 진행.

정답 (25\_ios\_090\_2): Canva

* 실행 근거:  
  * /private/var/containers/Bundle/Application/.../iTunesMetadata.plist 파싱.  
  * com.canva.canvaeditor (Canva: AI Photo & Video Editor)의 purchaseDate가 2024-11-13 19:45:32 UTC 임을 입증.

##### **091**

**질문: What is the primary Voice Server IP address for the "newark" region in Discord?**  
오답1 : \-

* 실행 근거:  
  * Cache.db-wal 및 latency.discord.media/rtc API 캐시 엔드포인트 탐색.

오답2 : \-

* 실행 근거:  
  * Discord 설정 타임스탬프 및 수신 메일 아티팩트 교차 검증.  
  * newark 지역의 여러 IP 후보군(66.22.212.147, 66.22.214.141 등)을 나열했으나 1순위 확정 미완료.

오답3 : 66.22.212.147

* 실행 근거:  
  * Library/Caches/com.hammerandchisel.discord/Cache.db-wal 및 mmkv.default 내 lastGeoRankedOrder 파싱.  
  * newark 지역 최상위 우선순위 IP 66.22.212.147 확정.  
      
    

##### **092**

**질문: What is the latitude coordinate saved in the Weather app shared plist?**  
정답 : 36.1660667

* 실행 근거:  
  * /private/var/mobile/Containers/Shared/AppGroup/5A25F7AB-6542-44BF-BFF0-3A1B6E0EC1F1/Library/Preferences/group.com.apple.weather.plist 분석.  
  * LocationID:36.1660667:-86.777802 엔트리에서 정확한 위도값 36.1660667 추출.  
      
    

##### **093**

**질문: What was the result of the second handwritten math expression in Apple Notes?**  
정답 : 432

* 실행 근거:  
  * /private/var/mobile/Containers/Shared/AppGroup/.../NoteStore.sqlite 및 WAL 파일 필기 인식 데이터 파싱.  
  * 첫 번째 수식 12×18=216에 이어진 두 번째 수식 216×2=432에서 최종 정답 432 도출.  
      
    

##### **094**

**질문: Which app had its Microphone permission denied in TCC.db?**  
정답 : Snapchat (com.toyopagroup.picaboo)

* 실행 근거:  
  * /private/var/mobile/Library/TCC/TCC.db 파싱.  
  * service: kTCCServiceMicrophone, client: com.toyopagroup.picaboo, auth\_value: 0 (Denied) 레코드 도출.  
      
    

##### **095**

**질문: What was the promotional discount code included in the SMS from Zenni?**  
정답 : EARLYBF24

* 실행 근거:  
  * 2024-11-20 08:55:26 UTC 수신 SMS 본문 분석.  
  * *"Zenni: Early Black Friday \| ... with code: EARLYBF24"* 메세지에서 프로모션 코드 EARLYBF24 도출.

##### **096**

**질문: What is the Video ID and upload timestamp of the first TikTok video viewed?**  
정답 : 7436518844501347616 / 2024-11-12 22:11:09 UTC

* 실행 근거:  
  * /Library/AWEStorage/UnifyStorage.sqlite 및 tracker\_v3.sqlite 분석.  
  * 열람 기록 내 비디오 ID 7436518844501347616 디코딩을 통해 업로드 시각 2024-11-12 22:11:09 UTC 확인.

##### **097**

**질문: What beach was searched for in Apple Maps on 2024-11-03?**  
정답 : North Beach Park

* 실행 근거:  
  * MapsSync\_0.0.1 및 WAL 파일 조회.  
  * 2024-11-03 09:47:45 UTC 검색 기록 레코드에서 North Beach Park (Burlington, Vermont) 도출.  
      
      
    

##### **098**

**질문: What month and year was the iOS device initially activated/purchased?**  
오답1 : \-

* 실행 근거:  
  * com.apple.NewDeviceOutreach.plist 내 DefaultDeviceActivationDate 후보군(2022-05, 2023-06, 2024-06 등) 검토.

오답2 : \-

* 실행 근거:  
  * com.apple.mobileactivationd/Cache.db 생성 시각 분석 진행.

정답 : 2024-06

* 실행 근거:  
  * /private/var/root/Library/HTTPStorages/com.apple.mobileactivationd/httpstorages.sqlite 생성 시각 2024-06-25 16:45:11 UTC 확인.  
  * 보증 설정 파일과의 교차 검증으로 최초 활성화 달 2024-06 확정.  
    

##### 099

질문: Who is the author of the October 2023 wallpaper PDF file in iCloud Downloads?  
정답 : nicole vranjican

* 실행 근거:  
  * /private/var/mobile/Library/Mobile Documents/com\~apple\~CloudDocs/Downloads/October-2023-iphone-wallpaper-1170-x-2436-px-1.pdf 메타데이터 속성 파싱.  
  * Author 필드에서 nicole vranjican 도출.

##### **100**

**질문: What business name and address was viewed in Apple Maps MapsSync?**  
정답 : Dunkin' (1220 Williston Rd, South Burlington, VT)

* 실행 근거:  
  * MapsSync\_0.0.1 DB 내 조회 레코드 파싱.  
  * 상호명 Dunkin' 및 주소 1220 Williston Rd, South Burlington, VT 확정.

##### **101**

**질문: What is the redirect URL contained in the marketing email from Resume-Now?**  
오답1 : \-

* 실행 근거:  
  * Resume-Now 이메일 내 단축 링크 후보 분석.

오답2 : \-

* 실행 근거:  
  * /private/var/mobile/Library/Mail/MessageData/24/full.emlx (Object ID: 139095\) 파싱 진행.

오답3 : [https\://www\.resume-now.com/c/21504?mid=4138&...\&targ=/membership/signin.aspx?...\&targ=https\://www\.resume-now.com/documenthome](https://www.google.com/search?q=https://www.resume-now.com/c/21504%3Fmid%3D4138%26...%26targ%3D/membership/signin.aspx%3F...%26targ%3Dhttps://www.resume-now.com/documenthome)

* 실행 근거:  
  * full.emlx 원본 파일 분석.  
  * 수신된 마케팅 메일 내 실제 리다이렉트 타겟 URL 전체 구조 도출 및 확정.  
      
    

**102**  
**질문: What is the exact creation timestamp (UTC) of the Apple Note with handwritten math?**  
오답1 : \-

* 실행 근거:  
  * NoteStore.sqlite 내 ZCREATIONDATE1 타임스탬프 파싱.

오답2 : \-

* 실행 근거:  
  * UTC 시각과 기기 현지 시각(US Eastern) 변환 비교 진행.

오답3 : 2024-11-13 18:00:49 UTC

* 실행 근거:  
  * NoteStore.sqlite-wal 레코드 정밀 검증.  
  * 손글씨 노후 텍스트("12x18=216 ... 216x2=432") 항목의 생성 시각 2024-11-13 18:00:49 UTC (현지 시각 13:00:49) 확정.

**9\. 2025 CTF 이미지\_Android**

**이미지 기본 정보**

| 이미지명 | Android |
| :---: | :---: |
| 연도 | 2025 |
| 이미지 형식 | Logical Image |
| 이미지 용량 | 27GB |
| 출처 | [2025CTF](https://drive.google.com/drive/folders/1gHQsfx1hqCv-V4Anm2eYukB4jPtraNBH) |
| Autopsy Case명 | 26\_Android |
| 대상 OS | Android |
| 문항 수  | 16 |
| 실험자 | 박제윤, 전시연, 진세라 |

**문항별 실험 기록**

| 문항 | 정답 | AI 답\_박제윤 | AI 답\_진세라 | T/F |
| :---: | :---: | :---: | :---: | :---: |
| 103 | deer | \- | deer | T(50%) |
| 104 | c:geo | c:geo | c:geo | T |
| 105 | library champlain college | library at champlain college | library at Champlain College  | T |
| 106 | mary.jones7358 | mary.jones7358 | mary.jones7358  | T |
| 107 | Ultra | Ultra | Ultra | T |
| 108 | Google Pixel Watch 02N0 | Google Pixel Watch 02N0 | Google Pixel Watch 02N0  | T |
| 109 | Fortnight | Fortnight | Fortnight | T |
| 110 | Associate of Applied Science Marketing  | Associate of Applied Science Marketing | \- | T(50%) |
| 111 | Moran Frame | Moran Frame | Moran Plant / Moran Frame | T |
| 112 | German | \- | \- | F |
| 113 | Teddy Swims | \- | \- | F |
| 114 | noreply@fitbit.com | noreply@fitbit.com | noreply@fitbit.com  | T |
| 115 | 0 | 0 | 0 | T |
| 116 | 32  | \- | 274 | F |
| 117 | 4.23982000350952 | 4.5 | 4.5 | F |
| 118 | \#ee675c | \- | 566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078  | F |

| NO | Question |
| :---: | ----- |
| 103 | What animal was in the TikTok sent via text? |
| 104 | What was the name of the geocacheing app used? |
| 105 | What location was the user looking for on 2024-11-11 at 2:46:10 PM UTC?  |
| 106 | What is the user's TikTok username? |
| 107 | What was the SIM display name? |
| 108 | What device did the user connect to on 2024-11-05? |
| 109 | What song was the user listening to on 2024-11-30 at 8:45:00 AM? |
| 110 | What degree does Mary have? |
| 111 | What is the name of the structure seen in the picture taken at night? |
| 112 | What language was the nature website in? |
| 113 | What singer appeared in a TikTok video watched on 2024-11-15 at 1:01:26 AM UTC? |
| 114 | Who congratulated Mary on walking 10,000 steps? |
| 115 | How many followers does Mary have on TikTok? |
| 116 | How many spam numbers were created on 2024-11-27 at 02:42:52.972 UTC? |
| 117 | What’s the numerical rating for the app with the most installs? |
| 118 | What is the hex code for the Profile Picture with the number (802) 495-9063? |

**9.1 2025 CTF 이미지\_Android**

**이미지 기본 정보**

| 이미지명 | Android |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 25\_Android |
| 문항 수  | 16 |
| 실험자 | 박제윤 |
| 정답률 | 10/16(62%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| **103** | **deer** | **\-** | **F(3)** | **SMS / Messages Database, TikTok app cached feed videos, Web History & Notifications** |
| 104 | c:geo | c:geo | T | cgeo.geocaching |
| 105 | library champlain college | library at  champlain college | T | Chrome activity / Chrome searches and browsing history |
| 106 | mary.jones7358 | mary.jones7358 | T | com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml |
| 107 | Ultra | Ultra | T | telephony.db |
| 108 | Google Pixel Watch 02N0 | Google Pixel Watch 02N0 | T | /data/misc/bluedroid/bt\_config.conf |
| 109 | Fortnight | Fortnight | T | com.google.android.as/databases/history\_db |
| **110** | **Associate of Applied Science Marketing**  | **Associate of Applied Science Marketing** | **T(2)** | **marysresume.pdf** |
| **111** | **Moran Frame** | **Moran Frame** | **T(3)** | **PXL\_20241112\_024249328.jpg** |
| **112** | **German** | **\-** | **F(3)** | **Chrome on the phone, In-App Browsers, The Geocaching app (c:geo), Full Gmail mailbox & Texts** |
| **113** | **Teddy Swims** | **\-** | **F(3)** | **/data/data/com.zhiliaoapp.musically/cache/cachev2/v12025gd0000crdf5evog65ml3ljf1pg\_bytevc1\_720p\_604678.md1, TikTok feed caches and offline feed database, TikTok watch-event logs, TikTok notification log** |
| 114 | noreply@fitbit.com | noreply@fitbit.com | T | All mail Including Spam and Trash.mbox |
| 115 | 0 | 0 | T | com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml |
| **116** | **32** | **\-** | **F(3)** | **/data/data/com.google.android.dialer/databases/normalized\_spam.db, normalized\_spam.db-shm** |
| **117** | **4.23982000350952** | **4.5** | **F(3)** | **/data/data/com.android.vending/cache/streamdatastore/[streamdatastore.db](http://streamdatastore.db)** |
| **118** | **\#ee675c** | **\-** | **F(3)** | **/data/data/com.google.android.apps.messaging/databases/bugle\_db, com.google.android.apps.messaging/cache/image\_manager\_disk\_cache/, aLEAPP report** |

**AI 답변 및 실행 근거 상세 기록**  
**103**  
질문: What animal was in the TikTok sent via text?

오답1: \-

⬥ 2024-11-15 16:29:33 UTC에 \+18024959063 번호로 TikTok 링크(\[https\://www\.tiktok.com/@dochristmass/video/7436518844501347616\](https\://www\.tiktok.com/@dochristmass/video/7436518844501347616))가 전송됨.  
⬥ 2024-11-17 수신자가 "Laughed at..." 리액션을 남겼으나, 메시지 본문에는 캡션이나 미리보기 없이 단순 URL만 기록되어 있어 어떤 동물인지 식별 불가함.  
⬥ 정확한 확인을 위해서는 기기 내 이미지/비디오 캐시 및 썸네일을 조회하거나 온라인 링크를 직접 열어봐야 함을 안내함.

오답2: \-

⬥ 외부 온라인 링크 접근 요청이 거부되어 해당 URL을 직접 열지 못함.  
⬥ 기기 내부 오프라인 환경에서 틱톡 앱 데이터, 이미지/동영상 파일, 웹 캐시 내 썸네일 및 복사본 존재 여부를 재검색할지 여부를 묻고 있음.

오답3: \-

⬥ 캐시 복사본 부재: 틱톡 앱 내 10개의 피드 동영상 캐시가 있으나 해당 비디오 ID(7436518844501347616)와 일치하는 파일이 없음.  
⬥ 미리보기/캡션 부재: 웹 방문 기록, 캐시, 알림 어디에도 비디오 ID 및 @dochristmass 계정의 미리보기가 없음.  
⬥ 링크 복사 정황: URL 단절 매개변수(sender\_device=pc) 분석 결과 PC 웹사이트에서 복사되어 문자로 전달된 링크로, 폰의 틱톡 앱에서 실제 재생되지 않았음이 밝혀짐.  
⬥ 최종 결론: 오프라인 포렌식 데이터만으로는 동영상 속 동물을 식별할 수 없으며, 링크 직접 접속이 유일한 확인 방법임.

**104**  
질문: What was the name of the geocacheing app used?

정답: c:geo

⬥ 기기에 설치된 앱 로그 분석 결과 지오캐싱 전용 앱은 c:geo(cgeo.geocaching)가 유일함.  
⬥ 2024-10-23 19:58:02 UTC에 Canva, Blip, Audubon 등의 앱들과 함께 설치되었음을 확인함.

**105**  
질문: What location was the user looking for on 2024-11-11 at 2:46:10 PM UTC?

정답: library at champlain college

⬥ Chrome 브라우저 검색 이력 파싱 결과 타임존 오프셋(9시간 차이)이 적용된 05:46:10 UTC 타임스탬프에서 검색어 library champlain college를 확인함.  
⬥ 동일 시각 Chrome 캐시 쓰기 기록이 14:46:10 UTC에 정밀하게 일치하여 검색 대상 장소가 library at Champlain College임을 도출함.

**106**  
질문: What is the user's TikTok username?

정답: mary.jones7358

⬥ TikTok 앱의 설정 파일 com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml을 분석함.  
⬥ 로그인된 계정의 Username 필드에 명시된 사용자명이 mary.jones7358 (프로필 링크: \[tiktok.com/@mary.jones7358\](https\://tiktok.com/@mary.jones7358), 표시 이름: Mary Jones)임을 파싱함.

**107**  
질문: What was the SIM display name?

정답: Ultra

⬥ 시스템 DB telephony.db 내 siminfo 테이블의 로우 바이트 데이터를 파싱함.  
⬥ display\_name 필드에 기록된 SIM 표시명이 Ultra (Ultra Mobile 통신사, ICCID 8901240357120704346, 전화번호 \+1 802-829-2741, MCC/MNC 310/240)임을 확인함.

**108**  
질문: What device did the user connect to on 2024-11-05?

정답: Google Pixel Watch 02N0

⬥ 블루투스 설정 파일 /data/misc/bluedroid/bt\_config.conf 내 기록을 분석함.  
⬥ 2024-11-05 19:12:23 UTC에 블루투스로 페어링된 기기가 Google Pixel Watch (사용자 지정명: Mary’s Google Pixel Watch, MAC 주소: 14:22:3b:9a:19:01)임을 확인함.  
⬥ 당일 연동 타임라인 분석 결과:

* 19:11:52: Pixel Watch 동동 앱(com.google.android.apps.wear.companion) 설치  
* 19:12:23: 블루투스 워치 페어링 완료  
* 19:14:50: Fitbit 앱 설치  
* 19:21: Calm, Komoot, Strava 앱 설치

**109**  
질문: What song was the user listening to on 2024-11-30 at 8:45:00 AM?

정답: Fortnight

⬥ Pixel의 음악 인식 기능인 "Now Playing" 로그 DB(com.google.android.as/databases/history\_db 파일 내 recognition\_history 테이블)를 파싱함.  
⬥ 2024-11-30 08:44:18 \~ 08:45:23 UTC 시간대에 정확히 08:45:00을 포함하는 곡으로 Fortnight \- Taylor Swift (feat. Post Malone) (*The Tortured Poets Department* 앨범)가 인식 및 기록되어 있음을 확인함.  
⬥ 주변 재생 타임라인 데이터 (2024-11-30 UTC):

* 08:44:18 \~ 08:45:23: Fortnight \- Taylor Swift  
* 08:50:15: I Can Do It With a Broken Heart \- Taylor Swift  
* \~08:53 \~ 08:54: august \- Taylor Swift  
* \~08:55 \~ 08:56: cardigan \- Taylor Swift  
* \~09:00 \~ 09:02: Lover \- Taylor Swift

**110**  
질문: What degree does Mary have?

오답: \-

⬥ 이력서 파일(marysresume.pdf, Jones\_Resume2024.docx)이 존재하나 PDF 텍스트 압축 및 Autopsy 텍스트 파서의 데이터 손상으로 학위 정보 확인 불가함.  
⬥ 해결 방법으로 컴퓨터 제어 허용, Autopsy Indexed Text 탭 직접 확인, 또는 Gmail 백업(mbox) 분할 파싱을 제시함.

정답: Associate of Applied Science in Marketing

⬥ Takeout 이메일 백업 내 이력서 첨부파일(marysresume.pdf)의 Base64 데이터를 디코딩하여 'Education and Training' 섹션을 분석함.  
⬥ 이력서에 명시된 학위 정보: Associate of Applied Science, Marketing — Champlain College, Burlington, VT — 05/2022.  
Mary는 Champlain College에서 2022년 5월에 취득한 마케팅 전문학사(AAS) 학위를 소지하고 있음이 최종 확인됨.

**111**  
질문: What is the name of the structure seen in the picture taken at night?

오답1: \-

⬥ 기기 내 Google Takeout 메타데이터상 2024년 11월 11일 야간(EST 기준)에 촬영된 사진 2건을 식별함:

* PXL\_20241112\_024249328.jpg: 11월 11일 9:42 PM (02:42:49 UTC), GPS 좌표 44.4815861, \-73.2237028  
* PXL\_20241112\_030013300.jpg: 11월 11일 10:00 PM (03:00:13 UTC), GPS 좌표 44.4903611, \-73.2347194

⬥ 두 지점 모두 버몬트주 버링턴의 샴플레인 호수 수변 근처이나, 시각적 이미지 확인 없이는 구조물명을 추정할 수 없음.

오답2: \-

⬥ 추출 폴더 접근 요청이 재차 거절되어 사진 파일 직접 개봉이 불가능함.  
⬥ 이미지 파일 직접 첨부 또는 Autopsy 내 간접 정황(검색어, 지도, 렌즈 검색, 메시지 등) 추가 조사를 해결책으로 제시함.

정답: Moran Frame

⬥ 첫 번째 야간 사진 PXL\_20241112\_024249328.jpg (2024-11-12 02:42:49 UTC)의 GPS 좌표(44.4815861, \-73.2237028)를 교차 분석함.  
⬥ 해당 위치에서 약 60m 떨어진 거리에 야간 조명이 켜지는 수변 랜드마크인 옛 모란 석탄 화력발전소 철골 구조물 Moran Frame (475 Lake St, 좌표 44.4820645, \-73.2240637)이 위치함.  
⬥ 촬영 직전(02:42:25\~28 UTC) Google Maps 실행 기록이 존재하여 해당 랜드마크가 촬영 구조물일 가능성이 가장 높음.  
⬥ (18분 뒤 촬영된 두 번째 사진 PXL\_20241112\_030013300.jpg는 해안 자전거 도로 북쪽 1.3km 지점으로 인근에 명확히 일치하는 랜드마크가 없음)

**112**  
질문: What language was the nature website in?

오답1: \-

⬥ Android 기기 내 Chrome 방문 이력, 인앱 브라우저(Google, Discord, Root Browser, Gmail, Maps, Fitbit, TikTok), Takeout 활동 내역, 문자 메시지, Gmail 메일함(약 200건) 전수 조사 진행함.  
⬥ 검색된 브라우징 및 이메일 내역은 모두 영어(English) 기준이며, 유일한 비영어 항목은 강아지 동영상 관련 스페인어(Spanish) TikTok 알림 메시지 1건뿐임.  
⬥ 해당 질문은 현 안드로이드 기기가 아닌 타 기기(Chromebook, MacBook, iOS 등)의 데이터일 가능성이 높음을 제시함.

오답2: \-

⬥ Chrome 사이트 아이콘, 네트워크 이력, 주소창 바로가기, 뉴스 피드(CNN, CBS News, NPR, The Dodo 등), c:geo 앱, Discord/Google/Root Browser 인앱 브라우저 전수 재검색 결과 자연 관련 웹사이트 방문 기록 부재함.

오답3: \-

⬥ Chrome 디스크 웹 캐시 배치 분석 결과:

* 11 Nov, 14:44-14:46: Starbucks, Champlain College 검색  
* 15 Nov, 00:32: Google Support (Android 버전 도움말)  
* 15 Nov, 01:00: Facebook 로그인 페이지  
* 15 Nov, 04:19: Chrome 새 탭 뉴스 피드 아이콘/아이콘 썸네일  
* 17 Nov, 20:27: Nike Run Club 로그인

⬥ 3차에 걸친 정밀 수색 결과 본 기기(25\_Android)에는 자연 관련 웹사이트 접속 기록이 없으므로, 분석 대상을 다른 기기(특히 Chromebook 등)로 전환해야 함을 최종 확인 및 명시함.

**113**  
질문: What singer appeared in a TikTok video watched on 2024-11-15 at 1:01:26 AM UTC?

오답1: \-

⬥ 대상 파일 식별: 2024-11-15 01:01:26 UTC에 저장된 TikTok 캐시 비디오 파일 v12025gd0000crdf5evog65ml3ljf1pg\_bytevc1\_720p\_604678.md1 (Autopsy object ID 29155, 경로 /data/data/com.zhiliaoapp.musically/cache/cachev2/, 2.65 MB)를 확인했음.  
⬥ 메타데이터 파싱 결과: 임베디드 비디오 ID 태그(vid:v12025gd0000crdf5evog65ml3ljf1pg)만 존재할 뿐, 캡션, 계정명, 곡명 정보가 일절 포함되어 있지 않음.  
⬥ 추가 로그 검색: TikTok 피드 캐시, 오프라인 DB, 시청 이벤트 로그(01:02:22 UTC부터 시작), 네트워크 응답 수색 결과에서도 가수 이름을 확인할 수 없음.  
⬥ Autopsy에서 해당 객체(29155)를 파일 추출(Extract File(s)) 후 확장자를 .mp4로 변경하여 직접 재생해야 함을 안내함.

오답2: \-  
⬥ 추출 폴더 접근 요청이 다시 거절되어 비디오 개봉 및 프레임 확인이 차단됨.  
⬥ Autopsy 파일 리더는 비디오를 깨진 텍스트 형태로만 출력하므로 시각적 확인이 불가능함.  
⬥ 해결 대안으로 Autopsy에서 객체 29155 추출 후 .mp4 재생, 추출 파일 직접 첨부, 또는 Downloads\\UserB2-001 폴더 접근 허용을 요청함.

오답3: \-

⬥ TikTok 알림 로그 및 기기로 푸시된 비디오 ID 목록까지 확장 수색했으나, 01:01:26 UTC 재생 영상의 캡션/계정/곡명 정보는 발견되지 않음.  
⬥ 3차에 걸친 폴더 접근 요청 거절로 직접 파일 개봉이 불가하므로, 텍스트 아티팩트만으로는 영상 속 가수를 식별하는 것이 불가능함.  
⬥ 정답 확인을 위해서는 Autopsy 내 객체 29155 파일을 추출(.mp4)하여 재생하거나 이미지를 직접 첨부해야 함을 최종 확인 및 명시함.

**114**  
질문: Who congratulated Mary on walking 10,000 steps?

정답: [noreply@fitbit.com](mailto:noreply@fitbit.com)

⬥ Google Takeout의 Gmail 메일함(All mail Including Spam and Trash.mbox)을 파싱함.  
⬥ 2024년 11월 12일 03:33:45 UTC (PST 기준 11월 11일 19:33:45)에 Fitbit (noreply@fitbit.com)으로부터 수신된 자동 알림 이메일을 확인하였음.  
⬥ 메일 내용: *"Congrats on earning your first Sneakers badge\!"* (본문: *"Way to go\! You’ve walked 10,000 steps ... And by stepping up your game, you’ve achieved the Sneakers badge."*)

**115**  
질문: How many followers does Mary have on TikTok?

정답: 0

⬥ TikTok 계정 설정 파일 com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml (Autopsy object ID 39435, 2024-11-15 01:00:07 UTC 최종 업데이트) 내 프로필 데이터를 파싱함.   
⬥ Mary의 TikTok 계정(mary.jones7358, UID 7437302565630395435)의 Followers 수치가 0으로 기록되어 있음을 도출함.

**116**  
질문: How many spam numbers were created on 2024-11-27 at 02:42:52.972 UTC?

오답1: \-

⬥ 대상 파일: Google Phone의 스팸 리스트 DB /data/data/com.google.android.dialer/databases/normalized\_spam.db (Autopsy object ID 15221).  
⬥ 분석 상황: 2024-11-27 02:42:52.972 UTC는 Unix 타임스탬프 밀리초 값 1732675372972에 해당하며, 당시 스팸 목록 다운로드가 진행되어 02:42:52.928부터 02:42:53.055 사이 구간에 총 274개의 번호가 기록됨.  
⬥ 밀리초 단위 바이트 손상으로 인해 정확히 .972 시점에 해당되는 수치(주변 밀리초당 약 10\~30개 분포 추정)를 특정할 수 없음.  
⬥ SQLite 뷰어를 통해 SELECT COUNT(\*) FROM server\_spam\_table WHERE created \= 1732675372972; 쿼리를 실행하여 직접 확인할 것을 제안함.

오답2: \-

⬥ 해당 DB 내 스팸 번호들의 정렬 순서를 재확인함.  
⬥ 02:42:52.928부터 .055 구간 내 274개 데이터는 밀리초당 약 10\~30개씩 연속 저장되어 있으나, 정밀 경계선 바이트 손상 문제로 .972 정확한 카운트 도출에 실패함.

오답3: \-

⬥ 3차에 걸친 정밀 재검색에도 불구하고 .972 타임스탬프 밀리초 영역의 바이트 손상 문제는 텍스트 분석 환경에서 해소되지 않음.  
⬥ 정확한 팩트 확인을 위해서는 Autopsy에서 객체 15221 (normalized\_spam.db) 파일 추출 후 WHERE created \= 1732675372972 DB 쿼리를 직접 수행해야 함을 최종 명시함.

**117**  
질문: What’s the numerical rating for the app with the most installs?

오답1: 4.5

⬥ Google Play 스토어의 데이터베이스 /data/data/com.android.vending/cache/streamdatastore/streamdatastore.db (Autopsy object ID 5748, 2024-12-10 최종 업데이트) 내 저장된 앱 목록 약 120개의 다운로드 및 수치 평점 데이터를 분석했습니다.  
⬥ 가장 높은 다운로드 수인 10,000,000,000+ (100억+) 회를 기록한 앱은 Facebook (com.facebook.katana)이며, 해당 앱의 평점은 4.5 (총 1억 5천 1백만 개 평점 기준)입니다.  
⬥ 주요 스토어 목록 다운로드 비교:

* Facebook: Downloads 10,000,000,000+, Rating 4.5  
* Instagram: Downloads 5,000,000,000+, Rating 4.0  
* Messenger: Downloads 5,000,000,000+, Rating 4.7  
* WhatsApp Messenger: Downloads 5,000,000,000+, Rating

오답2: 4.5

⬥ Play 스토어 저장 데이터 전체 기준 최대 다운로드 앱은 여전히 Facebook (100억+ 다운로드)이며, 평점 수치는 4.5입니다.  
⬥ 만약 Mary가 기기에 '실제로 설치했거나 검색한 앱'들 중에서 최다 설치 수를 기록한 앱을 묻는 조건이라면, Discord (500,000,000+ / 5억+ 다운로드)가 해당하며 그 평점은 3.8입니다.

오답3: 4.5

⬥ Protobuf/Hex 수준의 정밀 파싱 검증 결과, 스토어 데이터 상 최다 설치 앱은 100억+ 회를 기록한 Facebook이며 표시 평점 텍스트는 4.5로 최종 확정됩니다.  
⬥ 반올림되지 않은 정밀 소수점 수치는 Autopsy 텍스트 리더의 일부 바이트 훼손으로 인해 4.5 이후 영역 확인이 불가하나, 표기 기준 기본값은 4.5입니다.  
⬥ 사용자가 실제 설치한 앱 목록 범위 내에서는 Discord (500M+ 다운로드, 평점 3.8)가 정답이 됩니다.

**118**  
질문: What is the hex code for the Profile Picture with the number (802) 495-9063?

오답1: \-

⬥ Google Messages DB (bugle\_db 및 WAL 로그, Autopsy objects 8516, 8518\) 내 해당 번호(802-495-9063) 데이터를 조회했습니다.  
⬥ profile\_photo\_uri 필드가 비어있고, 색상 설정값(color\_palette\_index \= 0, color\_type \= 0, extended\_color \= 0)이 0으로 기본 생성 아바타(content://.../AvatarContentProvider/...)를 사용 중입니다.  
⬥ DB 및 aLEAPP 리포트 내 텍스트 형태의 Hex 코드(\#RRGGBB) 데이터는 존재하지 않습니다.  
cache/image\_manager\_disk\_cache/ 폴더 내 캐시 PNG 파일(유력 후보: object ID 8491, 95×95 PNG)을 추출하여 스포이드(Eyedropper) 도구로 색상 값을 추출해야 합니다.

오답2: \-

⬥ 연락처 (802) 495-9063은 Ruth의 번호로, 첫 문자가 2024-11-13 17:32:19 UTC에 수신되었습니다.  
⬥ 메시지 수신 1초 후(17:32:20 UTC) 생성된 프로필 아바타 캐시 PNG 파일 566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078.0 (Autopsy object 8483, 7,913 bytes, RGBA PNG)을 최종 대상 파일로 식별했습니다.  
⬥ 이미지 픽셀 데이터가 압축되어 있어 Autopsy 텍스트 리더로는 색상 값을 직접 읽을 수 없으므로, 해당 객체(8483) 추출 후 이미지 편집기에서 Hex 코드를 확인해야 합니다.

오답3: \-

⬥ 주소록, 연락처 사진 폴더, Google Takeout, Messages 설정, aLEAPP 리포트 전체를 전수 수색했으나 텍스트 형태의 Hex 코드는 기록되어 있지 않습니다.  
⬥ 32비트 PNG 캐시 파일(object ID 8483, 17:32:20 UTC 작성)에 프로필 이미지 픽셀 데이터가 존재하므로, Autopsy에서 파일 추출(Extract File(s)) 후 확장자를 .png로 변경하여 그림판 등의 색상 추출기(Color picker)로 Hex 값을 확인해야 함을 최종 명시합니다.  
**9.3 2025 CTF 이미지\_Android**

**이미지 기본 정보**

| 이미지명 | Android |
| :---: | :---: |
| 이미지 형식 | Logical Image |
| Autopsy Case명 | 25\_Android |
| 문항 수  | 16 |
| 실험자 | 진세라 |
|  | 10/16(62%) |

**문항별 실험 기록**

| 문항 | 정답 | AI 답 | T/F | 조회한 아티팩트 |
| :---: | :---: | :---: | :---: | :---: |
| 103 | deer | deer | T | 문자 메시지 스레드 및 Tiktok 링크 |
| 104 | c:geo | c:geo | T | Installed-Programs Records(cgeo.geocaching) |
| 105 | library champlain college | library at Champlain College  | T | chrome search terms(‘Library champlain college’, ‘starbucks burlington vt’) |
| 106 | mary.jones7358 | mary.jones7358  | T | com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml  |
| 107 | Ultra | Ultra | T | [telephony.db](http://telephony.db)내 siminfo  |
| 108 | Google Pixel Watch 02N0 | Google Pixel Watch 02N0  | T | misc/bluedroid/bt\_config.conf, companion app 설치 기록 |
| 109 | Fortnight | Fortnight | T | [com.google.android.as/databases/history\_db](http://com.google.android.as/databases/history_db), aLEAPP report file |
| **110** | **Associate of Applied Science Marketing**  | **\-** | **F(3)** | **Discord Message, Gmail 첨부파일/다운로드(com.google.android.gm/files/downloads/.../attachments/.../marysresume.pdf)** |
| 111 | Moran Frame | Moran Plant / Moran Frame | T | 사진 metadata, GPS정보, DCIM/Camera/PXL\_20241112\_030013300.jpg |
| **112** | **German** | **\-** | **F(3)** | **chrome History DB, Chrome Cookie, Geocaching HQ 이메일** |
| **113** | **Teddy Swims** | **\-** | **F(3)** | **databases/aweme\_record, 비디오 및 이미지 캐시 파일** |
| 114 | noreply@fitbit.com | noreply@fitbit.com  | T | com.google.android.gm/databases/bigTopDataDB.515120409 |
| 115 | 0 | 0 | T | TikTok 프로필 (com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml) |
| **116** | **32** | **275** | **F(3)** | **스팸 DB (com.google.android.dialer/databases/normalized\_spam.db)**  |
| **117** | **4.23982000350952** | **4.5** | **F(3)** | **play store cache DB(com.android.vending/cache/streamdatastore/streamdatastore.db)** |
| **118** | **\#ee675c** | **566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078**  | **F(3)** | **Google Messages DB, [contacts2.db](http://contacts2.db), Discord profile kv-storage** |

**AI 답변 및 실행 근거 상세 기록**

##### **103**

**질문: What animal was in the TikTok sent via text?**  
오답1 : \- 

* 실행 근거: 2024-11-15 16:29:33 UTC에 \+18024959063 번호로 TikTok 링크([https\://www\.tiktok.com/@dochristmass/video/7436518844501347616](https://www.tiktok.com/@dochristmass/video/7436518844501347616))가 전송되었고, 2024-11-17 수신자가 "Laughed at..." 리액션을 남겼으나 메시지 본문에는 캡션/미리보기 없이 URL만 기록되어 있어 동물 식별에 실패함.  
* 실행 근거: 외부 온라인 링크 접근이 제한되어 URL을 열지 못함에 따라, 기기 내부 오프라인 환경에서 틱톡 앱 데이터, 동영상/이미지 캐시 내 미리보기 존재 여부를 재탐색함.


오답2 : \-

* 실행 근거: 틱톡 앱 피드 캐시 파일 내 비디오 ID(7436518844501347616) 불일치, URL 매개변수(sender\_device=pc) 분석 결과 PC 웹에서 복사되어 문자로 전달된 단절 링크로 폰 앱 내 재생 기록이 없음을 분석했으나 답변 작성 미완료.

정답 : Deer (사슴)

* 실행 근거: 문자 메시지 스레드 내 Ruth의 답장 문구 *"That is so funny\! There's so many deer\! 🦌 🦌 🦌"* 및 🦌(사슴) 이모지 리액션을 포렌식 파싱하여 동물이 Deer (사슴)임을 도출 및 확정함.


  

##### **104**

**질문: What was the name of the geocaching app used?**  
정답 : c:geo

* 실행 근거: 설치된 프로그램 패키지 기록(cgeo.geocaching) 분석. 2024-10-23 19:58:02 UTC에 설치된 지오캐싱 전용 앱이 c:geo임을 확인함.

##### **105**

**질문: What was the second search term performed on Chrome?**  
정답 : champlain college eats

* 실행 근거: Chrome Search Terms 데이터베이스 파싱.  
  * 1st: "starbucks burlington vt" (05:45:16 UTC)  
  * 2nd: "champlain college eats" (05:45:47 UTC)  
  * 3rd: "library champlain college" (05:46:09 UTC)

##### **106**

**질문: What is the user ID and exact account creation timestamp of the TikTok account?**  
정답 : 7437302565630395435 / 2024-11-15 00:57:51 UTC (또는 2024-11-15 00:57 UTC)

* 실행 근거: TikTok 공유 설정 파일 com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml 내 user\_id 레코드 7437302565630395435 파싱. 계정 생성 시각 Unix timestamp 1731632271을 UTC 변환하여 2024-11-15 00:57:51 UTC 도출.

##### **107**

**질문: What is the ICCID and display name of the SIM card?**  
정답 : 8901240357120704346 / Ultra

* 실행 근거: telephony.db 파일 내 siminfo 테이블 조회. display\_name: Ultra, ICCID: 8901240357120704346 레코드 도출.


  

##### **108**

**질문: What is the Bluetooth address and user-assigned name of the paired watch?**  
정답 : 14:22:3b:9a:19:01 / Mary’s Google Pixel Watch

* 실행 근거: 블루투스 설정 파일 misc/bluedroid/bt\_config.conf 파싱. 주소 14:22:3b:9a:19:01 및 사용자 할당 기기명 Mary’s Google Pixel Watch 도출.

##### 

##### **109**

**질문: What song was identified by Pixel "Now Playing" around 08:45 UTC on 2024-11-10?**  
정답 : Fortnight (feat. Post Malone) \- Taylor Swift

* 실행 근거: Pixel Now Playing DB com.google.android.as/databases/history\_db 파싱. 08:44:51 \~ 08:45:24 UTC 시점에 인식된 곡명 Fortnight by Taylor Swift (feat. Post Malone) 추출.


  

##### **110**

**질문: What was the source of Mary's resume PDF file?**  
오답1 : \-

* 실행 근거: Discord 대화 내 이력서 관련 채팅 및 스크린샷 위치를 확인했으나 정확한 다운로드 유입 소스 확정 실패.


오답2 : \-

* 실행 근거: Gmail 첨부파일 다운로드 경로(com.google.android.gm/.../attachments/.../marysresume.pdf)를 탐색했으나 연관 구인 알림 메일과의 최종 교차 검증 정리 미완료.


정답 : Received as an email attachment from Ruth (or Gmail)

* 실행 근거: Gmail DB 및 다운로드 캐시 분석. Ruth(ruthonthego98@gmail.com)가 전달한 이메일 첨부파일로 저장된 marysresume.pdf 경로 및 헤더를 확인함.


  

##### **111**

**질문: What landmark/structure is visible in the photos taken on 2024-11-11 night?**  
정답 : Moran Plant / Moran Frame

* 실행 근거: DCIM 사진 메타데이터(44.4903 N, 73.2346 W)를 기반으로 벌링턴 연안의 Moran Plant 철골 구조물로 특정함.

##### **112**

**질문: Which bird-related website/app was visited or installed?**  
오답1 : \-

* 실행 근거: Chrome 방문 기록 및 스크린샷(Screenshot\_20241104-224419.png)을 검토했으나 새 관련 앱/사이트 식별 미완료.


오답2 : \-

* 실행 근거: Reddit 메일 디제스트(r/birds) 및 스크린샷 아티팩트를 분석 중 정답 도출 정리 미완료.


오답3: \-

* 실행 근거: 2024-10-23에 설치된 조류 관련 앱 Audubon 패키지 설치 기록 및 Reddit r/birds 연관 데이터를 통해 확정함.


  

##### **113**

**질문: What was the video ID of the TikTok video watched at 01:01:26 UTC on 2024-11-15?**  
오답1 : \-

* 실행 근거: databases/aweme\_record 내 AWEME\_READ\_RECORD 테이블에서 시청 기록 및 비디오 캐시(.mdl)를 찾았으나 정리 미완료.

오답2 : \-

* 실행 근거: aweme\_record-wal 프레임 분석(타임스탬프 1731632486810 ms)을 거쳐 캐시 파일과 대조 진행 중.


정답 : 74240402836687786 (또는 7424040283668778614\)

* 실행 근거: aweme\_record-wal 및 캐시 MP4/HEVC 파일 v12025gd0000crdf5evog65ml3ljf1pg\_...mdl 레코드 파싱. 시청 시각 2024-11-15 01:01:26.810 UTC의 정확한 Video ID 74240402836687786 도출.


  

##### **114**

**질문: Who congratulated Mary on walking 10,000 steps?**  
정답 : noreply@fitbit.com 

* 실행 근거: Gmail DB bigTopDataDB.515120409 (Message ID: msg-f:1815486058534065946) 메일 본문 분석. 2024-11-12 03:33 UTC 수신 메일 \*"Congrats on earning your first Sneakers badge\!"\*에서 noreply@fitbit.com 확정


  

##### **115**

**질문: How many followers, following, and posted videos did the TikTok account have?**  
정답 : 0 

* 실행 근거: com.zhiliaoapp.musically/shared\_prefs/aweme\_user.xml 메타데이터 조회. 계정(mary.jones7358)의 Followers: 0, Following: 0, Videos posted: 0 수치를 입증함.

##### **116**

**질문: How many total spam numbers were downloaded in normalized\_spam.db at 02:42:52 UTC?**  
오답1 : \-

* 실행 근거: normalized\_spam.db 타임스탬프(1732675372972 ms) 범위(02:42:52.928 \~ 02:42:53.055 UTC)를 산출했으나 총 개수 미집계.

오답2 : \-

* 실행 근거: server\_spam\_table 조회 쿼리(created \= 1732675372972)를 작성하여 카운트 시도 중.

오답3 : 274

* 실행 근거: com.google.android.dialer/databases/normalized\_spam.db 내 server\_spam\_table 및 client\_spam\_table 쿼리 집계. 타임스탬프 1732675372972 기준 일치하는 스팸 전화번호 레코드 총 274건을 정밀 도출함.


  

##### **117**

**질문: What is the exact rating and download count range for Facebook in Play Store streamdatastore.db?**  
오답1 : \-

* 실행 근거: streamdatastore.db 내 Facebook(com.facebook.katana) 다운로드 수 "10,000,000,000+" 및 평점 표기 "4.5"를 파싱했으나 답변 정리 미완료.


오답2 : \-

* 실행 근거: Instagram, Messenger 등 다른 앱 수치와 비교 분석을 진행 중.


오답3: 4.5

* 실행 근거: Play Store 캐시 DB com.android.vending/cache/streamdatastore/streamdatastore.db 파싱. Facebook 앱의 평점 표기값 4.5 (저장 범위 4.45\~4.55) 및 다운로드 수 10,000,000,000+ 도출 및 확정.




##### **118**

**질문: What is the image hash of Ruth's profile photo in Google Messages cache?**  
오답1 : \-

* 실행 근거: Discord 아바타 해시(8569adcbd36c70a7578c017bf5604ea5)와 Google Messages DB bugle\_db 내 비어있는 profile photo 필드를 확인하여 혼동함.


오답2 : \-

* 실행 근거: Google Messages, Contacts, Meet 등 여러 DB를 탐색하며 프로필 이미지 디스크 캐시 파일 매칭 시도 중.


오답3 : 566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078

* 실행 근거: Google Messages 디스크 캐시 경로 /com.google.android.apps.messaging/cache/image\_manager\_disk\_cache/566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078.0 파싱. Ruth(+1 802-495-9063)에게 문자를 수신한 2024-11-13 17:32:20 UTC 시점에 생성된 PNG 캐시의 정확한 Hex 해시값 566cc257991cf2301c639c1a5229ac9bbd71d29019c0d8b2001591b94f184078을 확정함.

2025  
[2025\_image\_test\_zip](https://docs.google.com/presentation/d/1xAtdCPcIKwuhdm3om6znxU4A1FSuWDJ84HQaGWCm5wI/edit?usp=drive_link)

2026  
[2026\_image\_test\_zip](https://docs.google.com/presentation/d/15Gf-7Q8THqzUUA5d4wuDGwKO8Sz_kL2WvOJUB2wPy6c/edit?usp=drive_link)  
