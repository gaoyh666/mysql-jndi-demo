
mysql> create database db_example; -- Creates the new database
mysql> create user 'springuser'@'%' identified by 'ThePassword'; -- Creates the user
mysql> grant all on db_example.* to 'springuser'@'%'; -- Gives all privileges to the new user on the newly created database


apache-tomcat-9.0.36/conf/context.xml

<Context>  
    <Resource name="jdbc/exampleDB"
        auth="Container"
        type="javax.sql.DataSource"
        username="springuser"
        password="ThePassword"
        driverClassName="com.mysql.jdbc.Driver"
        url="jdbc:mysql://localhost:3306/db_example"
        maxTotal="8"
        maxIdle="4"/>
</Context>



