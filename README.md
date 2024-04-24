```
public class Ex_print {
    public static void main(String[] args) {
        //주석 : 컴퓨터에서 컴파일을 할 시 인식하지 못하는 코드
        //주석을 사용하는 이유
        //1. 코드에 설명이 필요할 때
        //2. 협업을 할 때 남에게 내 코드를 보여주기 위해서
        //3. 지금 당장은 사용하지 않을 코드라서 실행하고 싶지 않을때
        // 한줄 주석 : //
        // 여러줄 주석 : /**/
        // 주석 단축키 : ctrl + /
        //sysout -> ctrl + space
        System.out.println("hello world");//hello world를 출력하는 코드
        System.out.println(100);
        System.out.println(100+50);
        
        //문장뒤에 숫자를 더하면 숫자가 붙어서 나온다.
        System.out.println("안녕하세요" + 10);
        
        //쌍따옴표 안에 있는 것들은 숫자 일지라도 글자 취급을 합니다.
        System.out.println("2 + 2="+ 2+2);
        System.out.println("2 + 2="+ (2+2));
        
        //숫자 뒤에 붙는 문장은 문장의 특징을 갖고 그냥 붙는다 
        System.out.println(5+10+":"+(5+10));

    }
}
```

```
public class Ex_valueType {
    /*
     * 정수형 : 소수점이 없는 숫자 ( -1, 0 , 1)
     * - byte 1byte - -128 ~ 127
     * - short 2byte - -32,768 ~ 32,767
     * - int 4byte - -21억 ~ 21억 -> 일반적으로 많이쓰는 자료형
     * - long 8byte - -900경 ~ 900경 -> 금융권, 증권가
     * 
     * 문자형 : 한글자
     * - char 1byte
     * 
     * 실수형 : 소수점이 있는 숫자
     * - float 4byte
     * - double 8byte
     * 
     * 논리형 : boolen 1bit
     * */
}
```

