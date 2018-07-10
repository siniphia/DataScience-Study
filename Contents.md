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
  
