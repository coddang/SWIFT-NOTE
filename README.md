# Swift Programming NOTE π

<br>

# λͺ©μ 
  1. μΈμ΄μ λν μ νν μ΄ν΄
  2. νμ΅νλ λ΄μ©μ λν μμ½ μ λ¦¬
  3. λ¬Έμ ν΄κ²°μ νμν λͺλ Ήμ΄μ ν¨ν΄ μ λ¦¬(μκ³ λ¦¬μ¦)

<br>
<br>

## **μκ³  λμ΄κ° κ²** <br>
=> 'function', 'method', 'instance'λ μ²« κΈμλ₯Ό μλ¬Έμλ‘ νλ μΉ΄λ©μΌμ΄μ€ μ¬μ© <br>
=> 'protocol', 'extension', 'struct', 'class'λ μ²« κΈμλ₯Ό λλ¬Έμλ‘ νλ μΉ΄λ©μΌμ΄μ€ μ¬μ© <br>
=> Set, Dictionary, Array λ collection type <br>

> κ° νμ(Value Type): Struct, enum <br>
> μ°Έμ‘° νμ(Reference Type): class, closure

<br>
<br>

## **νμ΅**
**Class**

    - 1. λ¨μΌ μμμ΄ λλ€.
    - 2. κ°μ΄ Share κ° λλ€.
    - 3. Reference Type(μ°Έμ‘° νμ) -> λ°μ΄ν°λ₯Ό μ λ¬ν  λ κ°μ λ©λͺ¨λ¦¬μ μμΉλ₯Ό μ λ¬νλ€.
    - 4. μ ν΅μ μΈ κ°μ²΄μ§ν₯ νλ‘κ·Έλ¨μ OPP κ΄μ μμμ ν΄λμ€μ λμΌ
    - 5. Apple νλ μ μν¬μ λλΆλΆμ ν° λΌλλ classλ‘ μ΄λ£¨μ΄μ Έ μλ€.

**Struct**

    - 1. κ°μ΄ Copy κ° λλ€.
    - 2. Value Type -> λ°μ΄ν°λ₯Ό μ λ¬ν  λ κ°μ λ³΅μ¬ν΄μ μ λ¬
    - 3. CμΈμ΄ κ΅¬μ‘°μ²΄ λ³΄λ€ λ λ€μν κΈ°λ₯μ κ°μ§λ€.
    - 4. swift μ λλΆλΆμ ν° λΌλλ λͺ¨λ struct λ‘ λμ΄μλ€. 
    
    => μ°κ΄λ κ°μ νλλ‘ λͺ¨μμ νλμ λ°μ΄ν° νμμΌλ‘ λ¬Άμ΄λ΄κ³  μΆμ λ μ¬μ©
    => μ°Έμ‘°κ° μλ λ³΅μ¬λ₯Ό μν  λ, κ°μ ν λΉλ°μμ λ³κ²½νκ³  μΆμ λ μ¬μ©
    => μμ μ μμν  νμκ° μκ±°λ λ€λ₯Έ νμμ μμλ°μ νμκ° μμ λ μ¬μ©
    
    
**enum**

    - 1. λ€λ₯Έ μΈμ΄μ μ΄κ±°νκ³Όλ λ€λ₯Έ λ€μν κΈ°λ₯μ μ κ³΅νλ€.
    - 2. μμμ΄ λΆκ°λ₯
    - 3. κ° νμμ κ°μ§λ€.
    - 4. μ΄κ±°ν μμ²΄κ° νλμ λ°μ΄ν° νμμ΄λ€. μ μλ―Έν κ³΅ν΅μ μ κ°μ§ κ°μ λͺ¨μ κ²(λ¬, μ μ¬ λ©λ΄ λ±)
    - 5. case νλνλκ° μ μλ―Έν νλμ κ°, λ³μμ²λΌ μ·¨κΈλλ€.


<br>
<br>

