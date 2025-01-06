# PARA
#### 우분투에 파이썬 3.10 설치



Index
---
* 개요
* 개발 환경 설정

* 참고자료



개요
---
우분투 20.04.6에서 파이썬 3.10을 설치할 수 있다.
개발 환경 설정에 앞서 오라클 버츄얼박스와 우분투 20.04버전 iso파일을 설치한다.


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


Ubuntu 20.04 LTS 버전에서는 apt-get install로 python 3.8.10버전까지만 설치가 가능하다.
PPA를 이용하여 상위 버전의 python을 설치할 수 있다.

>sudo apt update
>
>sudo apt install software-properties-common -y
>

>sudo add-apt-repository ppa:deadsnakes/ppa
>

>sudo apt install python3.10 python3.10-venv python3.10-dev
>

>ls -la /usr/bin/python3
>
>sudo rm /usr/bin/python3
>
>sudo ln -s python3.10 /usr/bin/python3
>
>python3 --version
>


참고자료
---
https://sheepbelldoor.tistory.com/entry/Linux-PPA-Ubuntu-2004%EC%97%90%EC%84%9C-%ED%8C%8C%EC%9D%B4%EC%8D%AC-310-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0

https://gist.github.com/rutcreate/c0041e842f858ceb455b748809763ddb