```
public class Ex_valueType {
    public static void main(String[] args) {
        /*
         * 정수형 : 소수점이 없는 숫자 ( -1, 0 , 1)
         * - byte 1byte - -128 ~ 127
         * - short 2byte - -32,768 ~ 32,767
         * - int 4byte - -21억 ~ 21억 -> 일반적으로 많이쓰는 자료형
         * - long 8byte - -900경 ~ 900경 -> 금융권, 증권가
         * 
         * 문자형 : 한글자
         * - char 2byte
         * 
         * 실수형 : 소수점이 있는 숫자
         * - float 4byte
         * - double 8byte
         * 
         * 논리형 : boolen 1bit
         * 
         * 변수
         * 
         * 자료형 변수명; -> 변수의 선언
         * 변수명 = 데이터; -> 변수의 대입
         * 자료형 변수명 = 데이터; -> 변수의 초기화 (선언과 대입을 동시에)
         * 
         * 변수명선언 규칙
         * 
         * 1. 맨앞에 숫자가 들어가면 안된다.
         * 2. _를 제외하고 특수기호를 쓰면 안된다(~, !, @, #, $ ...)
         * 3. 이미 있는 키워드를 사용하면 안된다.(println, if,swith,for...)
         * 4. 절대로 한글로는 짓지 말 것.
         * 5. 첫글자는 소문자로 작성할 것
         * 6. 의미있는 단어로 이름을 지을 것(키 -> height, 이름 -> name
         * 숫자 -> num, number)
         * */
        
        //논리형 변수
        //논리형은 true, false 즉, 참 혹은 거짓 두가지 값만 가지고 있습니다.
        boolean b1 = true;
        
        System.out.println("b1의 값 " + b1);
        
        b1 = false;
        
        //문자형 변수
        char ch = 'A'; //문자형은 홑따옴표 안에 넣어야 하며 두글자 이상 넣을수 없습니다.
        System.out.println("ch의 값 "+ch);
        
        char ch2 = 65 + 1; //아스키코드 65 : A , 97 : a
        System.out.println("ch2의 값 "+ch2);
        
        //정수형 변수
        //byte b = 128;//byte자료형의 표현범위를 벗어나므로 오류가 난다.
        //System.out.println("b의 값 " + b);
        
        short s = 32767;
        int i = 550;
        
        System.out.println("s의 값 " + s);
        System.out.println("i의 값 " + i);
        
        //실수형 변수
        float f = 3.14f;//java에서 실수는 기본적으로 double형으로 인식하기 때문에
                       //float자료형을 사용한다는 것을 명시해줘야 합니다. (3.14f)
        double d = 3.141592;
        
        System.out.println("f의 값 "+ f);
        System.out.println("d의 값 " + d);
        
    }   
}
```
```
public class Ex1_casting {
    public static void main(String[] args) {
        //형변환(캐스팅)
        //1. 프로모션(자동형변환, 암시적 형변환)
        //- 작은 자료형에 큰 자료형을 대입하는 것(자동으로 바뀜)
        double d = 100.5; //8byte
        int n = 200; //4byte
        
        d = n;
        System.out.println("d= " + d);
        
        char ch = 'A';
        long l = 100; //8byte
        
        l = ch;
        
        System.out.println("l= " + l);
        
        //2. 디모션(강제형변환, 명시적형변환)
        //- 큰 자료형의 값을 작은 자료형에 대입하는 것(자동으로 이루어지지 않습니다.)
        char c = 'B'; //2byte
        int n1 = c + 1;
        
        c = (char)n1; //c는 2byte, n1 4byte
        System.out.println("c= " + c);
        
        float f = 5.5f; //4.xx byte
        int n2 = 0; //4byte
        
        n2 = (int)f; //실수 -> 정수로 형변환을 할 시 소수점 아래 숫자가 유실될 수 있습니다.
        System.out.println("n2= " +n2);
        
        byte b1 = 100;
        byte b2 = 20;
        //byte b3 = b1 + b2;
        int b4 = b1 + b2;
        //byte의 표현 범위가 127까지 밖에 되지 않다보니, byte끼리의 연산은 127을 넘어버릴
        //가능성이 높습니다. 이런 상황을 대비하여 java개발자들은 byte끼리의 연산이 수행될 때
        //int형으로 값을 받도록 만듦

    }
}
```
```
public class Ex1_operator {
    public static void main(String[] args) {
        //연산자
        /*
         * 1. 최고연산자:. ()
         * 2. 증감연산자 : ++ , --
         * 3. 산술연산자 : +, -, *, /, %(모듈러,나머지를 구하는 나누기)
         * 4. 시프트 연산자 : >>, <<, >>>
         * 5. 비교연산자 : <, >, <=, >=, ==, !=
         * 6. 비트연산자 : &, |, ^, ~ 
         * 7. 논리연산자 : &&, ||, !
         * 8. 조건(삼항)연산자 : ?, :
         * 9. 대입연산자 :=, +=, -=, *=, /=, %=
         * */
        
        //산술연산자 : 4칙연산과 나머지 연산자를 갖고있는 연산자
        //+, -, *, /, %
        
        int n1,n2,n3; //변수 3개를 동시에 선언
        
        n1 = 20;
        n2 = 7;
        n3 = n1 + n2;
        System.out.println("n1 + n2=" + n3);
        
        n3 = n1 - n2;
        System.out.println("n1 - n2= " + n3);
        
        n3 = n1 * n2;
        System.out.println("n1 * n2= " + n3);
        
        n3 = n1 / n2;
        System.out.println("n1 / n2= " + n3);
        
        n3 = n1 % n2;
        System.out.println("n1 % n2= " + n3);
        
        //짝수 홀수 가릴때
        //N의배수 구할 때 % N

    }
}
```
```
public class Ex2_operator {
    public static void main(String[] args) {
        //대입연산자
        // = 특정값을 변수에 전달하여 기억시킬 때 사용하는 연산자
        
        int n1 = 10; //n1이라는 int형 변수에 10이라는 정수를 대입함.
        int n2 = 7;
        
        System.out.println("=연산자 : n1 = " + n1 + ", n2= " + n2);
        
        int n3 = 5;
        int n4 = 9;
        
        System.out.println("+=연산자: n3 += n4 " + (n3+=n4));//n3 = n3 + n4;
        System.out.println("n3의 값 : " + n3);
        int n5 = 10;
        int n6 = 3;
        
        System.out.println("-=연산자: n5 -= n6 " + (n5-=n6));//n5 = n5 - n6;
        
        int n7 = 12;
        int n8 = 5;
        
        System.out.println("/=연산자: n7 /= n8 " + (n7 /= n8));//n7 = n7 / n8
        
    }

}
```
```
public class Ex3_operator {
    public static void main(String[] args) {
        //비교연산자
        //비교연산자는 변수나 상수의 값을 비교하여 참과 거짓을 판단하는 연산자
        //그러므로 결과값은 반드시 true, false로만 반환 된다.
        
        int n1 = 10;
        int n2 = 20;
        boolean result;
        result = n1 < n2;
        System.out.println("n1 < n2 : " + result);
        
        result = n1 > n2;
        System.out.println("n1 > n2 : " + result);
        
        // < : 작다
        // > : 크다
        // <=, >= 는 항상 꺽쇠가 =보다 먼저옵니다.
        // == : 같다.
        // != : 같지 않다.
        
        result = n1 == n2;
        System.out.println("n1 == n2 : " + result);
        
        result = n1 != n2;
        System.out.println("n1 != n2 : " + result);
        
        
        //논리 연산자
        //비교 연산자를 통한 연산이 2개 이상 필요할 때 사용합니다.
        int a = 5;
        int b = 10;
        
        result = a < b && a != b;
        System.out.println("&&연산자 : " + result);
        
        //&&는 and를 뜻하고
        //참 && 참 -> 참
        //참 && 거짓 -> 거짓
        //거짓 && 참 -> 거짓  앞쪽연산이 false일 때 뒤쪽연산을 수행하지 않고 넘어간다.
        //거짓 && 거짓 -> 거짓
        
        result = (a+b) < 10 && (a+=2) > 5;
        System.out.println(result);
        System.out.println("a의 값 : " + a);
        
        // ||은 or의 뜻
        // 참 || 참 -> 참
        // 참 || 거짓 -> 참
        // 거짓 || 참 -> 참
        // 거짓 || 거짓 -> 거짓
        
        result = (a += 2) > 5 || b == 5;
        System.out.println(result);
        System.out.println("a의 값 : " + a);
        
        // !
        // not의 뜻
        // true -> false
        // false -> true
        System.out.println(!result);

    }
}
```
```
public class Ex4_operator {
    public static void main(String[] args) {
        //비트 연산자
        /*
         * 논리 연산자와 유사하지만 bit단위(2진수)의 연산만 가능하다.
         * */
        //true -> 1
        //false -> 0
        
        int a = 10; //1010
        int b = 7;  //0111
        
        //1010
        //0111
        //0010 결과
        
        int c = a & b; //논리곱(and) - 2진수로 바꿨을 때 두 값이 모두 1일 때만 결과가 1 이외에는 0
        System.out.println("c : " + c);
        
        int a2 = 12; //1100
        int b2 = 8;  //1000
        
        //1100
        //1000
        //1100
        
        int c2 = a2 | b2; //논리합(or) - 2진수로 둘중 하나라도 1이면 1 나머지는 0
        System.out.println("c2 : " + c2);
        
        System.out.println("-----------------------------------------");
        
        //시프트 연산자
        //bit단위의 연산을 수행하지만 오른쪽 혹은 왼쪽으로 이동시켜 값에대한 변화를 준다.
        
        int a3 = 12; //1100
        int b3 = 2;  //0010
        
        int c3 = a3 >> b3; //a를 b만큼 오른쪽으로 이동
        System.out.println("c3 : " + c3);
        
        int d = c3 << b3; //c3를 b만큼 왼쪽으로 이동
        System.out.println("d : " + d);
        
        char ch = 'F'; //1000110
        int num = 1;
        char ch_result = (char)(ch >> num);
        System.out.println("ch_result :" + ch_result);
        
        
    }
}
```
```
public class Ex5_operator {
    public static void main(String[] args) {
        //증감연산자
        //1씩 증가시기커나, 1씩 감소시키는 연산자
        //선행증감, 후행증감
        // ++, --
        
        int a = 10;
        System.out.println("a : " + ++a);//11 선행증가 : 즉시 1 더해준다.
        System.out.println("a : " + a++);//11 후행증가 : 다음번에 사용할 때 1을 더해준다.(외상)
        System.out.println("a : " + a);//12
        
        int b = 20;
        System.out.println("b : " + --b);//19 선행 감소 : 즉시 1을 빼준다.
        System.out.println("b : " + b--);//19 후행 감소 : 다음번에 사용할 때 1을 빼준다.
        System.out.println("b : " + b);//18
        System.out.println("-----------------------------------");
        int c = 1;
        ++c;//2
        ++c;//3
        c++;//3(+1)
        ++c;//5
        c++;//5(+1)
        c++;//6(+1)
        ++c;//8
        //c의 값은?
        System.out.println("c : " + c);
        
        //삼항연산자
        //하나의 조건을 정의하여 조건이 참이경우 실행할 명령, 거짓일 경우 실행할 명령을 반환받는 연산자.
        // ? :
        int a2 = 10;
        int b2 = 15;
        boolean result; //논리형 변수 선언
        
        result = ++a2 >= b2 ? true : false;
        System.out.println("result : " + result);
        
        char result2;
        
        result2 = (a2+=1) >= b2 ? 'O' : 'X';
        System.out.println("result2 : " + result2);
        
        int result3;
    
        result3 = a2 <= b2 ? 1 : 0;
        System.out.println("result3 : " + result3);

    }
}
```
```
public class Ex6_operator {
    public static void main(String[] args) {
        int a = 10;
        int b = 12;
        //                                          a = a + b
        //++a >= b || 2 + 7 <= b && 13 - b >= 0 && (a += b) - (a % b) > 10;
        // 11 >= 12 ||  9 <= 12 && 1 >= 0 && 23 - 11 > 10
        // false || true && true && true
        // true && true && true
        // true && true
        // true
        
        /*
         * 과수원이 있다.
         * 
         * 배, 사과, 오렌지를 키우고 있는데 하루에 생산되는 양은 각각
         * 5,7,5개
         * 
         * 과수원에서 하루에 생산되는 총 개수를 출력하고
         * 시간당 전체 과일의 평균 생산 개수를 출력
         * (평균값을 담는 변수는 float으로 할 것)
         * */
        
        int pear = 5;
        int apple = 7;
        int orange = 5;
        
        int total = pear + apple + orange;
        float avg = (float)total / 24; // 정수 / 정수 -> 정수
                                // 정수 / 실수 , 실수 / 정수 -> 실수
        System.out.println("하루에 생산되는 과일의 수 : " + total + "개");
        
        System.out.println("시간당 평균 생산 개수 : " + avg + "개");
        
    }
}
```
```
public class Ex1_if {
    public static void main(String[] args) {
        /*
         * 제어문 : 프로그램의 흐름을 제어하는 문장
         * 
         * 조건문과 반복문으로 나눈다.
         * 
         * 조건문 : if, switch
         * 반복문 : while, for
         * 
         * */
        
        //if문의 구조
        /*
         * if(조건식){
         *      조건식이 참일 때 실행할 명령
         * }
         * */
        //null : 어떠한 값으로도 초기화 되지 않은 상태, 내가 만들어서 사용할 예정이다 라는걸
        //컴파일러(jvm)에게 알려주는 용도의 키워드 이다.
        int n = 50;
        String str = null;
        
        if(n > 100) {
            str = "n은 100보다 작습니다.";
        }
        System.out.println(str);
        
        
        if(n % 2 == 0) {//짝수 홀수를 판별할 때
            System.out.println(n+"은 짝수 입니다.");
        }
        
        if(n % 5 == 0) {//N의 배수를 구할 때
            System.out.println(n+"은 5의 배수입니다.");
        }
        
        
        System.out.println("-------------------------------");
        
        
        //if - else
        /*
         * if(조건식){
         *      조건식이 참일 때 실행할 명령
         * } else {
         *      조건식이 거짓일 때 실행할 명령
         * }
         * */
        
        int i = 50;
        String str2 = null;
        
        if(i > 100) {
            str = "i는 100보다 큽니다.";
        } else {
            str = "i는 100보다 작습니다.";
        }
        System.out.println(str);
        
        
        if(++i >= 50) {
            str = "i는 50이상의 수";
        } else {
            str = "i는 50미만의 수";
        }
        System.out.println(i);
        System.out.println(str);
        
        System.out.println("---------------------------------------");
        /*
         * 변수 age에 나이를 대입하고, 30세 이상이면
         * "30살 이상입니다." 라고 출력하고, 그렇지 않으면 "나이를 더 드셔야 겠네요"라고 출력하는
         * if-else문을 구현한 후 마지막으로 "감사합니다" 라는 문장을 출력해보세요.
         * */
        int age = 25;
        String str3 = null;
        if(age >= 30) {
            str3 = "30살 이상입니다.";
        } else {
            str3 = "더 드셔야 겠네요";
        }
        System.out.println(str3);
        
        
        System.out.println("감사합니다.");
        
        //위 코드를 삼항연산자로 구현하기.
        
        int age2 = 26;
        String str4 = age2 >= 30 ? "30살 이상입니다" : " 더 드셔야 겠네요";
        
        System.out.println(str4);

    }
}
```
```
public class Ex2_if {
    public static void main(String[] args) {
        //if , else if , else
        /*
         * if(조건식1){
         *  조건식1이 참일 때 실행할 명령
         * } else if(조건식2){
         *  조건식1이 거짓이고 조건식2가 참일 때 실행할 명령
         * }else if(조건식3){
         *  조건식1,2이 거짓이고 조건식3가 참일 때 실행할 명령
         * }else if(조건식4){
         *  조건식1,2,3이 거짓이고 조건식4가 참일 때 실행할 명령
         * } else {
         *  조건식1과 2가 모두 거짓일 때 실행할 명령
         * }
         * */
        
        int score = 59; //점수를 담을 변수를 70으로 초기화
        
        if(score > 100) {
            System.out.println("100이하의 점수를 입력해주세요");
        } else if(score >= 90) {
            System.out.println("성적은 A입니다.");
        } else if(score >= 80) {
            System.out.println("성적은 B입니다.");
        } else if(score >= 70) {
            System.out.println("성적은 C입니다.");
        } else if(score >= 60) {
            System.out.println("성적은 D입니다.");
        } else {
            System.out.println("성적은 F입니다.");
        }

    }
}
```
```
public class Ex1_switch {
    public static void main(String[] args) {
        //switch : 비교값과 조건값을 통해 결과를 출력하는 제어문
        /*
         * switch(비교값){
         *      case 조건값:
         *          비교값과 조건값이 일치할 때 실행할 명령
         *      break;
         *      case 조건값:
         *          비교값과 조건값이 일치할 때 실행할 명령
         *      break;
         *      case 조건값:
         *          비교값과 조건값이 일치할 때 실행할 명령
         *      break;
         * }
         * */
        // 비교값과 조건값의 타입은 일치해야 한다.
        // 조건값은 중복될 수 없다.
        
        //특정 값을 바로 찾아들어가기 때문에 if문에 비해 처리속도가 빠르다.
        int n = 3;
        
        switch(n) {
        case 1:
            System.out.println("1. 게임하기");
            break; //switch를 빠져나오는 키워드
        case 2:
            System.out.println("2. 게임소개");
            break;
        case 3:
            System.out.println("3. 종료");
            break;
        default://비교값과 조건값이 하나도 일치하는게 없을 경우 실행
            System.out.println("잘못입력하셨습니다.");
            break;
        }
        
        int score = 80;
        
        /*
         * switch(score) { case 100: System.out.println("성적은 A입니다."); break; case 99:
         * System.out.println("성적은 A입니다."); break; case 98:
         * System.out.println("성적은 A입니다."); break; case 97:
         * System.out.println("성적은 A입니다."); break; case 96:
         * System.out.println("성적은 A입니다."); break; case 95:
         * System.out.println("성적은 A입니다."); break; case 94:
         * System.out.println("성적은 A입니다."); break;
         * 
         * }
         */
        
        //if문의 경우 범위를 지정해서 제어하는 데 유리하다.

    }
}
```
```
public class Ex2_switch {
    public static void main(String[] args) {
        
        char ch = 'A';
        
        switch(ch) {
        case 'A':
            System.out.println("점수는 100~90점 사이입니다.");
            break;
        case 'B':
            System.out.println("점수는 89~80점 사이입니다.");
            break;
        case 'C':
            System.out.println("점수는 79~70점 사이입니다.");
            break;
        case 'D':
            System.out.println("점수는 69~60점 사이입니다.");
            break;
        case 'F':
            System.out.println("점수는 59점 이하입니다.");
            break;
        }
    }
}
```
```
public class Ex3_switch {
    public static void main(String[] args) {
        //switch문의 비교값으로 사용 가능한 자료형
        //1) 정수 ( byte,short,int)
        //2) 문자형(char)
        //3) 문자열(String)
        
        String str = "박";//한글자도 문자열로 표현이 가능하다.
        
        switch(str) {
        case "박":
            System.out.println("박길동");
            
        case "이":
            System.out.println("이길동");
            
        case "독고":
            System.out.println("독고길동");
        
        case "홍":
            System.out.println("홍길동");
            break;
        }
          
    }
}
```
```
public class Ex4_switch {
    public static void main(String[] args) {
        //달을 담는 정수형 변수 month를 하나 만들고
        //해당 달이 몇일까지 있는지 switch문을 이용해서 작성하세요.
        //ex) 4월 한달은 oo일 입니다. , 2월은 oo일 입니다.
        
        int month = 5;
        
        switch(month) {
        case 1: case 3: case 5: case 7:
        case 8: case 10: case 12:
            System.out.println(month + "월은 31일까지 있습니다.");
            break;
        case 2:
            System.out.println(month + "월은 28일까지 있습니다.");
            break;
        case 4: case 6: case 9: case 11:
            System.out.println(month + "월은 30일까지 있습니다.");
            break;
        }
        
        System.out.println("----------------------------------------------");
        
        //두개의 정수를 초기화 하고(숫자는 맘대로)
        //연산자(+,-,*,/) 하나를 저장하는 변수를 초기화 하고 switch문으로
        //정수를 연산하는 코드를 작성해보자.
        // 출력결과 : 5 + 7 = 12
        
        int a = 5; //초기화 : 선언 + 대입
        int b = 7;
        
        char ch = '/';
        //String str = "+";
        
        switch(ch) {
        case '+':
            System.out.println(a + "+" + b + "="+(a+b));
            break;
        case '-':
            System.out.println(a + "-" + b + "="+(a-b));
            break;
        case '*':
            System.out.println(a + "*" + b + "="+(a*b));
            break;
        case '/':
            System.out.println(a + "/" + b + "="+(a/b));
            break;
        }
    }
}
```
```
public class Ex1_single_for {
    public static void main(String[] args) {
        //제어문 : 프로그램의 흐름을 제어하는 문장
        // - 조건문 : if, switch
        // - 반복문 : while, for
        
        // for : 특정 수행문을 원하는만큼 반복하는 문장
        // for(초기식(변수); 조건식(초과,미만,이상,이하); 증감식(후행)){
        //   조건식이 참일 때 반복할 명령
        //}
        
        //1~3까지 출력하기 System.out.println(); -> 출력문 반복 작성
        
        for(int i = 0; i <= 2; i++) {
            
            System.out.println(i+1);
            
        }
        System.out.println("---------------------");
        //1~10까지 출력하는 for문 작성하기
        for(int i = 1; i <=10; i++) {
            System.out.println(i);
        }
        
        System.out.println("---------------------");
        //10부터 1까지 거꾸로 출력하는 for문 작성하기
        int number2 = 10;
        for(int i = 0; i <= 9; i++) {
            System.out.println(number2);
            number2--;
        }
        
        //1. 내가 몇번을 반복할건지 확실하게 정하기 
        //2. 지역변수(초기식 i)를 사용할 수 있으면 사용하기 (사용해도 되고 안해도 되고)
        
        System.out.println("------------------------");
        
        //1~5까지 총 합을 for문을 통해 출력하기
        int sum = 0; //총 합을 담을 변수
        
        for(int i = 1; i<=5; i++) {
            sum += i; //sum = sum + i
        }
        
        System.out.println("1~5까지의 총 합 : " + sum);
        
        System.out.println("------------------------");
        //정수형 변수 n 에 임의의 정수를 하나 대입하고
        //1~n까지 총 합을 for문을 통해 출력하기
        int n = 3;
        int total = 0; //1~n까지의 총 합을 담아줄 변수
        
        for(int i = 1; i <= n; i++) {
            total += i; //total = total + i
        }
        System.out.println("1~"+n+"까지의 합 : " + total);
        System.out.println("------------------------");
        //정수형 변수 dan 에다 2~9 사이의 정수를 받고
        //해당 구구단을 for문을 이용하여 출력하세요.
        //출력결과
        //2
        //4
        //6
        //8
        //10
        //12
        //14
        //16
        //18
        
        int dan = 5; //구구단 2~9 *연산을 8번 해야된다.
        for(int i = 2; i<=9; i++) {
            System.out.println(dan +"x"+ i+"="+(dan*i));
        }
        
        System.out.println("------------------------");
        //1~10까지 반복하는 문장에서 3의 배수만 출력하는 for문을 작성해보세요.
        //출력결과
        //3
        //6
        //9
        
        for(int i = 1; i <= 10; i++) {
            if(i % 3 == 0) {
                System.out.println(i);
            }
        }
        
        System.out.println("------------------------");
        
        //1~20까지 홀수만 출력하는 for문 작성하기
        for(int i = 1; i<=20; i++) {
            if(i % 2 !=0) {
                System.out.println(i);
            }
        }
    }
}
```
```
import java.util.Random;

public class Ex2_while {
    public static void main(String[] args) {
        //while : for문 보다는 간결한 문법을 지닌 반복문(선비교, 후처리)
        //구조
        //while(조건식){
        //  조건식이 참 일 동안 반복할 명령
        //}
        
        int num = 3; 
        
        while(num <5) {
            System.out.println('a');
            num++;
        }
        
        //while문 작성 요령
        //1. 시작값을 갖는 변수 생성하기
        //2. 몇번 반복할지 횟수를 정해준다.(조건식)
        //3. 반복문이 종료될 수 있도록 시작값에 변화를 줘야 합니다.
        
        /*
         * while(true) { System.out.println(1); }
         */
        
        System.out.println("---------------------------------------");
        
        //do - while문 : 선처리 후 비교
        //제어문 중 유일하게 마지막에 ;을 가진다.
        //구조
        //do{
        //  조건이 참일 동안 반복할 명령
        //}while(조건식);
        
        int n = 11;
        
        do {//조건이 맞지 않아도 무조건 한번은 실행을 합니다.
            System.out.println(n);
        }while(n<=10);
        
        //for vs while
        //for문은 내가 반복하고자 하는 횟수를 정확하게 알 때 사용합니다.
        //while문은 반복하고자 하는 횟수가 정확하지 않을 때도 사용합니다.
        
        System.out.println("----------------------------------------");
        
        //난수 생성하기(2~9까지의 난수)
        int random = new Random().nextInt(8) + 2;
        
        while(random != 7) {
            System.out.println(random);
            random = new Random().nextInt(8) + 2;
        }
        
    }
}
```
```
public class Ex3_multi_for {
    public static void main(String[] args) {
        //중첩 for문 : for문 안에 for문이 포함되어 있는 경우
        /*
         * for(초기식;조건식;증감식){
         *      for(초기식;조건식;증감식){
         *          조건이 참일 때 반복할 명령
         *      }//inner for
         * }//outer for
         * */
        
        //2중 for문의 경우 해결해야 할 문제가 두 개 일 때 사용합니다.
        
        //구구단
        for(int i = 2; i<=9; i++) {
            for(int j = 2; j<=9; j++) {
                System.out.println(i + "x" + j + "=" + (i*j));
            }
        }
        
        
        //1 2
        //1 2
        
        for(int i = 1; i <=2; i++) {
            for(int j = 1; j<=2; j++) {
                System.out.print(j+" ");
            }
            System.out.println();
        }
        
        // 1 1 1 1
        // 1 1 1 1
        // 1 1 1 1
        // 1 1 1 1
        
        for(int i = 0; i<4; i++) {
            for(int j = 0; j <4; j++) {
                System.out.print(1+" ");
            }
            System.out.println();
        }
        
        // A B C D
        // A B C D
        // A B C D
        // A B C D
        

        
        for(int i = 0; i <4; i++) {
            for(int j = 65; j<69; j++) {
                System.out.print((char)j+" ");
            }
            System.out.println();
        }
        System.out.println("------------------------------------");
        
        // A B C D
        // E F G H
        // I J K L
        
        char ch = 'A';
        
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j <4; j++) {
                System.out.print(ch++ +" ");
            }
            System.out.println();
        }
        
        // * * * *
        // * * * *
        // * * * *
        
        char ch2='*';
        for(int i= 0; i<3; i++) {
            for(int j =0; j<4; j++) {
                System.out.print(ch2+" ");
            }
            System.out.println();
        }
        System.out.println("------------------------------------");
        //*
        //* *
        //* * *
        //* * * *
        //* * * * *
        
        for(int i = 0; i < 5; i++) {
            for(int j = 0; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        System.out.println("------------------------------------");
        
        //        *
        //      * *
        //    * * *
        //  * * * *
        //* * * * *
        
        for(int i = 0; i <5; i++) {
            for(int j= 0; j <5 -(i+1); j++) {
                System.out.print(" ");
            }
            for(int k = 0; k<=i; k++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
```
public class Ex_printf {
    public static void main(String[] args) {
        int su1 = 10;
        int su2 = 7;
        System.out.println(su1+"+"+su2+"="+(su1+su2));
        
        //printf의 f는 format이라는 뜻을 갖고 있습니다.
        //형식문자
        //1) %d : 정수형을 입력받을 때 사용합니다.
        //2) %c : 문자형을 입력받을 때 사용합니다.
        //3) %s : 문자열을 입력받을 때 사용합니다.
        //4) %f : 실수형을 입력받을 때 사용합니다.
        
        System.out.printf("%d+%d=%d\n",su1,su2,(su1+su2));
        
        int age= 25;
        //저의 나이는 25살 입니다.
        System.out.printf("저의 나이는 %d살 입니다.\n",age);
        
        //저의 나이는 25살이고 키는 170입니다.
        System.out.printf("저의 나이는 %d살 이고 키는 %d입니다.\n",age,170);
        
        //저의 혈액형은 AB형입니다.
        System.out.printf("저의 혈액형은 %s형입니다.\n","AB");
        
        //원주율은 3.141592입니다.
        System.out.printf("원주율은 %.1f입니다.\n",3.141592);
        
        //저의 나이는 25살이고 
        //키는 170이고 
        //혈액형은 AB형입니다.
        System.out.printf("저의 나이는 %d살이고\n키는 %d이고\n혈액형은%s입니다.",age,170,"AB");
        
        
        System.out.println("------------------------------------------------");
        // 1 2  3  4
        // 5 6  7  8
        // 9 10 11 12
        
        int count = 1;
        for(int i = 0; i <3; i++) {
            for(int j = 0; j <4; j++) {
                System.out.printf("%04d ",count++);
            }
            System.out.println();
        }
        System.out.println("------------------------------------------------");
       
    }
}
```
```
public class Ex1_break {
    public static void main(String[] args) {
        //break문 : 반복문 내에서 break문을 만나게 되면 가장가까운 반복문을 빠져나갈 때 사용합니다.
        
        //1)break 문 밑에는 다른 문장이 올 수 없다.
        //2)break 문은 반복문 안에서만 사용할 수 있다.
        
        for(int i = 1; i <=2;i++) {
            for(int j = 1; j<=5; j++) {
                if(j % 2 == 0) {
                    break;
                    
                }
                System.out.printf("%d ",j);
            }
            System.out.println();
        }
    }
}
```
```
public class Ex2_break {
    public static void main(String[] args) {
        
        //while에서의 break 사용법
        
        int n = 3;
        while(true) {
            System.out.println(n);
            n++;
            
            if(n > 10) {
                break;
            }
        }
    }
}
```
```
public class Ex3_label_break {
    public static void main(String[] args) {
        //label : 특정 반복문에 이름표를 붙여 두 개 이상의 반복문을
        //제어할 수 있도록 하는 키워드
        
        //label은 항상 쌍으로 존재합니다.
        //label의 이름은 자기가 원하는대로 사용이 가능합니다.
        
        //label은 자신을 포함하고 있는 상위 개념에게만 달 수 있습니다.
        
        happy:for(int i = 1; i<=3; i++) {
            
            for(int k = 1; k<=10; k++) {
                System.out.printf("%d ",k);
            }
            
            for(int j = 1; j<=10; j++) {
                if(j % 2 == 0) {
                    break happy;
                }
                System.out.printf("%d ",j);
            }
            
            System.out.println();
        }
    }
}
```
```
public class Ex1_continue {
    public static void main(String[] args) {
        //continue문 : 반복문내에서 continue문을 만나면 가장 가까이 있는 반복문의 증감식으로 올라갑니다.
        for(int i = 1; i<=2; i++) {
            for(int j = 1; j<=5;j++) {
                if(j % 2 ==0) {
                    continue;
                }
                
                System.out.printf("%d ",j);
            }
            System.out.println();
        }
    }
}
```
```
public class Ex2_continue {
    public static void main(String[] args) {
        int n = 0;
        
        while(n < 10) {
            n++;
            if(n % 2 != 0) {
                //while문에서 continue를 만나게 되면 조건식으로 이동
                continue;
            }
            System.out.println(n);
        }
        
        System.out.println("--------------------------------------------");
        
        n = 0; //대입
        
        w:while(n < 10) {
            n++;
            
            switch(n) {
            case 1:
                System.out.println("switch문 1번 거쳐감");
                //switch문에서 break는 반복문을 빠져나가는게 아닌 switch문만 나가게 됩니다.
                break w; //label을 사용하면 내가 짝으로 지정한 반복문을 빠져나올 수 있습니다.
            case 2:
                System.out.println("switch문 2번 거쳐감");
                //switch문만 단독으로 사용했을 때는 continue를 사용할 수 없습니다.
                continue;
            }
            System.out.println(n);
        }
    }
}
```
```
import java.util.Scanner;

