
`깃 브랜치 이름 변경`
```bash
git config --global init.defaultBranch main
```

---

`vscode에서 숨겨진 파일 보기`
1. vscode 환경설정
2. exclude 검색
3. 맨위에서 /.git 양식 제거

---

`로컬에 파일 만들고 git에 연결하는 방법`
```bash
git remote add origin https://github.com/rlfhrdyd/gitSumm.git

git add .
git commit -m "how to change branch main"
git push origin main
```

---

`git log 짧게 보는 방법`
```bash
git log --oneline
```

---

`커밋 유형 지정`
```text
FEAT : 새로운 기능의 추가
FIX: 버그 수정
DOCS: 문서 수정
STYLE: 스타일 관련 기능(코드 포맷팅, 세미콜론 누락, 코드 자체의 변경이 없는 경우)
REFACTOR: 코드 리펙토링
TEST: 테스트 코트, 리펙토링 테스트 코드 추가
CHORE: 빌드 업무 수정, 패키지 매니저 수정(ex .gitignore 수정 같은 경우)
```