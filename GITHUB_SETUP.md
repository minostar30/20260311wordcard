# GitHub 저장소 업로드 방법

로컬 저장소는 준비되었습니다. 아래 단계대로 GitHub에 새 프로젝트를 생성하세요.

## 1단계: GitHub에서 새 저장소 만들기

1. [GitHub](https://github.com)에 로그인
2. 오른쪽 상단 **+** → **New repository** 클릭
3. 다음 설정 입력:
   - **Repository name**: `korean-wordcard` (또는 원하는 이름)
   - **Description**: `2세 아동용 한글 학습 단어카드 게임` (선택)
   - **Public** 선택
   - ⚠️ **"Add a README file" 체크하지 마세요** (이미 있음)
4. **Create repository** 클릭

## 2단계: 원격 저장소 연결 및 푸시

GitHub에서 저장소를 만든 후 아래 명령어를 실행하세요.  
`YOUR_USERNAME`을 본인의 GitHub 사용자 이름으로 바꾸세요.

```powershell
cd "c:\Users\SD2-21\Downloads\korean-wordcard"

# 원격 저장소 연결
& "C:\Program Files\Git\bin\git.exe" remote add origin https://github.com/YOUR_USERNAME/korean-wordcard.git

# main 브랜치로 푸시 (현재 master이면 main으로 변경 후 푸시)
& "C:\Program Files\Git\bin\git.exe" branch -M main
& "C:\Program Files\Git\bin\git.exe" push -u origin main
```

## HTTPS 인증

`git push` 시 GitHub 로그인 창이 뜨면:
- **Username**: GitHub 사용자 이름
- **Password**: Personal Access Token (PAT)

> 비밀번호 대신 [Personal Access Token](https://github.com/settings/tokens)이 필요합니다.