public class Ex1_Scanner {
    public static void main(String[] args) {
        //Scanner 클래스 : 키보드에서 값을 직접 입력받아 변수에 저장할 수 있도록 하는 클래스
        Scanner sc = new Scanner(System.in);//scanner 정의
        
        //키보드에서 int타입의 값을 입력받고 엔터를 치는 순간
        //num변수에 사용자가 입력받은 값을 대입해 준다.
//      System.out.print("정수를 입력해 주세요 : ");
//      int num = sc.nextInt();
//      System.out.println(num);
//      
//      System.out.print("문자열을 입력해 주세요 : ");
//      String str = sc.next();
//      System.out.println(str);
        
        //키보드에서 이름,나이를 입력받고 출력해보기
        
        //출력결과
        //이름 : ooo
        //나이 : oo
        
//      String name;
//      int age;
//      
//      System.out.print("이름을 입력해 주세요 : ");
//      name = sc.next();
//      System.out.print("나이를 입력해 주세요 : ");
//      age = sc.nextInt();
//      
//      System.out.printf("이름 : %s\n",name);
//      System.out.printf("나이 : %d\n",age);
        
        //키보드에서 값을 입력받고, 입력받은 수에 해당하는 구구단을 출력해보세요.
        //2~9 이외의 숫자를 입력할 시 "2~9 사이의 숫자만 입력하세요" 라고 출력하기
//      while(true) {
//          System.out.print("단을 입력해 주세요 : ");
//          int dan = sc.nextInt();
//          
//          if(dan < 2 || dan > 9) {
//              System.out.println("2~9사이의 숫자만 입력하세요");
//          } else {
//              for(int i = 1; i <=9; i++) {
//                  System.out.printf("%d X %d = %d\n", dan, i, dan*i);
//              }
//              break;
//          }
//      }
        
        //Scanner를 통해서 정수 n을 입력받는다.
        //그리고 1부터 입력받은 정수 n까지의 총합을 계산하여 그 결과를 출력하는 프로그램을 작성하세요.
        //예를들어 정수 5를 입력받으면 1 + 2 + 3+ 4 + 5 의 연산결과인 15를 출력해야 한다.
        
        //출력결과
        //총합 : 15
        System.out.print("정수를 입력해 주세요 : ");
        int n = sc.nextInt();
        int total = 0;
        for(int i = 1; i <=n; i++) {
            total += i;
        }
        System.out.printf("1부터 %d까지의 합은 %d입니다.",n,total);        
    }
}
```
```
public class Ex1_array {
    public static void main(String[] args) {
        //배열(array) : 같은 자료형끼리 데이터를 모아둔 하나의 묶음
        //데이터의 효율적인 관리를 위해서 반드시 필요합니다.
        
        //정수형 변수 -> 여러개가 필요하면 변수를 많이 만들어야 합니다.
        int su1 = 100;
        int su2 = 200;
        int su3 = 300;
        int su4 = 400;
        
        //편하게 자원들을 관리하고 제어하기 위해서는
        //다음과 같은 배열을 생성한다.
        //1) 배열 선언
        //자료형 [] 배열명;
        int[] ar;
        
        //2) 배열 생성
        ar = new int[4];
        
        //3) 배열 초기화
        int[] arr = {100,200,300,400};//초기화 시 중괄호에 넣은 데이터 개수 만큼 방이 만들어 집니다.
        
        //4) 생성 후 대입
        ar[0] = 100;
        ar[1] = 200;
        ar[2] = 300;
        ar[3] = 400;
        
        //배열의 출력
        System.out.println(ar[0]);
        System.out.println(ar[1]);
        System.out.println(ar[2]);
        System.out.println(ar[3]);
        System.out.println("----------------------");
        
        //배열의 출력2
        for(int i = 0; i<4; i++) {
            ar[i] = i+1;
            System.out.println(ar[i]);
        }
    }
}
```
```
public class Ex2_array {
    public static void main(String[] args) {
        char[] ch;
        ch = new char[4];
        //char[] ch = new char[4];
        
        ch[0] = 'J';
        ch[1] = 'A';
        ch[2] = 'V';
        ch[3] = 'A';
        //배열 내용 출력
        for(int i = 0; i <ch.length; i++) {
            System.out.printf("ch[%d] : %c\n", i, ch[i]);
        }
        
        String[] str = new String[3];
        str[0] = "hello";
        
        for(int i = 0; i<str.length; i++) {
            System.out.println(str[i]);
        }
        System.out.println(ch);//문자형 배열의 이름으로 출력시 내용이 잘 출력되는 모습을 볼 수 있다.
        System.out.println(str);//문자열 배열의 이름으로 출력시 내용이 이상하게 나오는 모습을 볼 수 있다.
    }
}
```
```
public class Ex3_array {
    public static void main(String[] args) {
        //배열 arr에 담겨있는 모든 값의 합을 출력하세요
        //결과 : oo
        
        int[] arr = {10,20,30,40,50};
        
        int total = 0;
        
        for(int i = 0; i <arr.length; i++) {
            total += arr[i];
        }
        
        System.out.printf("결과 : %d\n", total);
        
        //발생된 난수 money를 동전으로 바꾸면 각 동전이 몇개씩 필요한지
        //판단하는 코드를 작성하세요.
        //금액은 10~ 5000원까지 1의자리 숫자는 0으로 만든다.
        
        //가능한 적은 수의 동전을 사용하세요
        
        //4170
        //500원 : 8
        //100원 : 1
        //50원 : 1
        //10원 : 2
        
        //1. 10~5000원까지 난수생성 (1의 자리는 0이 되는 방법 생각하기)
        //2. 동전이 담겨있는 배열 만들기
        //3. 몫을 구하는 나누기, 나머지를 구하는 나누기를 활용
    }
}
```
```
public class Ex1_multi_array {
    public static void main(String[] args) {
        
        int test[][] = new int [2][3];
        
        test[0][0] = 100;
        test[0][1] = 200;
        test[0][2] = 300;
        
        test[1][0] = 400;
        test[1][1] = 500;
        test[1][2] = 600;
        
        //System.out.println(test[0][0]);
        
        for(int i =0; i <test.length; i++) {
            for(int j = 0; j< test[i].length; j++) {
                System.out.print(test[i][j]+ " ");
            }
            System.out.println();
        }
        
        System.out.println("--------------------------------");
        String[][] java = {{"¿µÈñ","java:90","android:100"},
                           {"Ã¶¼ö","java:100","android:80", "jsp:100"}
                          };
        
        for(int i = 0; i < java.length; i++) {
            for(int j = 0; j <java[i].length; j++) {
                System.out.print(java[i][j] + " ");
            }
            System.out.println();
        }
        System.out.println("--------------------------------");
        int num[][] = new int[2][];
        num[0] = new int[3];
        num[1] = new int[2];
        int n = 0;
        
        for(int i = 0; i<num.length; i++) {
            for(int j = 0; j <num[i].length; j++) {
                System.out.print((num[i][j]= n+=100) + " ");
            }
            System.out.println();
        }   
    }
}
```
```
public class Ex2_multi_array {
    public static void main(String[] args) {
        //아래 2차원 배열의 요소들의 총합,평균을 구하여 출력하세요
        int arr[][] = {{1,2,3,4,5},
                       {6,7,8},
                       {11},
                       {16,17,18,19}
                       };
        int count = 0;
        int total = 0;
        double avg = 0.0;
        for(int i = 0; i <arr.length; i++) {
            for(int j = 0; j <arr[i].length; j++) {
                total+= arr[i][j];
                count++;
            }
        }
        avg = total/count;
        System.out.println("총합 : " + total);
        System.out.println("평균 : " + avg);
        
        
    }
}
```
```
import java.util.Scanner;

