# BITAmin MLOps 2주차 · 실습 시연 결과

발표자료 제작을 위해 **한 계정으로 수행한 기술 리허설**입니다.
참가자용 시작 코드는 [공개 템플릿](https://github.com/fisfin/bitamin-mlops-week2-starter)에서 받습니다.
이 저장소의 루트 app.py는 네 역할을 합친 완성 코드입니다.

- [실제 PR·충돌·실행 기록](week2/README.md)
- [A 전처리 PR #1](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/1)
- [B Logistic Regression PR #2](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/2)
- [C Random Forest와 충돌 해결 PR #3](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/3)
- [D 평가 지표 PR #4](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/4)

## 실행

```bash
python -m pip install -r requirements.txt
python app.py
```

Windows Python 3.10.11에서 LR·RF와 다섯 지표 출력을 확인했습니다.
[week1의 실제 제출 PDF](week1/README.md)는 사용자가 제공한 지난주 제출 파일을 보존한 것입니다.
실제 조원의 초대 수락·타인 리뷰는 이 단일 계정 리허설에서 수행하지 않았습니다.

이번 안내는 Windows 시작 메뉴의 **Ubuntu 터미널**에서 시작합니다. VS Code는 필수가 아닙니다.
`gh` 설치·로그인은 인증 오류가 생긴 사람만 진행합니다. `.gitignore`는 발표자료 7쪽의 터미널 명령으로 생성하고 코드·README는 nano로 편집합니다.
참가자 자료의 1~30쪽은 실습, 31~37쪽은 화면·편집·파일·인증 도움말입니다.
혼자 연습할 때는 새 템플릿 저장소를 만들어 시작하세요. 이미 병합된 이 저장소에서 시작하면 같은 충돌 흐름이 나오지 않습니다.
