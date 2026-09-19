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
실제 조원의 초대 수락·타인 리뷰 및 실제 1주차 결과는 이 리허설에 포함하지 않았습니다.
혼자 연습할 때는 새 템플릿 저장소를 만들어 시작하세요. 이미 병합된 이 저장소에서 시작하면 같은 충돌 흐름이 나오지 않습니다.
