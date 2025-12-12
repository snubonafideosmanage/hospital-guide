# 병원 안내문 웹사이트 배포 가이드

## 📋 개요
반듯한정형외과 환자 안내문을 QR코드로 쉽게 접근할 수 있는 모바일 최적화 웹사이트입니다.

## 🎯 구성 내용

### 1. 메인 페이지 (index.html)
- 4개 카테고리로 구성된 대시보드
- 모바일 친화적인 반응형 디자인
- 직관적인 네비게이션

### 2. 카테고리별 페이지
- **주사치료 주의사항** (injection-precautions.html)
- **부위별 치료 안내** (body-parts.html) - 10개 부위
- **비급여 항목 안내** (non-covered.html) - 2페이지
- **뼈주사 안내** (bone-injection.html)

### 3. 주요 기능
- 이미지 클릭 시 크게 보기 (모달 뷰)
- 모바일 최적화 레이아웃
- 부드러운 애니메이션 효과
- ESC 키로 모달 닫기

## 🚀 GitHub Pages 배포 방법

### 방법 1: GitHub 웹사이트에서 직접 업로드

1. **GitHub 저장소 생성**
   - https://github.com 접속 및 로그인
   - 우측 상단 "+" 버튼 → "New repository" 클릭
   - Repository name: `hospital-guide` (원하는 이름)
   - Public 선택
   - "Create repository" 클릭

2. **파일 업로드**
   - "uploading an existing file" 링크 클릭
   - hospital-guide 폴더의 모든 파일을 드래그&드롭
   - "Commit changes" 클릭

3. **GitHub Pages 활성화**
   - Repository 상단의 "Settings" 탭 클릭
   - 좌측 메뉴에서 "Pages" 클릭
   - Source에서 "Deploy from a branch" 선택
   - Branch를 "main"으로 선택, 폴더는 "/(root)" 선택
   - "Save" 클릭

4. **접속 URL 확인**
   - 몇 분 후 페이지 상단에 배포 URL이 표시됩니다
   - 형식: `https://사용자명.github.io/hospital-guide/`

### 방법 2: Git 명령어 사용 (터미널)

```bash
# hospital-guide 폴더로 이동
cd hospital-guide

# GitHub에서 생성한 저장소 URL로 연결 (본인 URL로 변경)
git remote add origin https://github.com/사용자명/hospital-guide.git

# 푸시
git push -u origin main
```

그 후 위의 "방법 1"의 3번(GitHub Pages 활성화)을 따라하세요.

## 📱 QR 코드 생성

배포 완료 후:

1. 최종 URL 확인 (예: https://사용자명.github.io/hospital-guide/)
2. QR 코드 생성 사이트 방문
   - https://www.qr-code-generator.com/
   - https://www.naver.com (네이버 QR코드)
3. URL 입력하여 QR 코드 생성
4. 다운로드하여 병원 안내문에 인쇄

## 🔧 파일 수정 방법

### 이미지 교체
1. GitHub 저장소에서 해당 이미지 파일 클릭
2. 우측 상단 휴지통 아이콘으로 삭제
3. "Upload files"로 새 이미지 업로드 (파일명 동일하게)

### HTML 수정
1. 해당 HTML 파일 클릭
2. 연필 아이콘(Edit) 클릭
3. 내용 수정 후 "Commit changes"

## 📂 파일 구조

```
hospital-guide/
├── index.html                    # 메인 페이지
├── injection-precautions.html    # 주사치료 주의사항
├── body-parts.html               # 부위별 치료 안내
├── non-covered.html              # 비급여 항목
├── bone-injection.html           # 뼈주사 안내
└── *.png                         # 안내문 이미지들
```

## 💡 사용 팁

### 환자용 안내
- QR 코드를 병원 대기실, 접수처, 진료실에 비치
- "스마트폰으로 QR코드를 찍어 안내문을 확인하세요"라고 안내

### 관리
- 이미지만 교체하면 내용 자동 업데이트
- 파일 수정 후 약 1-2분 후 변경사항 반영

### 추가 기능
- Google Analytics 추가 가능 (접속 통계)
- 검색 기능 추가 가능
- 다국어 버전 제작 가능

## ⚠️ 주의사항

- 모든 이미지 파일명은 한글로 되어 있어야 합니다 (현재 구조 유지)
- 파일명 변경 시 HTML 파일의 src 경로도 함께 수정해야 합니다
- GitHub Pages는 무료이지만 Public 저장소만 가능합니다

## 🆘 문제 해결

### 페이지가 표시되지 않는 경우
1. Settings → Pages에서 올바르게 설정되었는지 확인
2. 브라우저 캐시 삭제 후 재접속
3. URL이 정확한지 확인 (https:// 포함)

### 이미지가 표시되지 않는 경우
1. 파일명이 정확한지 확인 (대소문자, 공백 주의)
2. 모든 이미지 파일이 업로드되었는지 확인
3. 브라우저 개발자 도구(F12)에서 에러 메시지 확인

## 📞 추가 지원

더 자세한 도움이 필요하시면:
- GitHub Pages 공식 문서: https://docs.github.com/pages
- QR 코드 생성 가이드 참고

---
반듯한정형외과 BONAFIDE ORTHOPEDIC CLINIC
