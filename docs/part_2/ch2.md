---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.1
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# El Modelo IS-LM (II): Mercado de Dinero

## Introducción
<a id=’intro’></a>

En el capítulo anterior analizamos el mercado de bienes. En esta abordaremos el mercado de dinero para completar las dos piezas determinantes del modelo IS-LM. Este a su vez es el determinante principal del sistema de demanda agregada (DA), que relaciona el gasto efectivo agregado que tiene lugar en una economía con el nivel general de precios. la oferta agregada (SA) relaciona el nivel de producción, e indirectamente también el nivel de empleo, con el nivel de precios. La SA y la DA determinan el nivel de equilibrio en un horizonte de tiempo que podemos llamar medio, más largo del que estamos contemplando aquí en todo caso, y en el cual los precios son rígidos a corto plazo. Aquí supondremos los precios como un parámetro. Rigurosamente, deberíamos decir que los precios están predeterminados (en este horizonte temporal), pero la realidad es que en términos prácticos actúa como una variable exógena.

Pueden observar a su alrededor para cerciorarse del enorme peso de estos dos componentes en la vida cotidiana. Pero las elaboraciones teóricas no son tan inmediatas como pueden serlo en ciencia experimentales como la física. Porque la economía en primera instancia no es una ciencia experimental. Hay estudios experimentales clásicos y recientes muy relevantes en el campo de la economía, pero las condiciones específicas de los mercados que dan lugar a una asignación de recursos concreta están sujetas a cambios, en numerosas ocasiones por no decir casi siempre, continuos, impredecibles y a veces persistentes que por su naturaleza no se pueden reproducir. Y así como las ciencias experimentales recurren a los laboratorios para reproducir sucesos y poder establecer leyes por medio de métodos deductivos, la economía debe elaborar modelos puramete teóricos, basados en principios axiomáticos. Los modelos no deben ser impuestos por lo tanto como un dogma, sino como un artificio, a ser posible el mejor o el más manejable de los existentes, para la elaboración de datos que puedan ser contrastados con los hechos empíricos, por naturaleza irrepetibles. Por lo tanto, la crítica a la teoría, como la crítica de Lucas o de la propia Teoría General de Keynes, solamente puede elaborarse mediante las propuestas concretas de métodos alternativos; los investigadores puede aplicar los modelos existentes o construir modelos nuevos para mejorar el poder explicativo de una teoría siempre en etapa de construcción.

Los estudiantes de economía están habituados a comenzar sus conocimientos teóricos con principios microeconómicos basados en axiomas de comportamiento en una economía perfectamente competitiva. En estos primeras lecciones, el dinero no juega ningún papel relevante en la asignación de recursos que no sea el de mero velo descrito por la dicotomía clásica. En cursos más avanzados, y con ayuda de sus primeras herramientas neoclásicas, ya serán capaces de construir un modelo básico de equilibrio general walrasiano, y también se habrán convencido de la eficiencia en el sentido de Pareto de las asignaciones de equilibrio general en una economía perfectamente competitivo. 

Antes de intentar hacer ninguna definición formal del dinero, lo cual es probablemente imposible, sería conveniente indicar algunas observaciones triviales que relacionan nuestro universo cotidiano con el modelo IS-LM: la realidad que nos rodea está por doquier repleta de bienes y servicios, máquinas, bienes de equipo, materias primas necesarias para la producción de estos últimos. Todas han sido vendidas en un momento dado; si no están puestas en venta o planeado hacerlo, potencialmente sí lo son. Indirectamente, ese potencialde venta, aunque no define el dinero, lo revela a los sentidos y a la observación. La venta singular de estos bienes implica el contacto de productores y vendedores, ya sea por medios directos o a través de intermediarios. Este contacto se produce obviamente en los mercados. En el capítulo anterios contemplamos algunos detalles de ese entramado. El modelo IS-LM, cuya finalidad consiste en describir el comportamiento de una economía con desempleo keynesiano, tiene la particularidad de que explica los mercados de bienes y el mercado de dinero como un sistema íntegrado. Esto quiere decir algo tan simple como la imposibilidad de comprender uno de los mercados sin el otro. Asimismo, acomoda el modelo clásico como el caso especial de pleno empleo. El mercado de dinero, como el de cualquier activo en general, se suele analizar con el mismo método que cualquier otro mercado: a partir de sus variables de oferta y sus variables de demanda. Pero para comprender a fondo estos factores debemos detenernos un instante en aspectos más generales de los abarcados por el dinero.

