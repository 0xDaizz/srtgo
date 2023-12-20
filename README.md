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

```
[?] 메뉴 선택 (↕:이동, Enter: 완료): SRT 예매 시작
 > SRT 예매 시작
   KTX 예매 시작
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
   2023/12/19 Tue
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

[?] 출발 시각 선택 (↕:이동, Enter: 완료, Ctrl-C: 취소): 10
   00
   02
   04
   06
   08
 > 10
   12
   14
   16
   18
   20
   22

[?] 예약할 열차 선택 (↕:이동, Space: 선택, Enter: 완료, Ctrl-C: 취소):
 > [X] [SRT 323] 12월 20일, 수서~동대구(10:00~11:40) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 325] 12월 20일, 수서~동대구(10:30~12:17) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 327] 12월 20일, 수서~동대구(10:50~12:30) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 381] 12월 20일, 수서~동대구(12:04~13:55) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 331] 12월 20일, 수서~동대구(12:28~14:08) 특실 매진, 일반실 매진, 예약대기 불가능
   [X] [SRT 333] 12월 20일, 수서~동대구(12:50~14:34) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 335] 12월 20일, 수서~동대구(13:00~14:46) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 337] 12월 20일, 수서~동대구(13:30~15:16) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 339] 12월 20일, 수서~동대구(13:55~15:25) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 341] 12월 20일, 수서~동대구(14:30~16:10) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 343] 12월 20일, 수서~동대구(15:05~16:45) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 345] 12월 20일, 수서~동대구(15:29~17:14) 특실 매진, 일반실 매진, 예약대기 불가능
   [ ] [SRT 347] 12월 20일, 수서~동대구(15:56~17:41) 특실 매진, 일반실 매진, 예약대기 불가능
```

## Acknowledgment

This project is heavily dependent on [SRT](https://github.com/ryanking13/SRT) and [korail2](https://github.com/carpedm20/korail2).
