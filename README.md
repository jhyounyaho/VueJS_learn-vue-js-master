# learn-vue-js

### Vue는 무엇인가?

MVVM 패턴의 뷰모델(ViewModel) 레이어에 해당하는 화면(View)단 라이브러리  
![vuejs_mvvm](https://user-images.githubusercontent.com/42309919/103294353-13bfef80-4a35-11eb-9fec-3b69c99c8af8.PNG)

### 같은 컴포넌트 레벨 간의 통신 방법

![vuejs_samelevel](https://user-images.githubusercontent.com/42309919/103330948-14916980-4aa7-11eb-9a71-568b1c85df78.PNG)

### v 디렉티브

https://kr.vuejs.org/v2/guide/index.html

#### v-model

양식에 대한 입력과 앱 상태(data 안에 있는 value)를 '양방향'으로 바인딩  
ex) v-model='message'

#### v-bind

엘리먼트 속성 바인딩 (data 안에 있는 value)  
ex) v-bind:title='message'

#### v-on

Vue 인스턴스에서 메소드를(methods 안에 있는 함수) 호출하는 이벤트 리스너 추가  
사용자가 앱과 상호 작용할 수 있게 하기 위해 사용  
ex) v-on:click='reserveMessage'

#### v-if, v-else

Vue 엘리먼트가 Vue에 삽입/업데이트/제거될 때 자동으로 트렌지션 효과 적용 (data 안에 있는 value)  
조건 미충종식 dom에서 제거

#### v-show

조건 미충족시 display:none (data 안에 있는 value)

#### v-for

배열의 데이터를 바인딩 (data 안에 있는 value - array)  
ex) v-for='todo in todos'

### computed와 watch

https://kr.vuejs.org/v2/guide/computed.html  
직관성과 유지보수를 위해 템플릿 내에는 최대한 심플하게 표현할 것  
복잡한 로직이라면 반드시 computed or watch 사용

#### 공통점

- data를 변경 할 수 있다.

#### 차이점

computed                
- 종속 대상을 따라 저장(캐싱)된다. 종속된 대상이 '변경'될 때만 함수를 실행한다.                
- 대부분의 경우 computed 속성이 더 적합                
                                                                
methods
- 렌더링을 다시 할 때마다 '항상' 함수를 실행한다.                
- 비동기식 또는 시간이 많이 소요되는 조작을 수행하려는 경우에 가장 유용                
