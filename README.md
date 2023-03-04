# Reclutamiento-de-personal-analistaDeDatos

<h3 align="center">Actividad #1(Analisis de identificacion de personas califidas para un puesto de analisis de datos en Excel)</h3>
<p align="left">
Una agencia de reclutamiento de personal ayuda a todo tipo de empresas a encontrar personas calificadas para ocupar puestos de trabajo de análisis de datos abiertos. La agencia recopiló datos sobre las solicitudes de empleo de las oportunidades publicadas en su sitio web para el año 2019.
La agencia pide que se optimice proceso de solicitud en línea. La tarea es resumir los datos de solicitudes de empleo de la agencia y poder responder a las siguientes preguntas:
</p>

-¿Cuál fue el número total de solicitudes recibidas por mes en 2019?

-¿En qué meses se recibió el menor y el mayor número de solicitudes totales?

-¿Cuál fue el número promedio de solicitudes recibidas por mes?

<h4> Para ello se trabajara con la siguiente hoja de calculo:</h4> [Datos sin porcesar:Excel](https://github.com/HelenCVM/Reclutacion-analistaDeDatos/blob/main/datos-sin-procesar.xlsx) 

<hr>
<h4> Problematica:</h4>Encontrar personas calificadas para optar por puestos de trabajo de analistas de datos con la informacion recolectada del sitio web de una agencia

<hr>
<h3 align="center">:ballot_box_with_check:Solución</h3>
<h4>Variables o etiquetas:</h4>Los datos de la agencia contienen información sobre todas las solicitudes de empleo de análisis de datos recibidas en 2019. Los datos incluyen los siguientes encabezados de columna: Identificación del solicitante, Fecha, Título del trabajo, Ubicación del trabajo, Contratación y Solicitud fácil. A continuación, se muestra una descripción de cada encabezado de columna y ejemplos de valores.
<ul>
  <li>ID(Identificador):Identificador único para los solicitantes</li>
  <li>Date(Fecha):Fecha y hora de recepción de cada solicitud</li>
  <li>Job Title(Título del trabajo)El puesto de analista de datos solicitado</li>
  <li>Job Location(Lugar de trabajo):Ubicación del puesto de trabajo</li>
  <li>Hired(Contratado):Indica si un candidato ha sido contratado</li>
  <li>Easy Apply(Fácil de aplicar):</li>(Verdadero) si la solicitud se presentó directamente en el sitio web de la agencia;(Falso) si la solicitud se descargó y presentó por correo electrónico.
</ul>

<h4>PASOS:</h4>
<ol>
  <li>Ordenar los datos(por fecha(Date))</li>
  <li>Añadir hoja de calculo con nombre(datos_de_resumen). Esta nueva hoja va a dar respuesta a las preguntas iniciales del analisis</li>
  <li>En la fila 1 agregamos las etiquetas A1:(Mes(Month) y B1:(Applicants(Solicitantes))</li>
  <li>En la celda A2 agregamos el mes (Enero(January)) y usamos el "autocompletar" para rellenar todos los meses</li>
  <li>Volvemos a la hoja (datos_sin_procesar). Agregamos en la celda G1 la etiqueta (Mes(Month).</li>
  <li>En la celda a continuacion G2, vamos a utilizar la funcion "TEXTO" para convertir los valores numericos de la fecha en texto, que ayudara a determinar la cantidad de solicitudes por mes. En celda G2 quedaria la funcion -> =TEXTO(B2,"mmmm") y utilizo el autocompletar para llenar todas las celdas de la columna con el mes correspondiente.</li>
  <li>Volver a la hoja de calculo (datos_de_resumen).En la celda B2 utilizo la funcion CONTAR.SI para contar la cantidad de solicitudes durante el mes, es decir las veces que aparece un criterio en un intervalo</li>
  <li>En la celda B2, escribe =CONTAR.SI('datos_sin_procesar'!G:G,A2). La primera entrada ('datos_sin_procesar'!G:G) se refiere al intervalo en el cual se están contando los datos. El intervalo está en tu hoja de datos sin procesar ('datos_sin_procesar'!) e incluye toda la columna G(G:G). Esta columna contiene los datos de los meses. La segunda entrada (A2) se refiere al criterio que deseas contar. En este caso, el valor de la celda A2 de tu hoja de datos de resumen es “Enero(January)”. La función te dirá cuántas veces aparece Enero(January) (el criterio) en la columna Fecha (el intervalo).</li>
  <li>Copiamos la funcion para las siguientes celdas</li>
  <li>Usar la funcion (SUM) para sumar todas las solicitudes del año. El celda A14 escribo(Total) y en B14 la funcion (=SUMA(B2:B13))</li>
  <li>Usar la funcion MIN para calcular el menor número de solicitudes recibidas en un mes.En la celda A16 escribe (MIN) y en la celda B16 escribe =MIN(B2:B13)</li>
  <li>Usar la funcion MAX para calcular el mayor número de solicitudes recibidas en un mes.En la celda A17 escribe (MAX) y en la celda B17 escribe =MAX(B2:B13)</li>
  <li>Usar la funcion PROMEDIO para calcular el promedio de solicitudes mensuales recibidas en 2019.En la celda A18 escribe (PROMEDIO) y en la celda B18 escribe  =PROMEDIO(B2:B13).</li>
</ol>

<hr>
<h3 align="center">:ballot_box_with_check:Respuestas</h3>
<ul>
  <li>¿Cuál fue el número total de solicitudes recibidas por mes en 2019?----R/</li>
  <p>January	2387</p>
<p>February	2312</p>
<p>March	2536</p>
<p>April	2544</p>
<p>May	2954</p>
<p>June	2990</p>
<p>July	3138</p>
<p>August	2969</p>
<p>September	2865</p>
<p>October	2751</p>
<p>November	2508</p>
<p>December	2642</p>
  <li>¿En qué meses se recibió el menor y el mayor número de solicitudes totales?----R/</li>
Menor numero de solicitudes------February	2312
Mayor numero de solicitudes------July	3138
  <li>¿Cuál fue el número promedio de solicitudes recibidas por mes?----R/El número promedio de solicitudes recibidas por mes fue de2.716,333333</li>
</ul>

