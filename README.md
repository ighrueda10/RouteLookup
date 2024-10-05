# RouteLookup
Route Lookup Trie

Este proyecto implementa una estructura de datos de tipo Trie para la búsqueda eficiente de rutas IP. La estructura Trie permite almacenar y buscar prefijos de direcciones IP de manera compacta, reduciendo el tiempo de búsqueda y optimizando el almacenamiento.

Descripción del Proyecto

El propósito de este proyecto es proporcionar una implementación eficiente para la búsqueda de rutas IP, una operación crucial en sistemas de enrutamiento y redes de datos. Utilizando una estructura de datos de tipo Trie, el proyecto almacena los prefijos de rutas y realiza búsquedas rápidas para determinar el interfaz de salida adecuado para cada paquete. La compresión del Trie se utiliza para optimizar aún más la estructura, eliminando nodos innecesarios y reduciendo la complejidad de la búsqueda.

Este proyecto está diseñado para ser utilizado como una herramienta de aprendizaje y evaluación para la implementación de técnicas de búsqueda y compresión en estructuras Trie. Se incluyen archivos de prueba para evaluar la eficiencia del algoritmo.

Características Principales

Inserción de Prefijos: Los prefijos se insertan en la estructura Trie a partir de sus representaciones binarias, lo que permite una organización jerárquica de las rutas.

Compresión del Trie: Se aplica un algoritmo de compresión al Trie para reducir el número de nodos y mejorar la eficiencia de las búsquedas.

Búsqueda de Direcciones: Se realiza una búsqueda para encontrar la mejor coincidencia (longest prefix match) para cada dirección IP a partir de los prefijos almacenados.

Manejo de Entradas y Salidas: El programa lee tablas de ruteo y direcciones IP desde archivos de entrada y escribe los resultados de las búsquedas en un archivo de salida.

Estadísticas de Búsqueda: Se genera un resumen del rendimiento de las búsquedas, incluyendo el número medio de accesos a nodos y el tiempo de búsqueda promedio.

Archivos de Prueba

routing_table: Este archivo contiene una tabla de rutas con prefijos y sus correspondientes interfaces de salida. Cada línea representa una entrada de la tabla de ruteo, compuesta por un prefijo IP y una interfaz de salida.

prueba(i): Archivos que contienen direcciones IP de prueba para poner a prueba el algoritmo de búsqueda. Cada línea de estos archivos contiene una dirección IP que el programa intentará enrutar utilizando el Trie.

Uso

El programa toma dos archivos como parámetros de entrada:

Un archivo de tabla de rutas (FIB) con prefijos y sus correspondientes interfaces de salida.

Un archivo de paquetes de entrada para realizar la búsqueda de sus direcciones IP.

El formato para ejecutar el programa es:

Por ejemplo:

En este ejemplo, el archivo routing_table contiene los prefijos IP que se cargarán en el Trie, y prueba1 contiene direcciones IP que se utilizarán para realizar búsquedas y determinar la interfaz de salida correspondiente.

Compilación

Para compilar el código, puedes utilizar un compilador como GCC. Asegúrate de tener todos los archivos fuente (main.c, io.c, utils.c) en el mismo directorio y ejecuta el siguiente comando:

Esto generará un archivo ejecutable llamado route_lookup_trie.

Ejecución

Después de compilar el programa, puedes ejecutarlo como se explicó anteriormente, proporcionando los archivos de tabla de rutas y direcciones de prueba como argumentos. El programa mostrará información detallada sobre la estructura del Trie antes y después de la compresión, así como los resultados de las búsquedas de las direcciones IP ingresadas.

Además, el programa imprimirá estadísticas generales que incluyen:

Número de nodos en el árbol: Indica cuántos nodos hay en el Trie después de insertar todos los prefijos.

Número de paquetes procesados: Cantidad de direcciones IP buscadas en el Trie.

Número medio de accesos: Número promedio de nodos accedidos durante las búsquedas.

Tiempo medio de acceso: Tiempo promedio que toma acceder a un nodo durante las búsquedas.

Ejemplo de Salida

El programa imprimirá la estructura del Trie antes y después de aplicar la compresión, mostrando cada nodo con su prefijo y puerto asociado. También se imprimirán los resultados de las búsquedas para cada dirección IP del archivo de entrada, incluyendo el puerto correspondiente y el número de nodos accedidos.

Al final de la ejecución, se mostrará un resumen con las estadísticas generales mencionadas anteriormente.

Funciones Principales

create_node(): Crea un nuevo nodo para ser insertado en el Trie.

insert(): Inserta un nodo en la estructura Trie según el prefijo proporcionado.

comprimir(): Comprime la estructura Trie eliminando nodos innecesarios para optimizar el rendimiento.

search(): Busca la mejor coincidencia para una dirección IP dentro del Trie.

show_trie(): Muestra la estructura del Trie, útil para depuración y visualización.

free_tree(): Libera la memoria utilizada por la estructura Trie.

Requisitos

Compilador C: Se recomienda GCC para compilar el proyecto.

Archivos de Entrada: Deben proporcionarse dos archivos de entrada, uno para la tabla de rutas (routing_table) y otro para las direcciones IP de prueba (prueba(i)).
