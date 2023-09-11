# INVENTARIO_Y_VISUALIZADOR

En este repositorio se encuentra el código fuente de dos proyectos de automatización que se complementan entre sí. Se encuentran enlazados mediante el MACRO que el encargado de almacén de CDT, Jhon Rojas Franklin, usa para poder actualizar el invnetario con los préstamos y devoluciones que presenta en la rotación de los activos que se almacenan. El proceso incia con la APP_INVENTARIO, mediante la cual el encargado de almacén puede ingresar activos que han sido adquiridos recientemente, ingresando los detalles de nombre, marca, entre otro campos, además de una imagen referencial del producto. La aplicación retorna como Outputs un código automático y secuencial para poder realizar el etiquetado de los nuevos productos; así como un link de Drive de las imágenes que se suben a la App. El paso intermedio es la actualización constante en el Macro con el que ya cuenta el encargado de almacén para poder realizar el registro de los préstamos y devoluciones. Con ello se actualiza la cantidad disponible de activos de un tipo, que es que finalmente se usará para el último paso. El último paso se refiere al Visualizador que se encuentra disponible en la Biblioteca Digital de Instructores, donde pueden consultar los instrumentos, herramientas, y componentes con los que se encuentran, consultar la sede y la cantidad para que procedan a realizar los respectivos préstamos para sus actividades programadas.

## APP_INVENTARIO

Esta App desarrollada para el uso del encargado del inventario CDT, le permite como administrador, poder ingresar información para nuevos productosadquiridos, listarlos, editar los campos y darlos de baja. El libro de Google Spreadsheets que sirve como una base de datos es la que se encuentra en el siguiente [enlace] (https://docs.google.com/spreadsheets/d/1oj4fCsHiHw7voG6v47k5zkiZozLsL4hRcEalTbIQ72I/edit#gid=0). Asimismo, el link de la implementación es el siguiente [enlace](https://script.google.com/a/macros/ferreyros.com.pe/s/AKfycbySWFAhsDwY8dMgjXEoVoEXAtfsYwbYVzIEbqMV30M80RmLg8JsLua2WdqZc6WfVwGE/exec). Por otro lado, si es que existen cambios en cualquiera de los archivos de la aplicación, se debe generar una nueva implementación. Cuando se abre la página principal del APP_INVENTARIO, se puede visualizar lo siguiente:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/7ca98a71-1395-40a7-9654-e620f351601b)

Donde puede visualizar los detalles de los productos ya existentes y registrados dentro del Spreadsheets que sirve como base de datos para este propósito. Para poder ingresar la información de productos nuevos, se debe aperturar el modal que se encuentra en el botón de agregar:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/059bdfd9-3ff7-4cbb-ac67-c1a270740872)

Lo que se apreciará serán los campos necesarios para poder registrar una nueva herramienta.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/3ba4606f-44bf-4b64-9990-d81712aa9072)

Varios campos son obligatorios, solo no es necesario colocar comentarios e imagen, esto es opcional. Para lo obligatorio aparecerá la siguiente advertencia para poder cargar la información mediante el botón de INGRESAR.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/cafe80a4-da69-46af-b7df-7236ee3397f8)

En el campo de acciones correspondientes a cada uno de los activos ingresados, encontramos el botón de editar y el de dar de baja.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/2e036073-3b04-4741-80e6-6733d1773a31)

Finalmente, para poder realizar las búsquedas de activos, se cuentan con varios campos, como los mostrados abajo, para poder tener más presción y rapidex en mediante una búsqueda específica dentro de los parámetros que comparten todos los productos.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/3a74ec53-0797-46bb-8d96-b6d78b6ce869)

### BÚSQUEDA DE BUGS

Los bugs o fallas que se pueden generar dentro de la implementación de esta aplicación se pueden deber básicamente al borrado de registros directamente desde el Spreadsheets, lo que no es recomendable. Es por ello que se han colocado diversas opciones desde el aplicativo para poder evitar la manipulación directa y hacer más interactiva la búsqueda y edición de los registros.

Por otro lado, el conocimiento de la estructura general de los archivos podría permitir la edición o adición de funcionalidades de acuerdo a la necesidad. En estos archivos encontramos:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/d1153069-32ce-4c84-ba53-3bdd7eb43e44)

El archivo de Index.html contiene la estructura del texto HTML y los estilos de la tabla de la página de ingreso, así como los modales correspondientes a las opciones de Agregar, Editar y Eliminar los registros. En cada uno de ellos, se ha escrito código correspodiente a los campos que contienen y al tipo de variables que soportan, así como si es que son campos requeridos o no. El archivo de Code.gs contiene las líneas necesarias para poder ejecutar acciones en el Spreadsheets desde el aplicativo de App Scripts, así como para poder guardar automáticamente y poder obtener los enlaces de las imagenes que se suben en referencia a cada registro. El archivo de JavaScript permite que se realicen las acciones de Mostrar los registros del Spreadsheets en la pantalla de la aplicación, como la búsqueda y supresión de los registros que no coinciden con la búsqueda.

Asimismo, existen librerías que permiten que esta aplicación funcione de manera adecuada, las cuales son jquery y bootstrap. Para cualquier modificación, tomar en cuenta que estas librerías se encuentran al inicio y al final del archivo Index.html.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/fc889d30-6a29-4e95-b621-6ed9e123053b)

## VISUALIZADOR DE LA BD

Finalmente, también se cuenta con un visualizador en la Biblioteca Digital de Instructores que permite que ellos puedan encontrar con facilidad y en tiempo real la información relacionada a la cantidad en tiempo real de los activos que se prestan y se devuelven rotativamente por parte del encargado del almacén. También tiene opciones de buscadores en la parte superior para facilitar la ubicación de las herramientas, instrumentos, equipos o componenentes que se necesitan. El link del Spreadsheets que sirve como base de datos para esta implementación se encuentra en el siguiente [enlace] (https://docs.google.com/spreadsheets/d/1zlv0DeiRQDRLgR45ScdAs4u_WXOsB-8V8tZtXKfpc4I/edit#gid=0), y el link de la implementación se encuentra en el siguiente [enlace] (https://script.google.com/a/macros/ferreyros.com.pe/s/AKfycbzaBV5PQ2ht4aQYcYQ1mnTaIgMbRnXDnNw5HBrqfGk-yHTcslpEjbTN99tDTxzcO5C1/exec). 

Lo que se visualizará en la página de ingreso a la aplicación es lo siguiente:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/a16c6f40-87ee-4808-81b3-90db5f6e2088)

Como se puede observar, en la parte superior tiene campos para poder realizar la búsqueda libre o mediante campos desplegables que permiten facilitar la misma. También se muestra la cantidad actualizada de existencias de cada activo. 

### BÚSQUEDA DE BUGS

En este caso, el archivo de Spreadsheets no debe ser manipulado porque puede conllevar a resultados catastróficos y de corrupción de la base de datos y por lo tanto, de todo lo que se muestra en el visualizador. Asimismo, se cuenta con los tres mismos archivos que se describieron previamente.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/INVENTARIO_Y_VISUALIZADOR/assets/144281326/cb8e3fbe-82fd-4a24-a322-9b2becae106c)

El código para estas dos implementaciones será distribuido en dos carpetas diferentes para evitar la confusión porque los ficheros de ambos tienen el mismo nombre.