El modelo IS-LM conlleva como contrapartida una serie de simplificaciones considerables que le impiden contemplar la realidad de los mercados de todo el espectro de activos que determinan la asignación de recursos. Debido a su carácter estático, los tipos de interés y la inflación, o la inflación esperada, solo pueden ser establecidos mediantes supuestos *ad hoc*, por tanto carentes de premisas microeconómicas sólidas. En realidad, tampoco debemos achacar errores a Keynes debido a herramientas que no disponía. La teoría de la utilidad esperada que cimentará las bases más tarde en la macroeconomía moderna, se desarrolla solo después de la II Guerra Mundial, gracias a las contribuciones de von Neumann y Morgensten (1947); los avances teóricos en métodos dinámicos estocásticos solo han sido posibles después de la revolución digital. Por otra parte, la resolución de modelos económicos está sujeta a la conocida *maldición de la dimensionalidad*, o costes marginales crecientes, medidos en términos de computación, de añadir dimensiones a un sistema teórico. 

En tal sentido debemos entender la demanda de saldos reales keynesiana. Al añadir el componente de especulación a la demanda clásica de dinero, lo que hace en realidad es vincular la velocidad de circulación de dinero a la economía productiva, incluido el mercado de trabajo. Si a este hecho le añadimos la extrema volatilidad intrínseca de la inversión autónoma debida a las alteraciones bruscas en el nivel de confianza de los empresarios, es posible dotar a la política fiscal un papel predominante. Con pleno empleo,
el mercado de bienes y el mercado de dinero se desconectan porque desaparece el componente especulativo del dinero. Bajo tales condiciones, la velocidad de circulación del dinero es alta y estable. Por el contario, cuando el dinero cumple el papel de depósito de valor por a sacudida de fiebres especulativas se produce la venta masiva de activos; la cotización de las empresas cae en picado porque caen las expectativas de ingresos; el empleo se desploma. El consumo hace lo propio al hacerlo el ingreso, y con ello el proceso inicial desencadena una serie de choques adversos en un círculo vicioso. Solamente el gobierno puede rescatar a la economía de esta situación, por medio de políticas públicas que reactiven la demand agregada, y con ello la producción y el consumo.   

Dicho esto, introducir el dinero en la teoría económica con principios microeconómicos robustos no es una tarea sencilla. En la época de Keynes, era materialmente imposible. Al menos podemos deducir, debido a los dos teoremas del bienestar económico que se enseña en los cursos de licenciatura, que el dinero solo puede darse en economías con *fallos de mercado*. En realidad, todas las hipótesis que definen los mercados competitivos fallan: el uso del dinero está estrechamente ligado con la presencia de factores inciertos que afectan a la toma de decisiones: su uso resulta especialmente provechoso en contextos caracterizados por la incertidumbre y la información asimétrica. Además, el dinero reduce los costes de transacción al eliminar el trueque. El dinero efectivo, esto es, aquel que con carácter general podemos o deseamos tener literalmente en el bolsillo con mayor o menor fortuna, se emite en las economías actuales bajo un régimen monopolístico y garantizado por leyes y regulaciones muy concretas y estrictas. El monopolio de emisión de la base monetaria por parte de los bancos centrales no ha sido en absoluto una constante en la historia. Tampoco el efectivo es la única fuente de dinero generalmente aceptado. Pero es un dato general en todas las economías del planeta, y se justifica en los libros a raíz de otros fallo de mercado: la presencia de externalidades de red, con ejemplos tan destacables como el mismo patrón oro, o la economía internacional basada en el dólar, ya sea bajo el criterio de convertibilidad (al oro) o después de ella, tras la citada crisis de Bretton Woods. Existen más externalidades positivas, y según la obra de Keynes podemos adivinar la posibilidad de externalidades negativas, especialmente bajo fiebres especulativas con potencial para crear la misma incertidumbre que el dinero debería por su propia construcción contribuir a erradicar.

Tales complicaciones pueden resolverse con mayor claridad si contemplamos un fallo adicional de mercado: el dinero tiene un carácter doble de bien privado y público. El primero de estos atributos es obvio; el segundo conlleva la construcción de una infraestructura tecnológica que facilita unas transacciones que no están garanizadas por ningún subastador walrasiano. 

En la primera sección recordaremos algunos conceptos básicos con la finalidad de contextualizarlos en la esfera social y política. Posteriormente pasaremos a analizar los componentes de demanda y de oferta

## Dinero, Crédito y Trueque

El dinero es una unidad de cuenta medio de pago generalmente aceptado que evita la doble coincidencia de intereses precisa para que se pueda producir el trueque o intercambio puro. No es necesaria, como lo demuestra la historia en numerosas ocasiones, dotar al dinero del atributo jurídico de curso legal para que ejerza sus funciones. Incluye, además del dinero en efectivo, por su propia definición los saldos de las cuentas corrientes, cheques de viaje y otros activos líquidos en función del indicador (hay varios de ellos) con el que necesitemos trabajar. 

