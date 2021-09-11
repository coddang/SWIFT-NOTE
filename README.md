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
