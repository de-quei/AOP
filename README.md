# AOP (Aspect Oriented Programming)

### 특징
1. 관점 지향 프로그래밍
2. 로깅 / 트랜잭션 / 보안 등에서 사용.
3. 관심사(메서드 호출)를 등록하면, 스프링은 메서드가 호출되는지 계속 지켜보다가 메서드 호출 시 자동을 메서드 전/후에 어드바이스(다른메서드)가 호출되는 것

---

### 용어 정리
1. `joint point` : 관심사로 등록될 가능성이 있는 메서드의 집합
2. `point cut` : 실제 관심사
3. `advice` : point cut에 적용되는 것
4. `weaving` : point cut + advice를 적용하는 것
5. `target class` : advice를 받는 클래스
6. `proxy 객체` : advice를 target class에 적용해서 생기는 객체

---

### Advice를 적용하는 시점
1. `before` : 메서드 호출 전에 동작하는 advice
2. `after` : 메서드 호출 후에 동작하는 advice
3.  `around` : 메서드 호출 전/후 동작하는 advice
4.  `after-turning` : 프로그램이 에러없이 완료되었을 때 동작하는 advice
5.  `after-throwing` : 예외 발생 시 동작하는 advice

---

### 필요 라이브러리
1. aspectweaver
2. aspectjrt

---

### 이 코드의 파일 구조
> 1. kr.hs.Study > Main.java
> 2. kr.hs.Study.Beans.TestBean1 - method1() / method2()
> 3. kr.hs.Study.Beans.Advisor.AdviceClass - before()
> 4. **resources > config.xml**
> 5. pom.xml