Si tenemos en cuenta que los primeros documentos escritos en Sumeria ya hacían mención a unidades de cuenta, basadas en el trigo, y a un buen número de normas jurídicas de regulación comercial, parece obvio que el dinero se remonta a etapas prehistóricas. Si incorporamos en la definición del dinero atributos simbólicos, tal y como es común en la antropología económica, no podríamos remontarnos a los orígenes del dinero sino a patir de tiempos muy remotos, en lo aquel tendría conexiones muy estrechas con la religión y el poder. De hecho, en la historia antigua el crédito se emitía desde los templos o en los palacios, que constituyeron los ejes de articulación política de las primeras ciudades. En templos y palacios se encontraban los escribas; más tarde, ya en el siglo XVII en los países anglosajones, los escribanos, junto a los orfebres, formaron los primeros bancos de depósitos

Algunas características físicas son necesarias para que un activo pueda cumplir el papel de dinero como alternativa al trueque: aquel debe ser ligero, manejable, divisible y escaso. Por ejemplo, no valdría un elemento pesado o incómodo de transportar, pegajoso o demasiado abundante como las piedras comunes. El dinero ha adoptado diversas formas, de acuerdo siempre al nivel tecnológico del momento: bienes, metal, papel, depósitos bancarios, y desde los últimos diez años también criptomonedas. Nunguno de estos progresos excluye definitivamente al resto y ninguno es un resultado trivial, sino la consecuencia de desarrollos tecnológicos muy notables como el uso de los metales, del papel, de la imprenta, y desde la última década, también se han añadido herramientas de computación o de técnicas de encriptación hasta el punto de hacer posible, sobre el papel al menos, la existencia de sistemas monetarios descentralizados.

Sin embargo, estas características no son suficientes para dotar a un bien el atributo de dinero. Para ello es necesaria la *aceptación general*, lo cual equivale a un código de creencias comunes. El mundo actual, ya desde la caída del régimen de Bretton Woods a principios de los años 70, se rige por un mundo de dinero fiduciario (*fiat money*), que indica por su propia etimología la confianza como elemento de su definición, lo cual no quiere decir que antes de la crisis de Bretton Woods no fuera necesario compartir un conjunto de creencias para establecer una economía propiamente monetaria. 

A lo largo de la historia de Occidente, han coexistido el dinero metálico y el crédito con el trueque hasta bien entrado el siglo XIX. Los primeros bancos de hecho están ligados al comercio internacional y a la emisión de pagarés, letras de cambio, títulos de crédito y depósitos que posibilitaban transacciones a gran escala. Esta era la regla común en las principales rutas comerciales del Mediteráneo, así como en las ferias internacionales al menos desde el siglo XIII. En tierras de Arabia se sabe que ya se usaban instrumentos muy similares a las letras de cambio desde el VIII de nuestra era. En épocas posteriores, alrededor del siglo XVII, los orfebres jugarían un papel predominante en la formación de los primeros bancos, principalmente en las economías anglosajonas, y muy especialmente Inglaterra, que estaban comenzando su hegemonía mundial. En sus comienzos, los bancos no creaban títulos convertibles en efectivo, ya que no se utilizaban sus depósitos para otorgar créditos a terceros, como sucede en el sistema de reservas fraccionarias que predomina actualmente. Sin embargo, las letras de cambio podían saldarse por terceras personas, generando cadenas de pagos transfronterizas que materializaban complejas redes de transacciones internacionales.

Ya en el siglo XVIII, sobre todo en eṕocas de auge económico, proliferó en Europa Occidental la práctica por parte de los bancos comerciales de extender unas notas promisorias sobre compañías afiliadas o sucursales, similares a los pagarés, pero compensadas con la venta de una letra de cambio girada por la parte acreedora. El objetivo de estas operaciones podía ser la obtención de créditos regulares y por lo tanto fomentar la eficiencia. Mas no era siempre el caso: Adam Smith ya alertó acerca de estas operaciones financieras podían disfrazarse de letras de cambio ordinarias, fomentando la opacidad en ciertos ámbitos del mundo corporativo.

Pe Estos efectos externos han propiciado el establecimiento paulatino de monopolios de emisión, que en la actual se lleva a cabo por los bancos centrales. Antes de proceder a su análisis, creemos conveniente definir las funciones que cumple el dinero. 


## Demanda

Las funciones del dinero son, lógicamente, los argumentos racionales para postular la función de demanda de saldos reales establecida en la curva IS-LM:

