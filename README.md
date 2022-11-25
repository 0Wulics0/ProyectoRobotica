<h1 align="center"; style="text-align:center;">Proyecto Final</h1>

## Robótica
### Jorge Daza, Camilo Martín, Daniel Pineda, Daniel Melo, Santiago Mariño

# Introducción

A nivel industrial se busca optimizar de manera correcta algunos procesos, de modo que aumente la eficiencia de los mismos. En este proyecto se busca diseñar e implementar una herramienta personalizada para realizar un proceso de ensamble de un gripper, mediante una ventosa controlada por una señal digital conectada a una electroválvula. Para ellos se realizaron corroboraciones de la programación mediante simulaciones en Robot Studio y pruebas de firmeza para la ventosa.

# Diseño del Gripper

El diseño planteado fue inspirado en unas pinzas de presión.

![Pinzas_depresion](/Img/PinzasPresion.jpg)

Al analizar esta herramienta se notó que es un mecanismo de cuatro barras. Con esto en mente se empezaron a diseñar los eslabones que conformarían el ensamble. Para este proceso se tuvo en cuenta la siguiente consideración; que el ancho de estos no debería ser menor de 50mm, con el objetivo de facilitar la adhesión de las piezas a la ventosa. Por otro lado, el diámetro de los agujeros para los pasadores se determinó de 8mm, decisión orientada a prevenir contratiempos en el proceso del ensamble. Tomando en cuenta las consideraciones previamente mencionadas, se modeló el gripper en Inventor, variando las distancias entre agujeros (longitudes del mecanismo de cuatro barras) hasta tener un resultado satisfactorio, resultando en las siguientes piezas. 

![PlanoGripper](/Img/planoGripperPiezas.jpg)

Como se ve en la imagen superior, las distancias del mecanismo de cuatro barras resultaron siendo de 50, 80, 80 y 75 mm. Con lo que se obtiene el siguiente montaje.

Para fabricar el gripper se optó por usar corte laser en MDF por su bajo costo, reducido tiempo de producción y además porque el material residual del proceso se puede utilizar directamente como la base de recogida para el proceso de ensamblaje. 

# Diseño herramienta

Para el diseño de la herramienta se tuvo en cuenta el dimensionamiento de la ventosa, para lo cual fue necesario acceder a este dispositivo en el laboratorio y tomar sus respectivas medidas, como se presenta en la siguiente figura:

![Medidas](/Img/MedidasRef.jpeg)

A partir de esto se modelo en Inventor la ventosa, para realizar un dimesionamiento correcto.

![Ventonsa Modelados](/Img/Ventosa3D.jpeg)

Luego de esto se comenzó el diseño de la herramienta con los parámetros dados, tal como la orientación de la ventosa con respecto al eje Z, del plato portaherramientas.

![Herramienta Inventor 2D](/Img/HerramientaInventor2D.jpeg)

Se observa que para obtener poco despercio de material se realizó un diseño con partes huecas, esto no afectará la implementación de la herramienta pues esta, estará sometida a pocas cargas o esfuerzos (cortantes), en esta zona. Así mismo se observa que en la base que irán diversos agujeros para unir este dispositivo con el controlador ABB.

![Herramienta Inventor 3D](/Img/HerramientaInventor3D.jpeg)

Finalmente se realizo la impresión 3D de esta herramienta en ácido poliláctico (PLA), el resultado final se presenta a continuación.

![Herramienta](/Img/Herramienta.jpeg)

# Materiales del proyecto
# Ensamble

Para el ensamble del sistema, se preparo el espacio de trabajo colocando las piezas del gripper y realizando la respectiva calibración. En cuanto a la herramienta se acomodo la ventosa, al diseño presentado anteriormente, y luego de esto se atornillo al plato portaherramienta con los respectivos tornillos M5, sin pasar de la respectiva medida recomendada.

[![WorhObject](https://img.youtube.com/vi/LBgoFYejHUw/0.jpg)](https://youtube.com/shorts/LBgoFYejHUw?feature=share)
(Video)

# Espacio de trabajo 
# Simulación

Para la simulación se realizo el diseño de las piezas con las que se iba a trabajar en Inventor, luego estas se exportaron a Robot Studio para poder crear el espacio de trabajo de manera adecuada, se realizo el seguimiento de las trayectorias a lo largo de toda la pieza con el manipulador.

[![WorhObject](https://img.youtube.com/vi/9qHaZTjxoxA/0.jpg)](https://youtu.be/9qHaZTjxoxA)
(Video)

Durante esta simulación se encontraron algunos targets fallidos, para esto fue necesario revisar las orientaciones de los mismos, pues estos tienen configuraciones opuestas a las del manipulador, por lo tanto fue necesario realizar pistas intermedias para que el robot pudiera alcanzar los targets necesarios según la orientación y posición objetivo.

[![WorhObject](https://img.youtube.com/vi/8Jlcn76TU88/0.jpg)](https://youtu.be/8Jlcn76TU88)
(Video)

Luego de esto se procedió a implementar el código de RAPID en el controlador ABB.


# Resultados
