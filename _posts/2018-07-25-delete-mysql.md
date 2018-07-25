---
layout: post
title: "맥에서 MySQL 삭제하기"
description: "MySQL에 문제가 있어 삭제해야할 때."
modified: 2018-07-26
tags: [MySQL]
---

맥에서 MySQL 사용 시 몇가지 이유로 MySQL 완전 삭제를 해야할 경우가 있다. 그럴 때 터미널에서 다음과 같이 따라하자

<br />

1. 터미널을 실행한다.

<img src="/images/fulls/180726_1/01.jpg" class="fit image">

<br />

2. 다음 코드를 위에서부터 한줄씩 차례로 입력한다.

~~~
sudo rm /usr/local/mysql
sudo rm -rf /usr/local/mysql*
sudo rm -rf /Library/StartupItems/MySQLCOM
sudo rm -rf /Library/PreferencePanes/My*
vim /etc/hostconfig and removed the line MYSQLCOM=-YES-
rm -rf ~/Library/PreferencePanes/My*
sudo rm -rf /Library/Receipts/mysql*
sudo rm -rf /Library/Receipts/MySQL*
sudo rm -rf /var/db/receipts/com.mysql.*
~~~
<br />

3. MySQL이 삭제 되었다! 재설치가 필요하다면 [다음 포스트]()를 참고하면 된다. :-)
