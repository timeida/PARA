# PARA
#### 우분투에 파이썬 3.10 설치



Index
---
* 개요
* 개발 환경 설정

* 참고자료



개요
---
우분투 22.04.6


개발 환경 설정
---
우분투 설치 후 setting에서 지역을 캐나다로 바꿔야 Therminal이 열린다.
하지만 권한이 없다. 따라서 관리자 권한을 주기 위해 다음 코드들을 터미널에 복붙한다.
>su
>
>visudo -f /etc/sudoers
>

그럼 다음과 같은 코드를 찾을 수 있을 것이다.
>root    ALL=(ALL:ALL) ALL
>
위의 코드를 아래 코드로 바꾼다. 이때 '유저'는 오라클에서 초기 설정한 유저명이다.
>"유저"    ALL=(ALL:ALL) ALL


---
>sudo apt-get update
>
>sudo apt-get upgrade
>
>sudo apt-get install python3-pip
>
distutils, pip 설치
>sudo apt install --reinstall python3-distutils
>
>sudo apt install --reinstall python3-pip
>
ultralytics 설치
>pip install ultralytics
>




참고자료
---
https://sheepbelldoor.tistory.com/entry/Linux-PPA-Ubuntu-2004%EC%97%90%EC%84%9C-%ED%8C%8C%EC%9D%B4%EC%8D%AC-310-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0

https://gist.github.com/rutcreate/c0041e842f858ceb455b748809763ddb