## **λ§€μ¨λ λͺ¨μ**

  1. type(of: )
  2. remove(at: index)
  3. removeFirst()
  4. removeLast()
  5. removeValue(forkey: )
  6. contains()
  7. insert(something, at: index)
  8. append()
  9. popLast()
  10. sort() -> μμ΄ μ°μ  μ λ ¬ / μλ³Έ κ° λ³κ²½
  11. sorted() -> νκΈ μ°μ  μ λ ¬ / λ³΅μ¬λ κ° μ λ¬(μ½κΈ° μ μ©)
  12. sorted(by: ) / > (λ΄λ¦Όμ°¨μ) < (μ€λ¦μ°¨μ)
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
  24. stride(from: ,to: ,by: ) -> to μ΄μ κΉμ§ byμ μν΄ μ°μ°
  25. stride(from: ,through: ,by: ) -> throughμ μλ ₯λ μκΉμ§ byμ μν΄ μ°μ°
  26. array.randomElement()
  27. array.shuffled()
  28. .isEmpty
  29. print(something, terminator: κΈ°λ³Έμ μΌλ‘ μ€λ°κΏ μ²λ¦¬)
  30. components(separatedBy: )
  31. split(by: )
  32. trimmingCharacters(in: ["! # λ± λ¬Έμμ΄ μμͺ½ μ κ±°ν  λ¬Έμ"])
  33. components(separatedBy: ["1", "!", "$", "%" λ±]).joined()
  34. .zip(sequence1, sequence2)
  35. .valueUpdate(Value, forKey: Key)
  36. .flatMap
  37. compactMap

<br>
<br>


## μ κ·Ό μ μ΄

    - κ°μ²΄μ§ν₯ νλ‘κ·Έλλ°(OOP) μμ μλνλ μ€μν κ°λμ΄λ©° μ΄λ₯Ό κ΅¬ννλ ν΅μ¬κΈ°λ₯μ μ κ·Ό μ μ΄μ΄λ€.
    - Q. μ κ·Ό μ μ΄λ μ½λλΌλ¦¬ μνΈμμ©μ ν  μ νμΌ κ° λλ λͺ¨λ κ°μ μ κ·Όμ μ νν  μ μλ κΈ°λ₯μΌλ‘, μ κ·Όμ μ΄λ₯Ό ν΅ν΄ μ½λμ μμΈν κ΅¬νμ μ¨κΈ°κ³  νμ©λ κΈ°λ₯λ§ μ¬μ©νλ μΈν°νμ΄μ€λ₯Ό λ§λ€ μ μλ€.
    => μ κ·Ό μ μ΄λ₯Ό μ¬μ©νλ μ΄μ λ κ°μ²΄μ§ν₯ νλ‘κ·Έλλ°μμ μΊ‘μνμ μλνλ₯Ό ν΅ν΄ μΈλΆμμ μ κ·Όνλ©΄ μλλ μ½λμ μ κ·Όμ λ§κΈ° μν΄μμ΄λ€. 

### μ¬μ©ν΄μΌ ν  λ
    => [x] λΆνμν νμΌμ΄λ λͺ¨λμ μ κ·Όμ λ§μ μλμΉ μμ κ²°κ³Όλ₯Ό νΌνκ³  μΆμ λ
    => [x] νμμ μΈ λΆλΆλ§ μ κ·Όμ νμ©ν΄μΌ ν  μ μ μ²΄ μ½λμ λΈμΆ κ°λ₯μ±μ μ°¨λ¨ν  λ

 - μ€μννΈμ μ κ·Ό μ μ΄: λͺ¨λ + μμ€νμΌ κΈ°λ° μ€κ³ 
 
 **λͺ¨λ**: λ°°ν¬ν  μ½λμ λ¬Άμ λ¨μλ‘ Swiftμμ  importλ₯Ό ν΅ν΄ λΆλ¬μ€κ² λλ€. / μ) νλ μμν¬, λΌμ΄λΈλ¬λ¦¬, μ νλ¦¬μΌμ΄μ
**μμ€νμΌ**: νλμ μ€μννΈ μμ€ μ½λ νμΌμ μλ―Έ(μ€μννΈλ λ³΄ν΅ νμΌ νλμ νμ νλ, But μ¬λ¬ ν΄λμ€ κ΅¬μ‘°μ²΄ μ΄κ±°ν μΆκ° λ  μ μμ)


## μ κ·Ό μμ€
    - μ κ·Ό μ μ΄λ μ κ·Ό μμ€ ν€μλλ₯Ό ν΅ν΄ κ΅¬ννλ€.
    - κ° νμ(class, enum, struct)μ νΉμ ν μ κ·Ό μμ€μ μ§μ  κ°λ₯
    - νμ λ΄λΆμ property, method, initializer, subscript μλ μ κ·Ό μμ€ μ§μ  κ°λ₯
    - μ κ·Ό μμ€ ν€μλλ <open, public, Internal, fileprivate, private> 5κ°μ§λ‘ λλλ€.
    

