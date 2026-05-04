# ⚡ WORD CLAW

중2 맞춤 영어 학습 + 보상 시스템 PWA

## 파일 구성
```
wordclaw-app/
├── index.html   ← 앱 전체 (이 파일 하나로 동작)
├── manifest.json ← PWA 설치용
└── README.md
```

## 포함 기능
- ✅ 이메일 회원가입 / 로그인
- ✅ 소셜 로그인 UI (Google, Kakao, Naver, Apple)
- ✅ 부모님 카카오 연결 온보딩
- ✅ 대시보드 (미션, 진도, 주간 차트, 보상)
- ✅ 플래시카드 학습 (130개 단어)
- ✅ 5종 퀴즈 (의미/단어/스펠링/빈칸/해석)
- ✅ 스마트 복습 시스템 (오답 자동 재출제)
- ✅ AI 예문 생성 (Claude API)
- ✅ 미션 & 등급 시스템 (Bronze~Legend)
- ✅ 부모 승인 시뮬레이션
- ✅ 클로 머신 (보상 캡슐 뽑기)
- ✅ AI 일일 학습 리뷰 (Claude API)
- ✅ 부모 뷰 (승인/리포트)
- ✅ 설정 화면
- ✅ LocalStorage 데이터 영속성

## 배포 방법

### 1. GitHub Pages (무료, 가장 빠름)
```bash
# GitHub 저장소 생성 후
git init
git add .
git commit -m "WORD CLAW v1.0"
git push origin main
# Settings → Pages → main branch 선택
# https://yourname.github.io/wordclaw
```

### 2. Netlify (무료, 드래그앤드롭)
1. netlify.com 접속
2. index.html 파일을 드래그앤드롭
3. 완료! (자동 URL 생성)

### 3. Vercel (무료)
```bash
npm i -g vercel
vercel --name wordclaw
```

### 4. 로컬 실행
```bash
# Python 3
python -m http.server 8080
# → http://localhost:8080
```

## Claude API 설정
현재 AI 기능은 Claude API를 직접 호출합니다.
실제 배포 시 API 키 보안을 위해 백엔드 프록시를 추가하세요:

```
[앱] → [자체 백엔드 서버] → [Claude API]
```

## 다음 단계 (백엔드 연동)
- Supabase로 실제 DB 연동
- 카카오 알림톡 API 연동
- 소셜 로그인 실제 연동
- 푸시 알림 (FCM)

## 기술 스택
- React 18 (CDN, 빌드 불필요)
- Babel Standalone (JSX 변환)
- Claude API (AI 기능)
- localStorage (데이터 저장)
- CSS3 애니메이션

