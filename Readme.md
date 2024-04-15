# 수리통계학 공부 
- 김충락 교수 kocw 수리통계학 강의
  - 수리통계학(I): 1~5장, 2020년 1학기
  - 수리통계학(II): 6~10장, 2020년 2학기 
- 교재: Introduction to mathematical statistics, Hogg, 6e
- 김충락 교수 강의노트
  - 교재의 내용이 잘 정리되어 있음
  - 유도 과정이 교재보다 자세함
  - 교재에 없는 내용도 다소 있음
- 강의내용에서 질문(?)이나 어려운 부분(!)을 여기에 정리

# 1장. 확률과 확률분포
- $\sigma$-field의 정의!
- Boral $\sigma$-field의 정의?
    
# 2장. 다변량 분포
- 다중적분에서 Jacobian의 직관적 의미?
- 여러 정리들을 증명하는데 double expectation theorem을 이용!
- Theorem 2.4.1: 조건부 기대값이 선형으로 나타날 때, 이 결과들의 직관적 의미는?  
  $E[Y|X]=\mu_2+\rho\frac{\sigma_2}{\sigma_1}(X-\mu_1)$  
  $E[Var(Y|X)]=\sigma^2(1-\rho^2)$  
  
# 3장. 몇 가지 특수한 분포
- 조합 계산식을 쉽게 설명하면? 
- 각 분포의 직관적 설명와 유례?
  - Poisson, Gamma, Chi-square, Beta 분포
- 윤영님 교수 블로그
  - 포아송 분포: 단위 시간 당 어떤 사건이 발생하는 횟수
  - 지수 분포: 어떤 사건이 한 번 발생하는 데 걸리는 시간(혹은 시간 간격)
  - 감마 분포: 어떤 사건이 여러 번($\alpha$ 번) 발생하는데 걸리는 시간
- 통계학에서 자유도의 의미는?
  - 자유도 = 표본의 개수 - 제약조건의 수
  - 통계적 추정을 할 때 표본 중 모집단에 대한 정보를 주는 독립적인 자료의 수 (Wikipedia)
- Gamma 분포와 다른 분포들(Poisson, Beta)과의 관계를 쉽게 설명하면?
- Chi-square 분포, t 분포, F 분포에서 각각 자유도의 의미는?
- 정규분포에서 표본 평균과 표본 분산이 독립이 되는 이유는?
- 정규 분포 $N(\mu,\sigma^2)$에서 추출한 임의 표본 $X_1,...,X_n$ 에서 얻어지는 통계량
  - 표본 평균 $\bar X=\frac{1}{n}\sum_i X_i$은 정규분포 $N(\mu,\sigma^2/n)$를 따름
  - 표본 분산 $s^2=\frac{1}{n-1}\sigma_i (X_i)^2$은 ?
  - $\frac{(n-1)s^2}{\sigma^2}$은 Chi-square $\chi^2(n-1)$를 따름?
  - $\frac{\bar X-\mu}{s/\sqrt{n}}$은 Student t 분포 $t(n-1)$를 따름?

## 4장. 일치성, 그리고 극한 분포  
- 용어 정리
  - population (모집단), parameter (모수), sample (표본)
  - random sample (임의 표본), statistic (통계량)
  - sample mean (표본 평균), sample variance (표본 분산)
- 기대값과 관련된 수식 ($x,y$는 확률 벡터, $A,B$는 상수 행렬)
  - $E[Ax]=AE[x]$
  - $\text{Cov}(Ax,Bx)=A\text{Cov}(x,y)B^T$
- 정리 5.1.2 증명?
  - $P(|X_n-X|+|Y_n-Y|\ge\epsilon)$  
    $\le P(|X_n-X|\ge \epsilon/2) + P(|Y_n-Y|\ge \epsilon/2)$
- consistent estimator와 unbiased estimator의 차이점과 좋은 예제?
- 확률적 수렴과 분포적 수렴
  - 두 개념의 차이를 쉽게 설명하면?
  - 확률적 수렴 $\rightarrow$ 분포적 수렴
- CDF는 왜 right continous 할까?
- central limit theorem
  - $\sqrt{n} (\bar{X}-\mu) \xrightarrow{\mathcal{D}} N(0,\sigma^2)$
  - $\sqrt{n} (g(\bar{X})-g(\mu)) \xrightarrow{\mathcal{D}} N(0,g^{'}(\mu)^2 \sigma^2)$ (by $\Delta$ method)
- variance stablizing transformation?
  - 분산이 unknown parameter에 의존하지 않게 해주는 변환
  - 이항분포의 분산 안정화 변환은 arcsin square-root 이다.
  - 이 변환을 어떻게 찾을까? 
    
  
