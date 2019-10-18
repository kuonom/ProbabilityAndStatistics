# 확률및통계학

중간고사 시험범위 공부 및 정리 (chapter 1 ~ chapter 7)



## Chapter1

### 1.0 Introduction

​	통계란 데이터를 분석, 해석, 종합, 묘사 하는데 도움을 주는 방법들의 모음이다.

- descriptive statistic(기술통계학) - 정리, 표현, 요약, 해석 등을 통해 자료의 특성을 규명하는 통계적 방법

- inferential statistics(통계적 추론) - 모집단에 대해 미지의 양상을 알기 위해 통계학을 이용해 추측하는것

  

### 1.1 Population, Sample, and Observations

- Units/Observations - 우리가 측정하거나 수집한 데이터   $\omega$

- Population - 모든 유닛들 $\omega \in \Omega$

- Sample - Population의 일부분  $\{\omega_1,\omega_2,\cdots,\omega_n\} \subseteq \Omega$

  
### 1.2 Variables

- Variable - Observation 에서 특정한 feature는 statistical variable X로 측정된것

  

#### Qualitative/Quantitative

- Qualitative variables - 순서를 가질 수 없는 values x
  
  - 눈의 색, 정당 이름, 교통수단 등
  
- Quantitative variables - 논리적으로나 자연적으로 순서를 가질 수 있는 변수
  
  - 신발 사이즈, 집 가격, 공부한 기간, 몸무게, 키
  
    

#### Discrete/Continuous

- Discrete variables - 유한하거나 셀 수 있는 값의 values를 가짐
  
  - 모든 Qualitative variables는 discrete
  
- Continuous variables - 무한한 수의 values를 가짐

  

#### Scale

- Nominal Scale - 순서화 되지않는 값 - 성별, 종교, 지역
- Ordinal Scale - 순서는 정해질 수 있는데, 그 해당 값의 차이는 의미가 있지 않음(ranking만 함) - education level, satisfaction score, 시험 등수
- Continuous Scale - 연속적인 variable가 순서화 될 수 있는것, 값들의 차이는 의미가 있음 - 키, 몸무게, age
- Interval Scale - 같은 간격을 가지는 척도 - 온도계 - 0이라고 진짜 0은 아님
- Ratio Scale - Interval Scale과 비슷하지만 0은 진짜 0임. 데이터끼리 사칙연산 가능
- Absolute Scale - ratio scale과 같은데  natural unit 에서 측정된것 뺀것(? ?) - 자녀 수



#### Grouped Data

- Grouped/ Categorical Variable  - 범주변인(categorical variable)은 논리적인 순서가 없을 수 있음

  ex) 혈액형[A, B, AB, O] / 우유종류[딸기우유, 초코우유, 커피우유]

- Binary Variable : Grouped variable 중 오직 2개의 값만 가지는 것.

### 1.3 Data Collection

- Survey - 질문을 하거나 질문지를 만들어 데이터 모으는것
- Experiments - controlled 환경에서 데이터를 수집하는것
- Observational Data - 반복적으로 수집되는 데이터 (조사를 만들거나 환경을 설정하지 않음)
- Primary and Secondary Data - primary data는 우리스스로 수집한거, secondary는 다른사람이 수집한것



### 1.4 Create a Data Set

- Data matrix - 데이터를 편리한 방법으로 저장해둔것 모통 Row가 observations, Column이 variables
  $$
  \begin{pmatrix}
  \omega & Variable1 & Variable2 &\cdots &Variablep\\
  1 & x_{11} & x_{12} & \cdots & x_{1p} \\
  2 & x_{21} & x_{22} & \dots & x_{2p} \\
  \vdots & \vdots & \vdots & & \vdots \\
  n & x_{n1} & x_{n2} & \dots & x_{np} \\
  \end{pmatrix}
  $$
  
- Transformation - 

  - $g(x) = a + bx, b>0$ (Inverval scale)
  - $g(x) = bx, b>0$ (ratio scale)



## Chapter2

summarizing이나 visualizeing을 하려면, 어떤 통계적 방법을 사용하는것이 적절한지는 variable의 type에 달렸다. 



### 2.1 Absolute and Relative Frequencies

- Discrete Data

  - k categories, $a_1, \cdots,a_k$
  - Absolute frequenty $n_j$ : jth category의 observation 갯수
  - Relative frequency : absolute frequency를 total number n으로 나눈것
$$
f_j = f(a_j) = {n_j\over n}, j=1,2,\cdots,k
$$
- Continuous Data
- absolute frequency는 별로 좋지않음(k가 너무 많기 때문에), 그래서 intervals을 둠



### 2.2 Empirical Cumulative Distribution Function

​	

### 2.3 Graphical Represectation of a Variable

- Bar Chart
  - nominal or ordinal variables
- Pie Chart
- Histogram



### 2.4 Kernel Density Plot

histograms의 artificial categorization

histogram을 smooth하게 만드는 방법

각 지점에서 kernel function을 구해서 다 더하고 n 으로 나눔





# Chapter3

data를 해석하는 summary



### 3.1 Measures of Central Tendency

사람들은 average와 비교하고 싶어하는 경향이 있음 - average는 어떻게 찾을까?

#### Arithmetic Mean

모든 데이터의 합 / N

#### Arithmetic Mean for Grouped Data

모든 구간의 relative frequncy * mid-value 의 합
$$
\bar{x} = {1\over n} \sum_{j=1}^k{n_jm_j}=\sum_{j=1}^{k}{f_jm_j}
$$

##### Properties of the Arithmetic Mean

전체 평균과 group의 평균과의 편차들의 합은 0 이다

만약 data를 $y_i=a+bx_i$   같이 선형 transform 하면  $\bar{y}=a+b\bar{x}$ 



#### Median 

중간값

Grouped에서는 1부터 m-1까지 relative frequency의 합이 0.5가 안되고 1부터 m까지의 합은 0.5보다 크거나 같다면 class $K_m$이 median을 포함한다고 생각함 그러면 median을 정의하는것은 x^~_0.5 = e_m-1 + 0.5 - m-1까지 합 / fm * Km의 interval 즉 m-1부터 0.5까지 부분의 Km의 전체 relative frequency 에 대한 비율을 구해 Km의 간격과 곱한다. (고르게 데이터가 분포돼있다고 판단하기 때문에)
$$
\tilde{x}_{0.5}=e_{m-1}+{{0.5-\sum_{j=1}^{m-1}f_j} \over f_m}d_m
$$
$d_m$ = width of the interval $K_m$ 



#### Quantiles

 x% 되는 구간$\tilde{x}_{a}$ 라고 표시. Quartile = 25, 50, 75 quantiles



#### Quantile-Quantile plot(QQ-Plots)

두개의 Quantile을 하나의 표로 나타낸 것



#### Mode

가낭 높은 frequency가 나타나는 구간 $\bar{x}_M=[30,35]$



#### Geometric Mean

모든 n observation을 다 곱한다음 n제곱근 취함
$$
\bar{x}_G = \sqrt[n]{\prod_{x=1}^n x_i}
$$
평균 성장률 같은 계산에서 사용. $B_t = B_0 * \bar{x}_G^t$

평균 성장 factor. $x_t = {B_t \over B_{t-1}}$

#### Harmonic Mean





