---
layout: post
title: "MySQL 설치 및 환경설정 (with Sequel Pro)"
description: "MySQL을 설치하고 이용을 위해 환경을 세팅한다."
modified: 2018-07-26
tags: [MySQL, SequelPro]
---

MySQL을 설치하고 환경설정하는 방법을 소개한다. MySQL은 DB 프로그램 중 가장 많이 쓰이는 프로그램 중 하나이다. MS-SQL과 달리 프리웨어라 개인 프로젝트 시 활용하기에 적합하다.


<br />

## MySQL 설치

MySQL의 경우, Homebrew로도 설치가 가능하나 다음 과정은 홈페이지에서 프로그램을 직접 다운받아 설치한다.
<br />
<br />
1. MySQL을 공식 홈페이지에서 다운로드한다.

   [여기](https://dev.mysql.com/downloads/mysql/)를 누르면 운영체제에 맞게 설치가 가능하다.

   <img src="/images/fulls/180726_2/01.png" class="fit image">

   <br />

   현재 나의 맥은 High Sierra ver 10.13.5이기 때문에 자동으로 위의 버전이 추천되었다. 혹시 맥 외의 운영체제라면 주황색 네모 속의 옵션으로 운영체제를 선택하고 **Download 버튼**을 누르면 된다.

   <img src="/images/fulls/180726_2/02.png" class="fit image">

   <br />

   **No thanks, just start my download.**를 눌러주면 바로 다운로드가 시작된다.


<br />
2. 설치 파일을 실행한다. Configuration 단계 전까지 순서대로 노란 사각형을 눌러준다.

   <img src="/images/fulls/180726_2/03.png" class="fit image">

   <img src="/images/fulls/180726_2/04.png" class="fit image">

   <img src="/images/fulls/180726_2/05.png" class="fit image">

   <img src="/images/fulls/180726_2/06.png" class="fit image">


<br />
3. MySQL 8.0.11 버전에서는 새로운 인증 방법을 사용할 수 있다. 이전에 MySQL 설치 시에는 지정해주는 임시 비밀번호를 꼭 기억하고 있어야만 해서 종종 재설치를 했어야 했는데 그런 불편함이 사라졌다!

   <img src="/images/fulls/180726_2/07.jpg" class="fit image">

   <br />

   Use Strong Password Encryption 옵션을 선택하고  Next를 누르면

   <img src="/images/fulls/180726_2/08.jpg" class="fit image">

   <br />

   내가 원하는 비밀번호를 입력할 수 있다. 알파벳, 숫자, 그 외의 문자를 섞어서 적어도 8자리 이상의 비밀번호를 작성해주면 된다. 설정 후에 Finish를 눌러주면,


<br />
4. MySQL 설치가 완료되었다.

   <img src="/images/fulls/180726_2/09.png" class="fit image">


<br />
5. MySQL을 터미널에서 실행해본다.

~~~
cd /usr/local/mysql/bin
sudo ./mysql -p
~~~

   위 코드를 한줄씩 입력 후 sudo 실행을 위한 내 계정 비밀번호, mysql 설치 시 설정한 비밀번호를 차례로 입력하면 다음과 같이 MySQL이 실행되는 것을 볼 수 있다.

   <img src="/images/fulls/180726_2/14.png" class="fit image">


<br />
6. MySQL의 설치가 완료되면 환경 설정에 다음과 같은 메뉴가 생긴다.

   <img src="/images/fulls/180726_2/11.png" class="fit image">

   <br />

   이를 클릭하면 다음과 같은 창이 뜬다. 초록불이 들어와 있다면 서버가 잘 돌아가고 있는 중이다.

   <img src="/images/fulls/180726_2/12.png" class="fit image">





<br />
<br />



## Sequel Pro 설치하기

MySQL을 지원하는 여러 툴이 있지만, 맥에서 사용할만한 툴으로는 Sequel Pro가 있다. 일단 **무료(!!!!)**이고 맥용 네이티브 어플리케이션으로 만들어졌기 때문에 상대적으로 (나는) 선호한다.
<br />
1. Sequel Pro를 공식 홈페이지에서 다운로드 한다.

   [여기](http://www.sequelpro.com)를 누르면 바로 들어갈 수 있다.

   <img src="/images/fulls/180726_2/15.png" class="fit image">

   <br />

   **Download 버튼**을 누르면 다음처럼 바로 다운로드가 이루어진다. *(설치에 특별한 옵션은 없다.)*

   <img src="/images/fulls/180726_2/16.png" class="fit image">




<br />
2. 설치 후 Sequel Pro를 실행시키면 다음과 같은 화면이 나온다.

   <img src="/images/fulls/180726_2/17.png" class="fit image">


<br />
3. 아래의 정보를 입력한 후 로그인(Connect)한다.

~~~
Name : 내가 작성하는 DB 이름(아무거나)
Host : localhost(=127.0.0.1)
Username : root
Password : MySQL 설치 시 설정한 비밀번호
~~~

   <img src="/images/fulls/180726_2/18.png" class="fit image">


<br />
4. 접속이 잘 되는 것을 확인할 수 있다.

   <img src="/images/fulls/180726_2/19.png" class="fit image">

<br />
   간단한 쿼리 `show databases;` 를 입력하고 오른쪽 중간의 Run Previous를 누르면 잘 실행됨을 알 수 있다.

   <img src="/images/fulls/180726_2/20.png" class="fit image">
