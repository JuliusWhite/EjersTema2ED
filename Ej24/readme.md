## 24. Build. Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo .jar para código fuente en Java con Maven. Haz uso de un buildfile.


julius@julius-VirtualBox:~/EjersTema2ED/Ej24$ mvn  archetype:generate  -DgroupId=com.miempresa.app  -DartifactId=mi-app  -Dversion=1.0.0 \
>        -DarchetypeArtifactId=maven-archetype-quickstart  -DinteractiveMode=false


[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] >>> maven-archetype-plugin:3.2.0:generate (default-cli) > generate-sources @ standalone-pom >>>
[INFO] 
[INFO] <<< maven-archetype-plugin:3.2.0:generate (default-cli) < generate-sources @ standalone-pom <<<
[INFO] 
[INFO] 
[INFO] --- maven-archetype-plugin:3.2.0:generate (default-cli) @ standalone-pom ---
[INFO] Generating project in Batch mode
[INFO] ----------------------------------------------------------------------------
[INFO] Using following parameters for creating project from Old (1.x) Archetype: maven-archetype-quickstart:1.0
[INFO] ----------------------------------------------------------------------------
[INFO] Parameter: basedir, Value: /home/julius/EjersTema2ED/Ej24
[INFO] Parameter: package, Value: com.miempresa.app
[INFO] Parameter: groupId, Value: com.miempresa.app
[INFO] Parameter: artifactId, Value: mi-app
[INFO] Parameter: packageName, Value: com.miempresa.app
[INFO] Parameter: version, Value: 1.0.0
[INFO] project created from Old (1.x) Archetype in dir: /home/julius/EjersTema2ED/Ej24/mi-app
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  10.339 s
[INFO] Finished at: 2021-11-29T11:27:49+01:00
[INFO] ------------------------------------------------------------------------


julius@julius-VirtualBox:~/EjersTema2ED/Ej24$ 


julius@julius-VirtualBox:~/EjersTema2ED/Ej24$ cd  mi-app  &&  ls
pom.xml  src


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ cat  pom.xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.miempresa.app</groupId>
  <artifactId>mi-app</artifactId>
  <packaging>jar</packaging>
  <version>1.0.0</version>
  <name>mi-app</name>
  <url>http://maven.apache.org</url>
  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ nano  src/main/java/com/miempresa/app/App.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ nano  src/main/java/com/miempresa/app/Aritmetica.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ nano  src/test/java/com/miempresa/app/AppTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ nano  src/test/java/com/miempresa/app/AritmeticaTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ nano  pom.xml


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ mvn  compile


[INFO] Scanning for projects...
[INFO] 
[INFO] ----------------------< com.miempresa.app:mi-app >----------------------
[INFO] Building mi-app 1.0.0
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ mi-app ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/julius/EjersTema2ED/Ej24/mi-app/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ mi-app ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 2 source files to /home/julius/EjersTema2ED/Ej24/mi-app/target/classes
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  4.044 s
[INFO] Finished at: 2021-11-29T11:31:37+01:00
[INFO] ------------------------------------------------------------------------


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ mvn  package


[INFO] Scanning for projects...
[INFO] 
[INFO] ----------------------< com.miempresa.app:mi-app >----------------------
[INFO] Building mi-app 1.0.0
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ mi-app ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/julius/EjersTema2ED/Ej24/mi-app/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ mi-app ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ mi-app ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/julius/EjersTema2ED/Ej24/mi-app/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ mi-app ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 2 source files to /home/julius/EjersTema2ED/Ej24/mi-app/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ mi-app ---
[INFO] Surefire report directory: /home/julius/EjersTema2ED/Ej24/mi-app/target/surefire-reports

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running com.miempresa.app.AritmeticaTest
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.273 sec
Running com.miempresa.app.AppTest
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.001 sec

Results :

Tests run: 2, Failures: 0, Errors: 0, Skipped: 0

[INFO] 
[INFO] --- maven-jar-plugin:3.0.2:jar (default-jar) @ mi-app ---
[INFO] Building jar: /home/julius/EjersTema2ED/Ej24/mi-app/target/mi-app-1.0.0.jar
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  20.351 s
[INFO] Finished at: 2021-11-29T11:32:40+01:00
[INFO] ------------------------------------------------------------------------


julius@julius-VirtualBox:~/EjersTema2ED/Ej24/mi-app$ mvn  exec:java


[INFO] Scanning for projects...
[INFO] 
[INFO] ----------------------< com.miempresa.app:mi-app >----------------------
[INFO] Building mi-app 1.0.0
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] >>> exec-maven-plugin:1.2.1:java (default-cli) > validate @ mi-app >>>
[INFO] 
[INFO] <<< exec-maven-plugin:1.2.1:java (default-cli) < validate @ mi-app <<<
[INFO] 
[INFO] 
[INFO] --- exec-maven-plugin:1.2.1:java (default-cli) @ mi-app ---


Dados los números 5 y 2


La suma es 7


La resta es 3


La multiplicación es 10


La división es 2.5


[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.146 s
[INFO] Finished at: 2021-11-29T11:33:08+01:00
[INFO] ------------------------------------------------------------------------
