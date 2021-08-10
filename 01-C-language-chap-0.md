# [C_language_chap_0]

## 1. 컴퓨터의 구성 요소

- User, Input device, Computer, Ouput device

- ### Hardware

  - Mainboard
    - Power supply - 전원공급
    - Primary memory(RAM, ROM) - 주기억장치 - 전원을 끄면 데이터가 삭제됨
      - RAM(Random Access Memory)
        - Volatile type of memory
        - Random access
    - Secondary memory(HDD, SSD) - 보조기억장치 - 전원을 꺼도 데이터가 남아 있음
      - HDD(Hard Disk Drive)
      - SSD(Solid State Drive)
      - FDD(Floppy Disk Drive)
      - Magnetic Tape
    - CPU(Central Processing Unit) - 중앙처리장치
    - Graphics card - 그래픽카드 - 내부적으로 CPU를 가지고 있음 = GPU
      - GPU(Graphics Processing Unit)
        - memory와 CPU 포함
    - Display
    - Input-Output Units

  ### Software

  

## 2. 컴퓨터를 킬 때 일어나는 일

### 부팅 절차

1. 전원 공급
2. 부트 프로그램 실행(ROM BIOS : 운영체제 중 가장 기본적인 소프트웨어이자 컴퓨터의 입출력을 처리하는 펌웨어)
3. 하드웨어 검사
4. 운영체제 로드 : 운영체제는 보조기억 장치에 설치 됌, 컴퓨터 실행 시 보조기억장치에서 주기억장치로 로드
5. 운영체제 실행

- 부팅은 주기억장치가 보조기억장치에 있는 운영체제 프로그램을 복사해 와서 CPU와 통신하면서 실행



## 3. 운영체제가 해주는 일들

- 자원 관리

  - 메모리 관리
  - 프로세스 관리
  - 주변장치 관리
  - 파일 관리

- 시스템 관리

  - 시스템 보호
  - 네트워킹
  - 명령 해석기

  

## 4. CPU의 기본 구조

### 언어 단계

- High level programming language
- Assembly language
- Machine code(CPU의 사용언어)

### CPU의 구성 요소

- Control Unit

- ALU(Arithmetic Logic Unit)

- Registers

  - PC(Program Counter) : 다음 명령어의 메모리 주소 저장
  - Accumulator : 연산에 사용되는 데이터 저장
  - IR(Instruction Register) : 메모리에서 읽어온 명령어 저장
  - Status Register : 현재 CPU의 상태를 저장
  - MAR(Memory Address Register) : 읽거나 쓴 메모리주소 저장
  - MBR(Memory Buffer Register) : 메모리에서 읽어온 데이터 저장

  

## 5. 정보의 단위

- 데이터 => 처리과정 => 정보
- 비트(Bit: Binary digit) : 정보의 기본 단위
- 1바이트(byte) = 8bit : 메모리 주소의 기본 단위
- 16bit, 32bit = word : CPU가 데이터를 다루는 기본 단위(레지스터의 크기).



## 6. 2진수

- 2의 보수 정수 표현법에서 -0과 0은 같다
- signed와 unsigned의 차이 : 숫자의 범위



## 7. 기타

- 컴퓨터가 이진법을 사용한 이유

  => 처음에는 진공관으로 on/off => 트랜지스터 => 트랜지스터를 압축해서 배열

- 캐쉬메모리

  => 자주 사용하는 부분은 저장해 놓고 빠르게 꺼내 쓰는 메모리

- 메모리는 - 순차 접근(순차적으로), 임의 접근(주소를 가지고 바로바로)으로 나눠진다.
  => CPU와 address bus, control bus, data bus로 통신
  => 임의 접근(random access)을 하기 위해서 사실 pointer가 존재
  => 속도가 향상
  => 하드웨어에 대해 좀 더 세밀한 조작이 가능