public class Ex1_String {
    public static void main(String[] args) {
        //모든 자바 프로그램은 Class파일 형태로 이루어져있습니다.
        //대표적인 클래스 String클래스에 대해서 알아보도록 하겠습니다.
        
        //String 클래스는 두가지 특징을 갖고 있습니다.
        //1)객체 생성 방법이 두가지(암시적,명시적)
        //2)한 번 생성된 문자열의 내용은 변하지 않는다.(불변의 특징)
        
        String s1 = "abc"; //암시적 객체 생성
        String s2 = "abc";
        
        //암시적 객체 생성을 할 때 이미 앞에 같은 문자열로 생성된
        //암시적 객체가 있다면 앞서 생성된 객체의 주소를 재사용한다.
        
        //명시적 객체 생성 :거의 모든 클래스가 객체를 생성하는 법
        
        String s3 = new String("abc"); //명시적 객체 생성
        String s4 = new String("abc");
        
        //== 연산자는 기본자료형을 비교할 때는 값을 비교한다.
        //객체끼리 비교를 할 때는 주소를 비교하는 연산자로 기능이 바뀝니다.
        if(s1 == s2) {
            System.out.println("s1과 s2는 주소가 같습니다.");
        } else {
            System.out.println("s1과 s2는 주소가 다릅니다.");
        }
        System.out.println("-----------------------------------");
        if(s3 == s4) {
            System.out.println("s3과 s4는 주소가 같습니다.");
        } else {
            System.out.println("s3과 s4는 주소가 다릅니다.");
        }
        
        System.out.println("-----------------------------------");
        if(s1.equals(s2)) {
            System.out.println("s1과 s2의 내용이 같습니다.");
        } else {
            System.out.println("s1과 s2의 내용이 다릅니다.");
        }
        System.out.println("-----------------------------------");
        Scanner sc = new Scanner(System.in);
        
        System.out.print("문자열입력 : ");
        String s5 = sc.next();
        
        
        if(s5 == s1) {
            System.out.println("s5와 s1의 주소가 같습니다.");
        } else {
            System.out.println("s5와 s1의 주소가 다릅니다.");
        }
        System.out.println("-----------------------------------");
        
        //불변의 법칙
        //처음에 안녕 이라고 적힌 메모리 영역에 할당이 되는데 "하세요"가 붙는 순간
        //"안녕" 뒤에 붙는게 아닌 "안녕하세요"라고 하는 메모리를 새롭게 할당 받는다.
        //남아있는 "안녕"은 JVM의 GC가 힙영역을 돌며 사용하지 않는 쓰레기 메모리를 주워간다.
        String greet = "안녕";
        greet += "하세요";
        System.out.println(greet);
    }
}
```
```
public class Ex2_String_Method {
    public static void main(String[] args) {
        //메서드(함수)는 어떤 작업을 수행하기 위한 명령문의 집합이다.
        //메서드를 사용하는 가장큰 이유는 반복적으로 사용되는 코드를 줄이기 위해서이다.
        //자주 사용되는 내용의 코드를 메서드로 작성해두고 필요할 때마다 호출만 하면 된다.
        
        String str = "Hong Gil Dong";
        
        //length() : 문자열의 길이를 셀 때 사용하고 값을 int값으로 반환합니다.
        System.out.println("문자열의 str의 길이 : " + str.length());
        
        //indexof() : 소괄호 안에서 글자를 처음으로 만나는 위치의 index값을 받습니다.
        int index = str.indexOf('G');
        System.out.println("맨 처음 만나는 G의 위치 : " + index);
        
        index = str.indexOf("Dong");
        System.out.println("맨 처음 만나는 Dong의 위치 : " + index);
        
        //lastindexof() : 글자를 거꾸로 찾는다.
        index = str.lastIndexOf('o');
        System.out.println("마지막 문자 o의 위치 : "+index);
    
        //charAt() : 인덱스 번호를 갖고 해당 인덱스에 해당하는 글자를 가져온다.
        char c = str.charAt(4);
        System.out.println("추출한 문자 : " + c);
        
        //substring() : 출력하고 싶은 부분의 인덱스를 적어서 문자열 잘라내기
        String str2 = str.substring(0,5);//0번부터 5글자 가져와라
        System.out.println("0번째부터 5미만 인덱스 까지의 문자열 : " + str2);
        
        //equalsIgnoreCase() : 대소문자를 무시하고 알파벳이 같으면 참
        String exam = "APPLE";
        if(exam.equalsIgnoreCase("apple")) {
            System.out.println("exam은 apple입니다.");
        } else {
            System.out.println("exam은 apple이 아닙니다.");
        }
        
        //trim() : 문자열 앞 뒤의 의미없는 공백을 제거
        String id = " abc ";
        if((id.trim()).equals("abc")) {
            System.out.println("로그인 성공");
        } else {
            System.out.println("로그인 실패");
        }
        
        String number = "1";//숫자모양이긴 하지만 문자열
        System.out.println(Integer.parseInt(number) + 10);
        
        //split() : 소괄호 안에 기준으로 문자열을 분할
        String arr[] = str.split(" ");
        for(int i = 0; i <arr.length; i++) {
            System.out.printf("arr[%d] : %s\n", i, arr[i]);
        }

        //기본자료형의 wrapper 클래스
        //int -> Integer
        //char -> Character
        //boolean -> Boolean
        //byte -> Byte
        //long -> Long
        //float -> Float
        //double -> Double

    }
}
```
```
import java.util.Scanner;

