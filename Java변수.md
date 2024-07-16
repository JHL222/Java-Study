변수의 종류
자바에서는 변수를 크게 두 가지로 나눌 수 있습니다:

기본 자료형(Primitive Data Types)
참조 자료형(Reference Data Types)
1. 기본 자료형
기본 자료형은 자바에 내장된 자료형으로, 총 8가지가 있습니다.

정수형
byte: 8비트 정수 (-128 ~ 127)
short: 16비트 정수 (-32,768 ~ 32,767)
int: 32비트 정수 (-2,147,483,648 ~ 2,147,483,647)
long: 64비트 정수 (-9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807)
실수형
float: 32비트 부동 소수점
double: 64비트 부동 소수점
문자형
char: 16비트 유니코드 문자 (0 ~ 65,535)
논리형
boolean: true 또는 false 값을 가짐
2. 참조 자료형
참조 자료형은 객체를 참조하는 변수입니다. 자바에서는 배열, 클래스, 인터페이스 등이 참조 자료형에 속합니다.

변수 선언과 초기화
변수를 사용하려면 먼저 선언하고, 필요에 따라 초기화해야 합니다.

변수 선언
변수를 선언할 때는 자료형과 변수명을 지정합니다.

int number;  // 정수형 변수 number 선언
double price;  // 실수형 변수 price 선언
char letter;  // 문자형 변수 letter 선언
boolean isValid;  // 논리형 변수 isValid 선언
변수 초기화
변수를 선언하면서 동시에 초기화할 수 있습니다.

int number = 10;  // 정수형 변수 number 선언 및 초기화
double price = 99.99;  // 실수형 변수 price 선언 및 초기화
char letter = 'A';  // 문자형 변수 letter 선언 및 초기화
boolean isValid = true;  // 논리형 변수 isValid 선언 및 초기화
변수를 초기화하지 않고 사용하려고 하면 컴파일 에러가 발생합니다.

변수의 사용 범위(스코프)
변수의 사용 범위는 변수가 선언된 위치에 따라 달라집니다.

지역 변수(Local Variable): 메소드나 블록 내부에서 선언되며, 해당 메소드나 블록 내에서만 사용 가능합니다.
인스턴스 변수(Instance Variable): 클래스의 인스턴스(객체)가 생성될 때마다 인스턴스 변수도 함께 생성됩니다. 클래스의 메소드들 사이에서 공유할 수 있습니다.
클래스 변수(Class Variable): static 키워드를 사용하여 선언하며, 클래스 레벨에서 공유되는 변수입니다. 모든 인스턴스가 같은 값을 공유합니다.
예제
public class Example {
    // 클래스 변수
    static int classVariable = 10;

    // 인스턴스 변수
    int instanceVariable = 20;

    public void method() {
        // 지역 변수
        int localVariable = 30;

        System.out.println(localVariable);
        System.out.println(instanceVariable);
        System.out.println(classVariable);
    }

    public static void main(String[] args) {
        Example example = new Example();
        example.method();
    }
}
이 예제에서 localVariable은 method 내에서만 사용 가능하고, instanceVariable은 Example 클래스의 인스턴스에서 사용 가능하며, classVariable은 모든 인스턴스에서 공유됩니다.