**μ κ·Ό μμ€** | **ν€μλ** | **μ κ·Όλ** | **λ²μ** | **λΉκ³ ** |
--------------|------------|------------|----------|---------|
κ°λ°© μ κ·Ό μμ€ | open | λμ(5) | λͺ¨λ μΈλΆκΉμ§ | classμμλ§ μ¬μ© |
κ³΅κ° μ κ·Ό μμ€ | public | 4 | λͺ¨λ μΈλΆκΉμ§ |    |
λ΄λΆ μ κ·Όμμ€ | internal | 3 | λͺ¨λ λ΄λΆ |    |
νμΌ μΈλΆλΉκ³΅κ° μ κ·Όμμ€ | fileprivate | 2 | νμΌ λ΄λΆ |    |
λΉκ³΅κ° μ κ·Ό μμ€ | private | λ?μ(1) | κΈ°λ₯ μ μ λ΄λΆ |    |



<br>
<br>
<br>
<br>



## μ λ€λ¦­(Generic)

- μ λ€λ¦­μ ν΅ν΄ νμμ λν μ μ°μ±μ κ°μ§ μ μλ€. μ λ€λ¦­μΌλ‘ κ΅¬νν κΈ°λ₯κ³Ό νμμ 
μ¬μ¬μ© κ°λ₯νκ³  μ½λμ μ€λ³΅μ μ€μΌ μ μλ€. <br>
- μ€μννΈ νμ€ λΌμ΄λΈλ¬λ¦¬λ λ§μ μ λ€λ¦­ μ½λλ‘ κ΅¬νλμ΄ μλ€. <br>
- Array, Dictionary, Set κ³Ό κ°μ νμ = λͺ¨λ μ λ€λ¦­ μ»¬λ μ <br>
- μ μλ λ¬Έμμ΄ νμμ μμλ‘ κ°λ λ°°μ΄μ λ§λλ κ²κ³Ό μ΄λ€ νμλ λ°°μ΄ μμλ‘ κ°μ§ μ μλ κ²μ λͺ¨λ μ λ€λ¦­ λλΆμ΄λ€.   <br>

``` swift
μ)
var array: [Int] = [10, 20, 30, 40]
var set: Set<Int> = [50, 40, 30, 20]
var dictionary: [String: Int] = ["κΉ": 100, "μ΄": 300, "λ°": 200]
```

### μ λ€λ¦­ μ¬μ©μ 
=> μ λ€λ¦­μ΄ νμν λ©μλλ νμ μ΄λ¦ λ€μ  "<>" λΆμ΄κ³  κ·Έ μ¬μ΄μ μ λ€λ¦­μ μν λ§€κ°λ³μλ₯Ό λ£μ΄ νκΈ° <br> μ) <T>, <U>, <I>

μ λ€λ¦­ μ¬μ©μ μνλ νμμ΄λ ν¨μ <νμ λ§€κ°λ³μ> (ν¨μ λ§€κ°λ³μ) <br>


<br>
<br>



## **μμ**

### νλ‘νΌν°(property) <br>
    - μ μ₯ νλ‘νΌν°: Stored property
    - μ°μ° νλ‘νΌν°: Computed property
    - μΈμ€ν΄μ€ νλ‘νΌν°: instance property
    - νμ νλ‘νΌν°: type property