public class Ex3_String {
    public static void main(String[] args) {
        //키보드에서 숫자와 특수문자를 제외한 알파벳을 무작위로 입력받습니다.
        //입력받은 문자열에서 소문자 a가 몇개 있는지 판별하는 프로그램을 작성하세요.
        //결과
        //입력 : qwerqwer
        //a의 개수 : 0
        
        Scanner sc = new Scanner(System.in);
        System.out.print("문자열을 입력해 주세요 : ");
        String rnd = sc.next();
        
        int count = 0;
        
        for(int i = 0; i <rnd.length(); i++) {
            if(rnd.charAt(i) == 'a') {
                count++;
            }
        }
        System.out.println("a의 개수 : " + count);
        
        //회문수
        //앞으로 읽어도  뒤로 읽어도 똑같이 읽히는 문자열 판별하기
        //예를들어 토마토, 기러기, 스위스 ,별똥별, 12121
        //키보드에서 입력받은 후 회문인지 아닌지 판별하는 프로그램을 구현하세요.  
    }
}
```
```
public class ComMain {
    public static void main(String[] args) {
        //클래스명  객체명 = new 클래스명();
        Computer com1 = new Computer(); //객체 생성
        
        com1.getInfo();
        
        Computer com2 = new Computer();
        com2.color = "black";
        
        com2.getInfo(); 
    }
}
```
```
public class Computer {
        //컴퓨터 대량생산의 위한 설계도를 만드는 작업
        //클래스의 구성요소
        //1) 변수
        //2) 함수
    int ssd = 1024;
    int ram = 64;
    float cpu = 5.0f;
    String color = "white";
    
