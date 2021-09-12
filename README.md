# Swift Programming NOTE 📕

# 목적
  1. 언어에 대한 정확한 이해
  2. 학습했던 내용에 대한 요약 정리
  3. 문제해결에 필요한 명령어와 패턴 정리(알고리즘)

<br>
<br>

## **알고 넘어갈 것** <br>
=> 'function', 'method', 'instance'는 첫 글자를 소문자로 하는 카멜케이스 사용 <br>
=> 'protocol', 'extension', 'struct', 'class'는 첫 글자를 대문자로 하는 카멜케이스 사용 <br>
=> Set, Dictionary, Array 는 collection type <br>

> 값 타입(Value Type): Struct, enum <br>
> 참조 타입(Reference Type): class, closure

<br>
<br>

## **학습**
**Class**

    - 1. 단일 상속이 된다.
    - 2. 값이 Share 가 된다.
    - 3. Reference Type(참조 타입) -> 데이터를 전달할 때 값의 메모리의 위치를 전달한다.
    - 4. 전통적인 객체지향 프로그램의 OPP 관점에서의 클래스와 동일
    - 5. Apple 프레임 워크의 대부분의 큰 뼈대는 class로 이루어져 있다.

**Struct**

    - 1. 값이 Copy 가 된다.
    - 2. Value Type -> 데이터를 전달할 때 값을 복사해서 전달
    - 3. C언어 구조체 보다 더 다양한 기능을 가진다.
    - 4. swift 의 대부분의 큰 뼈대는 모두 struct 로 되어있다. 
    
    => 연관된 값을 하나로 모아서 하나의 데이터 타입으로 묶어내고 싶을 때 사용
    => 참조가 아닌 복사를 원할 때, 값을 할당받아서 변경하고 싶을 때 사용
    => 자신을 상속할 필요가 없거나 다른 타입을 상속받을 필요가 없을 때 사용
    
    
**enum**

    - 1. 다른 언어의 열거형과는 다른 다양한 기능을 제공한다.
    - 2. 상속이 불가능
    - 3. 값 타입을 가진다.
    - 4. 열거형 자체가 하나의 데이터 타입이다. 유의미한 공통점을 가진 값을 모은 것(달, 점심 메뉴 등)
    - 5. case 하나하나가 유의미한 하나의 값, 변수처럼 취급된다.


<br>
<br>

## **매써드 모음**

  1. type(of: )
  2. remove(at: index)
  3. removeFirst()
  4. removeLast()
  5. removeValue(forkey: )
  6. contains()
  7. insert(something, at: index)
  8. append()
  9. popLast()
  10. sort() -> 영어 우선 정렬 / 원본 값 변경
  11. sorted() -> 한글 우선 정렬 / 복사된 값 전달(읽기 전용)
  12. sorted(by: ) / > (내림차순) < (오름차순)
  13. union()
  14. intersection()
  15. subtracting()
  16. hasSuffix()
  17. hasPrefix()
  18. append(contentsOf: )
  19. firstIndex(of: )
  20. lastIndex(of: )
  21. dropLast()
  22. reversed()
  23. enumerate()
  24. stride(from: ,to: ,by: ) -> to 이전까지 by에 의해 연산
  25. stride(from: ,through: ,by: ) -> through에 입력된 수까지 by에 의해 연산
  26. array.randomElement()
  27. array.shuffled()
  28. .isEmpty
  29. print(something, terminator: 기본적으로 줄바꿈 처리)
  30. components(separatedBy: )
  31. split(by: )
  32. trimmingCharacters(in: ["! # 등 문자열 양쪽 제거할 문자"])
  33. components(separatedBy: ["1", "!", "$", "%" 등]).joined()
  34. .zip(sequence1, sequence2)
  35. .valueUpdate(Value, forKey: Key)

<br>
<br>


## 접근 제어

    - 객체지향 프로그래밍(OOP) 에서 은닉화는 중요한 개념이며 이를 구현하는 핵심기능은 접근 제어이다.
    - Q. 접근 제어는 코드끼리 상호작용을 할 시 파일 간 또는 모듈 간의 접근을 제한할 수 있는 기능으로, 접근제어를 통해 코드의 상세한 구현은 숨기고 허용된 기능만 사용하는 인터페이스를 만들 수 있다.
    => 접근 제어를 사용하는 이유는 객체지향 프로그래밍에서 캡슐화와 은닉화를 통해 외부에서 접근하면 안되는 코드의 접근을 막기 위해서이다. 

### 사용해야 할 때
    => [x] 불필요한 파일이나 모듈의 접근을 막아 의도치 않은 결과를 피하고 싶을 때
    => [x] 필수적인 부분만 접근을 허용해야 할 시 전체 코드의 노출 가능성을 차단할 때

 - 스위프트의 접근 제어: 모듈 + 소스파일 기반 설계 
 
 **모듈**: 배포할 코드의 묶음 단위로 Swift에선 import를 통해 불러오게 된다. / 예) 프레임워크, 라이브러리, 애플리케이션
**소스파일**: 하나의 스위프트 소스 코드 파일을 의미(스위프트도 보통 파일 하나에 타입 하나, But 여러 클래스 구조체 열거형 추가 될 수 있음)


## 접근 수준
    - 접근 제어는 접근 수준 키워드를 통해 구현한다.
    - 각 타임(class, enum, struct)에 특정한 접근 수준을 지정 가능
    - 타입 내부의 property, method, initializer, subscript 에도 접근 수준 지정 가능
    - 접근 수준 키워드는 <open, public, Internal, fileprivate, private> 5가지로 나눈다.
    

**접근 수준** | **키워드** | **접근도** | **범위** | **비고** |
--------------|------------|------------|----------|---------|
개방 접근 수준 | open | 높음(5) | 모듈 외부까지 | class에서만 사용 |
공개 접근 수준 | public | 4 | 모듈 외부까지 |    |
내부 접근수준 | internal | 3 | 모듈 내부 |    |
파일 외부비공개 접근수준 | fileprivate | 2 | 파일 내부 |    |
비공개 접근 수준 | private | 낮음(1) | 기능 정의 내부 |    |



<br>
<br>
<br>
<br>


