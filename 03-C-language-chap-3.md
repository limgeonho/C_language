# [C_language_chap_3]

## 1. 데이터와 자료형

- 메모리를 효율적으로 사용하기 위해 나눠져 있음
- 문자(char)도 정수(int)에 포함

![데이터와자료형](https://user-images.githubusercontent.com/73927750/129585103-dff8c0f8-eca6-4cb3-9742-9dff117d0f21.png)



## 2. Variable and Constant

```c
  const int angle = 1004;
  // const : qualifier 한정자
  // int : data type 자료형
  // symbolic constant 변수
  // literal constant 리터럴 상수
```



## 3. scanf()함수의 기본적인 사용법 => 사용자의 입력을 받아옴

```c
int i = 0;
  
scanf("%d", &i); // 중요! &(ampersand)를 통해 i의 주소를 넘겨줌
```



## 4. printf format specifier

| Format Specifier | Type                          |
| ---------------- | ----------------------------- |
| %c               | Character                     |
| %d               | Signed integer                |
| %e or %E         | Scientific notation of floats |
| %f               | Float values                  |
| %g or %G         | Similar as %e or %E           |
| %hi              | Signed integer (short)        |
| %hu              | Unsigned Integer (short)      |
| %i               | Unsigned integer              |
| %l or %ld or %li | Long                          |
| %lf              | Double                        |
| %Lf              | Long double                   |
| %lu              | Unsigned int or unsigned long |
| %lli or %lld     | Long long                     |
| %llu             | Unsigned long long            |
| %o               | Octal representation          |
| %p               | Pointer                       |
| %s               | String                        |
| %u               | Unsigned int                  |
| %x or %X         | Hexadecimal representation    |
| %n               | Prints nothing                |
| %%               | Prints % character            |

## 

## 5. Integer and Real-numbers(정수와 실수)

- floating point 표현법 사용(부동소수점)
- Sign, Exponent, Fraction
  - Sign : 부호를 의미
  - Exponent : 지수 부분
  - Fraction : 분수 부분
- E = 10으로 생각하고 E1 = 10, E0 = 1, E-1 = 1/10
- 32bit single precision
  => float
- 64bit double precision
  => double

![정수와실수](https://user-images.githubusercontent.com/73927750/129587183-cde9d6d0-82bd-4141-bb78-c765a9024e04.png)



## 6. 정수의 overflow와 underflow

- 정수의 범위를 넘어가면 나타나는 현상

![언더플로우](https://user-images.githubusercontent.com/73927750/129587321-4eabf7c3-19cb-4583-89ad-4ea8ff1c17c6.png)



## 7. 2진수와 8진수와 16진수

- 2진수(Binary) : 숫자 앞에 0b를 표기
- 8진수(Octal) : 숫자 앞에 0을 표기하며, 출력시 format specifier로 %o를 사용
- 16진수(Hexadecimal) : 숫자 앞에 0x를 표기하며, 출력시 format specifier로 %x를 사용



## 8. Fixed-width-integers(고정 너비 정수형)

```c
#include <stdio.h>
#include <stdint.h>    // 크기별로 정수 자료형이 정의된 헤더 파일

int main()
{
    int8_t num1 = -128;                    // 8비트(1바이트) 크기의 부호 있는 정수형 변수 선언
    int16_t num2 = 32767;                  // 16비트(2바이트) 크기의 부호 있는 정수형 변수 선언 
    int32_t num3 = 2147483647;             // 32비트(4바이트) 크기의 부호 있는 정수형 변수 선언
    int64_t num4 = 9223372036854775807;    // 64비트(8바이트) 크기의 부호 있는 정수형 변수 선언

    // int8_t, int16_t, int32_t는 %d로 출력하고 int64_t는 %lld로 출력
    printf("%d %d %d %lld\n", num1, num2, num3, num4); // -128 32767 2147483647 9223372036854775807

    uint8_t num5 = 255;                      // 8비트(1바이트) 크기의 부호 없는 정수형 변수 선언
    uint16_t num6 = 65535;                   // 16비트(2바이트) 크기의 부호 없는 정수형 변수 선언
    uint32_t num7 = 4294967295;              // 32비트(4바이트) 크기의 부호 없는 정수형 변수 선언
    uint64_t num8 = 18446744073709551615;    // 64비트(8바이트) 크기의 부호 없는 정수형 변수 선언

    // uint8_t, uint16_t, uint32_t는 %u로 출력하고 uint64_t는 %llu로 출력
    printf("%u %u %u %llu\n", num5, num6, num7, num8); // 255 65535 4294967295 18446744073709551615

    return 0;
}
```



## 9. Character(문자형)

- 문자도 사실 2진수로 표기해서 처리함
- ASCII(American Standard Code for Information Interchange)

![아스키](https://user-images.githubusercontent.com/73927750/129589833-20095275-2794-43ce-ba2f-db4b7b2f176b.png)



## 10. Floating-point types(부동소수점)

![부동소수점](https://user-images.githubusercontent.com/73927750/129590649-6e4815ac-0775-4863-8d28-7c22ed6fa949.png)

![부동소수점2](https://user-images.githubusercontent.com/73927750/129590739-cc76b536-f741-4a72-8044-7fc1cb481fb8.png)



## 11. Limit of floating-point types

- round-off errors
- overflow
- underflow



## 12. Boolean types

- True False
- true = 1, false = 0
- bool로 선언
- #include <stdbool.h>
- 내부는 정수형
- 크기는 1byte(메모리의 주소를 배정 받을 수 있는 가장 작은 단위가 1byte라서)
- 컴퓨터는 false가 아닌 것은 모두 true로 처리



## 13. Complex types

- #include <complex.h>
- double _Complex z = 1 + 2*I;
- creal(z) => 실수
- cimag(z) => 허수