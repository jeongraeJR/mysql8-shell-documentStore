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
/*JavaScript */
\js

/* Python */ 
\py

/* sql */
\sql
```