    //컴퓨터의 정보를 반환할 메서드를 만들어보자
    //메서드란 어떤 작업을 수행하기 위한 명령문들의 집합
    //반복적으로 사용되는 코드를 줄이기 위해서 반드시 필요한 개념

    //메서드의 구성
    //접근제한자 반환형 메서드명(파라미터){명령}
    public void getInfo() {
        System.out.println("ssd : " + ssd + "GB");
        System.out.println("ram : " + ram + "GB");
        System.out.println("cpu : " + cpu + "Ghz");
        System.out.println("color : " + color);
        System.out.println("--------------------------");
    }
        //접근제한자
        //1. public : 모든 접근을 허용. 같은 프로젝트 내의 모든 객체들이 사용할 수 있도록 허용.
        //2. private : 현재 클래스 내에서만 사용을 허가
        //3. protected : 상속관계의 객체들에만 사용을 허가
        //4. default : 같은 패키지(폴더)내의 객체에만 사용을 허가(아무것도 쓰지 않으면 default)
        
        //반환형은 메서드가 처음부터 끝까지 수행을 마친 뒤 반환해야할 값이 있을경우 기입
        //int, String, boolean등 기본자료형을 포함하여 사용자가만든 객체로도 반환 가능
        //아무것도 반환하지 않을 때는 void
        
