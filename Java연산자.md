산술 연산자 (Arithmetic Operators)
비교 연산자 (Relational Operators)
논리 연산자 (Logical Operators)
비트 연산자 (Bitwise Operators)
대입 연산자 (Assignment Operators)
기타 연산자 (Miscellaneous Operators)
각 연산자들의 기능과 사용법을 살펴보겠습니다.

1. 산술 연산자 (Arithmetic Operators)
산술 연산자는 기본적인 산술 연산을 수행합니다.

+ : 덧셈
- : 뺄셈
* : 곱셈
/ : 나눗셈
% : 나머지
java
코드 복사
int a = 10;
int b = 5;

System.out.println("a + b = " + (a + b)); // 15
System.out.println("a - b = " + (a - b)); // 5
System.out.println("a * b = " + (a * b)); // 50
System.out.println("a / b = " + (a / b)); // 2
System.out.println("a % b = " + (a % b)); // 0
2. 비교 연산자 (Relational Operators)
비교 연산자는 두 값을 비교하고, 결과를 boolean으로 반환합니다.

== : 같음
!= : 같지 않음
> : 큼
< : 작음
>= : 크거나 같음
<= : 작거나 같음
java
코드 복사
int a = 10;
int b = 5;

System.out.println("a == b: " + (a == b)); // false
System.out.println("a != b: " + (a != b)); // true
System.out.println("a > b: " + (a > b)); // true
System.out.println("a < b: " + (a < b)); // false
System.out.println("a >= b: " + (a >= b)); // true
System.out.println("a <= b: " + (a <= b)); // false
3. 논리 연산자 (Logical Operators)
논리 연산자는 논리적인 조건을 결합하거나 부정합니다.

&& : 논리 AND
|| : 논리 OR
! : 논리 NOT
java
코드 복사
boolean x = true;
boolean y = false;

System.out.println("x && y: " + (x && y)); // false
System.out.println("x || y: " + (x || y)); // true
System.out.println("!x: " + (!x)); // false
4. 비트 연산자 (Bitwise Operators)
비트 연산자는 정수형 변수의 비트 단위 연산을 수행합니다.

& : 비트 AND
| : 비트 OR
^ : 비트 XOR
~ : 비트 NOT
<< : 왼쪽 시프트
>> : 오른쪽 시프트
>>> : 논리적 오른쪽 시프트
java
코드 복사
int a = 5;  // 0101
int b = 3;  // 0011

System.out.println("a & b: " + (a & b)); // 1 (0001)
System.out.println("a | b: " + (a | b)); // 7 (0111)
System.out.println("a ^ b: " + (a ^ b)); // 6 (0110)
System.out.println("~a: " + (~a)); // -6 (..1010, 2의 보수)
System.out.println("a << 1: " + (a << 1)); // 10 (1010)
System.out.println("a >> 1: " + (a >> 1)); // 2 (0010)
System.out.println("a >>> 1: " + (a >>> 1)); // 2 (0010)
5. 대입 연산자 (Assignment Operators)
대입 연산자는 변수에 값을 할당하거나, 산술 및 비트 연산 후 결과를 변수에 저장합니다.

= : 대입
+= : 더한 후 대입
-= : 뺀 후 대입
*= : 곱한 후 대입
/= : 나눈 후 대입
%= : 나머지를 구한 후 대입
&= : 비트 AND 후 대입
|= : 비트 OR 후 대입
^= : 비트 XOR 후 대입
<<= : 왼쪽 시프트 후 대입
>>= : 오른쪽 시프트 후 대입
>>>= : 논리적 오른쪽 시프트 후 대입
java
코드 복사
int a = 10;

a += 5;  // a = a + 5
System.out.println("a += 5: " + a); // 15

a -= 3;  // a = a - 3
System.out.println("a -= 3: " + a); // 12

a *= 2;  // a = a * 2
System.out.println("a *= 2: " + a); // 24

a /= 4;  // a = a / 4
System.out.println("a /= 4: " + a); // 6

a %= 3;  // a = a % 3
System.out.println("a %= 3: " + a); // 0
6. 기타 연산자 (Miscellaneous Operators)
자바에는 위의 연산자 외에도 다양한 연산자가 있습니다.

조건부 연산자 (Conditional Operator) 또는 삼항 연산자 (Ternary Operator)
조건식의 결과에 따라 값을 반환합니다.

? :
java
코드 복사
int a = 10;
int b = 20;
int max = (a > b) ? a : b;  // a와 b 중 큰 값을 max에 대입
System.out.println("max: " + max); // 20
인스턴스 확인 연산자 (instanceof)
객체가 특정 클래스의 인스턴스인지 확인합니다.

java
코드 복사
String str = "Hello";
boolean isString = str instanceof String;
System.out.println("str instanceof String: " + isString); // true
