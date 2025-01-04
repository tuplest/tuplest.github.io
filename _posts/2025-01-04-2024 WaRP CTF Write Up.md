---
title: 2024 WaRP CTF Write Up
data: 2025-01-04 11:18:07 +0900
categories: [ctf, "2024"]
tags: [ctf, warp, rev]
author: Tuple
description: 2024 WaRP CTF Write Up (rev/misc)
toc: true
use_math: true
---

## 2024 WaRP CTF

2024년 12월 27일부터 29일까지 이틀 간 진행된 경기과학고등학교 WaRP 주최의 WaRP CTF에 친구들과 함께 참여하였다. 웹하는 팀원 한 명의 버스로 어쩌다 1등까지 하게 되었는데 나는 리버싱 한 문제 풀이와 다른 팀원의 미스크 문제 풀이를 돕는 것 밖에 하지 못 했다. 출제된 리버싱 문제 중 하나를 업솔빙했지만 너무 심하게 버스 탄 것 같아서 다음에는 조금 더 분발하고자 한다.

## REV

### Obfuscation Basic 101

![image](https://github.com/user-attachments/assets/11b1319a-b254-4b52-9d9d-3fcb9cfda90a)
문제 파일을 다운로드 받은 후 ida를 통해 열면 위와 같은 엄청난 모습의 그래프 뷰를 볼 수 있다.  
자세히 보면 가장 위의 초기화 및 입력 블록 하나와 가장 아래 성공 또는 실패의 블록 두 개를 제외하면 중간의 70개의 블록이 모두 유사한 형태로 이루어져 있다는 것을 알 수 있다. (참고로 해당 문제 파일의 함수는 크기가 너무 커 ida에서는 디컴파일되지 않는다.)

![image](https://github.com/user-attachments/assets/36ed8225-9085-4f2c-abfe-99ebaf79e68f)
위는 블록 하나의 모습인데 보면 알 수 있듯이 입력받은 문자열에서 특정 인덱스를 가져오고 어떠한 값과 곱한 후 레지스터 ebx에 계속해서 더한다. 위 이미지에서는 나오지 않았지만 블록의 가장 아래를 보면 이렇게 해서 정해진 ebx가 32bit의 어떠한 값과 레지스터 r15를 xor 연산한 결과와 일치하는지 검증하는 코드가 있고 다르면 프로그램을 종료하는 것을 볼 수 있다.


### Ethereversing

## MISC

### Diary