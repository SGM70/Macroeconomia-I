---
jupytext:
  formats: ipynb,md:myst,py:hydrogen
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

# El Modelo IS-LM (I):  Equilibrio en el Mercado de Bienes y Servicios
<a id=’cap_1’></a>

+++

## Introducción
<a id=’intro’></a>

El modelo IS LM se desarrolló de manera casi inmediata a la publicación del la *Teoría General* de [John Maynard Keynes](https://en.wikipedia.org/wiki/John_Maynard_Keynes), escrita en el año 1936 y viene a desarrollar, si bien de manera imperfecta, sus ideas fundamentales. Este libro señala para muchos autores el comienzo de la macroeconomía, y aunque se puede discutir la autoría particular, no cabe duda de que la época histórica de la Teoría General costituye el caldo de cultivo perfecto para el desarrollo de teorías macroećonómicas. Conviene señalar que el modelo IS-LM de corto plazo, en respuesta fulminante a las formulaciones neoclásicas predominantes en su fecha. El modelo clásico, punto de mira de la crítica de Keynes, está formado por cuatro elementos fundamentales: el mercado de bienes, el mercado laboral, el mercado de dinero y el patrón oro bajo el cual se articuló durante una buena parte de los siglos XIX y hasta la II Guerra Mundial. En el mercado de bienes, [la ley de Say](https://es.wikipedia.org/wiki/Ley_de_Say), las condiciones de producción determinan los niveles de ingreso, producción y empleo. Esta ley va a excluir la posiblidad de desempleo involuntario toda vez que los mercados de bienes y servicios, así que el mercado de trabajo, operen bajo condiciones perfectamente competitivas. El mercado de dinero se rige por la teoría cuantitativa, la cual remonta sus orígenes a las penurias económicas causadas por la inflación creada en los países de Europa Occidental que, en el siglo XVI presenciaron un aumento sin precedentes causados por la reducción en sus costes de producción, debido a una serie de factores que no vamos a discutir aquí por razones de espacio. La teoría cuantitiva por su parte da lugar a la proposición de [*neutralidad del dinero*](https://es.wikipedia.org/wiki/Neutralidad_del_dinero), también conocida como *dicotomía clásica*, que establece una separación entre los mercados de bienes y el mercado de dinero. O lo que es lo mismo, la cantidad de dinero en circulación no afecta a la asignación de recursos a largo plazo. En su versión relativa, la magnitud relevante no es el total, sino la tasa de crecimiento del dinero en circulación, pero el principio viene a ser el mismo. 

Tras un largo desarrollo de ideas poco formalizadas, fueron [Alfred Marshall](https://en.wikipedia.org/wiki/Alfred_Marshall) e [Irving Fisher](https://en.wikipedia.org/wiki/Irving_Fisher), de manera independiente desde sus escuelas respectivas de Cambridge y Yale, quienes le dieron un versión definitiva, con ligeras diferencias de exposición. Esta teoría explica la inflación a largo plazo como una magnitud proporcional a la tasa de crecimiento de la oferta de dinero en circulación. Esta es una implicación del postulado de que la velocidad de dinero en circulación es constante, sin perjuicio de las oscilaciones que pueda sufrir a corto plazo. El principio del [*laissez faire*](https://en.wikipedia.org/wiki/Laissez-faire) garantizaría por sí misma la estabilidad de los principales agregados económcos. El gobierno debería limitarse equilibrar el presupuesto público, por una parte, y a mantener la estabilidad monetaria garantizada por el [patrón oro](https://en.wikipedia.org/wiki/Gold_standard) y Como consecuencia de la misma, se cumple el principio de neutralidad monetaria. Este principio, combinado con la ley de Say, nos viene a decir que el potencial económico de un país depende fundamentalmente de sus recursos económicos; plena industrialización, el capital físico asumiría, al menos *a priori*, un papel relevante. Los desequilibrios causados por las oscilaciones de las variables monetarias tenían por lo tanto efectos transitorios, debido al carácter intrínsecamente autoregulador, homeostático, de los mercados libres de fricciones. Estas últimas están causadas, en buena medida y siempre de acuerdo con la escuela neoclásica, por el excesivo nivel de intervención pública, o de colusión empresarial que alterar la asignación de recursos de una nación. Los desequilibrios originados en el seno de los mercados de internacionales disponían de los mecanismos estabilizadores propios del patrón oro, como se ha señalado con anterioridad. Las entradas de dinero de un país con superávit en la balanza comercial se verían tarde o temprano compensadas por la pérdida de competitividad originada por los ajustes al alza en el nivel de precios.

<img src="../images/GD.jpg" alt="drawing" width="400"/>

La visión de Keynes es diferente, pero más que por principios, por una cuestión de enfoque. En efecto, fue alumno de Marshall en Cambridge y se adcribió a la teoría cuantitativa del dinero antes del advenimiento de la [Gran Depresión](https://es.wikipedia.org/wiki/Gran_Depresi%C3%B3n). Sin embargo, este acontecimiento lo urgió a cambiar su propia doctrina, basada en una visión a corto plazo. Uno de los hechos más relevantes, consistía en la desesperación masiva producida por el desempleo y las empresas que por todos los rincones del mundo se encontraban en quiebra. Esta situación tuvo además efectos persistentes, en contradicción con las premisas de la doctrina neoclásica. Y, lo que no es menos importante, trascendió a todos los ámbitos de la sociedad y de la política. Surgieron regímenes totalitarios en Europa Occidental que dieron al traste con las libertades políticas e individuales y alteraban de manera sustancial los mecanismos de asignación de recursos. Tales desarrollos espantaban a Keynes, hasta el punto de que algunos autores sostienen que la macroeconomía surgió, por lo menos parcialmente, como respuesta a esta circunstancia. El hecho que sí están comúnmenmente aceptados, y cuyas causas últimas se llegaron a convertir en el [Santo Grial](https://fraser.stlouisfed.org/files/docs/meltzer/bermac95.pdf) del conocimiento macroeconómico, es que la gran Depresión es una crisis de demanda. En caso contrario no podría comprenderse la deflación asociada a la crisis. Irving Fisher advirtió a los efectos devastadores de la deflación sobre el sistema de pagos originados por la devaluación de los instrumentos de deuda (*debt deflation*), que al estar denominados en términos nominales, alteran la distribución de la renta en favor de las unidades deudoras a medida que se deteriora el tejido productivo. 

En cualquier caso, la idea de Fisher no cuajó hasta tiempos mucho más recientes, ya después de la decadencia del modelo IS-LM que estamos analizando, y de la que hablaremos más tarde en este capítulo de manera muy breve. Este es un modelo de desempleo, y en ese sentido se desmarca del modelo clásico. Pero también lo integra como un caso particular, aceptando sus implicaciones bajo pleno empleo. Las implicaciones en términos de política son enormes según la economía se rija de acuerdo a un régimen u otro: en economías con desempleo involuntario, otorgando un papel previamente inexistente al estado para aplicar los estabilizadores automáticos capaces de corregir los desequilibrios causados por el lado de la demanda. En concreto, se abría la puerta para la intervención estatal por medio de políticas fiscales expansivas, que cobraban generalmente la forma obras públicas e infraestructuras. Bajo el régimen clásico, la Ley de Say indica por el contrario que las condiciones de oferta son las determinantes del nivel de empleo y producción a largo plazo. El principio de neutralidad monetarioadotaba por el contrario a los bancos centrales un papel relevante para el control de la inflación.

La ley psicológica fundamental de Keynes, que definiremos en la [sección 2](#is) de este capítulo, así como la función de inversión privada están detrás de esta inversión causal. La primera relaciona el consumo agregado con el ingreso disponible (neto de impuestos). En el sistema clásico el consumo está determinado por factores de elección intertemporal, al estarlo el ahorro privado por pura coherencia lógica aún, si bien estos factores no formalizados aún en modelos formales. En el mercado de fondos prestables, el ahorro y la inversión determinan el tipo de interés, real, vigente en el mercado de fondos prestables. La inversión según Keynes se desmarca asimismo del modelo clásico de una manera contundente. Con los hechos recientes de la Gran Depresión como pieza clave argumental, Keynes opinaba que la inversión era altamente volátil, debido a que las expectativas empresariales y en general las creencias humanas estaban guidas de manera aparente caprichosa por instintos y emociones, que se apartaban del enfoque racionalista subyacente en el modelo clásico. Sin atacar los principios del sistema capitalista, las oscilaciones en la inversión privada tenían un efecto multiplicativo en la demanda agregada a partir de la función de consumo kenesiana anteriornmente señalada, al depender esta del nivel de ingresos, que se hallaba mermado por los choques adversos. Este fenómeno, conocido como [multiplicador fiscal](https://en.wikipedia.org/wiki/Fiscal_multiplier), añadía un toque de veracidad a la conveniencia de las obras públicas, que ya habían sido de hecho advertida por autores distintos a Keynes. Los [espíritus animales](https://en.wikipedia.org/wiki/Animal_spirits_(Keynes)) iban a prevalecer en la obra de Keynes a la [mano invisible](https://www.britannica.com/topic/invisible-hand) de Adam Smith.

La Gran Recesión que tuvo lugar en a finales del año 2007 guarda numerosas similitudes con la Gran Depresión. Ambas tuvieron su origen tras una década de euforia económica, conocidas con el nombre de [burbujas](https://en.wikipedia.org/wiki/Economic_bubble) especulativas y de orígenes remotos. Las burbujas son revalorizaciones persistentes de las cotizaciones de un activo, ya sean estos tulipanes, título de deuda soberana o hipotecas, por encima de su valor fundamental. El problema de las burbujas es doble: no se puede conocer su presencia hasta que implosionan, dado que el valor fundamental de un activo es inobservable o bien sujeto a múltiples fuentes de fluctuaciones; además siempre estallan, y cuando lo hacen, suelen dejar secuelas impredecibles y muy nocivas en la economía, con efectos propagadores que trascienden su foco. Puede afirmarse que según el pensamiento de Keynes, las burbujas, los espíritus animales y las crisis de demanda son fenómenos muy estrechamente relacionados, hasta el punto de que no pueden entenderse cada uno de ellos sin el resto. La presencia de burbujas especulativas de hecho recala lógicamente en el mercado de dinero: durante la crisis de demanda y tras el estallido de las burbujas, el público tiende a atesorar dinero en grandes cantidades, contradiciendo el mero papel de velo concedido por los clásicos. La velocidad de circulación del dinero se estanca a la par que aumenta su demanda. Estos fenómenos serán motivo de discusión del siguiente capítulo y servirán para computar la solución del modelo en función de sus parámetros estructurales.

El modelo IS-LM, como ya sabemos, es un modelo de economía cerrada a los mercados internacionales. Los precios fijos (dados exógenamente), consecuentemente con la visión de corto plazo de su autor. No obstante, se trata de un modelo de determinación simultánea del ingreso agregado (PIB) y de los tipos de interés. Estos son por la naturaleza de los mercados financieros mucho más flexibles que los precios de bienes de consumo. Habrá que esperar hasta el año 1962 a las contribuciones contemporáneas pero otra vez independientes, de [Robert Mundell](https://en.wikipedia.org/wiki/Robert_Mundell) y [Marcus Fleming](https://en.wikipedia.org/wiki/Marcus_Fleming) para extender el modelo IS-LM, de corto plazo, a una economía abierta. Unos años antes, en 1956, [Robert Solow](https://en.wikipedia.org/wiki/Solow%E2%80%93Swan_model) y [Trevor Swan](https://en.wikipedia.org/wiki/Trevor_Swan) realizaron otra extensión, si bien a costa de cancelar una de sus ecuaciones, la correspondiente al dinero, con el objetivo de analizar la tasa de crecimiento a la largo plazo de una economía con parámetros idénticos a los descritos en este capítulo. [Phillip Cagan](https://en.wikipedia.org/wiki/Phillip_D._Cagan) realizó un ejercicio similar al anterior, solo que eliminando la curva IS, para analizar el fenómeno de la hiperinflación con un modelo dinámico construído a partir de la curva LM. Todas estas contribucioes fueron a su vez los gérmenes adecuados para el desarrollo de todo un acervo de modelos que formaron la macroeconomía moderna que conocemos actualmente.

En este capítulo abordaremos el equilibrio en el mercado de bienes e introduciremos los principales componentes de la demanda agregada siguiedo las hipótesis del modelo IS-LM. Aprenderemos de paso la diferencia existente entre la representación de modelos *reducidos* y *estructurales*, distinción muy presente a día de hoy
tanto en las publicaciones teóricas como en las aplicaciones macroeconométricas. Utilizaremos este punto de partida para elaborar la [crítica de Lucas](http://people.sabanciuniv.edu/atilgan/FE500_Fall2013/2Nov2013_CevdetAkcay/LucasCritique_1976.pdf), que dio lugar a un cambio de paradigma en los modelos macroeconómicos, los cuales fueron construidos, sobre todo a partir de los años 80 y hasta la fecha, con sólidos fundamentos microeconómicos y un tratamiento consistente de las formación de expectativas por parte del público que amortiguaban, al menos potencialmente, los efectos en apariencia beneficiosos de las intervenciones gubernamentales.

## La Demanda Agregada
<a id=’is’></a>

Podemos pensar por el momento en un modelo sencillo sin sector público. De acuerdo con las hipótesis del modelo IS-LM, las ecuaciones de comportamiento vigentes en el mercado de bienes y servcios vienen determinadas por la ley psicológica fundamental de keynes y por la inversión privada 

- **La ley psicológica fundamental de Keynes**: una regla de consumo  *ad hoc*, esto es, sin premisa microeconómica de ningún tipo. En todo caso, vamos a dar por cierta la hipótesis de que el consumo es una actividad vinculada exclusivamente a las familias. Esta ley establece que el consumo agregado es una función creciente del ingreso disponible. En su versión original, Keynes pensaba que la relación entre la relación entre la propensión marginal a consumir debía decrecer a medida que aumentaba el ingreso, debido a la existencia de un componente de consumo de subsistencia, que debía ser determinado al margen de las ganancias materiales obtenidas por cualquier individuo. Sin embargo, siguiendo la tradición de los textos convencionales, y teniendo en cuenta que la introducción de un coeficiente cuadrático negativo no añadaría implicaciones serias a nuestro problema, vamos a imponer una relación lineal, o para ser más preciso, *afín*, ya que esta relación tendrá un componente independiente, llamado comúnmente, en la literatura macro, *autónomo*. La propensión marginal a consumir es un coeficiente estrictamente comprendido entre cero y uno uno, $0\geq c<1$ ($c=0$ no afecta a la lógica numérica del modelo, pero carece de sentido económico). El componente autónomo del consumo, $C_0\geq0$ puede interpretarse como un nivel de consumo de subsistencia que debe producirse para mantener la vida de las personas y que,  al margen de sus condiciones económicas, está fijado por determinantes biológicos o culturales:

$$
C = C_0 + cY
$$(eq:C)

- **La inversión privada** de bienes de produción es una relación que decrece con el coste de oportunidad de la inversión de nuevas plantas de producción y bienes de equipo. Este coste está directamente relacionado con los tipos de interés reales sumando los costes de explotación, su período de maduración, los riesgos que conlleva y la depreciación del capital. Para entender de manera precisa esta noción, habremos de descomponer los tipos reales en sus componentes. Los tipos de interés de mercado en realidad constitiyen una cesta innumerable de activos financieros de renta fija, incluidos los bonos corporativos o aquellos emitidos por organizaciones no lucrativas. Se establecen, salvo en contadas excepciones, en términos nominales, como es el caso de todas las transacciones de mercado efectuadas con dinero. La manera más directa de organizar la información disponible de los tipos de interés es por lo tanto a partir de las entidades que emiten la deuda, ya sean estas públicas o privadas, así como de su horizonte temporal. Conviene pensar en los mercados financieros como un circuito, de complejidad creciente hasta extremos difíciles de imaginar no hace mucho tiempo, que vincula los mercados monetarios y los mercados de capital. Los primeros sigien la lógca de ciclos de frecuencia alta (corto plazo), al contrario de los segundos. Dentro de esta primera consideración, los tipos de interés de referencia serían de largo plazo, superiores al año. Además, Irvin Fisher formuló por primera vez, a principios del siglo XX, la ecuación que lleva su nombre, y que descompone la los tipos de interes nominales de un título de  de renta fija $i$ como la suma de los tipos reales de ese activo $r$ y de la tasa de inflación esperada $\pi$; es decir,

$$
i = r + \pi
$$(eq:fish)
Por el momento, y en la lógica del modelo ISLM, que es estática y carece de incertidumbre, supondremos que la tasa de inflación esperada es constante. Sin embargo, en economías más cercanas al mundo real, los tipos de interés reales no son directamente observables. Habría que esperar algunos años, hasta el trabajo de Friedman y Phelps a comienzos de la década de los 60, para que la noción de expectativas cobrara una forma precisa. De acuerdo con estas explicaciones se establece que la inversión, al igual que el consumo, tiene una relación lineal con un componente autónomo $I_0\geq0$. La relación entre el coste real de la inversión está descrito por el coeficiente $b>0$. Analíticamente,

$$
I = I_0 - b(i-\pi)
$$(eq:I)

Las variables endógenas del modelo IS-LM, $Y, i>0$ son asimismo aceptables solo dentro del rango de los números positivos. La **demanda agregada** la obenemos sumando los componentes de gasto aportados por las familias y por las empresas, expresadas en las ecuaciones {eq}`eq:C` y {eq}`eq:I`, utilizando para determinar esta última variable la ecuación de Fisher {eq}`eq:fish`:

$$
DA = A + cY - b(i-\pi),
$$(eq:DA)

donde 

$$\label{eq:A}
A = C_0 + I_0,
$$(eq:A)

representa el componente *autónomo* del gasto (demanda).

En equilibrio, la oferta agregada coincide con la demanda agregada; o lo que es lo mismo,

$$
Y = A + cY -b(i-\pi)
$$(eq:eq)

La expresión {eq}`eq:DA`  es la versión reducida del mercado de bienes y servicios en el modelo IS-LM. Al final de este cuaderno aprenderán que esta representación es robusta a extensiones del modelo más realistas, siempre que se mantenga su estructura lineal y estática subyacente. Concretamente podremos añadir un sector público, y posteriormente, en el marco del modelo IS-LM-BP, un sector exterior. En todo caso, los modelos estructurales se acaba reduciendo a una versión reducida para computar sus soluciones, que en nuestro análisis particular toma la forma {eq}`eq:DA`. Los parámetros del modelo reducido  serán una función más o menos compleja de los parámetros que relacionan las variables estructurales. En este modelo sencillo, las mismas se reducen a las ecuaciones de comportamiento agregado del sector privado {eq}`eq:C` y {eq}`eq:I`. 

### Ahorro e Inversión: el Mercado de Fondos Prestables

Siguiendo con el modelo de dos sectores, nos será más sencillo capturar una relación entre ahorro e inversión que, por su naturaleza puramente contable, se mantiene en su esencia en las cuentas nacionales. Por lo tanto, nos abstraeremos de momento con las discrepancias existentes entre la doctrina clásica y la keynesiana, que en este marco simple se reduce a la ecuación de consumo {eq}`eq:C`. Nótese esta triple relación, derivadas de las ecuaciones {eq}`eq:C`, {eq}`eq:I`, {eq}`eq:fish`, {eq}`eq:eq`, la última de las cuales es la condición de equilibrio en el mercado de bienes, mientras que las dos restantes se establecen por definición, denotando $S$ como el nivel de ahorro privado:

$$
\begin{gather*}
Y =& C+S\\  DA =& C+I\\ Y=& DA.\\
\end{gather*}
$$

Esta triple igualdad, que captura el equilibrio en el mercado de bienes, puede sintetizarse en una sola, la igualdad entre la inversión y el ahorro:

$$I=S$$

Si observamos la ley psicológica fundamental de Kenyes en {eq}`eq:C`, concluiremos que el ahorro privado, en el marco de las decisiones del consumidor, cumple un papel residual, de manera que se irá acomodando al nivel de ingreso. En presencia de desempleo, un aumento en la tasa de ahorro no tiene más consecuencia que una rducción en el consumo, con ulteriores reducciones en los niveles de producción y empleo que no hacen sino agravar la situación inicial. Este hecho, conocido com la [paradoja de la frugalidad](https://es.wikipedia.org/wiki/Paradoja_del_ahorro), contradice el sistema clásico, de acuerdo con el cual el nivel ahorro nacional conduce a niveles de propesperidad a largo plazo al aumentar los fondos disponibles para la inversión. De acuerdo con ley de Say, la oferta, en este caso medido por la oferta de crédito o fondos prestables genera su propio mercado, la inversión. Además, y no por ello de manera menos importante, el ahorro contribuye a reducir el coste de financiación de las inversiones productivas privadas, ajeno a todo tipo de actividades especulativas o espíritus animales que vayan más allá del mero [arbitraje](https://en.wikipedia.org/wiki/Arbitrage).

+++

## Código
### Descripción


El código de la primera celda, con excepción de la primera línea, lo pueden archivar en un doc `*.py` e importarlo haciendo `import [nombre del módulo]`

Vamos a hacer uso de [`sympy`](https://www.sympy.org) con `Eq`, `solve` y `lambdify`

```{code-cell} ipython3
%cd /var/home/sam/Lab/intro
from pymacro.gen import *
from pymacro.relation import Linear
from pymacro.diccionarios import *
from tabulate import tabulate
from sympy import Eq, solve, lambdify, init_printing
import matplotlib.pyplot as plt
import numpy as np

init_printing()

agg_demand =  Linear(
    var=[Y,i-pi], 
    coeff=[c,-b], 
    auto=A,
    default = default_is
    )

equilibrium = Eq(Y, agg_demand.expr)
num_eq = equilibrium.subs(default_is)
is_expr = solve(equilibrium,i)[0] # Como el modelo es lineal, sabemos que solo tiene una solución
is_num = is_expr.subs(default_is) # Esta es la ecuación algebraica de la curva IS
```

```{code-cell} 
Gen(is_dict).info()
```

Exploren con `Tab` métodos y funciones disponibles. Una retahíla de ecuaciones:

* `equilibrium` La ecuación simbólica de equilibrio, todavía parcial (¡recuerden el texto de Samuelson!), en el mercado de bienes
* `agg_demand` es el lado derecho de la ecuación de equilibrio. El lado izquierdo se corresponde con la producción $Y$
* `num_eq` La misma ecuación, con valores numéricos
* `is_expr` La expresión de la curva IS, que en este caso es recta.
* `is_num` La misma expresión con los valores de los parámetros sustituidos, para elaborar el gráfico.

```{code-cell} ipython3
agg_demand.expr
```

```{code-cell} ipython3
equilibrium
```

```{code-cell} ipython3
num_eq
```

```{code-cell} ipython3
is_expr
```

### Gráficos

#### Preparando el camino

El algoritmo es bastante sencillo. La parte más complicada está en el uso de `sympy`. las funciones que uso son muy sencillas. `Eq` y `solve`, `simplify`, cuyas funciones hablan por sí solas; `lambdify` es un poco más sofisticada, pero simplemente traduce las ecuaciones abstractas a objetos susceptibles de ser cuantificados, para poder hacer el gráfico. porque con los símbolos se pueden manipular algunas operaciones, muchas, abstractas, pero no cuantificar. Todo eso en una semana lo tienes claro, y con el ejemplo, más.  

`numpy` solo se utiliza para hacer el grid del eje de abscisas ($Y$) con `linspace` e introducir en la ecuación de la curva IS, transformada previamente por lambdify para obtener el grid del eje de ordenadas (i). Ese es el algoritmo. En breve pasamos a introducir la LM, y al final de la segunda semana trabajaremos con la ecuaciones de equilibrio general (bienes y dinero).

```{code-cell} ipython3
# Los grids
grid = lambdify(Y, is_num)
shift = shift_grid(is_expr, default_is, A=12, c=.5) # Definimos los desplazamientos

# Pseudoparámetros 
i_max_1 = default_is['A']/default_is['b']
i_max_2 = shift[0][1]
i_max = max(i_max_1, i_max_2)
y_max_1 = default_is['A']/(1-default_is['c'])
y_max_2 = shift[0][0]
y_max = max(y_max_1, y_max_2)
grid_size = 500
grid_y = np.linspace(0,y_max,grid_size) 
grid_2 = shift[1](grid_y)
```

#### Efecto combinado: desplazamiento debido a un aumento del gasto <br> autónomo y de una reducción de la propensión marginal a consumir

```{code-cell} ipython3
fig, ax = plt.subplots()
ax.plot(grid_y, grid(grid_y), color='blue')
ax.plot(grid_y, grid_2, color='red')
ax.set_xlim([0,y_max])
ax.set_ylim([0,i_max])
ax.set_xlabel('Production, $Y$')
ax.set_ylabel('Interest Rates, $i$')
plt.show()
```

## Variables Estructurales
<a id=’estr’></a>


### Componentes Principales

El código de abajo les ofrece las ecuaciones estructurales del mercado de bienes de la versión lineal del modelo IS-LM, una vez introducido el sector público. Estas definen la renta disponible, esto es libre de impuestos, el consumo, la inversión, el gasto público y los impuestos necesarios para financiarlo. A excepción de los componentes autónomos del gasto, denotados con un subíndice $0$, todas ellas tiene en común su relación, lineal, con las variables endógenas, que están por determinar mientras no describamos el mercado de dinero. Los parámetros que definen tales relaciones están denotados en letras griegas, en contraposición a los parámetros del modelo reducido, por lo menos a lo largo de este capítulo. Estos parámetros denotan las respuestas de cada sector de la economía, como señala la tabla de abajo. Por claridad de exposición nos conviene agrupar la totalidad de los parámetros en dos vectores:

$$
\theta = [A_0, \beta, \xi, \tau, \pi] \\
$$

donde

$$
\begin{gather*}
A_0 =& [C_0, I_0, G_0, T_0]\\
\beta =& [\beta_c, \beta_i, \beta{g}]\\
\xi =& [\xi_c, \xi_i, \xi_g]
\end{gather*}
$$

De momento vamos a simplificar y supondremos que la carga fiscal es soportada en su totalidad por las familias, pero lo cierto es que el código se puede extender de manera trivial para adaptar esta posibilidad. Esta hipótesis se debe a que en la mayoría de textos se supone que el principal determinante de la inversión en su coste y no el nivel de ingreso. Por lo tanto, las implicaciones cuantitativas de este supuesto no deberían ser sustanciales. 

En esta sección demostraremos que toda versión estructural del mercado de bienes puede *reducirse* a una expresión del tipo {eq}`eq:A`, donde

$$ \label{para}
A = A(\theta), \,\, b = b(\theta), \,\, c = c(\theta) \\ 
$$(eq:para)

Recordemos que la [Sección 1.2](#ch_1.1), y la ecuación {eq}`eq:DA` se construyó a partir de una versión muy simple, carente de sector público. En aquella economía, la ecuación anterior se reduce a $A=C_0 + I+0,$ $b=b$ y $c=c$. A continuación vamos a ver que estas relaciones se complican considerablemente cuando incorporamos un sector público, o bien extendemos los componentes del gasto en relación a la ley psicológica fundamental de Keynes en su versión lineal, y la función de inversión de las ecuaciones relativas al modelo simple {eq}`eq:C` y {eq}`eq:I`, respectivamente. Afortunadamente, los ejercicios se realizan de manera automática; tal es el caso de los equipos profesionales que trabajan en las principales instituciones económicas de todos los ámbitos; y este es el caso desde hace más de medio siglo, pues en caso contrario, no existirían medios humanos para empreder la solución de los modelos utilizados.

```{code-cell} ipython3
:tags: []

Gen(is_struct).info()
```

## Código

En este modelo con tres sectores, ingreso disponible, consumo, inversión, gasto público e impuestos totales, las relaciones son lineales

```{code-cell} ipython3
T = Linear(
    var=[Y,i-pi], 
    coeff=[τ,0], 
    auto=T_auto,
    default = default
).expr

Y_d = Y - T

C = Linear(
    var=[Y_d,i-pi], 
    coeff=[ξ_c,-beta_c], 
    auto=C_auto,
    default = default
).expr

I = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_i,-beta_i], 
    auto=I_auto,
    default = default
).expr

G = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_g,-beta_g], 
    auto=G_auto,
    default = default
).expr
```

**Por ejemplo,**

```{code-cell} ipython3
C
```

```{code-cell} ipython3
I.subs(default)
```

### Reducción a la versión estructural

```{code-cell} ipython3
DA = C + I + G
da_exp = DA.expand()
da_exp
```

 #### Recuperamos los parámetros del modelo reducido
 
Finalmente recuperamos las expresiones concretas establecidas en la ecuación (\ref{para}), la cual como recordarán nos proporciona los parámetros del sistema reducido en función de los parámetros del modelo estructural.

```{code-cell} ipython3
c = da_exp.coeff(Y)
c
```

```{code-cell} ipython3
b = -da_exp.coeff(i)
b
```

```{code-cell} ipython3
A = da_exp + b*i -c*Y
A = A.simplify()
A
```

#### Y Obtenemos los valores numéricos del sistema reducido

```{code-cell} ipython3
default_is['A'] = A.subs(default)
default_is['b'] = b.subs(default)
default_is['c'] = c.subs(default)
default_is
```

```{code-cell} ipython3
grid_2 = shift_grid(is_expr, default_is)[1](grid_y)
ymax = default_is['A']/(1-default_is['c'])
i_max = shift_grid(is_expr, default_is)[0][1]
fig, ax = plt.subplots()
ax.plot(grid_y, grid_2, color='red')
ax.set_xlim([0,y_max])
#ax.set_ylim([0,float(i_max)])
ax.set_xlabel('Production, $Y$')
ax.set_ylabel('Interest Rates, $i$')
plt.show()
```

### La Variable de Estado

Para solucionar el modelo completo, debemos construir la curva LM, definida en el mismo espacio de variables endógenas. La intersección de ambas curvas proporciona la solución del modelo. En cursos introductorios de macroeconomía suele comenzarse la exposición del bloque de demanda con un modelo de una sola ecuación; el conocido como modelo Renta-Gasto, o simplemente RG. En este caso simple, se impone $b=0$, de manera que la solución del mismo se halla implícita en {eq}`eq:eq`, y se obtiene inmediatamente despejando la única variable endógena del modelo:

$$
Y = \frac{A}{1-c}
$$

En el modelo IS-LM este modelo se extiende para añadir una variable explicativa más: los tipos de interés. Para tal fin, y esto lo conocemos de las matemáticas elementales, se hace necesaria una ecuación más, que en nuestro caso no será otra cosa que aquella que determina el equilibrio en el mercado de dinero. Por este motivo se hacía necesario encontrar los coeficientes de las variables del modelo reducido a partir de las variables estructurales. En los ejercicios econométricos el problema es a menudo inverso, y se conoce con el nombre de identificación: se trata de como, partiendo del modelo reducido, capturar las variables estructurales, que se hacen necesarias para las tareas de predicción, así como imposible la labor de realizar todo tipo de inferencia estadística. Un mismo modelo reducido, puede observarse


### La Crítica de Lucas


No puede comprenderse macroeconomía en los tiempos actuales sin conocer los fundamentos de la crítica de Lucas. Por fortuna, no es necesario resolver en su totalidad del modelo IS-LM para comprender sus fundamentos, de manera que podemos comenzar sin más preámbulos. En 1976, Robert Lucas escribió un artículo que cambió el paradigma de los modelos macroeconómicos utilizados hasta entonces y que estaban basados en esta misma estructura. Como se apuntó en la [Introducción](#intro) de este capítulo, este modelo, y en realidad todos aquellos que vale la pena mencionar, son extensibles, puediendo acomodar muchos mercados adicionales, así como otros factores, no exclusivamente económicos. Todo el período posterior a la II Guerra Mundial había basado sus predicciones económicas, así como los efectos de las políticas presupestarias, monetarias, financieras o cambiarias en este modelo. Asimismo, las contribuciones de Solow y Swan hacían posible acomodar original versiones dinámicas del modelo general para contemplar el comportamiento de las economías a largo con ejercicios macroeconométricos de grandes escalas

La crítica se basa en el hecho de que, si contemplamos los fundamentos microeconómicos, así como la formación de expectativas consistentes con los parámetros del modelo subyacente y no en ecuaciones ad hoc como las estipuladas en {eq}`eq:C` y {eq}`eq:I`, es altamente probable que las alteraciones en la política económica cambien a su vez los parámetros estructurales. Lucas hacía énfasis en los cambios producidos en los parámetros correspondientes al sector privado; es decir, aquellos parámetros con subíndices $c$ e $i$, incluidos los componentes autónomos de la demanda agregada. 

+++

## Ejercicios
1. ¿Qué significa de manera precisa la expresión *condiciones de mecado perfectamente competitivas*?
1. Describan a partir del modelo estructural una economía con dos sectores, consumo e inversión, con $\beta_c$ = 0 y $\xi_i=0$, y obtengan su forma reducida
2. A partir del modelo desarrollado en el primer ejercicio, introduzcan un sector público. Establezca la hipótesis de que $G$ y $T$ son exclusivamente autónomos.
3. Introduzcan desde el modelo del ejercicio anterior una tasa marginal impositiva comprendida entre cero y uno, tao.
4. Introduzcan un sector público, estableciendo la hipótesis de que los impuestos y el gasto público son autónomos
5. Realicen un gráfico que represente el desplazamiento del  gasto autónomo.
6. Idem para la propensión marginal a consumir
7. Obtenga la pendiente de la curva IS.
9. El sistema analizado no representa un modelo completo. ¿Puede razonar este argumento? 
10. Solucione el modelo Renta Gasto a partir de la técnica desarrollada en eta página
11. ¿Por qué las deflaciones deberían estar asociadas a una crisis de demanda, tal y como se afirma en la [Introducción]?

+++

### 1

Recuerden que las $\xi$ agrupan las respuestas al ingreso $Y$, y que las $\beta$ hacen lo propio con $i$. También recuerden que los subíndices de a,bos conjuntos de parámetros se corresponden con los sectores de la economía. Por otra parte, $\tau$ es la tasa impositiva marginal.

```{code-cell} ipython3
ceros = {
    'G_0':0,
    'T_0':0,
    'xi_i': 0,
    'xi_g': 0,
    'tau': 0,
    'pi': 0,
    'beta_c': 0,
    'beta_g': 0
}

default = default | ceros
```

¿Pueden construir una función para evitar repetir este código?

```{code-cell} ipython3
T = Linear(
    var=[Y,i-pi], 
    coeff=[τ,0], 
    auto=T_auto,
    default = default
).expr

Y_d = Y - T

C = Linear(
    var=[Y_d,i-pi], 
    coeff=[ξ_c,-beta_c], 
    auto=C_auto,
    default = default
).expr

I = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_i,-beta_i], 
    auto=I_auto,
    default = default
).expr

G = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_g,-beta_g], 
    auto=G_auto,
    default = default
).expr
```

```{code-cell} ipython3
DA = C + I + G
da_exp = DA.expand().subs(ceros)
c = da_exp.coeff(Y)
b = -da_exp.coeff(i)
A = da_exp + b*i -c*Y
A = A.simplify()
A
```

Y ahí tienen toda la info necesaria para hacer gráficos, etc.

```{code-cell} ipython3
agg_demand =  Linear(
    var=[Y,i-pi], 
    coeff=[c,-b], 
    auto=A,
    default = default
    )
#Y es la producción
equilibrium = Eq(Y, agg_demand.expr)
num_eq = equilibrium.subs(default)
is_expr = solve(equilibrium,i)[0] # Como el modelo es lineal, sabemos que solo tiene una solución
is_num = is_expr.subs(default) 
```

Venga, ahora interpreten un poco lo que están haciendo. Aquí mism, en esta celda en *markdown*

+++

### 2

¿Difícil? Vamos a suponer $G=T=3$: o lo que es lo mismo, que no hay déficit público y que por lo tanto el presupuesto público está equilibrado. Con las herramientas de *Python*, todo se reduce a familarizarse un poco con los diccionarios y otras, así llamadas por su equivalente en inglés, estructuras de datos. En la primera celda parto de la base de que `default` es igual al valor correspondiente al existente *dentro* del archivo diccionario.py

```{code-cell} ipython3
:tags: []

pub_intro = {'G_0':3, 'T_0':3}
default = default | ceros | pub_intro
default
```

Esta celda de abajo definitivamente conviene expresarla en forma de función con el diccionario `default` como argumento. Pero todo a su debido tiempo.

```{code-cell} ipython3
T = Linear(
    var=[Y,i-pi], 
    coeff=[τ,0], 
    auto=T_auto,
    default = default
).expr

Y_d = Y - T

C = Linear(
    var=[Y_d,i-pi], 
    coeff=[ξ_c,-beta_c], 
    auto=C_auto,
    default = default
).expr

I = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_i,-beta_i], 
    auto=I_auto,
    default = default
).expr

G = Linear(
    var=[Y,i-pi], 
    coeff=[ξ_g,-beta_g], 
    auto=G_auto,
    default = default
).expr

DA = C + I + G
da_exp = DA.expand().subs(ceros)
c = da_exp.coeff(Y)
b = -da_exp.coeff(i)
A = da_exp + b*i -c*Y
A = A.simplify()
agg_demand =  Linear(
    var=[Y,i-pi], 
    coeff=[c,-b], 
    auto=A,
    default = default
    )
#Y es la producción
equilibrium = Eq(Y, agg_demand.expr)
num_eq = equilibrium.subs(default)
is_expr = solve(equilibrium,i)[0] 
is_num = is_expr.subs(default)
```

Interpreten eso. Por ejemplo, ¿por qué aparecen los impuestos multiplicados por la propensión a consumir $\xi_c = c$ en la expresión correspondiente al gasto autónomo $A$, descrita en función de los parámetros estructurales?

```{code-cell} ipython3

```
