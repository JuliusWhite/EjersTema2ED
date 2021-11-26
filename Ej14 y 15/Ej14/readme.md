## 14. Lenguaje C++. Código en varios archivos. Obtener el código objeto a partir del código fuente de los 3 archivos siguientes:
//-------------


// datos.cpp


//-------------


#include <string>

  
std::string mensaje = "Hola a todos y todas";

  
  int num1 = 8;

  
  int num2 = 10;

  
  //-------------

  
  // main.cpp

  
  //-------------

  
  #include <iostream>

  
  using namespace std;

  
  int suma (int a, int b);

  
  extern string mensaje;

  
  extern int num1, num2;

  
  int main(){

  
  cout << mensaje << endl;

  
  cout << suma (num1, num2) << endl;

  
  return 0;

  
  }

  
  //-------------

  
  // suma.cpp

  
  //-------------

  
  int suma (int a, int b) {

  
  return a + b;

  
  }
