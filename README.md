# Deploy-JavaSpringBoot-with-MySql-



#download maven 	apache-maven-3.6.3-bin.zip from this url : https://maven.apache.org/download.cgi

After That :
  1) open console in the root folder and write : mvn install 
  2) add app.yaml in the root file 
  3) write these instructions inside the app.yaml :
 31)runtime: java
32)env: standard
33)runtime_config:
 34) jdk: openjdk8
35)env_variables:
 36) SPRING_PROFILES_ACTIVE: "gcp,mysql"
37)handlers:
-371) url: /.*
 372) script: this field is required, but ignored
373)manual_scaling: 
 374) instances: 1
  
 4) application.propereties 
        server.port=${port:8081}			  
spring.datasource.url=jdbc:mysql://ip for sql /instance name
spring.datasource.username= username
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update

5)open console in the root folder and write : gcloud app deploy target/jar file.jar

6) in google cloud  choice and create instance  after that select connections in Authorised networks add 0.0.0.0/0 and save it 

##################################################################################################
                  
