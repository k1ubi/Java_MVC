<div align="center">
<img src="./assets/hero.svg" width="100%"/>
</div>


```
▓▒░ 0x00 // ABOUT ░▒▓
```


Minimal Java MVC skeleton with login and register flows. Servlet-based
architecture, MySQL backend, no framework. Intended as a clean starting point
for coursework or small Java web projects.

<br>

```
▓▒░ 0x01 // STACK ░▒▓
```


| | |
|---|---|
| language | Java (Servlets) |
| database | MySQL |
| server | Apache Tomcat |
| pattern | Model-View-Controller |

<br>

```
▓▒░ 0x02 // SETUP ░▒▓
```


```bash
# 1. import schema
mysql -u root -p < schema.sql

# 2. update DB credentials in src/main/resources/db.properties

# 3. deploy WAR to Tomcat
mvn clean package
cp target/java_mvc.war $CATALINA_HOME/webapps/
```

<br>

<div align="center">

`.: . . : <[ end of transmission ]> : . :.`

</div>
