산술 연산자 (Arithmetic Operators)
관계 연산자 (Relational Operators)
논리 연산자 (Logical Operators)
비트wise 연산자 (Bitwise Operators)
대입 연산자 (Assignment Operators)
증감 연산자 (Increment and Decrement Operators)
조건부 연산자 (Conditional Operator)
콤마 연산자 (Comma Operator)
주소 및 간접 참조 연산자 (Address and Indirection Operators)
기타 연산자 (Miscellaneous Operators)
각 연산자의 기능과 사용법을 살펴보겠습니다.

1. 산술 연산자 (Arithmetic Operators)
산술 연산자는 기본적인 산술 연산을 수행합니다.

+ : 덧셈
- : 뺄셈
* : 곱셈
/ : 나눗셈
% : 나머지

int a = 10;
int b = 5;

printf("a + b = %d\n", a + b); // 15
printf("a - b = %d\n", a - b); // 5
printf("a * b = %d\n", a * b); // 50
printf("a / b = %d\n", a / b); // 2
printf("a % b = %d\n", a % b); // 0
2. 관계 연산자 (Relational Operators)
관계 연산자는 두 값을 비교하고, 결과를 0 또는 1로 반환합니다.

== : 같음
!= : 같지 않음
> : 큼
< : 작음
>= : 크거나 같음
<= : 작거나 같음

int a = 10;
int b = 5;

printf("a == b: %d\n", a == b); // 0
printf("a != b: %d\n", a != b); // 1
printf("a > b: %d\n", a > b); // 1
printf("a < b: %d\n", a < b); // 0
printf("a >= b: %d\n", a >= b); // 1
printf("a <= b: %d\n", a <= b); // 0
3. 논리 연산자 (Logical Operators)
논리 연산자는 논리적인 조건을 결합하거나 부정합니다.

&& : 논리 AND
|| : 논리 OR
! : 논리 NOT

int x = 1;
int y = 0;

printf("x && y: %d\n", x && y); // 0
printf("x || y: %d\n", x || y); // 1
printf("!x: %d\n", !x); // 0
4. 비트wise 연산자 (Bitwise Operators)
비트wise 연산자는 정수형 변수의 비트 단위 연산을 수행합니다.

& : 비트 AND
| : 비트 OR
^ : 비트 XOR
~ : 비트 NOT
<< : 왼쪽 시프트
>> : 오른쪽 시프트

int a = 5;  // 0101
int b = 3;  // 0011

printf("a & b: %d\n", a & b); // 1 (0001)
printf("a | b: %d\n", a | b); // 7 (0111)
printf("a ^ b: %d\n", a ^ b); // 6 (0110)
printf("~a: %d\n", ~a); // -6 (..1010)
printf("a << 1: %d\n", a << 1); // 10 (1010)
printf("a >> 1: %d\n", a >> 1); // 2 (0010)
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

int a = 10;

a += 5;  // a = a + 5
printf("a += 5: %d\n", a); // 15

a -= 3;  // a = a - 3
printf("a -= 3: %d\n", a); // 12

a *= 2;  // a = a * 2
printf("a *= 2: %d\n", a); // 24

a /= 4;  // a = a / 4
printf("a /= 4: %d\n", a); // 6

a %= 3;  // a = a % 3
printf("a %%= 3: %d\n", a); // 0
6. 증감 연산자 (Increment and Decrement Operators)
증감 연산자는 변수의 값을 1만큼 증가하거나 감소시킵니다.

++ : 증가 연산자
-- : 감소 연산자
증감 연산자는 전위(pre)와 후위(post) 두 가지 형태로 사용될 수 있습니다.


int a = 10;
int b = 10;

printf("++a: %d\n", ++a); // 전위 증가: 11
printf("b++: %d\n", b++); // 후위 증가: 10 (먼저 b의 값을 사용한 후 증가)
printf("b: %d\n", b); // 증가된 b의 값: 11

a = 10;
b = 10;

printf("--a: %d\n", --a); // 전위 감소: 9
printf("b--: %d\n", b--); // 후위 감소: 10 (먼저 b의 값을 사용한 후 감소)
printf("b: %d\n", b); // 감소된 b의 값: 9
7. 조건부 연산자 (Conditional Operator) 또는 삼항 연산자 (Ternary Operator)
조건식의 결과에 따라 값을 반환합니다.

? :

int a = 10;
int b = 20;
int max = (a > b) ? a : b;  // a와 b 중 큰 값을 max에 대입
printf("max: %d\n", max); // 20
8. 콤마 연산자 (Comma Operator)
콤마 연산자는 두 개 이상의 표현식을 나열하여 순차적으로 실행되게 합니다. 마지막 표현식의 값이 전체 표현식의 값이 됩니다.


int a, b, c;
a = (b = 3, c = b + 2); // b는 3이 되고, c는 b+2로 5가 되며, a는 5가 됨
printf("a: %d, b: %d, c: %d\n", a, b, c); // 5, 3, 5
9. 주소 및 간접 참조 연산자 (Address and Indirection Operators)
주소 연산자는 변수의 주소를, 간접 참조 연산자는 포인터가 가리키는 값을 얻습니다.

& : 주소 연산자
* : 간접 참조 연산자

int a = 10;
int *p = &a; // p는 a의 주소를 가리킴

printf("a의 주소: %p\n", (void*)&a); // a의 주소 출력
printf("p가 가리키는 값: %d\n", *p); // p가 가리키는 값, 즉 a의 값 출력
10. 기타 연산자 (Miscellaneous Operators)
기타 다양한 연산자가 존재합니다.

sizeof 연산자
변수나 데이터 타입의 크기를 바이트 단위로 반환합니다.


int a = 10;
printf("int의 크기: %zu 바이트\n", sizeof(int)); // int의 크기 출력
printf("a의 크기: %zu 바이트\n", sizeof(a)); // a의 크기 출력
형 변환 연산자 (Type Cast Operator)
변수나 값을 특정 타입으로 변환합니다.


double pi = 3.14159;
int truncatedPi = (int)pi; // pi를 정수형으로 변환
printf("truncatedPi: %d\n", truncatedPi); // 3