- **Unidad de cuenta** El dinero sirve como unidad de medida para fijar el valor de las mercancías, de los servicios, así como de los acuerdos contractuales que se llevan a cabo normalmente en la vida social, como los impuestos, para contabilizar la hoja de balance de una empresa o de un estado. En la medida esta función incluye también los contratos de deuda, se dice que el dinero sirve de estándard para los *pagos diferidos*. Asimismo, no debe subestimarse la capacidad del dinero, como unidad de valor para generar información pública a través del sistema de precios, pues recuerden que el subastador walrasiano no deja de ser una ficción teórica, por muy útil que resulte.
- **Medio de pago** El dinero se utiliza para el intercambio de mercancías, servicios, activos. En este sentido se dice que el dinero se demanda por el **motivo de transacciones**. En otras palabras, se reducen los costes de transacciones, lo cual repercute en una mejora de la eficiencia, por lo menos con respecto al trueque. Por motivos de exposición, vamos a incluir en esta partida exclusivamente los pagos regulares. Existen una serie de gastos monetarios que tienen lugar de forma imprevista, que por tanto no estarían sujetos al motivo de transacciones. Los activos que cumplen esta función son conocidos como *activos líquidos*.
- **Depósito de valor o precaución** El dinero es un activo más, como lo puede ser un árbol, un libro o un título financiero. Un activo no es más que un depósito de valor, y como tal el dinero cumple esa función, que no es otra que la de asignar consumo intertemporal a lo largo del ciclo vital de una persona, incluyendo su progenie. Parte de las transaciones están sujetas a imprevistos, ya sea por el lado del gasto o del ingreso, susceptibles de alterar significativalemnte la demanda de dinero. 

- **Especulación** Keynes incluyó este componente o motivo en la demanda de dinero en su *Teoría General*, en clara ruptura con la teoría cuantitativa (clásica). La especulación es una cualidad general propia de los activos, y cuando se produce genera las burbujas que mencionamos en la Introducción del capítulo anterior. El motivo de especulación se resume en aquel que tiene lugar sobre la base de posibles revalorizaciones o devaluaciones futuras del activo, en este caso, el dinero. Esto quiere decir que si el público advierte nubarrones negros en el futuro, puede aumentar su demanda de dienro antes de que el peligro ni siquiera se avecine. Aunque Keynes no lo expuso de esta manera otros autores neokeynesianos sí que lo hicieron, ya asumiendo la crítica de Lucas y formalizadas adecuadamente las expectativas sobre acontecimientos futuros (*forward-looking expectations*). Este sería un caso especial de las profecías autocumplidas (*self-fulfilling prophecies*), porque un aumento en la demanda de dinero conducente a un colapso en la velocidad de circulación del dinero produce los nubarrones anticipados, probablemente sin otra causa más que el propio desplazamiento exógeno en las creencias. 

A pesar de estas consideraciones, Keynes respetó la *ausencia de ilusión monetaria*, ya impuesta en los autores clásicos. Esta hipótesis indica que la demanda de dinero de un individuo se determina en términos reales, esto es, de acuerdo a su poder adquisitivo. Esto quiere decir que cada peso que una unidad económica mantiene en su cuenta corriente o en su bolsillo debe medirse en relación al nivel de precios vigente en los mercados.

Estamos es condiciones de enunciar la ecuación que describe la demanda de dinero. Sus argumentos no son otros que las variables de estado del modelo, $Y, i$, los niveles de producción y tipos de interés. El motivo de transacciones, así como el motivo de precaución son capturados por $Y$; el motivo especulativo queda capurado por su relación con $i$, y refleja el coste de oportunidad de mantener dinero. Es fácil de comprender que este coste incluye los intereses nominales que se dejan de percibir por lo que Keynes denominó la preferencia por la liquidez. Analíticamente, la demanda de dinero será denotada como una función, en nuestro caso y sin pérdida de generalidad, lineal:

$$
L(Y,i)=kY-hi,
$$(eq:L)
donde $k$ y $h$ son dos parámetros positivos.

La curva LM es una ecuación de equilibrio en el mercado de dinero. Recordemos que en ausencia de ilusión monetaria, $L$ está denominada en unidades reales. Teniendo en cuenta este hecho, denotemos por $P$  y $M$ el nivel de precios y la cantidad de dinero en circulación en un período determinado. En equilibrio, debe cumplirse la siguiente igualdad:

$$
\frac{M}{P}=kY-hi
$$(eq:M)

Esta ecuación, junto con la IS definida en el capítulo anterior, determina el modelo IS-LM. En total, lo componen cuatro parámetros de comportamiento, dos variables endógenas ($Y, i$) y tres variables exógenas ($A, M, P$) que podemos reducir a dos, definiendo la oferta de dinero en términos reales $m=\frac{M}{P}$ (ausencia de ilusión monetaria).

