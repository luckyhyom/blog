# 맥북 에어 M1 포맷 전 체크리스트

## 1. 백업
- [ ] Homebrew 패키지 목록 백업: `brew leaves > brew-list.txt`

## 2. 로그아웃 (필수, 순서 중요)
- [ ] **"나의 Mac 찾기(Find My Mac)" 끄기** ← 이거 안 끄고 포맷하면 활성화 잠금 걸림
- [ ] Apple ID 로그아웃 (시스템 설정)
- [ ] iMessage 로그아웃
- [ ] iCloud 로그아웃

## 3. 포맷
- [ ] macOS Recovery 진입 (M1: 전원 버튼 길게 누르기)
- [ ] 디스크 유틸리티로 디스크 지우기
- [ ] macOS 재설치

## 4. 재설치 후 복구
- [ ] Apple ID 로그인
- [ ] git 전역 설정 복원
- [ ] Homebrew 재설치 후 `brew-list.txt` 기반 패키지 재설치

## 5. 설치 순서 (의존성 순)

### 5-1. 베이스 (다른 모든 설치의 전제조건)
- [ ] Xcode Command Line Tools: `xcode-select --install`
- [ ] Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

### 5-2. CLI 도구 (brew-list.txt 기반, nvm 포함)
- [ ] `brew install $(cat brew-list.txt)` 로 일괄 설치
- [ ] `colima start` (docker 데몬 구동)

### 5-3. GUI 앱 (brew-casks.txt 기반)
- [ ] `brew install --cask $(cat brew-casks.txt)` 로 일괄 설치
  - google-chrome, visual-studio-code, notion, obsidian, cmux
- [ ] KakaoTalk — brew cask 없음, [공식 사이트](https://www.kakaocorp.com/page/service/service/KakaoTalk)에서 수동 설치