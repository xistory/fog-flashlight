## Part 01 하드웨어 ##

### Chapter 01 라즈베리 파이 구조 및 개발환경 만들기 ###

#### Section 01 라즈베리 파이의 구조와 기본적으로 필요한 주변 아이템 ####

01 필요한 아이템들과 도구들

02 라즈베리 파이 전용 주변장치들

#### Section 02 라즈베리 파이에 사용된 중앙처리 장치 (ARM 프로세서) ####

#### Section 03 라즈베리 파이의 운영체제 (라즈비언) 설치 ####

01 라즈베리 파이 하드웨어 연결 및 운영체제 설치

02 라즈비언 최초 부팅 및 윈도우 타입 운영체제 실행

### Chapter 02 입출력 포트 구조 및 특징 ###

#### Section 01 라즈베리 파이 입출력 포트들 ####

01 USB

02 LAN

03 CSI 헤더

04 HDMI포트

05 전원부

06 DSI 헤더

07 SD카드 슬롯

08 GPIO 헤더

09 아날로그 비디오 출력

10 오디오 출력

11 JTAG 포트

12 LED

#### Section 02 일반 입출력 포트 [(General Purpose Input Output)](GPIO.md) ####

### Chapter 03 센서 종류와 연결법 ###

#### Section 01 센서란 무엇인가? ####

01 정밀도(Precision)와 정확도(Accuracy)

02 해상도(Resolution)

03 센서 값의 보정(Calibration)

#### Section 02 센서출력 값을 읽는 방법 ####

01 I2C방식 센서의 연결

02 ADC 칩과 센서의 연결

#### Section 03 센서의 종류 ####

01 온도 센서

02 가속도 센서 (Accelerometer)

03 초음파 센서를 이용한 거리 측정

04 근거리 장애물 인지 센서

05 적외선을 이용한 움직임 인지 센서 (PIR)

06 가스 센서

07 먼지 센서

08 물리적 힘 인지 센서 (Strain Gauge)

09 빛을 인지 하는 CDS

10 회전 센서

11 터치 센서 (터치 스위치)

12 전류 소비 측정 센서

13 호올 효과 (Hall Effect) 측정 센서

#### Section 04 기본 전자 회로 지식 ####

01 저항 (Ω)

02 캐패시터 (F)

03 인덕터 (H)

04 다이오드

05 트랜지스터

06 트랜스포머

07 직접 회로 (Integrated Circuit, IC)

### Chapter 04 직렬 통신과 사용법 ###

#### Section 01 직렬 통신이란 무엇인가? ####

#### Section 02 UART와 MAX3232 ####

#### Section 03 회로 구현 ####

01 RS-232를 통한 직렬 통신

02 USB 를 통산 직렬 통신

03 라즈베리 파이에서 직접 직렬 통신

#### Section 04 간단한 UART 통신하기 ####

#### Section 05 Serial Peripheral Interface (SPI) ####

## Part 02 소프트웨어 ##

### Chapter 01 간단한 리눅스 명령어 및 리눅스 시스템 구성 ###

#### Section 01 리눅스란 무엇인가? ####

#### Section 02 커맨드 라인에서 리눅스 알아보기 ####

01 /bin과 /sbin에 있는 필수적인 명령어

02 리눅스 파일 시스템과 간단한 명령어 알아 보기

### Chapter 02 파이선 기본 ###

#### Section 01 파이선 기본 설정 및 Hello World ####

#### Section 02 일반 컴퓨터에서 파이선 실행하기 ####

#### Section 03 파이선 기본 문법 ####

01 연산

02 변수 (Variable)

03 반복문 (For Loop)

04 while

05 조건문 If와 비교

06 리스트 (list)

07 함수 (Function)

08 다중 할당 (Multiple Assignment), 다중 리턴 값 (Multiple Return Values)

09 예외 (Exception)

#### Section 04 파이선의 객체지향 프로그래밍 ####

#### Section 05 파일 관리 ####

01 파일 읽기

02 파일 쓰기

#### Section 06 인터넷 (Internet) ####

#### Section 07 GUI ####

01 Tkinter

### Chapter 03 입출력 포트 제어 및 직렬 포트 프로그래밍 ###

#### Section 01 GPIO 사용하기 ####

01 핀 번호 매기기

02 채널 설정하기

03 GPIO 입력

04 GPIO 출력

05 리소스 비우기

#### Section 02 I2C사용하기 ####

#### Section 03 온도 센서 사용하기 ####

#### Section 04 PWM 사용하기 ####

#### Section 05 PWM을 사용하여 서보 모터 제어하기 ####

#### Section 06 스텝 모터 제어하기 ####

#### Section 07 ADC 모듈 사용하기 ####

#### Section 08 릴레이 스위치 제어하기 ####

01 릴레이 스위치를 이용하여 전구 스탠드 제어

#### Section 09 LCD 문자열 출력하기 ####

### Chapter 04 인터넷 연결 - 사물 인터넷 (Internet of Things) ###

#### Section 01 Internet of Things (IoT) 란 무엇인가? ####

#### Section 02 Xively 사용법 ####

#### Section 03 Xively와 라즈베리 파이 연결 ####

01 장치 등록하기

02 장치 등록하기 위한 라즈베리 파이 설정

03 파이선 프로그램 환경설정

04 간단한 프로그램 작성

05 Xively 웹페이지에서 데이터 확인하기

#### Section 04 Xively 를 이용한 IOT 구현하기 ####

01 개발 단계

02 The Developer Workbench 세부 사항

03 데이터 읽고 쓰기

#### Section 05 Xively와 통신하기 ####

01 HTTPS

02 Sockets

03 요청 문법

04 MQTT

05 데이터 포맷

### Chapter 05 스마트 홈 구현 ###

#### Section 01라즈베리 파이의 각 모듈 프로그램 통합하기 ####

#### Section 02 라즈베리 파이의 센서 값을 Xively와 연결하기 ####

#### Section 03 iPad와 iPhone에서 온도센서 값 확인하기 ####

#### Section 04 안드로이드 스마트 폰과 Xively 연결 ####

01 안드로이드 개발 환경 구축

02 Xively 안드로이드 라이브러리