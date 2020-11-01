# Vanilla Redux

### 1. Store === state (데이터가 되어야 할 부분)

- 기본적으로 데이터(값)를 넣을 장소를 만들어 준다.
- 버튼으로 숫자를 늘리고 줄이는 것으로 대입해보았을 때 바로 숫자가 늘어나고 줄어드는 값을 말한다.
- 그 값을 바로 store에 저장해야 한다.

### 2. Reducer === modifier

- function이며 데이터를 modify 한다.
- 이때, 오로지 Reducer를 통해서만 데이터를 Modify 할 수 있다.

### 3. Action === Event

- dispatch로 Message(이벤트)를 보내어 대화할 수 있다.
- 무조건 object로 정의되어야 하며, type이 정의되어 있어야 함.

### 4. Redux 사용 시 주의하기

- state를 Mutate 하면 절대 안된다. (직접 상태를 수정X, Object를 return해서 사용하는 것.)
  ex) etc.push("값추가"); <- 이런 것을 하지 않는 것이 핵심.

---

# REACT-REDUX

### 1. connect

- 컴포넌트를 Store에 연결 해 준다.
- store.dispatch() : setter
- store.getState() : getter
- mapStateToProps : 기본적으로 함수이며 state, 컴포넌트의 props가 args. === getState() 기능임.
- mapDispatchToProps : 데이터를 보내는 측에서 dispatch를 동작하여 리덕스에 보내는 것 가능.
