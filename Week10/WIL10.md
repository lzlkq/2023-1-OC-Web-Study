# 기초 웹 스터디 10주차

### js 3 자바 스크립트 개발 환경과 실행 방법

1. **웹 브라우저**

1.1 개발자 도구 

- 개발자 도구

![스크린샷 2023-06-18 172942.png](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-18%20172942.png)

- 개발자 도구 기능

![스크린샷 2023-06-18 173111.png](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-18%20173111.png)

1.2 콘솔

- 자바스트립트 코드에서 에러가 발생하여 애플리케이션이 동작하지 않을 때 우선적으로 살펴보아야 할 곳
- console.log 함수 : 소괄호 안에 있는 확인하고 싶은 값을 콘솔에 출력해 확인
- REPL(Read Eval Print Loop) : 입력 수행 출력 반복, 코드를 직접 입력해 결과를 확인 할 수 있음

1. **Node.js**

외부 라이브러리를 도입하거나 여러 가지 도구를 사용할 때 Node.js와 npm 필요

2.1 Node.js와 npm 

- Node.js
    - 브라우저 이외의 환경에서 동작 시킬 수 있는 자바스크립트 실행 환경
    - 주로 서버 사이드 애플리케이션 개발에 사용
    - Node.js는 백엔드 영역의 서버 애플리케이션 개발뿐만 아니라 프런트엔드 영역의 다양한 도구나 라이브러리도 Node.js 환경에서 동작 → 자바스크립트 개발에 필수적인 환경
- npm(node package manager)
    - 자바스크립트 패키지 매니저
    - CLI(Command Line Interface) 제공

### js11 객체와 변경불가성(Immutability)

- 변경불가성(Immutability)
    - 객체가 생성된 이후 그 상태를 변경할 수 없는 디자인 패턴
    - 함수형 프로그래밍의 핵심 원리
- 객체
    - 참조 형태로 전달하고 전달 받음
    - 객체 변경 주 원인은 “레퍼런스를 참조한 다른 객체에서 객체를 변경” → 객체를 불변객체로 만들어 프로퍼티의 변경을 방지, 객체의 방어적 복사(defensive copy)를 통해 새로운 객체를 생성한 후 변경, Observer 패턴 사용

1. **Immutable value vs. mutable value**
- Javascript의 원시 타입(primitive data type)은 변경 불가능한 값(immutable value)이다.
    - Boolean
    - null
    - undefined
    - Number
    - String
    - Symbol (New in ECMAScript 6)
- 원시 타입 이외의 모든 값은 객체(Object) 타입 → 변경 가능한 값(mutable value)

1. **불변 데이터 패턴(Immutable data pattern)**

2.1 객체의 방어적 복사(defensive copy)  : Object.assign

- 타킷 객체로 소스 객체의 프로퍼티를 복사
- 소스 객체의 프로퍼티와 동일한 프로퍼티를 가진 타켓 객체의 프로퍼티들은 소스 객체의 프로퍼티로 덮어쓰기O
- 타킷 객체를 반환
- Object.assign을 사용하여 기존 객체를 변경하지 않고 객체를 복사하여 사용O → 객체 내부의 객체(Nested Object)는 Shallow copy

2.2 불변객체화를 통한 객체 변경 방지 : Object.freeze

- 객체 내부의 객체(Nested Object)는 변경O
- 내부 객체까지 변경 불가능하게 만들려면 Deep freeze

2.3 Immutable.js

- Object.assign, Object.freeze → 큰 객체에는 사용X → Immutable.js
- 영구 불변 (Permit Immutable) 데이터 구조를 제공

### js 13 타입체크

변수나 반환값의 타입을 사전에 지정하지 않는 자바스크립트의 동적 타이핑(Dynamic Typing) → 타입체크

1. **typeof**
- 타입 연산자(Type Operator) typeof는 피연산자의 데이터 타입을 문자열로 반환

```jsx
typeof '';              // string
typeof 1;               // number
typeof NaN;             // number
typeof true;            // boolean
typeof [];              // object
typeof {};              // object
typeof new String();    // object
typeof new Date();      // object
typeof /test/gi;        // object
typeof function () {};  // function
typeof undefined;       // undefined
typeof null;            // object (설계적 결함)
typeof undeclared;      // undefined (설계적 결함)
```

