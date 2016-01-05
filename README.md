#Config Connection Mariadb Database java #

Dowonload driver [Download Here](http://mvnrepository.com/artifact/org.mariadb.jdbc/mariadb-java-client/1.3.3) 
Download Common DBCP for connection Pooling [Download Here](http://mvnrepository.com/artifact/commons-dbcp/commons-dbcp/1.4) 
or maven :

``` xml
<dependency>
    <groupId>org.mariadb.jdbc</groupId>
    <artifactId>mariadb-java-client</artifactId>
    <version>1.3.3</version>
</dependency>
```
##Example Create Connection
``` java
private DataSource dataSource(){
	BasicDataSource dataSource=new BasicDataSource();
	dataSource.setDriverClassName("org.mariadb.jdbc.Driver");
	dataSource.setUrl("jdbc:mariadb://localhost:port:/databaseName");
	dataSource.setusername("your user name");
	dataSource.setPassword("your password");
return dataSource;
}
```