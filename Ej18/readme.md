## 18. Bibliotecas. Crea una biblioteca dinámica en C que proporcione las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente.


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ cat > aritmetica.h


int suma (int sumando1, int sumando2);


int resta  (int minuendo, int sustraendo);


int multiplicacion (int  numero1, int numero2);



float division (int dividendo, int divisor);


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ cat > aritmetica.c


int suma (int sumando1, int sumando2) {
	return (sumando1+sumando2);
}


int resta  (int minuendo, int sustraendo) {
	return (minuendo-sustraendo);
}


int multiplicacion (int  numero1, int numero2) {
	return (numero1*numero2);
}


float division (int dividendo, int divisor) {
	return (dividendo/(float)divisor);
}
julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ cat > main.c


 #include <stdio.h>
 
 
 #include "aritmetica.h"/*archivo de cabecera*/

 
 #define NUM1	5


 #define NUM2	2


int main (){


  printf ("Dados los números %d y %d\n", NUM1, NUM2);
  
  
  printf ("La suma es %d\n", suma (NUM1, NUM2));
  
  
  printf ("La resta es %d\n", resta (NUM1, NUM2));
  
  
  printf ("La multiplicación es %d\n", multiplicacion 
  
  (NUM1, NUM2));
  
  
  printf ("La división es %f\n", division (NUM1, NUM2));
  
  
  return 0;


}


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ gcc  -c  -fPIC  aritmetica.c


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ gcc  -shared  -fPIC  -o  libaritmetica.so  aritmetica.o


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ sudo cp  libaritmetica.so  /lib


[sudo] contraseña para julius: 


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ gcc  -o  main  main.c  libaritmetica.so


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ ldd  main
	linux-vdso.so.1 (0x00007ffcbb775000)
	libaritmetica.so => /lib/libaritmetica.so (0x00007f89834fc000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f898330a000)
	/lib64/ld-linux-x86-64.so.2 (0x00007f898351a000)


julius@julius-VirtualBox:~/EjersTema2ED/Ej18$ ./main


Dados los números 5 y 2


La suma es 7


La resta es 3


La multiplicación es 10


La división es 2.500000