- null과 배열의 경우 object, 함수의 경우 function를 반환
- Date, RegExp, 사용자 정의 객체 등 거의 모든 객체의 경우, object를 반환

→ typeof는 null을 제외한 원시 타입을 체크하는 데는 문제가 없지만 객체의 종류까지 구분하여 체크하려할 때는 사용하기는 곤란

1. **Object.prototype.toString**
- 객체를 나타내는 문자열을 반환

```jsx
Object.prototype.toString.call('');             // [object String]
Object.prototype.toString.call(new String());   // [object String]
Object.prototype.toString.call(1);              // [object Number]
Object.prototype.toString.call(new Number());   // [object Number]
Object.prototype.toString.call(NaN);            // [object Number]
Object.prototype.toString.call(Infinity);       // [object Number]
Object.prototype.toString.call(true);           // [object Boolean]
Object.prototype.toString.call(undefined);      // [object Undefined]
Object.prototype.toString.call();               // [object Undefined]
Object.prototype.toString.call(null);           // [object Null]
Object.prototype.toString.call([]);             // [object Array]
Object.prototype.toString.call({});             // [object Object]
Object.prototype.toString.call(new Date());     // [object Date]
Object.prototype.toString.call(Math);           // [object Math]
Object.prototype.toString.call(/test/i);        // [object RegExp]
Object.prototype.toString.call(function () {}); // [object Function]
Object.prototype.toString.call(document);       // [object HTMLDocument]
Object.prototype.toString.call(argument);       // [object Arguments]
Object.prototype.toString.call(undeclared);     // ReferenceError
```

→ 체의 종류(일반 객체, 배열, Date, RegExp, Function, DOM 요소 등)까지 식별O but, 객체의 상속 관계은 체크X

1. **Instanceof**
- DOM  tree의 객체 구성

![HTMLElement](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/HTMLElement.png)

- 타입 연산자(Type Operator)에는 앞서 살펴본 typeof 이외에 instanceof를 제공
- instanceof 연산자는 피연산자인 객체가 우항에 명시한 타입의 인스턴스인지 여부를 알려

1. **유사 배열 객체(array-like object)**
- length 프로퍼티를 갖는 객체 → 순회O
- 문자열, arguments, HTMLCollection, NodeList 등
- call, apply 함수를 사용하여 배열의 메소드를 사용O
- 배열인지 체크하기 위해서는 Array.isArray 메소드를 사용

### js 14 프로토 타입

1. **프로토 타입 객체**
- 클래스 없이(Class-less)도 객체 생성O
- 자바스크립트의 모든 객체는 자신의 부모 역할을 담당하는 객체와 연결 → 부모 객체의 프로퍼티 또는 메소드를 상속
- 부모 객체를 Prototype(프로토타입) 객체 또는 줄여서 Prototype(프로토타입) → 생성자 함수에 의해 생성된 각각의 객체에 공유 프로퍼티를 제공하기 위해 사용

![object_literal_prototype_chaining](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/object_literal_prototype_chaining.png)

1. ****[[Prototype]] vs prototype 프로퍼티****
- 함수 객체는 일반 객체와는 달리 [[Prototype]] 인터널 슬롯과 prototype 프로퍼티도 소유
- prototype 프로퍼티와 [[Prototype]]은 모두 프로토타입 객체를 가리키지만 관점의 차이가 있다.
- [Prototype]]
    - 함수를 포함한 모든 객체가 가지고 있는 인터널 슬롯이다.
    - 객체의 입장에서 자신의 부모 역할을 하는 프로토타입 객체를 가리키며 함수 객체의 경우 Function.prototype를 가리킨다.
- prototype
    - 함수 객체만 가지고 있는 프로퍼티이다.
    - 함수 객체가 생성자로 사용될 때 이 함수를 통해 생성될 객체의 부모 역할을 하는 객체(프로토타입 객체)를 가리킨다.

1. **constructor 프로퍼티**
- 객체의 입장에서 자신을 생성한 객체를 가리킨다.

1. **prototype chain**
- 자바스크립트는 특정 객체의 프로퍼티나 메소드에 접근하려고 할 때 해당 객체에 접근하려는 프로퍼티 또는 메소드가 없다면 [[Prototype]]이 가리키는 링크를 따라 자신의 부모 역할을 하는 프로토타입 객체의 프로퍼티나 메소드를 차례대로 검색

