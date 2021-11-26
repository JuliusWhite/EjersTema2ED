## 21. Bibliotecas. Busca información y explica las ventajas y desventajas de usar
bibliotecas dinámicas.

**Ventajas:**

-El código queda más claro y menos extenso que si utilizaramos librerías estáticas
- Ahorran más memoria y reducen el intercambio de páginas.
- El archivo .so es independiente del archivo .exe, siempre que la interfaz de salida permanezca igual (es decir, el nombre, los parámetros, el tipo de valor de retorno y la convención de llamada no cambien), reemplazar el archivo so no causará ningún impacto en el archivo .exe, mejorando así la capacidad de mantenimiento y la escalabilidad.
- Los programas escritos en diferentes lenguajes de programación pueden llamar a la misma librería para que funcionen siempre que sigan la convención de llamada de función.
- Son adecuadas para el desarrollo de software a gran escala, lo que hace que el proceso de desarrollo sea independiente y menos acoplado, lo que es conveniente para el desarrollo y las pruebas entre diferentes desarrolladores y organizaciones de desarrollo.


**Desventajas:**
- La velocidad es menor, ya que a diferencia de las librerías estáticas, necesitan ir a buscar cada una de las funciones requeridas cada vez que se hace un llamamiento.
- Si se quiere ejecutar el archivo es necesario tener instaladas las librerías en el sistema que lo va a ejecutar.
- En caso de modificar las librerías de alguna manera habría que modificar el código fuente del ejecutable para que éste funcionara con normalidad.
