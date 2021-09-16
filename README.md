# Swift Programming NOTE 📕

<br>

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



## 제네릭(Generic)

- 제네릭을 통해 타입에 대한 유연성을 가질 수 있다. 제네릭으로 구현한 기능과 타입은 
재사용 가능하고 코드의 중복을 줄일 수 있다. <br>
- 스위프트 표준 라이브러리는 많은 제네릭 코드로 구현되어 있다. <br>
- Array, Dictionary, Set 과 같은 타입 = 모두 제네릭 컬렉션 <br>
- 정수나 문자열 타입을 요소로 갖는 배열을 만드는 것과 어떤 타입도 배열 요소로 가질 수 있던 것은 모두 제네릭 덕분이다.   <br>

``` swift
예)
var array: [Int] = [10, 20, 30, 40]
var set: Set<Int> = [50, 40, 30, 20]
var dictionary: [String: Int] = ["김": 100, "이": 300, "박": 200]
```

### 제네릭 사용시 
=> 제네릭이 필요한 메서드나 타입 이름 뒤에  "<>" 붙이고 그 사이에 제네릭을 위한 매개변수를 넣어 표기 <br> 예) <T>, <U>, <I>

제네릭 사용을 원하는 타입이나 함수 <타입 매개변수> (함수 매개변수) <br>


<br>
<br>



## **상속**

### 프로퍼티(property) <br>
    - 저장 프로퍼티: Stored property
    - 연산 프로퍼티: Computed property
    - 인스턴스 프로퍼티: instance property
    - 타입 프로퍼티: type property



``` swift

class Person {
    var name: String = " "
    
    func selfIntroduce() {
        print("저는 \(name)입니다.")
    }
    
    // final 키워드를 통해 재정의를 방지할 수 있다. -> 자식 클래스에 물려 줬을 때 재정의를 방지 override 불가!
    final func sayHello() {
        print("Hello")
    }
    
    //타입 매써드
    //재정의 불가 타입 메써드 - static
    static func typeMethod() {
        print("type method - static")
    }
    
    // 재정의 가능
    class func classMethod() {
        print("type method - class")
    }
    
    // 재정의가 가능한 class 메써드라도
    // final 키워드를 사용하면 재정의 할 수 없다.
    // 매써드 앞에 'static' == 'final class'
    final class func finalClassMethod() {
        print("type method - final class")
    }
}

class Student: Person {
    var major: String = ""
    
    override func selfIntroduce() {
        print("저는 \(name)이고, 전공은 \(major)입니다. ")
        // 부모 클래스의 내용을 호출
        super.selfIntroduce()
    }
    
    override class func classMethod() {
        print("overriden type method - class")
    }
}


let yang: Person = Person()
let ming: Student = Student()

yang.name = "yang"
ming.name = "ming"
ming.major = "Swift"

yang.selfIntroduce()
ming.selfIntroduce()
Person.classMethod()
Person.finalClassMethod()

Student.classMethod()
Student.typeMethod()
Student.finalClassMethod()
```

``` swift

struct ClassMate {
    
    // 인스턴스 저장 프로퍼티
    var name: String = ""
    var `class`: String = "swift"
    var KoreanAge: Int = 0
    
    // 인스턴스 연산 프로퍼티
    var westernAge: Int {
        get {
            return KoreanAge - 1
        }
        
        set(inputValue) {
            KoreanAge = inputValue + 1
        }
    }
    
    // 타입 저장 프로퍼티
    static var typeDiscription: String = "학급 친구"
    
    // 인스턴스 매서드
    func selfIntroduce() {
        print("저는 \(self.class)반 \(name) 입니다.")
    }
    
    // 읽기 전용 인스턴스 연산 프로퍼티 get 만 구현이 되어 있으면 읽기 전용이다.
    var selfIntroducing: String {
        get {
            return "저는 \(self.class)반 \(name)이라고 합니다."
        }
    }
    
}

var 명식: ClassMate = ClassMate()
명식.KoreanAge = 25

명식.name = "유명식"
print(명식.name)

print(명식.selfIntroducing)
print("제 한국 나이는 \(명식.KoreanAge)살이고, 미국나이는 \(명식.westernAge)살 입니다.")


```

<br>
<br>