4.1 객체 리터럴 방식으로 생성된 객체의 프로토타입 체인

- 객체 생성 방법
    - 객체 리터럴 : 내장 함수(Built-in)인 Object() 생성자 함수로 객체를 생성하는 것을 단순화시킨 것 → prototype 프로퍼티O
    - 생성자 함수
    - Object() 생성자 함수

![printout_student_obj_from_chrome](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/printout_student_obj_from_chrome.png)

4.2 생성자 함수로 생성된 객체의 프로토타입 체인

- 함수 정의 방식
    - 함수선언식(Function declaration) → 리터럴 방식 사용
    - 함수표현식(Function expression) → 리터럴 방식 사용
    - Function() 생성자 함수
- 함수 리터럴 방식은 Function() 생성자 함수로 함수를 생성하는 것을 단순화 시킨 것

→ 3가지 함수 정의 방식은 결국 Function() 생성자 함수를 통해 함수 객체를 생성

→ 함수 객체를 생성하여도 모든 함수 객체의 prototype 객체는 Function.prototype

![스크린샷 2023-06-18 184805.png](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-06-18%20184805.png)

![constructor_function_prototype_chaining](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/constructor_function_prototype_chaining.png)

1. **프로토타입 객체의 확장**
- 추가/삭제된 프로퍼티는 즉시 프로토타입 체인에 반영

![extension_prototype](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/extension_prototype.png)

1. **원시타입(Primitive data type)의 확장**
- 원시 타입으로 프로퍼티나 메소드를 호출할 때 원시 타입과 연관된 객체로 일시적으로 변환되어 프로토타입 객체를 공유하게 된다.

![A](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/A.png)

1. **프로토타입 객체의 변경**
- 프로토타입 객체 변경 시점 이전에 생성된 객체기존 프로토타입 객체를 [[Prototype]]에 바인딩한다.
- 프로토타입 객체 변경 시점 이후에 생성된 객체변경된 프로토타입 객체를 [[Prototype]]에 바인딩한다.

![changing_prototype](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/changing_prototype.png)

- constructor 프로퍼티는 Person() 생성자 함수를 가리킨다.
- 프로토타입 객체 변경 후, Person() 생성자 함수의 Prototype 프로퍼티가 가리키는 프로토타입 객체를 일반 객체로 변경하면서 Person.prototype.constructor 프로퍼티도 삭제되었다. 따라서 프로토타입 체인에 의해 bar.constructor의 값은 프로토타입 체이닝에 의해 Object.prototype.constructor 즉 Object() 생성자 함수가 된다.

1. **프로토타입 체인 동작 조건**
- 객체의 프로퍼티를 참조하는 경우, 해당 객체에 프로퍼티가 없는 경우 → 프로토타입 체인 동작
- 객체의 프로퍼티에 값을 할당하는 경우 → 프로토타입 체인이 동작X

![condition_prototype_chaining](https://github.com/lzlkq/2023-1-OC-Web-Study/blob/main/Week10/condition_prototype_chaining.png)

### js17 this

**this 바인딩**

- 자바스크립트의 경우 함수를 호출할 때 함수가 어떻게 호출되었는지에 따라 this에 바인딩할 객체가 동적으로 결정

### **ECMAScript 3 화살표 함수**

1. **화살표 함수 선언**
- 화살표 함수의 기본 문법

```jsx
// 매개변수 지정 방법
    () => { ... } // 매개변수가 없을 경우
     x => { ... } // 매개변수가 한 개인 경우, 소괄호를 생략할 수 있다.
(x, y) => { ... } // 매개변수가 여러 개인 경우, 소괄호를 생략할 수 없다.

// 함수 몸체 지정 방법
x => { return x * x }  // single line block
x => x * x             // 함수 몸체가 한줄의 구문이라면 중괄호를 생략할 수 있으며 암묵적으로 return된다. 위 표현과 동일하다.

() => { return { a: 1 }; }
() => ({ a: 1 })  // 위 표현과 동일하다. 객체 반환시 소괄호를 사용한다.

() => {           // multi line block.
  const x = 10;
  return x * x;
};
```