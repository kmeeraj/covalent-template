Everytime to build the application follow these steps: <br/>
Step 1 : mvn clean install <br/>
Step 2 : cd social-vantage-server <br/>
Step 3 : mvn spring-boot:run <br/>
<br/>
For First time, you may get following error, as parent project is not yet installed:<br/>
Could not find artifact com.teradata:social-vantage-parent:pom:0.0.1-SNAPSHOT and 'parent.relativePath' points at no local POM @ line 6, column 10
<br/>
When you face the above issue, follow these steps:<br/>
Step 1: Go to pom.xml of parent folder (social-vantage-parent) remove modules as given below:<br/>
<modules><br/>
        <module>social-vantage-web-app</module><br/>
        <module>social-vantage-server</module><br/>
</modules><br/>
<br/>
Step 2: run mvn clean install<br/>
Step 3: go to web folder (social-vantage-web-app)<br/>
Step 4: run mvn clean install<br/>
Step 5: go to social-vantage-server<br/>
Step 6: run mvn clean install<br/>
Step 7: add reference of module of pom.xml of parent folder (social-vantage-parent)<br/>
  <modules><br/>
        <module>social-vantage-web-app</module><br/>
        <module>social-vantage-server</module><br/>
    </modules><br/>

Step 8: run mvn clean install
