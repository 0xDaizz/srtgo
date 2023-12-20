# SRT and KTX scheduler

- This module is designed to automate the reservation of SRT and KTX train tickets.
- Through the keyring module, the information such as username, password, departure station, and arrival station is stored on the local computer.
- After the reservation is completed, a Telegram notification will be sent.

  - Check [Bot Token 및 Chat Id 얻기](https://gabrielkim.tistory.com/entry/Telegram-Bot-Token-%EB%B0%8F-Chat-Id-%EC%96%BB%EA%B8%B0).

- Currently, only one SRT ticket can be obtained per transaction.

## Installation

```bash
git clone https://github.com/lapis42/srtgo
cd srtgo
pip install .
```

## Start

```bash
> srtgo
```

```bash
[?] 메뉴 선택 (↕:이동, Enter: 완료): SRT 예매 시작
 > SRT 예매 시작
   KTX 예매 시작
   SRT 예매 확인/취소
   KTX 예매 확인/취소
   SRT 로그인 설정
   KTX 로그인 설정
   텔레그램 설정
   나가기

[?] 출발역 선택 (↕:이동, Enter: 완료, Ctrl-C: 취소): 수서
 > 수서
   오송
   대전
   동대구
   부산
   포항

[?] 도착역 선택 (↕:이동, Enter: 완료, Ctrl-C: 취소): 동대구
   수서
   오송
   대전
 > 동대구
   부산
   포항

[?] 출발 날짜 선택 (↕:이동, Enter: 완료, Ctrl-C: 취소): 2023/12/20 Wed
 > 2023/12/20 Wed
   2023/12/21 Thu
   2023/12/22 Fri
   2023/12/23 Sat
   2023/12/24 Sun
   2023/12/25 Mon
   2023/12/26 Tue
   2023/12/27 Wed
   2023/12/28 Thu
   2023/12/29 Fri
   2023/12/30 Sat
   2023/12/31 Sun
   2024/01/01 Mon

[?] 출발 시각 선택 (↕:이동, Enter: 완료, Ctrl-C: 취소): 12
   00
   02
   04
   06
   08
   10
 > 12
   14
   16
   18
   20
   22

[?] 예약할 열차 선택 (↕:이동, Space: 선택, Enter: 완료, Ctrl-C: 취소):
 > [X] [SRT 355] 12월 20일, 수서~동대구(17:30~19:08) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 357] 12월 20일, 수서~동대구(18:00~19:34) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 359] 12월 20일, 수서~동대구(18:24~20:11) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 361] 12월 20일, 수서~동대구(18:37~20:29) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 365] 12월 20일, 수서~동대구(19:16~20:56) 특실 매진, 일반실 예약가능, 예약대기 불가능
   [X] [SRT 383] 12월 20일, 수서~동대구(19:25~21:10) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 369] 12월 20일, 수서~동대구(20:00~21:35) 특실 매진, 일반실 예약가능, 예약대기 불가능
   [ ] [SRT 371] 12월 20일, 수서~동대구(20:28~22:25) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 373] 12월 20일, 수서~동대구(21:00~22:41) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 375] 12월 20일, 수서~동대구(21:28~23:08) 특실 매진, 일반실 예약가능, 예약대기 불가능
   [ ] [SRT 377] 12월 20일, 수서~동대구(22:00~23:41) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 379] 12월 20일, 수서~동대구(22:40~00:25) 특실 매진, 일반실 매진, 예약대기 불가능

[?] 선택 유형 (↕:이동, Enter: 완료, Ctrl-C: 취소): 일반실 우선
 > 일반실 우선
   일반실만
   특실 우선
   특실만

..


🎊예매 성공!!!🎊
[SRT] 12월 20일, 수서~동대구(18:00~19:34) 36900원(1석), 구입기한 12월 20일 17:05
[2호차 2D (일반실) 어른/청소년 [36900원(600원 할인)]]


[?] 메뉴 선택 (↕:이동, Enter: 완료): SRT 예매 확인/취소
   SRT 예매 시작
   KTX 예매 시작
 > SRT 예매 확인/취소
   KTX 예매 확인/취소
   SRT 로그인 설정
   KTX 로그인 설정
   텔레그램 설정
   나가기

[?] 예약 취소 (Enter: 결정): [SRT] 12월 20일, 수서~동대구(18:00~19:34) 36900원(1석), 구입기한 12월 20일 17:05
   돌아가기
 > [SRT] 12월 20일, 수서~동대구(18:00~19:34) 36900원(1석), 구입기한 12월 20일 17:05

[?] 정말 취소하시겠습니까 (y/N): y

예약 내역이 없습니다
```

## Acknowledgment

This project is heavily dependent on [SRT](https://github.com/ryanking13/SRT) and [korail2](https://github.com/carpedm20/korail2).
