<div align="center">

```
   ___  ___  _   _  ___   ___  ____   _ _____ 
  |_  |/ _ \| | | |/ _ \  |  \/  | | | /  __ \
    | / /_\ \ | | / /_\ \ | .  . | | | | /  \/
    | |  _  | | | |  _  | | |\/| | | | | |    
/\__/ / | | \ \_/ / | | | | |  | \ \_/ / \__/\
\____/\_| |_/\___/\_| |_/ \_|  |_/\___/ \____/
```

`[ servlet login/register skeleton :: MySQL :: parameterized queries ]`

![java](https://img.shields.io/badge/JAVA-ff00c8?style=for-the-badge&logo=openjdk&logoColor=00fff9&labelColor=0a0014)
![mysql](https://img.shields.io/badge/MYSQL-00fff9?style=for-the-badge&logo=mysql&logoColor=0a0014&labelColor=0a0014)
![status](https://img.shields.io/badge/STATUS-COURSEWORK-ff00c8?style=for-the-badge&labelColor=0a0014)

</div>

<br>

```
▓▒░ 0x00 // SITREP ░▒▓
```

Minimal MVC skeleton demonstrating a servlet → DAO → MySQL flow for login and registration —
two verticals (`com.login`, `com.register`), each split into `Servlet` / `bean` / `dao` / `conn`.

<br>

```
▓▒░ 0x01 // FLOW ░▒▓
```

```
Login.html / Register.html
        │  POST
        ▼
LoginServlet / RegisterServlet  ──▶  LoginBean / RegisterBean
        │
        ▼
LoginDao.vaildate() / RegisterDao.Regiterindb()   (PreparedStatement, no string-built SQL)
        │
        ▼
     MySQL  (user_register table)
```

`LoginServlet` checks credentials against `user_register` and redirects to `Welcome.html` on
success or bounces back to `Login.html` on failure. `RegisterServlet` inserts a new row and
forwards to `index.html`. `web.xml` pins a `CONFIDENTIAL` transport-guarantee across `/*`, so
the container refuses plain HTTP.

<br>

```
▓▒░ 0x02 // RUN IT ░▒▓
```

```console
root@node:~/Java_MVC# # point WEB-INF/lib/mysql-connector-java-8.0.29.jar's target DB at a
root@node:~/Java_MVC# # `user_register` table, then deploy the WAR to a servlet container
root@node:~/Java_MVC# # (Tomcat/Jetty) that terminates HTTPS.
```

