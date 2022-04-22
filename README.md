# UAO-Project2-Object_Detection_Neuronal_Network
Red neuronal para la detección de objetos de carros, aviones, tanques, gatos y pingüinos, usando la arquitectura Faster R-CNN y el framework Detectron2. Esto fue desarrollado como segundo proyecto de la asignatura de Redes Neuronales Artificiales y Deep Learning en la Universidad Autónoma de Occidente.

****

## Descripción
_Este documento explica qué problema resuelve la red neuronal y cómo ejecutarla_

## ¿Qué contiene este repositorio?
Este repositorio contiene 3 archivos que son:

1. **Proyecto2_RNA_Carlos_Doffiny_SV.ipynb** el cual es el código hecho en Colab que contiene todo lo relacionado con el análisis de la data, y el diseño y construcción de la red neuronal, así como de su entrenamiento y validación.
2. **Reporte_Proyecto3_Carlos_Doffiny_S-V.pdf** el cual es el reporte en formato IEEE que contiene toda la explicación y documentación de cada uno de los procesos realizados durante el estudio del problema a resolver y la construcción de la red neuronal.
3. **test_photos** el cual es una carpeta que contiene las imágenes que no pertenecen originalmente al data set creado, y que se usan al final del código para comprobar la eficiencia de la red creada.

## ¿Qué problema resuelve esta red neuronal?
Esta red neuronal fue hecha como segundo proyecto para el curso de Redes Neuronales y Deep Learning en la Universidad Autónoma de Occidente, de Cali, Colombia. Y es capaz de detectar los objetos de 5 clases o categorías diferentes, a partir de la creación de un [data set](https://app.roboflow.com/carlos-doffiny-s-v/proyecto2_rna_carlos_doffiny_sv/1) de autoría propia, conformado por 30 imágenes de cada clase (carro, avión, tanque, gato y pingüino).

## ¿Cómo está dividido el data set?
Originalmente las 150 imágenes del data set están divididas de la siguiente forma: 
*   Datos de entrenamiento (70% - 105 imágenes)
*   Datos de validación (20% - 30 imágenes)
*   Datos de prueba (10% - 15 imágenes)

Pero a los datos de entrenamiento se les aplicaron diferentes técnicas de data augmentation con la finalidad de evitar el sobre entrenamiento de la red, por lo cual el data set termina estando formado por 360 imágenes que tienen la siguiente distribución:
*   Datos de entrenamiento (88% - 315 imágenes)
*   Datos de validación (8% - 30 imágenes)
*   Datos de prueba (4% - 15 imágenes)

## ¿Cómo ejecutar la red neuronal?
Para ejecutar la red neuronal se deben seguir los siguientes pasos:
1. Clonar el presente repositorio para poder descargar los archivos.
2. Ingresar al sitio web de [Google Colab](https://colab.research.google.com/).
3. En él aparecerá la siguiente ventana, y nos iremos a la última opción denominada **Subir**, en donde seleccionaremos el archivo llamado `Proyecto2_RNA_Carlos_Doffiny_SV.ipynb`. <p align="center"><img src="https://i.imgur.com/LJ5tLin.png"/></p> 
4. Una vez que se haya cargado el código, deberemos hacer click arriba a la derecha en donde dice **Conectar**, para que así poder utilizar los recursos gratuitos en la nube que ofrece Google Colab. <p align="center"><img src="https://i.imgur.com/zOuZjuf.png"/></p>
5. Para ejecutar la red, es obligatorio el uso de una GPU, y Google Colab nos ofrece una en `Entorno de Ejecución > Cambiar tipo de entorno de ejecución`, en donde se abrirá una ventanita emergente denominada Configuración del cuaderno, y en la primera opción de `Acelerado por hardware` vamos a seleccionar el GPU.<p align="center"><img src="https://i.imgur.com/BhGsSgC.png"/></p> 
6. Cuando ya aparezcan dos barras de RAM y Disco en donde anteriormente decía conectado,  seleccionaremos en la barra lateral de la izquierda **Archivos** y subiremos todos los archivos que están dentro de la carpeta llamada `test_photos`, puede ser una a una o la carpeta de una. <p align="center"><img src="https://i.imgur.com/C6pUBC6.png"/></p> 
7. Por último, solo quedaría ejecutar el código, presionando las teclas `Ctrl + F9` o en el menú superior seleccionar la opción de `Entorno de Ejecución > Ejecutar todas`

## Consideraciones especiales

1. La red neuronal actualmente está configurada para ejecutar 1500 épocas o ciclos de entrenamiento por lo cual tarda aproximadamente unos 130 minutos en entrenarse y validarse.
2. Si quieren cambiar, modificar o agregar cualquier parámetro o función nueva a la red, pueden hacerlo sin problemas, pero para ejecutar los cambios deberán seleccionar en el menú superior la opcion de `Entorno de Ejecución > Reiniciar y Ejecutar todo`
3. Antes de ejecutar la primera vez el código, ya estarán precargados los resultados de la última ejecución realizada antes de subir el código a este repo.
4. Luego de entrenar la red (puede ser con menos épocas, digamos unas 1200) pueden probarla con cualquier imagen que deseen, utilizando las dos últimas secciones de código, en donde solo tienen que agregar la imagen a los archivos, y copiar su nombre o su path si está dentro de una carpeta, en la primera línea de lectura de la imagen. <p align="center"><img src="https://i.imgur.com/P57OUX8.png"/></p> 

## Contribuciones
Formar una comunidad activa en donde todos podamos aprender y crecer juntos en nuestras jornadas de programación es muy gratificante, por lo cual cualquier contribución es muy apreciada. 
Si tienes alguna sugerencia para mejorar esto, por favor bifurca este repositorio y crea un pull request, o crea un issue con el tag `enhacement`

## Problemas y ayudas
En caso de presentar algún tipo de problema con el código, el data set o necesitar alguna ayuda para resolver una duda, por favor revisen los issues para ver si alguien anteriormente tuvo la misma duda, y sino, pueden crear uno nuevo sin problema.

## Licencia
Este proyecto utiliza una licencia del MI, cuyos detalles puedes encontrar en el archivo `LICENSE.md`. Siéntete libre de usar este proyecto como base para tus próximos proyectos.

## Links de interés
A continuación anexo algunos links de interés que me sirvieron de gran ayuda durante la elaboración del proyecto:
* [How to Train a Custom Faster R-CNN Model with Facebook AI's Detectron2 | Use Your Own Dataset](https://www.youtube.com/watch?v=4OXntFVfFio)
* [How to Train Detectron2 on Custom Object Detection Data](https://blog.roboflow.com/how-to-train-detectron2/)
* [Computer Vision Model Library](https://models.roboflow.com/)
* [Explicación detallada del algoritmo R-CNN más rápido](https://www.programmerclick.com/article/3370793669/)
* [Detectron2 API Documentation](https://detectron2.readthedocs.io/en/latest/modules/index.html)
* [Detectron2 Model Zoo and Baselines](https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md#coco-object-detection-baselines)


****
Programemos para hacer del mundo un mejor lugar :)



