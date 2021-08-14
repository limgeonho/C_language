# [C_language_chap_2]

## 1. 기본사항

- 변수 

  => 내가 직접 지정하지 않고 임의의 값이 할당되어도 원하는 로직에 의해 결과가 도출된다.

- 자료형

  => CPU입장에서는 서로 다른 자료형을 구별할 수 없기 때문에 미리 지정해준다.
  => 적절한 메모리 공간을 확보하기 위해서 => 성능에 영향

```c
#include <stdio.h> => 전처리기 : 컴파일 하기 직전에 실행되는 프로그램

int main(void)
{ // 스코프 영역
  // variable declaration
  int a;
  int b;
  int c;
  
  // assignment
  a = 1;
  b = 2;
  
  // operation
  c = a + b;
  
  // call or invoke
  printf("Result is %i", c);
  
  // value return
  return 0;
}
```



## 2. 변수를 선언하는 방법

```c
int main(void)
{
  // 메모리에 int를 담을 공간 확보
  // x라는 변수로 접근 가능
  int x;
  
  // 변수 x가 가리키는 공간에 값을 할당
  a = 1;

  return 0;
}

// 변수는 최대한 미리 사용할 변수들을 선언한다
// 변수 정의 규칙에 맞게 선언한다
```

- 변수명 짓는 규칙
  - 변수의 이름은 영문자(대소문자), 숫자, 언더스코어(_)로만 구성
  - 변수의 이름은 숫자로 시작될 수 없음
  - 변수의 이름 사이에는 공백을 포함할 수 없음
  - 변수의 이름으로 C언어에서 미리 정의된 키워드와 예약어는 사용할 수 없음



## 3. printf 함수

```c
#include <stdio.h>

int main(void)
{
  // 변수 선언과 동시에 값 할당
  int x = 1;
  int y = 2;
  
  int z = x + y;
  
  printf("%i + %i = %i", x, y, z);
  
  return 0;
}

// printf() => ()안에 출력내용
// == print formatted
```



## 4. 함수 만들기

```c
#include <stdio.h>

// Prototyping / Function declaration
void say_hello(void);
// => 원래는 함수의 선언이 main함수보다 위에 나와야 하지만 이렇게 선언하면 나중에 linker가 자동으로 연결해준다.

int main(void)
{
  say_hello();
  
  return 0;
}

// Function definition
void say_hello(void)
{
  printf("Hello");
  // => return타입이 void인 경우 return을 생략할 수 있다.
}
```



## 5. Debugger 사용법

- error는 syntax errors와 semantic error로 구성
  - syntax error : 문법 오류 => IDE나 컴파일러가 잡아줌
  - semantic error : 의미적 오류 => Debugger를 활용하여 해결



## 6. c파일 실행

1. gcc `<실행할 파일명.c>`.c -o `<exe파일명 지정>`
2. ./`<지정한 exe파일명>`
