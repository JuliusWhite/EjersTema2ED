## 19. Bibliotecas. Crea una biblioteca dinámica en Java que proporciona las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente.


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ mkdir aritmetica


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ cat > aritmetica/Aritmetica.java


package aritmetica;


public class Aritmetica {


  public static int suma (int sumando1, int sumando2) {
        return (sumando1+sumando2);
  }

  public static int resta  (int minuendo, int sustraendo) {
        return (minuendo-sustraendo);
   }

  public static int multiplicacion (int  numero1, int numero2) {
       return (numero1*numero2);
  }

  public static float division (int dividendo, int divisor) {
        return (dividendo/(float)divisor);
  }

}


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ javac  aritmetica/Aritmetica.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ jar  cvf  aritmetica.jar  aritmetica/*.class
manifiesto agregado
agregando: aritmetica/Aritmetica.class(entrada = 434) (salida = 265)(desinflado 38%)


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ sudo mv  aritmetica.jar  /usr/lib/jvm/java-8-openjdk-amd64/jre/lib/ext/aritm.jar
[sudo] contraseña para julius: 


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ cat > Main.java
import aritmetica.Aritmetica;


public class Main {


  private static final int NUM1 = 5;
  private static final int NUM2 = 2;


  public static void main (String[] args) {
    System.out.println ("Dados los números " + NUM1 + " y " + NUM2 );
    System.out.println ("La suma es " + Aritmetica.suma(NUM1, NUM2) );
    System.out.println ("La resta es " + Aritmetica.resta(NUM1, NUM2) );
    System.out.println ("La multiplicación es " + Aritmetica.multiplicacion(NUM1, NUM2) );
    System.out.println ("La división es " + Aritmetica.division(NUM1, NUM2) );
  }


}


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ javac Main.java


julius@julius-VirtualBox:~/EjersTema2ED/Ej19$ java Main


Dados los números 5 y 2


La suma es 7


La resta es 3


La multiplicación es 10


La división es 2.5