``` swift

class Person {
    var name: String = " "
    
    func selfIntroduce() {
        print("μ λ \(name)μλλ€.")
    }
    
    // final ν€μλλ₯Ό ν΅ν΄ μ¬μ μλ₯Ό λ°©μ§ν  μ μλ€. -> μμ ν΄λμ€μ λ¬Όλ € μ€¬μ λ μ¬μ μλ₯Ό λ°©μ§ override λΆκ°!
    final func sayHello() {
        print("Hello")
    }
    
    //νμ λ§€μ¨λ
    //μ¬μ μ λΆκ° νμ λ©μ¨λ - static
    static func typeMethod() {
        print("type method - static")
    }
    
    // μ¬μ μ κ°λ₯
    class func classMethod() {
        print("type method - class")
    }
    
    // μ¬μ μκ° κ°λ₯ν class λ©μ¨λλΌλ
    // final ν€μλλ₯Ό μ¬μ©νλ©΄ μ¬μ μ ν  μ μλ€.
    // λ§€μ¨λ μμ 'static' == 'final class'
    final class func finalClassMethod() {
        print("type method - final class")
    }
}

class Student: Person {
    var major: String = ""
    
    override func selfIntroduce() {
        print("μ λ \(name)μ΄κ³ , μ κ³΅μ \(major)μλλ€. ")
        // λΆλͺ¨ ν΄λμ€μ λ΄μ©μ νΈμΆ
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
    
    // μΈμ€ν΄μ€ μ μ₯ νλ‘νΌν°
    var name: String = ""
    var `class`: String = "swift"
    var KoreanAge: Int = 0
    
    // μΈμ€ν΄μ€ μ°μ° νλ‘νΌν°
    var westernAge: Int {
        get {
            return KoreanAge - 1
        }
        
        set(inputValue) {
            KoreanAge = inputValue + 1
        }
    }
    
    // νμ μ μ₯ νλ‘νΌν°
    static var typeDiscription: String = "νκΈ μΉκ΅¬"
    
    // μΈμ€ν΄μ€ λ§€μλ
    func selfIntroduce() {
        print("μ λ \(self.class)λ° \(name) μλλ€.")
    }
    
    // μ½κΈ° μ μ© μΈμ€ν΄μ€ μ°μ° νλ‘νΌν° get λ§ κ΅¬νμ΄ λμ΄ μμΌλ©΄ μ½κΈ° μ μ©μ΄λ€.
    var selfIntroducing: String {
        get {
            return "μ λ \(self.class)λ° \(name)μ΄λΌκ³  ν©λλ€."
        }
    }
    
}

var λͺμ: ClassMate = ClassMate()
λͺμ.KoreanAge = 25

λͺμ.name = "μ λͺμ"
print(λͺμ.name)

print(λͺμ.selfIntroducing)
print("μ  νκ΅­ λμ΄λ \(λͺμ.KoreanAge)μ΄μ΄κ³ , λ―Έκ΅­λμ΄λ \(λͺμ.westernAge)μ΄ μλλ€.")


```

<br>
<br>

## **μΈμ€ν΄μ€μ μμ± & μλ©Έ (init  / deinit)**

## **init**

**=> λͺ¨λ  μ μ₯ νλ‘νΌν°μλ κΈ°λ³Έ κ°μ λ£μ΄μΌ νλ€. λͺ¨λ  νλ‘νΌν°μ μ ν¨ν κ°μ΄ ν λΉλμ΄μΌ νλ€λ κ·μΉ λλ¬Έμ΄λ€.** <br>
**=> νλ‘νΌν°μ κΈ°λ³Έκ°μ λ―Έλ¦¬ ν λΉνλ©΄ μΈμ€ν΄μ€κ° μμ±λλ©΄μ λμμ μ΄κΈ° κ°μ κ°μ§κ² λλ€.** <br>

``` swift
class ClassA {
    var className: String = "No. 1 Swift"
    var classNickName: String = "μ€μννΈ"
    var classSince: Int = 2015
}
```
---

**=> κ·Έλ¬λ μ΄λ κ² μ΄κΈ° κ°μ μ§μ νλ κ²μ΄ μλλΌ μΈμ€ν΄μ€κ° μ΄κΈ°ν λμμ λ μνλ κ°μ λ£μ΄μ£Όκ³  μΆμ λκ° μμ κ²μ΄λ€. κ·Έλ΄λ init() μ μ¬μ©νλ€.** <br>


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

**=> κ·Έλ¬λ μ΄λ κ² νμ μ λ°μ μ€μ νλ€λ³΄λ©΄ μ€κ°μ classNickNameμ΄ μλ λ°λ μμ κ²μ΄κΈ° λλ¬Έμ μ΄λ¬ν κ²½μ°μ μ΅μλ νμμ μ¬μ©ν΄μ€λ€.** <br>


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
    
    // μ΄μ²λΌ initializer μμ λ£μ΄μ€λ λκ³  μλ£μ΄λ λ¬΄λ°©νλ€! λλ self.initμ ν΅ν΄ μλ μλ initμ κ°μ Έμμ μ€λ³΅μ½λλ₯Ό μ€μΌ μλ μλ€.
    
    // μμ μ μΈμ΄μλΌμ΄μ λ₯Ό μΈ λλ μμ convenience λ₯Ό λΆμ¬μ€μΌ νλ€.
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

