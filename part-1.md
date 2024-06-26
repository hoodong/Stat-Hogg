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
  - random samples의 표본평균이 정규분포에 수렴한다.
  - $\sqrt{n} (\bar{X}-\mu) \xrightarrow{\mathcal{D}} N(0,\sigma^2)$
  - $\sqrt{n} (h(\bar{X})-h(\mu)) \xrightarrow{\mathcal{D}} N(0,h'(\mu)^2 \sigma^2)$ (by $\Delta$ method)
- variance stablizing transformation?
  - 분산이 unknown parameter에 의존하지 않게 해주는 변환
  - 이항분포 $B(1,p)$의 분산 안정화 변환은 arcsin square-root이다. 왜냐하면
    - $\sqrt{n}(\bar{X}-p) \rightarrow N(0,p(1-p))$ by CLT
    - $\sqrt{n}(h(\bar{X})-h(p)) \rightarrow N(0,h'(p)^2p(1-p))$ by $\Delta$ method
    - $h'(p)^2 p(1-p)=c^2$ 가 되려면 $h(p)=2c\sin^{-1}(\sqrt{p})$
  - 포아송 분포 $\mathcal{P}(\lambda)$의 variance stablizing transformation은?
    - $\sqrt{n}(\bar{X}-\lambda) \rightarrow N(0,\lambda)$
    - $\sqrt{n}(h(\bar{X})-h(\lambda)) \rightarrow N(0,h'(\lambda)^2 \lambda)$
    - $h'(\lambda)^2 \lambda$ 이므로 $h(\lambda)=2c\sqrt{\lambda}$

## 5장. 기초적인 통계적 추론
- 추론 inference
  - 추정 estimation
    - 점 추정 point estimation
    - 구간 추정 interval estimation
  - 검정 testing
- 추출 sampling
  - 복원 추출 sampling with replacement
  - 비복원 추출 sampling without replacement
- 순서 통계량 order statistics
  - Y는 X의 순서통계량: $Y_i=X_{(i)}, \quad Y_1 < Y_2 < ... < Y_n$   
- 순서통계량의 jpdf
  - X-to-Y 변환은 1-1이고 n! 가지수 $(X_1,...,X_n)\rightarrow (Y_1,...,Y_n)$
  - X-to-Y 변환은 permutation 행렬 $\Pi_{ij}$로 나타낼 수 있다.
  - $\Pi_{ij}$는 단위행렬의 $i$번째와 $j$번째 행을 바꾼 것이다.
  - X-to-Y 변환은 permutation 행렬들의 곱이므로 Jacobian은 $\pm1$이다.
  - X가 random sample이므로 X의 jpdf는 $f(x_1)f(x_2)...f(x_n)$
  - 따라서 Y의 jpdf는 $g(y_1,...,y_n)=n!\prod\limits_{i=1}^{n}f(y_i)$ (n!이 들어가는 이유?)
- 순서통계량의 marginal pdf
  - jpdf에서 직접 구하기는 어려움 (n-1번의 적분이 필요?)
  - $Y_k$보다 $n-k$개가 크고 $k-1$개가 작은 경우의 수는 $\frac{n!}{(k-1)!(n-k)!}$
  - $P(Y > y_k)=1-F(y_k), P(Y < y_k)=F(y_k), P(Y=y_k)=f(y_k)$ 이므로 각 경우의 확률은 $[F(y_k)]^{k-1} f(y_k) [1-F(y_k)]^{n-k}$
  - 따라서 $g(y_k)=\frac{n!}{(k-1)!(n-k)!} [F(y_k)]^{k-1} f(y_k) [1-F(y_k)]^{n-k}$
- 마찬가지로 jpdf of $Y_i,Y_j (i < j)$
  - $i-1$개가 $Y_i$보다 작고, $n-j$개가 $Y_j$보다 크고, $j-i-1$개가 $Y_i$와 $Y_j$ 사이에 있다.
  - 따라서 $g(y_i,y_j)=\frac{n!}{(i-1)!(j-i-1)!(n-j)!} [F(y_i)]^{i-1} f(y_i) [F(y_j)-F(y_i)]^{j-i-1} f(y_j)[1-F(y_j)]^{n-j}$
- 표본과 분포가 주어졌을 때 q-q plot을 그리는 방법?
- 분위수의 신뢰구간
  - 무슨 의미인지? 쉽게 풀어서 정의하면?
  - 이것을 이항분포를 이용해서 유도하는 방법?
  - 수치를 이용한 예제?
