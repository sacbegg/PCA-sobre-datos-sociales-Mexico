# Análisis de componentes principales aplicado a índices sociales de México y su relación con la prueba PISA de matemáticas

Proyecto final de álgebra matricial de la Maestría en Cómputo Estadístico CIMAT Monterrey.

## Fuente de los datos y significado

- TI-corruption-perception-index.csv:
    - Link: https://ourworldindata.org/corruption
    - **Where is perceived corruption highest?** El Índice de Percepción de la Corrupción puntúa a los países en una
    escala de 0 a 100, en la que 0 significa que
    un país se percibe como muy corrupto y 100 significa que un país se percibe como muy limpio. El indicador es
    representativo de la opinión de los expertos, ya que se construye tomando las medias de varias encuestas
    estandarizadas a expertos, incluidas las de la Fundación Bertelsmann, el Foro Económico Mundial, el Banco Mundial
    y muchas otras.
- democracy.csv:
    - Link: https://ourworldindata.org/democracy

## ¿Qué son los indicadores sociales?

Los indicadores sociales son un conjunto de medidas cuantitativas que se utilizan para evaluar el desempeño social de un país. Estos indicadores pueden abarcar una amplia gama de temas, como la salud, la educación, la economía, el empleo, la pobreza, la desigualdad, la violencia, el bienestar social, entre otros. La idea es que los indicadores sociales permitan identificar las fortalezas y debilidades de un país en relación a su desarrollo social, y que proporcionen información valiosa para la toma de decisiones y la implementación de políticas públicas encaminadas a mejorar el bienestar de la sociedad.

## ¿Qué es la prueba PISA en matemáticas?

La prueba PISA es una evaluación a nivel internacional que se lleva a cabo cada tres años para medir el rendimiento académico de los estudiantes de 15 años en tres áreas: lectura, ciencias y matemáticas. La prueba PISA en matemáticas mide las habilidades y conocimientos de los estudiantes en matemáticas, y evalúa su capacidad para aplicar lo que han aprendido en situaciones cotidianas. La prueba PISA en matemáticas es desarrollada y administrada por la Organización para la Cooperación y el Desarrollo Económicos (OCDE), y se utiliza como una herramienta para comparar el desempeño de los estudiantes de diferentes países y mejorar la calidad de la educación en matemáticas a nivel mundial.

## ¿Qué es el análisis de componentes principales?

El análisis de componentes principales (PCA, por sus siglas en inglés) es una técnica
estadística utilizada para reducir la dimensión de un conjunto de datos. PCA se basa en
la idea de encontrar una nueva representación de los datos que preserve la información
importante pero que sea más compacta y fácil de manipular. Esto se logra mediante el
cálculo de nuevas variables llamadas componentes principales, que son combinaciones
lineales de las variables originales y están ordenadas de forma que la primera
componente principal explica la mayor cantidad de variabilidad en los datos, la segunda
componente principal explica la siguiente mayor cantidad de variabilidad, y así
sucesivamente.

## Pasos para realizar el cálculo de componentes principales sobre un conjunto de datos

La forma matemática de calcular las componentes principales de un conjunto de datos se puede expresar de la siguiente manera:

- Primero, se calcula la matriz de covarianza de los datos, que es una matriz cuadrada que contiene los valores de covarianza entre cada par de variables. La covarianza mide la relación lineal entre dos variables y nos indica si estas varían en la misma dirección (covarianza positiva) o en direcciones opuestas (covarianza negativa).

- A continuación, se calculan los autovectores y autovalores de la matriz de covarianza. Los autovectores son vectores que se mantienen en la misma dirección después de ser multiplicados por la matriz de covarianza, mientras que los autovalores son escalares que indican cuánto se amplía o reduce cada autovector al ser multiplicado por la matriz de covarianza.

- Finalmente, se ordenan los autovectores de forma que el primer autovector corresponda al autovalor más grande, el segundo autovector corresponda al siguiente autovalor más grande, y así sucesivamente. Estos autovectores ordenados se convierten en las componentes principales del conjunto de datos, y cada observación original se puede representar como una combinación lineal de estas componentes principales.

<div>
    <img src=https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/GaussianScatterPCA.svg/1024px-GaussianScatterPCA.svg.png width="400"/>
<div>
    
En la imagen superioir se muestra PCA aplicado a una distribución normal multivariante centrada en (1,3) con desviación estándar 3 en la dirección aproximada (0,866, 0,5) y desviación estándar 1 en la dirección perpendicular a la anterior. Los vectores muestran los autovectores de la matriz de correlación escalados mediante la raíz cuadrada del correspondiente autovalor, y desplazados para que su origen coincidan con la media estadística.

## ¿Cómo puede ayudar aplicar PCA sobre indicadores sociales?

Aplicar análisis de componentes principales sobre este tipo de datos podría ayudar a identificar las caracterisitcas más importantes para entender o predecir ciertos comportamientos sociales más influyentes de un país (los componentes principales), en este caso México. 
Esto podría permitir a un gobernante de un país enfocarse ya sea en los indicadores más problematicos o aquellos tales que su varianza influye directamente en el progreso y bienestar del país y sus ciudadanos.

## Conlusiones

Del análisis hecho se puede concluir que de los diez índices sociales de México extraídos de la página Our World Data, el número de fuerzas armadas y el gasto en educación son las características con mayor peso en los datos con respecto a la varianza, ya que son las variables que más cargan los componentes principales en dos dimensiones, qué además, logran explicar poco más de un 85% de la varianza total de los datos.

Por otro lado, resulta que estas mismas características están en el mismo cuadrante que la puntuación PISA de matemáticas en México y que en adición se correlacionan moderadamente y de forma positiva, mostrando que hay un patrón subyacente en las mismas.

De lo anterior podría decirse que un aumento en el gasto de educación genera un aumento en la puntuación PISA, sin embargo, resulta contradictorio decir que un aumento en el número de fuerzas armadas generaría un aumento en la destreza matemática de los adolescentes, por ello es importante mencionar que correlación no implica causalidad y que habría que hacer un análisis más profundo de los datos. 

## Límitaciones del análisis

Algunas limitaciones del análisis son las siguientes:

- Análisis con poca cantidad de índices sociales del país
- Pocos registros históricos para cada índice social
- Se realizó interpolación lineal para rellenar los datos faltantes, pudiendo esto afectar la calidad de los dato


