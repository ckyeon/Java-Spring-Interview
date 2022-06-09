# Java-Spring-Interview

## JAVA

---
### 1. What is the difference between string buffer and string builder?
---
#### 차이점
- 동기화의 유무에 차이가 있다.
- String Buffer: 동기화를 지원하여 멀티쓰레드 환경에서 안전하다.
- String Builder: 동기화를 지원하지 않아 멀티쓰레드 환경에서 안전하지 않지만, 단일쓰레드의 성능은 뛰어나다.

#### [ 부가 정리 ]
- String 과 다르게 가변성을 가져 `.append()`, `.delete()` 등을 이용해 동일 객체 내에서 문자열을 변경할 수 있다.   
> 즉, 문자열의 추가, 수정, 삭제가 빈번하게 발생할 경우라면 String Buffer나 String Builder를 사용해야 한다.

---
### 2. Where does the normal variables, objects store in memory?
---
#### Normal Variables
- Stack 영역에 저장된다.
#### Object
- Heap 영역에 저장된다.

#### [ 부가 정리 ]
- Class(Method) 영역
  - 클래스의 구성요소인 정적 변수, 생성자, 메소드, 멤버 변수를 저장한다.
  - 클래스와 인터페이스들의 런타임 상수 풀이다.
   
- Heap 영역
  - 동적으로 생성된 객체를 저장한다.
  - 생성된 객체를 참조하는 변수가 사라지면 Garbage Collector에 의해 할당이 해제된다.
  
- Stack 영역
  - 호출된 메소드 및 메소드 수행시 발생되는 지역 변수를 저장한다.
  - 스레드가 생성될 시 각 스레드마다 하나의 스택을 가진다.
  - 스택에서 Heap 영역의 객체를 참조할 수 있다.
---
### 3. Is java 100% OOP language? (Yes/No)? How to do you prove it?
---
#### NO
- 자바는 `int`, `float`, `char` 와 같은 객체가 아닌 primitive data type을 사용하기 때문이다.
- 100% OOP language가 되려면 객체가 아닌 primitive data type을 사용하면 안된다.
---
### 4, Why do we have difference memories like heap memory, stack memory, dynamic memory?
---
#### 1. 프로세스를 실행할 때 얼만큼의 메모리가 필요할지 모르는 상태이다.
#### 2. 1번의 이유로 실행할 프로세스의 코드가 최대로 사용할 수 있는 메모리를 계산하여 미리 할당해 놓는 것은 비효율적이다.
---