**=> μμμ  μΆμΆ μ΅μλμ μΈμ€ν΄μ€ μ¬μ©μ κΌ­ νμνμ§λ§ μ΄κΈ°κ°μ ν λΉνμ§ μκ³ μ ν  λ μ¬μ©νλ€.** <br>

``` swift

class NewIphone {
    var deviceName: String
    var owner: String!
    
    init(deviceName: String) {
        self.deviceName = deviceName
    }
    
    func purchasePhone() {
        print("μλ‘μ΄ μμ΄ν°μ μ΄λ¦μ \(deviceName) μ΄κ³  \(owner ?? "μ΅λͺμ λκ΅°κ°") λμ΄ μλ‘μ΄ μμ΄ν°μ μμ΅λλ€.")
    }
}

let iphone12pro: NewIphone = NewIphone(deviceName: "IPhone 12 Pro")
//iphone12pro.owner = "μ€λ°"
iphone12pro.purchasePhone()

```
---

**=> μ€ν¨ κ°λ₯ν init λ λ§λ€μ΄ μ€ μ μλ€.** <br>
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

=> deinitμ ν΄λμ€μ μΈμ€ν΄μ€κ° λ©λͺ¨λ¦¬μμ ν΄μ λλ μμ μ νΈμΆλκ² λλ©° μΈμ€ν΄μ€κ° ν΄μ λλ μμ μ ν΄μΌν  μΌμ κ΅¬νν  μ μλ€. <br>
=> deinitμ class typeμλ§ κ΅¬νμ΄ κ°λ₯νλ€. <br>

---

<br>
<br>
<br>

## **νμ μΌμ€ν(type casting)**
**=> "as" μ°μ°μ, "is" μ°μ°μ** <br>
=> μννΈμ νμμΊμ€νμ μΈμ€ν΄μ€μ νμμ νμΈνλ μ©λλ‘ μ¬μ©λκ±°λ ν΄λμ€μ μΈμ€ν΄μ€λ₯Ό λΆλͺ¨ νΉμ μμ ν΄λμ€μ νμμΌλ‘ μ¬μ©ν  μ μλμ§ νμΈνλ μ©λλ‘ μ¬μ©λλ€. <br>
=> dicλ₯Ό μ¬μ©ν  λ, Anyλ AnyObject λ₯Ό μ¬μ©νλ κ²½μ°κ° λ§μλ°, μ΄λ΄ λ νμμ νμΈν΄μΌ νλ―λ‘ λ§μ΄ μ¬μ©λ  μ μλ€. <br>

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
λλ

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

μ΄λ° νμμΌλ‘λ μ¬μ©λ  μ μλ€.

<br>
<br>

---

### **μ μΌμ€ν(UP casting)**
=> as λ is λ§νΌ λ§μ΄ μ¬μ©νμ§λ μλλ€. <br>
=> asλ₯Ό μ¬μ©νμ¬ λΆλͺ¨ν΄λμ€μ μΈμ€ν΄μ€λ‘ μ¬μ©ν  μ μλλ‘ μ»΄νμΌλ¬μκ² νμμ λ³΄λ₯Ό μ νν΄ μ€λ€. <br>
=> Any, AnyObject λ‘λ νμ μ λ³΄λ₯Ό λ³νν  μ μλ€. <br>
=> μμμ μΌλ‘ μ²λ¦¬λκΈ° λλ¬Έμ μλ΅ν΄λ λ¬΄λ°©  <br>

<br>

### **λ€μ΄ μΊμ€ν(Down casting)**
**=> as? λλ as! λ₯Ό μ¬μ© ν¨μΌλ‘μ¨ μμ ν΄λμ€μ μΈμ€ν΄μ€λ‘ μ¬μ©ν  μ μλλ‘ νλ€. μ»΄νμΌλ¬μκ² μΈμ€ν΄μ€μ νμμ λ³΄λ₯Ό μ νν΄μ€λ€.** <br>

