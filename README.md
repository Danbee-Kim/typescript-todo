# Typescript

### DOM 조작

- 타입스크립트는 DOM의 모든 타입 정의를 자동으로 인지한다.
- lib 프로퍼티를 사용하여 수동으로 컴파일러 옵션 지정 가능
- getElementById가 반환하는 게 제네릭 HTML요소 또한 null인 것만 인지

> Optional Chaining - ?
- 변수 뒤에 "?"를 붙여 해당 값이 있을 때만 진행
- 해당 값이 없으면 실행하지 않음

> Non-Null 단언 연산자 - !

- 절대 null이 되지 않는다고 단언
- 값이 확실하게 존재하고 null이 아닐 때만 사용
- 불확실한 런타임에서 작업할 때는 사용 금지

```javascript
const btn = document.getElementById('btn')!;
```

> Type Assertion 타입 단언 - as

- 어떤 타입인지 typeScript에 알려줌

```javascript
const mystery:unkown = "Hello World";

cosnt numChars= (mystery as string).length
```

- input 요소임을 알려줘야 value 값을 읽을 수 있음

```javascript
const input=document.getElementById("todoinput")!as HTMLInputElement;

btn.addEventListener("click",function(){
  alert(input.value)
})
```
