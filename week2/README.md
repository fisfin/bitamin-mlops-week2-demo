# 2주차 단일 계정 시연 기록

2026-09-19, 발표자료에 적힌 코드만 적용하여 실행한 기술 리허설입니다.
네 사람이 함께 수행한 제출물이 아니며 **타인 리뷰는 미수행**입니다.
리뷰 입력 화면은 제출하지 않은 예시로만 촬영했습니다. 실제 수업에서는 조원 전원이 다른 사람의 PR에 리뷰를 남겨야 합니다.

## 역할별 PR

공통 시작 commit: `889b94f`.

| 역할 | branch | 실제 PR | 상태 | 실제 타인 리뷰 |
|---|---|---|---|---|
| A 전처리 | feature/preprocessing | [#1](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/1) | Merged | 미수행 |
| B LR | feature/logistic-regression | [#2](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/2) | Merged | 미수행 |
| C RF | feature/random-forest | [#3](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/3) | Merged | 미수행 |
| D 평가 | feature/evaluation-metrics | [#4](https://github.com/fisfin/bitamin-mlops-week2-demo/pull/4) | Merged | 미수행 |

![main과 네 역할 branch](images/github-branches.png)

## 충돌과 해결

A, D, B 순서로 실제 GitHub에서 병합했습니다. B는 LR 설정을 변경하고 C는 같은 위치를 RF로 바꿔 충돌했습니다.
C branch에서 `git fetch origin` 후 `git merge origin/main`으로 충돌을 가져왔습니다.
슬라이드 24의 build_models 함수로 LR과 RF를 모두 보존하고 실행을 확인했습니다.

- [충돌 해결 commit 9f956f4](https://github.com/fisfin/bitamin-mlops-week2-demo/commit/9f956f43fa93b7500333755114a0ba9c9732379c)
- [모델 통합 main commit 5d8f46c](https://github.com/fisfin/bitamin-mlops-week2-demo/commit/5d8f46c2b8413d55099dfd889e1dcfad8601aeb4)

아래 경고는 병합이 끝난 뒤 **충돌 직전의 동일한 두 커밋**(main `92218b8`, C `694044b`)을 임시 branch로 비교하여 다시 촬영했습니다. 촬영용 branch는 정리했습니다. 실제 참가자는 본인의 C PR에서 해결 전 경고를 캡처합니다.

![동일한 두 커밋의 실제 GitHub 충돌 경고 재촬영](images/github-conflict.png)

![네 역할 PR Merged](images/github-merged-final.png)

## 최종 실행과 코드 확인

[실제 실행 로그](final-output.txt)

```text
=== Model comparison ===
                     accuracy  precision  recall      f1  roc_auc
Logistic Regression    0.7381     0.5043  0.7834  0.6136   0.8413
Random Forest          0.7828     0.6181  0.4759  0.5378   0.8220

Best model by F1: Logistic Regression
```

검증 환경: Windows Python 3.10.11, pandas 2.3.3, scikit-learn 1.7.2, joblib 1.6.0.
최종 app.py는 [완성 원본](https://github.com/Bo0sung/bitamin-mlops-2-snapshot/blob/1caa97f51e38bf2e71e534dca992adfca4bbbf97/app.py)과 LF 텍스트 기준으로 일치합니다.
SHA-256: `5422b825b0775d940c8bd23aaeba56aebe1e3f5247fd765a1526b0df61cc0da2`.

## 발표자가 직접 확인할 항목

- 발표 노트북의 기존 WSL·Conda 환경에서 인증·설치·학습을 확인합니다. 이 리허설의 학습은 Windows Python으로 수행했습니다.
- 조원 한 명과 실제 초대 수락 및 타인 리뷰 제출을 연습합니다.
- week1에는 실제 조의 결과를 넣습니다. 이 시연 저장소의 week1 안내문은 수행 증거가 아닙니다.

이 문서와 이미지도 별도 문서 branch의 PR로 반영합니다.
