# Configuración de las bases de datos de metabolómica

El siguiente código es para actualizar una base de datos de metabolómica para diabetes. Ya existen unas bases de datos previas y se busca realizar una actualizacion de los nombres de los metabolitos que posteriormente facilitaran análisis de vías metabólicas o analisis de agrupaciones por distintas características de los mismos.
Se creará:

Una base de datos con todos los metabolitos al basal y a 1 año y las principales variables de interés.

- Una base de datos con todos los metabolitos al basal y a 1 año con todos los participantes.

- Una base de datos con la codificación de los metabolitos que incluya: nombre del metabolito al basal y a 1 año, nombre real, HMDB, PubChem, KEGG, DrugBankID, Drug, plataforma donde se analizó, BiologicalFunction, MolecularFramework, Kingdom, super_class y class sub_class.

------------------------------------------------------------------------

## **Requisitos**

Lista de dependencias necesarias para ejecutar el código:

\- Lenguaje: R 4.x o superior; Python 3.xx o superior

\- Paquetes requeridos en R:

-   **`readr`:** Para leer y escribir datos en formatos delimitados (como CSV).
-   **`dplyr`:** Para manipulación de datos con una sintaxis clara y funcional (filtrar, agrupar, resumir, etc.).
-   **`readxl`:** Para leer archivos de Excel (.xls y .xlsx).
-   **`httr`:** Para realizar solicitudes HTTP y manejar APIs.
-   **`hmdbQuery`:** Para consultar la base de datos HMDB (Human Metabolome Database).
-   **`XML`:** Para trabajar con datos en formato XML.
-   **`xml2`:** Similar a XML, pero más moderno y compatible con el ecosistema tidyverse para manejar datos en XML.
-   **`furrr`:** Para procesamiento paralelo y uso de purrr (programación funcional) en múltiples núcleos.
-   **`progress`:** Para mostrar barras de progreso en operaciones largas.
-   **`parallel`:** Para realizar tareas paralelas usando múltiples núcleos del procesador.
-   **`doParallel`:** Extiende foreach para facilitar el uso de paralelismo.
-   **`rio`:** Para importar y exportar datos de diversos formatos.
-   **`reticulate`:** Para integrar Python con R, permitiendo usar librerías y scripts de Python dentro de R.

Instalación de paquetes en R:

```{r}
install.packages(c("readr", "dplyr", "readxl", "httr", "hmdbQuery", "XML", "xml2", "furrr", "progress", "parallel", "doParallel", "rio", "reticulate"))
```

\- Modulos requeridos en Python:

-   **`pandas`:** Biblioteca de Python utilizada para la manipulación y análisis de datos.
-   **`requests`:** Biblioteca para realizar solicitudes HTTP.
-   **`xml.etree.ElementTree`:** Módulo estándar de Python para trabajar con XML.
-   **`time`:** Biblioteca estándar de Python para manejar y controlar aspectos relacionados con el tiempo.