## **인스턴스의 생성 & 소멸 (init  / deinit)**

## **init**

**=> 모든 저장 프로퍼티에는 기본 값을 넣어야 한다. 모든 프로퍼티에 유효한 값이 할당되어야 한다는 규칙 때문이다.** <br>
**=> 프로퍼티에 기본값을 미리 할당하면 인스턴스가 생성되면서 동시에 초기 값을 가지게 된다.** <br>

``` swift
class ClassA {
    var className: String = "No. 1 Swift"
    var classNickName: String = "스위프트"
    var classSince: Int = 2015
}
```
---

**=> 그러나 이렇게 초기 값을 지정하는 것이 아니라 인스턴스가 초기화 되었을 때 원하는 값을 넣어주고 싶을 떄가 있을 것이다. 그럴때 init() 을 사용한다.** <br>


``` swift
class ClassB {
    var className: String
    var classNickName: String
    var classSince: Int
    
    init(className: String, classNickName: String, classSince: Int) {
        self.className = className
        self.classNickName = classNickName
        self.classSince = classSince
    }
    
}

let swiftClass1: ClassB = ClassB(className: "swift programming 1", classNickName: "SP", classSince: 2020)

```
---

**=> 그러나 이렇게 했을 시 반을 설정하다보면 중간에 classNickName이 없는 반도 있을 것이기 때문에 이러한 경우엔 옵셔널 타입을 사용해준다.** <br>


``` swift

class ClassC {
    var className: String
    var classNickName: String?
    var classSince: Int
    
//    init(className: String, classNickName: String, classSince: Int) {
//        self.className = className
//        self.classNickName = classNickName
//        self.classSince = classSince
//    }
    
    // 이처럼 initializer 에서 넣어줘도 되고 안넣어도 무방하다! 또는 self.init을 통해 아래 있는 init을 가져와서 중복코드를 줄일 수도 있다.
    
    // 자신의 인이셜라이저를 쓸 때는 앞에 convenience 를 붙여줘야 한다.
    convenience init(className: String, classNickName: String, classSince: Int) {
        self.init(className: className, classSince: classSince)
        self.classNickName = classNickName
    }
    
    init(className: String, classSince: Int) {
        self.className = className
        self.classSince = classSince
    }
}

let swiftClass2: ClassB = ClassB(className: "swift programming 2", classNickName: "SP", classSince: 2020)

let reactClass: ClassC = ClassC(className: "react programming", classSince: 2019)
```
---

**=> 암시적 추출 옵셔널은 인스턴스 사용에 꼭 필요하지만 초기값을 할당하지 않고자 할 때 사용한다.** <br>

``` swift

class NewIphone {
    var deviceName: String
    var owner: String!
    
    init(deviceName: String) {
        self.deviceName = deviceName
    }
    
    func purchasePhone() {
        print("새로운 아이폰의 이름은 \(deviceName) 이고 \(owner ?? "익명의 누군가") 님이 새로운 아이폰을 샀습니다.")
    }
}

let iphone12pro: NewIphone = NewIphone(deviceName: "IPhone 12 Pro")
//iphone12pro.owner = "오밀"
iphone12pro.purchasePhone()

```
---

**=> 실패 가능한 init 도 만들어 줄 수 있다.** <br>
``` swift

class PersonA {
    var name: String
    var age: Int
    var nickName: String?
    
    init? (name: String, age: Int) {
        if (0...120).contains(age) == false {
            return nil
        }
        
        if name.count == 0 {
            return nil
        }
        
        self.name = name
        self.age = age
    }
    
}


let tom: PersonA? = PersonA(name: "Tom", age: 121)
```

<br>
<br>


## **deinit**

=> deinit은 클래스의 인스턴스가 메모리에서 해제되는 시점에 호출되게 되며 인스턴스가 해제되는 시점에 해야할 일을 구현할 수 있다. <br>
=> deinit은 class type에만 구현이 가능하다. <br>

---

<br>
<br>
<br>

## **타입 케스팅(type casting)**
**=> "as" 연산자, "is" 연산자** <br>
=> 위프트의 타입캐스팅은 인스턴스의 타입을 확인하는 용도로 사용되거나 클래스의 인스턴스를 부모 혹은 자식 클래스의 타입으로 사용할 수 있는지 확인하는 용도로 사용된다. <br>
=> dic를 사용할 때, Any나 AnyObject 를 사용하는 경우가 많은데, 이럴 때 타입을 확인해야 하므로 많이 사용될 수 있다. <br>