En realidad, esta economía tiene un activo más, porque la compra o venta de dinero significa necesariamente el intercambio de activos. Por su naturaleza estática, este activo es un título de renta fija, es decir, un bono. Em otras palabras, la demanda de saldos reales (\ref{eq:L}) define la demanda de bonos como una función creciente del tipo de interés. Este mercado, así como el de otros activos, los vamos a abordar con maś detalle en capítulos próximos. A continuación nos vamos a conformar con demostrar que la solución del modelo IS-LM garantiza el equilibrio en el mercado de bonos: sea $B$ la oferta total de bonos, supuesta fija, la riqueza en manos del público está dada por $W = M + B$. Recordemos que $M$, al igual que $B$ está dada exógenamente, por lo que $W$ también es un dato exógeno. Sean los excesos de demanda de los mercados de dinero y de bonos, respectivamente, 

$$
\begin{align}
z_m &= L(Y,i)-\frac{M}{P} \\ 
z_b&=\frac{W}{P}-L(Y,i)-\frac{B}{P}
\end{align}
$$

Sumando términos y haciendo uso de la definición de $W$, concluimos que la suma de excesos de demanda de los mercados de boos y dinero es nula: 

$$
z_m+z_b=0
$$

Esta igualdad implica que el equilibrio  en uno solo de los mercados de activos garantiza el equilibrio en el mercado de bonos. Este es un caso particular de la Ley de Walras, según la cual la condición de equilibrio en un mercado con $n$ componentes (activos o bienes) se garantiza con el equilibrio de todos los bienes excepto uno, que podemos interpretar como el *bien numerario*, o aquel que sirve como unidad de cuenta. Este resultado garantiza la existencia de sistemas de precios relativos, establecidos en relación de unos bienes respecto a otros. Tambien nos indica que, ante la presencia de activos adicionales a los bonos, y teniendo en cuenta el la discusión previa, deberíamos considerar los costes en términos que en términos de cálculo tal ejercicio conlleva. 

## Oferta de Dinero

### Consideraciones generales