        //메서드명 말 그대로 함수의 이름(첫글자는 소문자로 시작한다)
    
        //파라미터는 외부에서 해당 메서드를 통해 특정 값을 전달하고자 할 때, 그 특정 값을 받아서
        //처리할 수 있도록 하는 역할

}
```
```
public class MethodMain {
    public static void main(String[] args) {
        //객체 생성
        MethodTest mt = new MethodTest();
        
        mt.test1();
        
        mt.f(2);
        
        System.out.println(mt.f2(1,2));
        
        int su = 10;
        
        mt.test(su);
        System.out.println("su : " + su);//11
        
        mt.f3();
        System.out.println(mt.f4(9,5));
    }
}
```
```
public class MethodTest {
    public void test1() {
        System.out.println("test1()메서드 호출함");
    }
    
    //f(x) = 2x + 1
    //f : 함수명
    //x : 파라미터
    //2x + 1 : 리턴값
    
    public void f(int x) {
        int total = 2*x + 1;
        System.out.println(total);
    }
    
    //두 수를 더하는 함수를 작성해보세요.
    //f(x,y) = x + y
    
    public int f2(int x, int y) {
        return x+y;
    }
    
    public void test(int n) {
        n++;
        System.out.println("n: " + n);
    }
    
    //1~5까지 총합을 출력하는 함수 만들기
    public void f3() {
        int total = 0;
        for(int i = 1; i<=5; i++) {
            total += i;
        }
        System.out.println(total);
    }
    
    //(호출할 때)두 수를 입력받아서 두 수까지의 총 합을 구하는 함수 만들기
    //5,9 -> 5+6+7+8+9
    public int f4(int x, int y) {
        int temp = 0;
        if (x > y) {
            temp = x;
            x = y;
            y = temp;
        }
        int total = 0;
        for(int i = x; i <=y; i++) {
            total += i;
        }
        return total;
    }
    
    
    //TimesTable이라고 하는 클래스를 만들고 showTable()이라고 하는 메서드를 정의한다.
    //showTable()메서드 구구단을 출력하는 코드를 작성
    //TimesTableMain클래스를 만들고 TimesTable객체를 생성하고 다음과 같은 결과를 출력하시오
    
    //Scanner를 통해 받는 값은 반드시 TimesTableMain클래스에서 하도록 한다.
    
    //출력할 단을 입력 : 5
    // 5 * 1 = 5
    // 5 * 2 = 10
    //  ...
    // 5 * 9 = 45   

}
```
```
public class TimesTable {
    public void showTable(int n) {
        for(int i = 1; i<=9; i++) {
            System.out.printf("%d x %d = %d\n",n,i,n*i);
        }
    }
}
```
```
import java.util.Scanner;

public class TimesTableMain {
    public static void main(String[] args) {
        
        TimesTable tt = new TimesTable();
        Scanner sc = new Scanner(System.in);
        System.out.println("단을 입력해주세요 : ");
        int dan = sc.nextInt();
        
        tt.showTable(dan);

    }
}
```
```
public class ComMain {
    public static void main(String[] args) {
        //클래스명  객체명 = new 클래스명();
        Computer com1 = new Computer(); //객체 생성
        com1.setBrand("apple");
        com1.getInfo();
        System.out.println(com1.getBrand());
        
        Computer com2 = new Computer();
        com2.color = "black";
        
        com2.getInfo(); 
    }
}
```
```
public class Computer {
    //setter & getter 피치못할 사정으로 수정하거나 출력해야 할 때
    //목적은 private으로 만들어진 변수의 값을 변경하거나 출력하고 싶을 때 사용하는 메서드
    
    private String brand="Samsung";
    int ssd = 1024;
    int ram = 64;
    float cpu = 5.0f;
    String color = "white";
    
    public void setBrand(String a) {//private에 있는 값을 세팅한다고 해서 setter
            brand = a;
    }
    
    public String getBrand() {//private에 있는 값을 가져온다고 해서 getter
        return brand;
    }
 
    public void getInfo() {
        System.out.println("ssd : " + ssd + "GB");
        System.out.println("ram : " + ram + "GB");
        System.out.println("cpu : " + cpu + "Ghz");
        System.out.println("color : " + color);
        System.out.println("Brand : " + brand);
        System.out.println("--------------------------");
    }
        //접근제한자
        //1. public : 모든 접근을 허용. 같은 프로젝트 내의 모든 객체들이 사용할 수 있도록 허용.
        //2. private : 현재 클래스 내에서만 사용을 허가
        //3. protected : 상속관계의 객체들에만 사용을 허가
        //4. default : 같은 패키지(폴더)내의 객체에만 사용을 허가(아무것도 쓰지 않으면 default)
        
        //반환형은 메서드가 처음부터 끝까지 수행을 마친 뒤 반환해야할 값이 있을경우 기입
        //int, String, boolean등 기본자료형을 포함하여 사용자가만든 객체로도 반환 가능
        //아무것도 반환하지 않을 때는 void
        
        //메서드명 말 그대로 함수의 이름(첫글자는 소문자로 시작한다)
    
