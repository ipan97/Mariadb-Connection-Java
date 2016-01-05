#Config Connection Mariadb Database java 
 
Dowonload driver [Download Here](central.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/1.3.3/mariadb-java-client-1.3.3.jar) 
Download Common DBCP for connection Pooling [Download Here](central.maven.org/maven2/commons-dbcp/commons-dbcp/1.4/commons-dbcp-1.4.jar) 
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