# 🌸 늘봄 - Backend

> 독거노인이나 가족과 따로 사는 분들을 위한 **음성 일기 공유 서비스** (백엔드)
<br>

## 📌 프로젝트 소개
**늘봄**은 사용자가 하루를 **음성으로 기록**하면 자동으로 **텍스트로 변환**하여 저장해 주는 서비스입니다.  
가족들은 언제 어디서나 이 **일기와 녹음 파일**을 함께 확인하며, 서로의 일상을 이어갈 수 있습니다.
<br>



## ✨ 주요 기능
- 🎙️ 음성 녹음 파일 업로드 및 관리
- 📝 음성 → 텍스트 변환(STT) 저장
- 👨‍👩‍👧 가족 단위 공유 및 댓글 기능    
  <br>



## 🛠️ 기술 스택
- **Framework** : Spring Boot
- **Database** : PostgreSQL + Spring Data JPA (Hibernate)
- **Authentication** : Spring Security + JWT
- **AI/STT** : OpenAI Whisper API (또는 Clova Speech API)
- **Infra** : Render / AWS S3 / Cloudflare R2
- **API Docs** : Swagger / SpringDoc OpenAPI
- **Migration** : Flyway  
  <br>



## 🎯 Git Convention

| 이모지 | 타입 | 설명 |
|--------|------|------|
| 🎉 `Start` | Start New Project | 프로젝트 시작 (`:tada:`) |
| ✨ `Feat` | 새로운 기능 추가 | 새로운 기능 구현 (`:sparkles:`) |
| 🐛 `Fix` | 버그 수정 | 버그 해결 (`:bug:`) |
| 🎨 `Design` | UI / CSS 수정 | UI 디자인 변경 (`:art:`) |
| ♻️ `Refactor` | 리팩토링 | 코드 구조 개선 (`:recycle:`) |
| 🔧 `Settings` | 설정 변경 | 환경설정, 설정 파일 수정 (`:wrench:`) |
| 🗃️ `Comment` | 주석 | 필요한 주석 추가/변경 (`:card_file_box:`) |
| ➕ `Dependency/Plugin` | 의존성 추가 | 라이브러리, 플러그인 추가 (`:heavy_plus_sign:`) |
| 📝 `Docs` | 문서 | 문서 수정 (`:memo:`) |
| 🔀 `Merge` | 병합 | 브랜치 병합 (`:twisted_rightwards_arrows:`) |
| 🚀 `Deploy` | 배포 | 배포 관련 작업 (`:rocket:`) |
| 🚚 `Rename` | 이름 변경 | 파일/폴더명 수정 또는 이동 (`:truck:`) |
| 🔥 `Remove` | 삭제 | 파일/코드 삭제 (`:fire:`) |
| ⏪️ `Revert` | 되돌리기 | 이전 버전으로 롤백 (`:rewind:`) |

<br>



## 📝 커밋 메시지 형식

형식: 작업 내용 요약

예: <br>
✨ Feat: 로그인 기능 구현  
🐛 Fix: 로그인 오류 해결

<br>



## 🌿Branch Convention (GitHub Flow)

- `main` : 배포 가능한 브랜치, 항상 배포 가능한 상태를 유지
- `develop` : 개발 중 사용할 브랜치
- `feature/{작성자 이름}/{description}` : 새로운 기능을 개발하는 브랜치
    - 예: `feature/minho/add-login-page`

<br>



## 🔀 Flow

1. `develop` 브랜치에서 `feature` 브랜치 생성.
2. 작업을 완료하고 커밋 메시지에 맞게 커밋.
3. Pull Request를 생성 / 팀원들의 리뷰.
4. 리뷰가 완료 후 `develop` 브랜치로 병합.
5. 배포 시점에 `develop` 브랜치를 `main` 브랜치로 병합.
6. `main` 브랜치 배포 <br>
#### 예시:
```bash
# 새로운 기능 개발 브랜치 생성
git checkout -b feature/minho/기능명

# 작업 후 커밋 & 원격 저장소에 푸시
git add .
git commit -m "✨ Feat: 기능 설명"
git push origin feature/minho/기능명

# ➡️ GitHub에서 PR(Pull Request) 생성
#    base: develop ← compare: feature/기능명
#    팀원들과 코드 리뷰 후 develop 브랜치로 병합
