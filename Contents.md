# Machine Learning
## Linear Regression
 굴곡이 없는 선형으로 이루어진 예측 모델로서 *예측값*과 *실제값*의 **평균제곱오차**(MSE; mean squared error)를 Cost Function으로 잡아 해당 함수값을 최소화시키는 W와 b값을 구해 모델을 생성한다.<br>
 
 
+ **Simple Linear Regression**<br>
 단 하나의 W값으로 이루어진 선형회귀모델로서 2차원 직선으로 표현됨<br><br>
+ **Multiple Linear Regression**<br>
 여러 개의 W값으로 이루어진 선형회귀모델<br>
    W가 2차원 : Flat Plane으로 표현됨<br>
    W가 N차원 : Hyperplane으로 표현됨<br>
   ※ **차원이 늘어난다고 구불구불한 곡선이 되는 것이 아니다!**<br><br>
  
## LASSO
 + **개념**<br>
 Linear Regression의 Cost Function에 **Penalty**(*α* x *L1-norm*)를 추가하는 방식<br><br>
 + **의미**<br>
 Cost Function을 최소화해야 모델을 구할 수 있기 때문에 Penalty 역시 최소화시켜야 한다. Penalty의 최소화 과정에서 몇몇 중요하지 않은 W값은 0이 되어 모델에 반영되지 않게 된다. 즉, **예측정확도는 유지**하면서도 **더 적은 feature로 모델을 생성**할 수 있어 혜자라고 말할 수 있다.<br><br>
 + **α의 역할**<br>
 **α값이 크면** Cost Function에서 Penalty 영역의 영향력이 커지기 때문에 더 많은 W를 0으로 만들게 되어 모델에 반영되는 feature 수가 줄어든다. 하지만 과도하면 **과소적합**이 일어난다.<br>
 **α값이 작으면** 위와 반대로 Penalty의 영향력이 작아지기 때문에 결과적으로 모델에 반영되는 feature 수가 줄어든다. 역시 과도하면 **과대적합**이 일어난다.<br>
 따라서 사용자는 *Cross-Validation*을 통해 α값을 직접 조정해가며 가장 적합한 모델을 찾아내야 한다!<br><br>
 
 ## RIDGE
  + **개념**<br>
  LASSO와 같은 방식이지만 W값들이 0에 가까워질 뿐 완전히 0이 되지는 않기 때문에 모든 feature가 모델에 반영된다. 모든 feature들을 살리고 싶을 때 사용한다.<br><br>
  
  
## Numpy
  + **소개**
    - Python Library
    - Array & Multi-Dimension Matrix Management *(C language based implementation -> **fast!**)*
    - Basic Math Calculation (Linear Algebra, Matrix Cal..)
      
  + **주요함수**  
    - **np.array([1,2,3], dtype='float32')** : 해당 내용을 명시한 자료형으로 담은 array를 반환
    - **np.linspace(a, b, n)** : a에서 b까지 n개로 균일하게 나눈 값을 저장한 array를 반환
    - **np.arange(a, b)** : a에서 b까지 1의 간격으로 변수들을 담은 array를 반환
    - **np.arange(a, b, n)** : 간격을 n으로 설정할 수 있음
    - **np.arange(b)** : a값을 주지 않으면 0부터 생성
    
  + **사이트**
    - numpy 공식사이트 <http://www.numpy.org/>
    - numpy reference <https://docs.scipy.org/doc/numpy/reference/>


## Matplotlib
  + **소개**
    - Python Library
    - Visualization Tool
    - Import -> Data Matching -> Plotting
    
  + **주요함수**
    - **plt.plot(x, y)** : plot 형식(점을 찍고 그 점들을 선으로 연결)으로 data를 표현할 것
    - **plt.scatter(x, y)** : scatter 형식(점만 찍어줌)으로 data를 표현할 것
    - **plt.show()** : 저장된 data를 시각화
    - *plot에 여러 함수를 넣어놓고 show를 호출하면 동시에 여러 그래프를 그릴 수 있음*
    
  + **사이트**
    - 기본예제 <http://thrillfighter.tistory.com/472>
    - matplotlib 공식사이트 <https://matplotlib.org/>
