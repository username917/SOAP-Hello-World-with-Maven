# SOAP-Hello-World-with-Maven
A SOAP Service (Hello World) done with Maven

Cogs and Levers. (2015). Create a web service with Maven. Retrieved on March 14, 2022 from:https://tuttlem.github.io/2015/12/05/create-a-web-service-with-maven.html

Error log:

1. “Could not initialize class org.apache.maven.plugin.war.util.WebappStructureSerializer” (https://www.codegrepper.com/code-examples/whatever/Could+not+initialize+class+org.apache.maven.plugin.war.util.WebappStructureSerializer)

Enter the following in your POM file:

<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-war-plugin</artifactId>
            <version>3.3.1</version>
        </plugin>
    </plugins>


</build>


2. “The superclass "javax.servlet.http.HttpServlet" was not found on the Java Build Path” (https://www.codegrepper.com/code-examples/java/The+superclass+%22javax.servlet.http.HttpServlet%22+was+not+found+on+the+Java+Build+Path)

Enter the following in your POM:
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>3.1.0</version>
    <scope>provided</scope>
</dependency>

THen, update your project:

Right click on project ---> 
  Properties ---> 
  Java Build Path ---> 
  Add Library... ---> 
  Server Runtime ---> 
  Apache Tomcat ----> Finish.
  
  
3. If your HTTP content continues to create an error after updating the file, retype a character in the content and save again to get rid of the error.
  
  




