# Java-Spring-Interview

## JAVA

### 1. What is the difference between string buffer and string builder?
- 차이점: 동기화의 유무에 차이가 있다.
   - String Buffer: 동기화를 지원하여 멀티쓰레드 환경에서 안전하다.
   - String Builder: 동기화를 지원하지 않아 멀티쓰레드 환경에서 안전하지 않지만, 단일쓰레드의 성능은 뛰어나다.
- 부가 정리
   - String 과 다르게 가변성을 가져 `.append()`, `.delete()` 등을 이용해 동일 객체 내에서 문자열을 변경할 수 있다.   
     > 즉, 문자열의 추가, 수정, 삭제가 빈번하게 발생할 경우라면 String Buffer나 String Builder를 사용해야 한다.