=> μ‘°κ±΄λΆ λ€μ΄ μΌμ€ν (as?) => μ±κ³΅μ κ²°κ³Όκ°μ΄ μ΅μλ νμμΌλ‘ λ°νλ¨ <br>
=> κ°μ  λ€μ΄ μΌμ€ν (as!) => λ€μ΄ μΌμ€νμ μ€ν¨νλ©΄ λ°νμ μ€λ₯ μν <br>


---
<br>
<br>
<br>



## **Assert, guard κ΅¬λ¬Έ (assertion, early exit)**
**μ΄ λ κ΅¬λ¬Έμ μ νλ¦¬μΌμ΄μ λμ μ€ μμ±νκ² λλ λ€μν κ°μ λμ μΌλ‘ νμΈνκ³  μμ νκ² μ²λ¦¬νλ€.**
<br>

### **Assertion**
    - assert(_:_:file:line:) ν¨μλ₯Ό μ¬μ©νκ² λλ€.
    - assert ν¨μλ λλ²κΉ λͺ¨λμμλ§ λμνλ€. 
    - λ°°ν¬νλ μ±μλ μ μΈλλ©° λλ²κΉ λμ€ μ‘°κ±΄μ κ²μ¦μ μν΄μ μ¬μ©λλ€.
    - μ΄λ€ μ‘°κ±΄μΌλ‘ κ²°κ³Όλ₯Ό κ²μ¦ ν  λ μ¬μ©
    - μμνλ μ‘°κ±΄μ΄ λ§λκ°? νμΈ


``` swift

var Age: Int = 30

assert(Age == 30, "Age != 30")

// age κ° 30μΌ κ²½μ°μ μ κ΅¬λ¬Έμ κ·Έλλ‘ μ§λμΉκ² λκ³  νλ¦¬κ² λλ©΄ λ€μ μλ λ©μμ§λ₯Ό λ°ννκ² λλ€. (assertion failed error λ°ν)

func assertionFunction(name: String?) {
    assert(name != nil, "name == nil")
    
    assert((name! != "Tom") && (name! != "Jammy"), "name is Tom or Jammy")
    print("Your name is \(name!). Hello, \(name!)")
}


assertionFunction(name: "Kim")
```

---

  
### **guard (Early Exit)**
    - guardλ₯Ό μ¬μ©νμ¬ μλͺ»λ κ°μ μ λ¬ μ νΉμ  μ€ν κ΅¬λ¬Έμ λΉ λ₯΄κ² μ λ¬ν©λλ€.
    - guardμ else λΈλ­μλ νΉμ  μ½λ λΈλ­μ μ’λ£νλ μ§μμ΄μΈ return, break κ° μμ΄μΌ νλ€.
    - νμ μΊμ€ν, μ΅μλκ³Ό μμ£Ό μ¬μ©λλ€. λ¨μμ‘°κ±΄μ νλ¨νκ³  μ’λ£ν  λλ μ¬μ©λλ€.
    - guard let (μ‘°κ±΄) else () return ()
---
##### **μμ **
``` swift

func functionwithGuard(age: Int?) {
    guard let unwrappedAge = age,
          unwrappedAge < 100,
          unwrappedAge >= 0 else {
        print("λμ΄κ° μλͺ» μλ ₯λμμ΅λλ€.")
        return
    }
    
    // Age κ° 100λ³΄λ€ μμΌλ©΄ μ’λ£νλΌλ κ΅¬λ¬Έλ μμ±ν  μ μλ€.
//    guard unwrappedAge < 100 else {
//        return
//    }
    
    
    print("λΉμ μ λμ΄λ \(unwrappedAge) μΈ μλλ€.")
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

**λμλλ¦¬μμλ λ§μ΄ μ¬μ©λλ€. μλνλ©΄ ν€κ°μ λΉΌμ€λ©΄ λͺ¨λ μ΅μλλ‘ λΉ μ§κΈ° λλ¬Έμ** <br>

``` swift
func someFunction(info: [String: Any]) {
    
    // κ΅¬λ¬Έμ΄ μ°Έμ΄λ©΄ nameμ ν€κ°μ ν λΉνκ³  μλλ©΄ μ’λ£
    guard let name = info["name"] as? String else {
        return
    }
    
    guard let age = info["age"] as? Int, age >= 0 else {
        return
    }
    print("\(name): \(age)")
}

```





