## 25. Build. Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo .jar para código fuente en Java con Gradle. Haz uso de un buildfile.




julius@julius-VirtualBox:~/EjersTema2ED/Ej25$ mkdir  miapp  &&  cd  miapp


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ gradle  init  --type  java-application


BUILD SUCCESSFUL in 1s
2 actionable tasks: 2 executed


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ rm  src/main/java/App.java  src/test/java/AppTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano  src/main/java/Main.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano  src/main/java/Aritmetica.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano  src/test/java/MainTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano  src/test/java/AritmeticaTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano  src/test/java/AritmeticaTest.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ ls


build.gradle  gradle  gradlew  gradlew.bat  settings.gradle  src


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ nano build.gradle 


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ ./gradlew  assemble


BUILD SUCCESSFUL in 3s
5 actionable tasks: 5 executed


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ cd build/classes/main  &&  java Main  &&  cd ../../..


bash: cd: build/classes/main: No existe el archivo o el directorio


julius@julius-VirtualBox:~/EjersTema2ED/Ej25/miapp$ java  -jar  build/libs/miapp.jar


Dados los números 5 y 2


La suma es 7


La resta es 3


La multiplicación es 10


La división es 2.5