Hemos constatado en la [Introducción](#intro) que el sistema bancario bajo el cual se articula el proceso de creación de dinero es el resultado de un largo proceso evolutivo. Y aunque sus orígenes sean muy anteriores al desarrollo de las primeras ciudades y de los primeros textos escritos, para comoprender el concepto del dinero tal y como lo conocemos actualmente debemos remontarnos a la era medieval. En las ferias se materializaba periódicamente el comercio internacional, donde se empezaron a anotar registros contables para saldar cuentas de una manera rápida y efectiva, y que a su vez promovieron la proliferación de instrumentos de crédito. Hay que tener en cuenta que el simple hecho de verificar una suma dada de dinero en metálico podía llevar  un tiempo considerable de trabajo. Ya a partir del siglo XIII, los principales centros financieros internacionales del medievo europeo estaban concentrados en Italia, cuya península desde la caída del Imperio Romano y hasta la Unificación iniciada a mediados del siglo XIX  estaba dividida en ciudades estado, autoorganizadas por elites de aristócratas, comerciantes y banqueros. Los puertos italianos se habían consolidado en el Mediterráneo, que abría sus rutas comerciales hasta las Indias Orientales; y su predominio en Europa no se vería amenazado hasta finales del siglo XVI. Para entonces iba a aparecer una República recién independizada de España: Holanda. No por casualidad, en estas regiones se van a producir los primeros intentos de consolidar una banca pública. 

En Venecia existía una *Camera del Frumento* (trigo), fundada en 1282, de carácter público, cuyo objetivo consitía en garantizar el suministro de grano para abastecer a la población. La Camera comenzó a emitir deuda y depósitos, algunos de ellosforzados, como en el caso de las dotes. A lo largo del siglo XIV, este sistema de banca pública fue paulatinamente sustituido por la iniciativa privada, dando lugar a episodios de inestabilidad financiera. Tras doscientos años de debates acerca de la necesidad de establecer un banco público con la función de prestamista de última instancia, se acabó fundando el Banco del Giro en el año 1524: una concesión pública que proporcionaba el monopolio de emisión de depósitos. En 1619, tras un cambio en los estatutos, el Banco del Giro se integraba como una institución permanente del estado veneciano. Es cierto que se había esfumado la etapa de esplendor de las repúblicas italianas, pero este episodio dejó la impronta de lo que probablemente fuera la primera experiencia de dinero fiduciario insitucionalizada. 

Los sistemas monetarios constituyen en su esencia una infraestructura, crecientemente compleja, que posibilita los pagos y las transferencias necesarias para el comercio tanto interno como doméstico que se efectúan en los estados. En la práctica, los bancos son centros públicos que amplían la magnitud y el alcance de las cadenas de pagos necesarias para la materialización del comercio. Algunos de ellos comenzaron a ejecutar funciones políticas. . Puede afirmarse en sentido abstracto que forman una 

Las ciudades de Amsterdam y Hamburgo encaraban problemas análogos a comienzos del siglo XVII. El Banco de Amsterdam (*Wisselbank*) se fundó al poco tiempo de la independencia de las Provincias Holandesas, en 1609. Holanda es una República pequeña, pero a través de las Compañías de las Indias, logró establecer un vasto imperio colonial. Como todo país pequeño, incluidas las repúblicas italianas, su sistema monetario estaba inundada de monedas, muchas de ellas degradadas, e instrumentos de pago de muy variada procedencia. El banco de Amsterdam se fundó en 1609 con la capacidad de emitir papel moneda una vez recicladas las monedas de mala calidad. En general, el dinero degradado es lógicamente fuente de inflación, y en consecuancia también lo puede ser de pobreza; y susceptible de generar desequilibrios económicos, financieros  Este dinero fue convertible en especie solo hasta 1684.  Se habían impuesto mecanismos de incentivos para universalizar el uso de los depósitos, al exigir el canje de las letras de cambio en sucursales bancarias, pero las comisiones eran desproporcionadamente altas para lograr una demanda generalizada. El caso de Hamburgo es tal vez menos conocido; sin embargo, de todos lo ejemplos citado, fue el único superviviente de las guerras napoleónicas. Debido a una serie de problemas, en 1770 se convirtió en el primer caso de dinero convertible en lingotes (*ingot standard*). Previamente, había asumido su papel de prestamista de última instancia en una crisis bancaria. En 1876, cinco años después del establecimiento del Imperio Alemán, se fundó con el Reichstag, que era el banco de Prusia.





Al igual que el Banco de Inglaterra, también 
pero las cuptas Adam Smith señaló las diferencias existentes entre los sistemas monetarios según el tamaño de la nación:  


 Esteo

### Agregados Monetarios
El dinero emitido por los bancos centrales en la economías actuales se denomina **base monetaria** ($H$) y consiste en los monedas y billetes en circulación de curso legal. La emisión se realiza bajo régimen de monopolio en la práctica totalidad de los estados contemporáneos. En sistemas de reservas fraccionarias como los actuales, el banco central suele fijar un coeficiente mínimo de reservas que los bancos deben mantener en forma de efectivo para asegurar la cadena de pagos, y evitar ruinas bancarias. Por lo tanto, la base montaria la podemos descompner en dos elementos: una, en manos de particulares, que denotaremos por $E$, y otra en forma de reservas bancarias $R$, que sirven para hacer frente a las demandas de efectivo los que ususarios de un banco pueden requerir contractualmente como contraprestación a sus depósitos. Parte de estas reservas pueden estar en forma de depósitos a cargo del banco central. Es decir,

$$
H = E + R
$$(eq:H)

La base monetaria agrega el pasivo del balance contable de los bancos centrales. El activo del balance está compuesto esencialmente por títulos gubernamentales e instrumentos de crédito. después de la crisis de 2007 surgieron numerosas herramientas especiales de crédito enfocadas en sectores específicos, así como la compra de títulos respaldados por hipotecas y otros activos. Estas operaciones fueron realizadas con el fin de rescatar el sistema financiero en su conjunto, incluidos bancos de inversión de renombre como el *Lehman Brothers* y requieren un análisis en un capítulo aparte. Lo que sí se puede decir es que la expansión de la hoja de balance de los bancos centrales de la práctica totalidad de los países del mundo ha sufrido en mayor o menor medida un aumento sin precedentes que dura hasta nuestros días. En la literatura anglosajona se conocen con el nombre de *quantitative easing*,  Una hoja de balance de un banco centra genérico puede resumirse de la siguiete manera.

<center>


|                  |  Banco Central|                |
| :---             |                    ----:  | -------------: |
| Crédito          |               | Efectivo ($E$) |
| Títulos          |               | Reservas ($R$) | 
|                  |               | Patrimonio neto|
\vspace{.1cm} 

<center/>

En una economía cerrada existen solamente dos maneras de alterar la cantidad de base monetaria: mediante las operaciones de descuento y mediante las operaciones de meracado abierto. Las primeras destacan el papel de los bancos centrales como pretamista de última instancia. Sin embargo, con el el fin de garantizar la estabilidad del sistema de pagos, en la práctica los bancos centrales desincentivan esta práctica, estableciendo una prima sobre los tipos de interés de descuento. De esta manera, los bancos centrales controlan la cantidad de dinero en circulación a través de operaciones en el mercado abierto. El mercado abierto, o mercado secundario, es el conjunto de mercados en los cuales se negocia la compraventa de títulos financieros ya consolidados en el mercado. En los mercados primarios, por el contrario, en las IPO's (*initial public offerings*) es la entidad emisora la que recibe el monto de las ventas. En las operaciones de mercado abierto las compras (ventas) de títulos en una catidad determinada, usualmente letras y bonos del tesoro, conllevan aumentos (disminuaciones) en la oferta monetaria de la misma magnitud.
    
Como se ha señalado a lo largo del capítulo, a la base monetaria debemos añadirle los depósitos bancarios $D$ para completar nuestra definición de dinero. Es decir,
    
$$\label{eq:mbd}
M = E+D = E+D
$$(eq:MED)

El resto del pasivo del sistema bancario consolidado es similar al de cualquier empresa: debido a su tamaño, los bancos suelen financiarse con bonos y acciones. Los títulos preferentes conllevan privilegios similares a las acciones, pero a diferencia de estas, no forman parte del patrimonio neto de una compañía. El activo del sistema bancario consolidado está formado esencialmente por créditos, reservas, títulos de otras compañías, y el inmovilizado. 
 
<center>

|                  |  Bancos  |           |
| --------         | ---------| ----------|
| Crédito          |          | Depósitos ($D$) |
| Reservas ($R$)   |          | Bonos     | 
| Títulos          |          | Títulos Preferentes|
| Inmovilizado     |          | Patrimonio neto    |
    
<center\>
 
La composición de los activos bancarios está estrictamente regulada, con el claro motivo de evitar quiebras regulares. Los créditos que financian proyectos de inversión pública o privada tienen un período de maduración a considerablemente largo y en sujetos en diferente medida a riesgos de impago. En cambio, los depósitos son a la vista, pues en caso contrario no podrían ser catalogados como dinero (*líquidos*). Esta disparidad de plazos es la fuente primordial de incertidumbre del sistema monetario, y la que justifica las regulaciones mencionadas. Algunas de estas regulaciones, como los [Acuerdos de Basilea](https://en.wikipedia.org/wiki/Basel_III),  ni siquiera tienen carácter vinculante. A pesar de ello, sus directrices y estándares son aprobados por los principales bancos centrales del mundo. 
    
Antes de concluir esta sección vamos a comprobar que, desde el punto de vista meramente contable, el dinero, así como los instrumentos financieros en general, no constituyen riqueza neta. En este sentido debe entenderse el velo monetario clásico. Si observamos la hoja de balance consolidada de los particulares, ni el dinero, ni, como es obvio, el crédito, forma parte del total de activos que constituyen la riqueza de una nación, dado que el saldo total de la hoja de balance de un pais, o la suma de las hojas de los balances del banco central, de los bancos privados, y de los particulares se reduce a la suma de sus activos reales, incluyendo por supuesto los intangibles. 

    
<center>

|                  |  Particulares  |           |
|   -----:         |   :----:       | ----------|
| Efectivo ($E$)         |                | Crédito   |
| Depósitos ($D$)  
| Bonos
  Títulos preferentes|           | 
| Activos no financieros|           |            |
    
<center/>  

### El Multiplicador Monetario

Para determinar la oferta de dinero en un sistema de reservas fraccionarias, debemos antes definir las reglas de comportamiento que definen la composición de efectivo y reservas en relación a los depósitos. de momento vamos a  suponer que la preferencia por la liquidez de los particulares los conduce a mantener una proporción aproximadamente estable de efectivo en relación a las cuentas corrientes, cheques bancarios u otros instrumentos de pago ofrecidos por las instituciones financieras. Como es natural, esta variable está sujeta a variables estacionales. Por ejemplo, en determinados períodos festivos es previsible que $e$ registre valores por encima de su promedio anual. Denotando por $e$ a este coeficiente, 

$$ 
e=\frac{E}{D}.
$$(eq:e)

Con motivo de la recesión global que sacudió en 2007, los bancos centrales comenzaron a ofrecer intereses a los reservas bancarias. Esta medida ya había sido promovida, entre otros autores, por Milton friedman, para compensar la el uso ineficiente de estos activos líquidos. En esta ocasión, los tipos de interés se habían reducido a niveles negativos, impidiendo a los bancos centrales hacer uso de las herramientas ordinarias de política monetaria para contrarrestar de manera efectiva los efectos nocivos de la crisis. Este problema se hacía especialmente grave en aquellos países que heredaban volúmenes de deuda soberana importantes, debido a que su capacidad para utilizar los estabilizadores automáticos estaban muy condicionados por el presupuesto público. Esta innovación añade un estímulo adicional al encaje bancario, o coeficiente de caja obligatorio.

Resumiendo, podemos descomponer el coeficiente de reservas $r$ del sistema bancario en dos elementos: el encaje bancario o $\rho$ y el componente voluntario $\nu$; es decir,

$$
r = \rho + \nu = \frac{R}{D}
$$(eq:r)

Si combinamos las expresiones {eq}`eq:MED`, {eq}`eq:e`, y {eq}`eq:r`, obtenemos una relación entre la base monetaria (*high-powered money*) y la oferta monetaria total:
    
$$
\frac{M}{H}=\frac{1+e}{e+r}=\frac{1+e}{e+\rho + \nu}\equiv \mu
$$(eq:mul)
    
El parámetro $\mu$ es conocido como el **multiplicador monetario** en un sistema de dinero fiduciario. El multiplicador monetario es una función de $e$ y de $r$. Antes de analizar esta expresión en su totalidad, vamos a comprobar que contiene como dos casos extremos un sistema de reservas fraccionario puro, así como el sistema de dinero convertible en especie. En el primero de los casos ($e=0$), (\ref{eq:mul}) se simplifica en la siguiente expresión, una vez que defiimos por comodidad, $r=1-\alpha$:
    
$$
\mu = \frac{1}{r}=\frac{1}{1-\alpha}=\sum_{n=0}^{\infty}\alpha^n.
$$(eq:mul_0)
 
En este caso, el multiplicador alcanza su valor máximo, para un valor fijo de $r$. Este ejemplo sirve entre otras cosas para ilustrar el multiplicador como la consecuencia de una cadena de créditos concedidos por el sistema bancario ante una variación exógena de la oferta monetaria.  Bajo un sistema monetario convertible ($r=1$), los bancos son meras instituciones de depósito. Resulta inmediato verificar que $\mu =1.$ Es decir, no hay efecto multiplicador.
    
Antes de 2007, su nombre estaba plenamente justificado, porque las reservas no creaban intereses. Sin embargo con motivo de las medidas extraordinarios llevadas a cabo por los principales bancos centrales, destinadas paliar la crisis financiera global, los intereses pagados a las reservas elevó el componente voluntario de reservas, que inicialmente era prácticamente nulo. Como puede apreciarse a partir de {eq}`mul`, un aumento considerable en $\nu$ reducirá el multiplicador monetario $\mu.$ Si valor de las reservas es lo suficientemente alto, como ha sido y es el caso en numerosos países, el valor de $\mu$ puede caer por debajo de la unidad, dejando su nombre en entredicho. 
    
Este factor ha contribuido sin lugar a dudas a amortiguar los efectos potencialmente inflacionarios de las diversas políticas de relajación monetaria anteriormente mencionadas. Otro factor ha consistido en la reducción de la velocidad de circulación monetaria, con efectos que perduran hasta la actualidad. De hecho, ambos factores han justificado la decisión de las autoridades monetarias a fin de evitar males mayores. El efecto contraproducente más claro de estas medidas consiste en la socialización de las pérdidas de los grandes bancos, a menudo originadas por la presencia de conflictos de intereses y el uso de información asimétrica. La justificación de estas medidas no es otra que la de evitar males mayores, respetando el papel de los grandes bancos (*too big to fail*) como proveedores de un bien público, pues de esto se trata el dinero al convertirse en objeto de política económica.


```{jupyter-execute}

```

```{code-cell} ipython3
import matplotlib.pyplot as plt
import numpy as np
from sympy import symbols, lambdify, Min, Max

R, i = symbols('R i')
i_star = 7
alpha = 10
i_d = 4 
i_r = 3
R_0 = .5
Rmin, Rmax = R_0*.5, R_0*1.5
imin, imax = 2, i_d+.5
size = 100
R_grid = np.linspace(Rmin,Rmax,size)
point_supply = (R_0-Rmin)/(Rmax-Rmin)
point_supply2 = (i_d-imin)/(imax-imin)
i_grid = np.linspace(0,i_d,size)
def reserve_demand(x, i_star=i_star, i_r=i_r, alpha=alpha):
    y = []
    for j in x:
        y.append(max(i_star - alpha*j, i_r))
    return y

def reserve_demand2(x, i_star=5, i_r=i_r, alpha=.25):
    return Max(i_star - alpha*x, i_r)
```

```{code-cell} ipython3
point_supply
```

```{code-cell} ipython3
fig, ax = plt.subplots()
ax.axvline(x=R_0, ymin=0, ymax=point_supply2, color='DarkBlue')
ax.axhline(y=4, xmin= point_supply, xmax=1, color='DarkBlue')
ax.plot(R_grid, reserve_demand(R_grid), color='orange')
ax.set_xlim(Rmin, Rmax)
ax.set_ylim(imin, imax)
```