``` swift
if () is () {
        print()
    } else if () is () {
        print()
    } else if () is () {
        print()
    }
}
```
또는

``` swift
switch () {
case is ():
    print()
case is ():
    print()
case is ():
    print()
default:
    print()
}
```

이런 형식으로도 사용될 수 있다.

<br>
<br>

---

### **업 케스팅(UP casting)**
=> as 는 is 만큼 많이 사용하지는 않는다. <br>
=> as를 사용하여 부모클래스의 인스턴스로 사용할 수 있도록 컴파일러에게 타입정보를 전환해 준다. <br>
=> Any, AnyObject 로도 타입 정보를 변환할 수 있다. <br>
=> 암시적으로 처리되기 때문에 생략해도 무방  <br>

<br>

### **다운 캐스팅(Down casting)**
**=> as? 또는 as! 를 사용 함으로써 자식 클래스의 인스턴스로 사용할 수 있도록 한다. 컴파일러에게 인스턴스의 타입정보를 전환해준다.** <br>

=> 조건부 다운 케스팅 (as?) => 성공시 결과값이 옵셔널 타입으로 반환됨 <br>
=> 강제 다운 케스팅 (as!) => 다운 케스팅에 실패하면 런타임 오류 위험 <br>


---
<br>
<br>
<br>



## **Assert, guard 구문 (assertion, early exit)**
**이 두 구문은 애플리케이션 동작 중 생성하게 되는 다양한 값을 동적으로 확인하고 안전하게 처리한다.**
<br>

### **Assertion**
    - assert(_:_:file:line:) 함수를 사용하게 된다.
    - assert 함수는 디버깅 모드에서만 동작한다. 
    - 배포하는 앱에는 제외되며 디버깅 도중 조건의 검증을 위해서 사용된다.
    - 어떤 조건으로 결과를 검증 할 때 사용
    - 예상했던 조건이 맞는가? 확인


``` swift

var Age: Int = 30

assert(Age == 30, "Age != 30")

// age 가 30일 경우에 위 구문을 그대로 지나치게 되고 틀리게 되면 뒤에 있는 메시지를 반환하게 된다. (assertion failed error 반환)

func assertionFunction(name: String?) {
    assert(name != nil, "name == nil")
    
    assert((name! != "Tom") && (name! != "Jammy"), "name is Tom or Jammy")
    print("Your name is \(name!). Hello, \(name!)")
}


assertionFunction(name: "Kim")
```

---

  
### **guard (Early Exit)**
    - guard를 사용하여 잘못된 값의 전달 시 특정 실행 구문을 빠르게 전달합니다.
    - guard의 else 블럭에는 특정 코드 블럭을 종료하는 지시어인 return, break 가 있어야 한다.
    - 타입 캐스팅, 옵셔널과 자주 사용된다. 단순조건을 판단하고 종료할 때도 사용된다.
    - guard let (조건) else () return ()
---
##### **예제**
``` swift

func functionwithGuard(age: Int?) {
    guard let unwrappedAge = age,
          unwrappedAge < 100,
          unwrappedAge >= 0 else {
        print("나이가 잘못 입력되었습니다.")
        return
    }
    
    // Age 가 100보다 작으면 종료하라는 구문도 작성할 수 있다.
//    guard unwrappedAge < 100 else {
//        return
//    }
    
    
    print("당신의 나이는 \(unwrappedAge) 세 입니다.")
}
```
---
<br>

``` swift
var count = 1

while true {
    guard count < 4 else {
        break
    }
    print(count)
    count += 1
}
```
---
<br>

**딕셔너리에서도 많이 사용된다. 왜냐하면 키값을 빼오면 모두 옵셔널로 빠지기 때문에** <br>

``` swift
func someFunction(info: [String: Any]) {
    
    // 구문이 참이면 name에 키값을 할당하고 아니면 종료
    guard let name = info["name"] as? String else {
        return
    }
    
    guard let age = info["age"] as? Int, age >= 0 else {
        return
    }
    print("\(name): \(age)")
}

```
