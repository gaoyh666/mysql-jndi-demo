
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



