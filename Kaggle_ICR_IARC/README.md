# Kaggle_ICR_IARC
ICR - Identifying Age-Related Conditions Kaggle Challenge

## [회고록]
■ 결과
- 8/10 대회 마감
- private score: 0.43
- 리더보드 1위의 private score: 0.3

■ 1~3위 솔루션 리뷰
- 1등 솔루션
	- 확률 재가중  
		\# https://www.kaggle.com/code/muelsamu/simple-tabpfn-approach-for-score-of-15-in-1-min  
		\# 조예람님이 리뷰하셨던 내용
- 2등 솔루션 리뷰
	- Stacking은 도움이 되지 않음
- 3등 솔루션 리뷰
	- catboost
	- 교차 계산

■ 우리와의 차이
- greeks dataset 유무 차이
	- 테스트 데이터셋에 greeks 컬럼이 없었음
	- TabPFN은 transformer 기반이기 때문에 시계열 성격때문에(position) 필요
	- 해당 노트북은 tabpfn은 transformer 기반이기 때문에 시계열 성격때문에(position) 필요
- 매우 많은 전처리 유무

■ 결론
- 캐글은 Stacking같은 앙상블 기법에 회의적이다.
- 의외로 간단한 기법이 높은 점수를 받았다. (대부분 catboost 사용)
- 높은 랭크에서 사후 보정은 사용하지 않았다.

■ 그외 팁
- factorize()
	- 오브젝트를 열거형이나 범주형 변수로 인코딩
	- https://www.kaggle.com/competitions/icr-identify-age-related-conditions/discussion/430907
- LGBMImputer