        //파라미터는 외부에서 해당 메서드를 통해 특정 값을 전달하고자 할 때, 그 특정 값을 받아서
        //처리할 수 있도록 하는 역할

}
```
```
public class Person {
    private String name;
    private String phone;
    
    //setter&getter
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        this.name = name;
    }
    
    public String getPhone() {
        return phone;
    }
    
    public void setPhone(String phone) {
        this.phone = phone;
    }
}
```
```
public class PersonMain {
    public static void main(String[] args) {
        
        Person p1 = new Person(); //명시적 객체 생성
        
        //객체 p1을 통해 정보를 저장해보자
        p1.setName("홍길동");
        p1.setPhone("010-1111-1111");
        
        //객체 p1으로부터 getPhone,getName함수를 호출하여 반환받는 값을
        //바로 출력하는 문장
        System.out.println(p1.getPhone());
        System.out.println(p1.getName());
        
        //Updown클래스를 생성하여 1~50 사이의 난수를 발생시킨다.
        //UpdownMain 클래스를 만들고 사용자가 직접 정수를 입력하여 받는다.
        //Updown클래스에서 사용자가 입력한 숫자를 판단하여
        //발생한 난수보다 크다면 down!을 출력하고 작다면 up!을 출력
        
        //사용자가 입력한 숫자와 난수가 같을경우 프로그램을 종료시킨다.
        
        //여유가 된다면 몇회만에 마췄는지도 출력
        //정답을 맞춘 경우 프로그램의 종료는 Updown클래스가 아닌 메인클래스에서 이루어지도록 한다.

    }
}
```
```
public class Overload {
    //메서드 오버로드(오버로딩) : 메서드의 '중복정의'라고 하며 하나의 클래스 내에서 같은 이름을 가진 메서드가
    //여러개 정의되는 것
    
    //**메서드 오버로드의 규칙**
    //1)메서드의 이름은 같아야함
    //2)파라미터의 개수가 다른 경우
    //3)파라미터의 개수가 같아도 타입이 다른경우
    //4)파라미터의 개수가 같아도 순서가 다른 경우
    
    public void result() {
        System.out.println("인자가 없는 메서드");
    }
    
    public void result(int n) {
        System.out.println("정수를 인자로 받는 메서드");
    }
    
    public void result(char n) {
        System.out.println("문자를 인자로 받는 메서드");
    }
    
    public void result(int a, int b) {
        System.out.println("정수 두개를 받는 메서드");
    }
    
    public void result(String n, int a) {
        System.out.println("문자열과 정수를 인자로 받는 메서드");
    }
    
    public void result(int a, String n) {
        System.out.println("정수와 문자열을 인자로 받는 메서드");
    }
}
```
```
public class OverloadMain {
    public static void main(String[] args) {
        //객체 생성하는법
        // 클래스명  객체명 = new 클래스명();
        Overload ov = new Overload();
        ov.result();
        ov.result(10);
        ov.result('a');
        ov.result(100,200);
        ov.result("홍",100);
        ov.result(100,"홍");
        
        System.out.println();
    }
}
```
```
public class ConTest {
    //생성자 : 객체가 생성될 때 메모리 할당을 위해 호출되는 영역
    //생성자는 객체가 생성될 때 처음 딱 한번만 자동으로 호출됩니다.
    //그 뒤로는 내 마음대로 호출할 수 없습니다.
    
    //생성자의 특징
    //클래스와 이름이 완전 동일하다(앞글자가 대문자)
    //반환형이 없다.
    
    //파라미터를 받는 생성자
    public ConTest(String name) {
        System.out.println(name+"으로 초기화됨");
    }
}
```
```
public class Person {
    //나이와 이름, 전화번호를 저장하는 전산 프로그램 개발을 위한 클래스
    int age;
    String name;
    String tel;
    
    //똑같은걸 계속 만드려고 한다면 기본생성자에 값을 넣어놓는것도 좋은 방법입니다.
    public Person() {
        age = 20;
        name = "이름을 입력하세요";
        tel = "번호를 입력하세요";
    }
    
    public Person(int age, String name, String tel) {
        this.age = age;
        this.name = name;
        this.tel = tel;
    }
}
```
```
public class PersonMain {
    public static void main(String[] args) {
        
        Person p1 = new Person(40,"홍길동","010-1111-1111");
        System.out.println(p1.age);
        System.out.println(p1.name);
        System.out.println(p1.tel);

        System.out.println("--------------------------------------");
        Person p2 = new Person(30,"홍길순","010-2222-2222");
        System.out.println(p2.age);
        System.out.println(p2.name);
        System.out.println(p2.tel);
        System.out.println("--------------------------------------");
        Person p3 = new Person();
        System.out.println(p3.age);
        System.out.println(p3.name);
        System.out.println(p3.tel);
        System.out.println("--------------------------------------");
        Person p4 = new Person();
        System.out.println(p4.age);
        System.out.println(p4.name);
        System.out.println(p4.tel);
    
    }
}
```
```
public class Pen {
    int price;
    String brand = "monami";
    String color;
    
    public Pen(int price, String color) {
        this.price = price;
        this.color = color;
    }
    
    public Pen() {
        price = 1000;
        brand = "monami";
        color = "white";
    }
}
```
```
public class PenMain {
    public static void main(String[] args) {
        
        Pen p1 = new Pen(); //1000원짜리 일반 모나미펜
        Pen p2 = new Pen();
        Pen p3 = new Pen(10000,"gold");//만원짜리 금색 모나미펜
    }
}
```
```
public class MakeBread {
    //메서드를 만드는데 각기 다른 기능을 호출하는 세 개의 메서드를 오버로딩으로 만들어서
    //메인클래스에서 각각의 메서드를 호출했을 때 다음의 결과가 나오는 코드를 작성해보자.
    // 메서드 이름 : makeBread();
    
    //결과
    //첫번째 메서드 호출시
    //빵을 만들었습니다.
    
    //접근제한자 반환형 함수명(){
    // 실행하고자 하는 명령
    //}
    
    public void makeBread() {
        System.out.println("빵을 만들었습니다.");
        System.out.println("-----------------------");
    }
    
    //두번째 메서드 호출시
    //빵을 만들었습니다.
    //빵을 만들었습니다.
    //요청하신 n개의 빵을 만들었습니다.
    
    public void makeBread(int n) {
        for(int i = 0; i <n; i++) {
            System.out.println("빵을 만들었습니다.");
        }
        System.out.printf("요청하신 %d개의 빵을 만들었습니다.\n",n);
        System.out.println("-----------------------");
    }
    
    //세번째 메서드 호출시
    //oo빵을 만들었습니다.
    //oo빵을 만들었습니다.
    //oo빵을 만들었습니다.
    //oo빵을 만들었습니다.
    //oo빵을 n개 만들었습니다.
    
    public void makeBread(String n, int a) {
        for(int i = 0; i < a; i++) {
            System.out.println(n + "을 만들었습니다.");
        }
        System.out.printf("%s을 %d개 만들었습니다.\n",n,a);
        System.out.println("---------------------------------");
    }
}
```
```
public class MakeBreadMain {
    public static void main(String[] args) {
        
        MakeBread mb = new MakeBread();
        
        mb.makeBread();
        mb.makeBread(5);
        mb.makeBread("소보로빵",5);
    }
}
```
```
import java.util.Random;

public class Updown {
    int random = new Random().nextInt(50)+1;
    String result = "";
    int count = 0;
    
    public String check(int n) {
        count++;
        if(n < random) {
            System.out.println("UP!");
        } else if(n > random) {
            System.out.println("DOWN!");
        } else {
            System.out.println(count + "회 만에 정답");
            result = "SUCCESS";
        }
        return result;
    }
}
```
```
import java.util.Scanner;

public class UpdownMain {
    public static void main(String[] args) {
        
        int number;
        String check;
        Updown ud = new Updown();
        
        while(true) {
            System.out.println("숫자 입력: ");
            Scanner sc = new Scanner(System.in);
            number = sc.nextInt();
            check = ud.check(number);
            
            if(check.equals("SUCCESS")) {
                break;
            }
        } 
    }
}
```
