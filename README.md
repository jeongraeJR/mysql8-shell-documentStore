# Install MySQL Shell (Ubuntu)
https://dev.mysql.com/doc/mysql-shell/8.0/en/mysql-shell-install-linux-quick.html
```
sudo apt-get update
sudo apt-get install mysql-shell
```

## Connect MYSQL Document Store With X shell
Document Store에 대한 커넥션은 MySQL Server의 X Plugin이 핸들링하게 되는데, 이를 위해서는 X Protocol로 통신을해야한다고 한다.
(X protocol의 기본 포트번호는 33060 )

```
mysqlsh root@localhost:33060
```

## Help
```
\help
```

## Change Language Interface
*MySQL shell 에는 X DevAPI가 내장되어있다 . X DevAPI는 다음과 같은 세가지 인터페이스를 제공한다.

(Python, JavaScript, sql)
```
\js

\py

\sql
```

## Concepts
* Schema (=Database)
* Collections (=Table)


## Create Schema
JavaScript 모드에서 스키마를 만드는 법은 아직 못찾았다 (추후 알아보기..)
그래서 SQL 모드로 바꿔서 스키마를 만들어보았다.

```
\sql
create database schemaName
```

## Get Collections
* db: 기본 개체이며, 현재 스키마에서 지정된 글로벌 변수이다. 예를들어 컬렉션을 검색하기 위해서는 db 변수에 사용 가능한 메서드를 사용한다.
* 스키마를 지정하기 위해서는 \use 명령어를 사용한다.
* db.getCollections() : 스키마의 컬렉션 목록을 참조하여 가져온다.
```
\js
db
\use schemaName
db.getCollections()
```