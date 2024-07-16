변수 선언
변수를 선언할 때는 먼저 데이터 타입을 지정하고, 그 다음에 변수명을 지정합니다. 예를 들어:


int number;
위 코드에서 int는 데이터 타입이고 number는 변수명입니다. 이 변수는 정수를 저장하는 데 사용됩니다.

기본 데이터 타입
C 언어에서는 다양한 기본 데이터 타입을 제공합니다:

정수형 (Integer Types)

int: 기본 정수형 (보통 4바이트)
short: 짧은 정수형 (보통 2바이트)
long: 긴 정수형 (보통 4바이트 또는 8바이트)
long long: 매우 긴 정수형 (보통 8바이트)
unsigned를 붙여 부호 없는 정수형으로 선언할 수 있습니다.

unsigned int positiveNumber;
실수형 (Floating-Point Types)

float: 단정밀도 부동 소수점 (보통 4바이트)
double: 배정밀도 부동 소수점 (보통 8바이트)
long double: 확장 정밀도 부동 소수점 (보통 10바이트 이상)
문자형 (Character Type)

char: 문자형 (보통 1바이트)
unsigned char를 사용하여 부호 없는 문자형으로 선언할 수 있습니다.
논리형 (Boolean Type)

C 언어는 표준 bool 타입을 포함하지 않지만, stdbool.h 헤더 파일을 포함하여 사용할 수 있습니다.

#include <stdbool.h>
bool isValid = true;
변수 초기화
변수를 선언하면서 동시에 초기화할 수 있습니다. 초기화는 변수에 처음 값을 할당하는 과정입니다.


int number = 10;
float temperature = 36.5;
char letter = 'A';
여러 변수 선언
한 줄에 여러 변수를 선언하고 초기화할 수도 있습니다.


int a = 1, b = 2, c = 3;
변수의 종류
C 언어에서는 변수의 사용 범위와 생명 주기에 따라 변수의 종류를 다음과 같이 나눌 수 있습니다:

지역 변수 (Local Variables)

함수 내부에서 선언되며, 해당 함수 내에서만 사용 가능합니다.
함수가 종료되면 메모리에서 사라집니다.

void myFunction() {
    int localVar = 10;
    // localVar는 이 함수 내에서만 사용 가능
}
전역 변수 (Global Variables)

모든 함수에서 접근할 수 있도록 함수 외부에서 선언됩니다.
프로그램이 종료될 때까지 메모리에 존재합니다.

int globalVar = 20;

void myFunction() {
    // globalVar는 모든 함수에서 접근 가능
}
정적 변수 (Static Variables)

지역 변수로 선언된 경우, 함수가 종료되어도 메모리에 유지됩니다.
전역 변수로 선언된 경우, 해당 파일 내에서만 접근 가능합니다.

void myFunction() {
    static int staticVar = 30;
    // staticVar는 함수가 호출될 때마다 초기화되지 않고 유지됨
}
레지스터 변수 (Register Variables)

CPU의 레지스터에 저장되도록 요청하는 변수입니다. 빠른 접근이 필요할 때 사용됩니다.
register 키워드를 사용하여 선언합니다.

void myFunction() {
    register int counter = 0;
    // counter는 레지스터에 저장되어 빠르게 접근 가능
}
예제 코드
다양한 변수 선언과 초기화를 포함하는 예제 코드를 살펴보겠습니다:


#include <stdio.h>
#include <stdbool.h>

// 전역 변수
int globalVar = 20;

void myFunction() {
    // 지역 변수
    int localVar = 10;
    static int staticVar = 30;
    register int counter = 0;

    // 변수 출력
    printf("localVar: %d\n", localVar);
    printf("staticVar: %d\n", staticVar);
    printf("counter: %d\n", counter);

    // 전역 변수 접근
    globalVar++;
    printf("globalVar: %d\n", globalVar);
}

int main() {
    // 기본 데이터 타입 변수 선언 및 초기화
    int number = 10;
    float temperature = 36.5;
    char letter = 'A';
    bool isValid = true;

    // 변수 출력
    printf("number: %d\n", number);
    printf("temperature: %.2f\n", temperature);
    printf("letter: %c\n", letter);
    printf("isValid: %d\n", isValid);

    // 함수 호출
    myFunction();
    myFunction();  // static 변수의 유지 확인

    return 0;
}
이 예제에서는 다양한 종류의 변수를 선언하고 초기화하며, 각각의 변수를 출력합니다. 또한, 전역 변수, 지역 변수, 정적 변수, 레지스터 변수의 사용 예시도 포함되어 있습니다.

