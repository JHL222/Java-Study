기본 자료형 (Primitive Data Types)
기본 자료형은 자바에 내장된 간단한 데이터 타입입니다. 총 8가지 기본 자료형이 있으며, 각각의 특성과 크기는 다음과 같습니다:

정수형 (Integer Types)
byte

크기: 8비트
값의 범위: -128 ~ 127
용도: 메모리 절약이 중요한 경우나 대용량 배열에서 사용
short

크기: 16비트
값의 범위: -32,768 ~ 32,767
용도: byte보다 넓은 범위가 필요할 때 사용
int

크기: 32비트
값의 범위: -2,147,483,648 ~ 2,147,483,647
용도: 기본 정수형 데이터 타입으로 가장 많이 사용
long

크기: 64비트
값의 범위: -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807
용도: 매우 큰 정수가 필요할 때 사용
실수형 (Floating-Point Types)
float

크기: 32비트
값의 범위: 1.4E-45 ~ 3.4E+38 (소수점 이하 7자리 정도의 정밀도)
용도: 부동 소수점 연산이 필요한 경우, 메모리 절약이 중요할 때 사용
double

크기: 64비트
값의 범위: 4.9E-324 ~ 1.8E+308 (소수점 이하 15자리 정도의 정밀도)
용도: 기본 실수형 데이터 타입으로 가장 많이 사용, 높은 정밀도가 필요할 때 사용
문자형 (Character Type)
char
크기: 16비트
값의 범위: 0 ~ 65,535 (유니코드 문자)
용도: 단일 문자를 저장할 때 사용
논리형 (Boolean Type)
boolean
크기: 1비트 (논리적으로는 1비트지만, 실제 메모리 사용량은 JVM에 따라 다를 수 있음)
값의 범위: true 또는 false
용도: 참(True) 또는 거짓(False) 값을 저장할 때 사용
참조 자료형 (Reference Data Types)
참조 자료형은 객체의 참조(주소)를 저장합니다. 기본적으로 배열, 클래스, 인터페이스가 참조 자료형에 포함됩니다.

클래스 (Class)

클래스는 객체를 생성하기 위한 템플릿입니다.
객체는 클래스의 인스턴스(instance)입니다.
클래스 타입 변수는 객체의 참조를 저장합니다.
인터페이스 (Interface)

인터페이스는 클래스가 구현해야 하는 메소드의 집합을 정의합니다.
인터페이스 타입 변수는 해당 인터페이스를 구현하는 객체의 참조를 저장합니다.
배열 (Array)

배열은 동일한 타입의 데이터가 순차적으로 저장되는 자료구조입니다.
배열 타입 변수는 배열 객체의 참조를 저장합니다.
예제 코드
public class DataTypeExample {
    public static void main(String[] args) {
        // 기본 자료형 변수 선언 및 초기화
        byte byteVar = 100;
        short shortVar = 10000;
        int intVar = 100000;
        long longVar = 100000L;
        float floatVar = 10.99F;
        double doubleVar = 100.99;
        char charVar = 'A';
        boolean booleanVar = true;
        
        // 참조 자료형 변수 선언 및 초기화
        String strVar = "Hello, World!";
        int[] intArray = {1, 2, 3, 4, 5};
        
        // 출력
        System.out.println("byteVar: " + byteVar);
        System.out.println("shortVar: " + shortVar);
        System.out.println("intVar: " + intVar);
        System.out.println("longVar: " + longVar);
        System.out.println("floatVar: " + floatVar);
        System.out.println("doubleVar: " + doubleVar);
        System.out.println("charVar: " + charVar);
        System.out.println("booleanVar: " + booleanVar);
        System.out.println("strVar: " + strVar);
        System.out.println("intArray[0]: " + intArray[0]);
    }
}
이 예제 코드에서는 다양한 기본 자료형과 참조 자료형 변수를 선언하고 초기화하며, 그 값을 출력합니다.
