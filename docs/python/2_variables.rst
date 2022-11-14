.. role:: raw-math(raw)
    :format: latex html

Variables y Operadores
======================

Atributos y Métodos
-------------------

Los lenguajes de programación contienen código con la finalidad de realizar un proyecto específico; y como sucede con cualquier lenguaje, el códogo se compone de unidades simples, en nuestro caso *ejecutables*, denominadas **instrucciones** (*statements*).

Las instruccions pueden ser de dos tipos: **asignaciones** y **expresiones**. Las primeras, como su propio nombre indica, otorgan un valor específico a un atributo; las expresiones involucran operadores con dichos datos.


En la programación orientada a objetos, estos se agrupan en datos, o **atributos**, y **métodos**, también comocidos como procedimientos . Estos últimos establecen patrones de comportamiento por medio de una serie de operaciones, de complejidad diversa, que modifican los datos iniciales. 

Las variables sirven para caracterizar a un dato o a un conjunto de datos. Para tal fin, necesitamos establecer identificadores, o en otras palabras, símbolos

Identificadores
---------------

A fin de obtener la lista de nombres reservados: ejecutar 

.. code:: ipython3

   help('keywords')

El mensaje obtenido será el siguiente:

.. parsed-literal::

    Here is a list of the Python keywords.  Enter any keyword to get more help.
    
    False               class               from                or
    None                continue            global              pass
    True                def                 if                  raise
    and                 del                 import              return
    as                  elif                in                  try
    assert              else                is                  while
    async               except              lambda              with
    await               finally             nonlocal            yield
    break               for                 not                 


Operadores
----------


.. container:: subsection
   :name: boolean-and-or-not

   .. rubric:: Operadores de Boole
      :name: boolean


 La siguiente tabla describe los operadores de Boole, odenados en orden ascendente según su prioridad.

   .. container:: responsive-table__container

      +-----------------+-------------------------------------------+--------+
      | Operation       | Resultado                                 | Notas  |
      +=================+===========================================+========+
      | ``x or y``      | si ``x`` es falso, ``y``, si no, ``x``    | (1)    |
      +-----------------+-------------------------------------------+--------+
      | ``x and y``     | si *x* es falso, ``x``, si no ``y``       | (1)    |
      +-----------------+-------------------------------------------+--------+
      | ``not x``       | if ``x`` es falso, ``True``, si no        | (2)    |
      |                 | ``False``                                 |        |
      +-----------------+-------------------------------------------+--------+                


 Notas


1. Solo se evalúa el segundo argumento si el primero es falso (*short-circuit operator*).

2. El operador ``not`` tiene una prioridad menor 
que los operadores que no son lógicos, de manera
que  ``not a == b`` is interpreted as
``not (a == b)``, y ``a == not b`` priduce un
error de sintaxis.


.. container:: subsection
   :name: comparisons

   .. rubric:: Comparaciones
      :name: comparison

Python dispone de ocho operadores de comparación,
tal y como se refleja en la siguiente tabla. Todos ellos
poseen la misma prioridad (mayor que la de los operadores lógicos). 
Las comparisons pueden encadenarse; por ejemplo,
``x == y <= z`` equivale a 
``x == y and y <= z``.

   .. container:: responsive-table__container

                     +----------------------+-----------------------------------------------+
                     | Operation            | Meaning                                       |
                     +======================+===============================================+
                     | ``<``                | strictly less than                            |
                     +----------------------+-----------------------------------------------+
                     | ``<=``               | less than or equal                            |
                     +----------------------+-----------------------------------------------+
                     | ``>``                | strictly greater than                         |
                     +----------------------+-----------------------------------------------+
                     | ``>=``               | greater than or equal                         |
                     +----------------------+-----------------------------------------------+
                     | ``==``               | equal                                         |
                     +----------------------+-----------------------------------------------+
                     | ``!=``               | not equal                                     |
                     +----------------------+-----------------------------------------------+
                     | ``is``               | object identity                               |
                     +----------------------+-----------------------------------------------+
                     | ``is not``           | negated object identity                       |
                     +----------------------+-----------------------------------------------+


Solamente son comparables los objetos numéricos de difrente tipo. 
El operador ``==`` siempre  define, aunque para 
los objetos pertenecientes a una clase, equivale a
`is <https://docs.python.org/3/reference/expressions.html#is>`_.

El resto de operadores  de comparación, ``<``, ``<=``, ``>`` y ``>=`` solo 
están definidos si tienen sentido. Por ejemplo, si comparamos un número complejo,
obtendremos la excepción 
`TypeError <https://docs.python.org/3/library/exceptions.html#TypeError>`__.

Los elementos (*instances*) pertenecientes  a dos clases diferentes
no podr'an ser comparables a menos que definamos en ellas el método
`__eq__() <https://docs.python.org/3/reference/datamodel.html#object.__eq__>`__.
Los criterios de comparación dentro de una clase están condicionados 
a la existencia de alguno de los siguientes métodos:
`__lt__() <https://docs.python.org/3/reference/datamodel.html#object.__lt__>`__,
`__le__() <https://docs.python.org/3/reference/datamodel.html#object.__le__>`__,
`__gt__() <https://docs.python.org/3/reference/datamodel.html#object.__gt__>`__,
y
`__ge__() <https://docs.python.org/3/reference/datamodel.html#object.__ge__>`__ 
`__lt__() <https://docs.python.org/3/reference/datamodel.html#object.__lt__>`__
y
__eq__() <https://docs.python.org/3/reference/datamodel.html#object.__eq__>`__


El comportamiento de los operadores 
`is <https://docs.python.org/3/reference/expressions.html#is>`__ y
`is not <https://docs.python.org/3/reference/expressions.html#is-not>`__
no es enteramente predecible, expcepto por el hecho de que
nunca muestran errores de excepción.
                  
Dos operadores con la misma prioridad:
`in <https://docs.python.org/3/reference/expressions.html#in>`__ y
`not in <https://docs.python.org/3/reference/expressions.html#not-in>`__,
los cuales son válidos para los iterables
`iterable <https://docs.python.org/3/glossary.html#term-iterable>`__,
o bien poseen el método ``__contains__()``.



.. container:: subsection
   :name: numeric-types-int-float-complex

   .. rubric:: Numeric Types —
               `int <https://docs.python.org/3/library/functions.html#int>`__,
               `float <https://docs.python.org/3/library/functions.html#float>`__,
               `complex <https://docs.python.org/3/library/functions.html#complex>`__\ `¶ <#numeric-types-int-float-complex>`__
      :name: Numeric Types

Existen tres tipos de **números**: **enteros**,
**decimales** (*floating*) y **complejos**. Los operadores de Boole 
de hecho se comportan como una subclase de los primeros . Integers
have unlimited precision. Más información acerca de la precisión de los 
nuḿeros decimales se puede encontrar 
`aquí <https://docs.python.org/3/library/sys.html#sys.float_info>`__.
La librería estándard incluye los tipos de número adicionales 
`fractions.Fraction <https://docs.python.org/3/library/fractions.html#fractions.Fraction>`__,
for rationals, y
`decimal.Decimal <https://docs.python.org/3/library/decimal.html#decimal.Decimal>`__.

Con la excepción de los números complejos, las siguientes operaciones son válidas. Pueden consultar la
`precedencia de los operadores artméticos que se presentan a continuación <https://docs.python.org/3/reference/expressions.html#operator-summary>`__):

   .. container:: responsive-table__container

                     +-------------------------+---------------------------+--------+
                     | Operación               | Resultado                 | Notes  |
                     +=========================+===========================+========+
                     | ``x + y``               | suma de ``x`` e ``y``     |        |
                     +-------------------------+---------------------------+--------+
                     | ``x - y``               | sustracción of  ``x``     |        |
                     |                         | and ``y``                 |        |  
                     +-------------------------+---------------------------+--------+
                     | ``x * y``               | producto de ``x`` e ``y`` |        |           
                     +-------------------------+---------------------------+--------+ 
                     | ``x / y``               | división de *x* e *y*     |        |                
                     +-------------------------+---------------------------+--------+
                     | ``x // y``              | división entera of ``x``  | (1)    |                
                     |                         | e ``x`` e ``y``           |        |                
                     +-------------------------+---------------------------+--------+
                     | ``x % y``               | resto de ``x / y``        | (2)    |                
                     +-------------------------+---------------------------+--------+
                     | ``-x``                  | valor opuesto de ``x``    |        |                
                     +-------------------------+---------------------------+--------+
                     | ``+x``                  | identidad de ``x``        |        |                
                     +-------------------------+---------------------------+--------+
                     | ``abs(x)``              | valor absoluto            |        | 
                     |                         | de  *x*                   |        |
                     +-------------------------+---------------------------+--------+
                     | ``int(x)``              | *x* converted to integer  | (3)    |
                     |                         |                           | (6)    |
                     +-------------------------+---------------------------+--------+
                     | ``float(x)``            | *x* converted to floating | (4)    | 
                     |                         | point                     | (6)    | 
                     +-------------------------+---------------------------+--------+
                     | ``complex(a,b)``        | a complex number with     | (6)    | 
                     |                         | real part *re*, imaginary |        | 
                     |                         | part *im*. *im* defaults  |        | 
                     |                         | to zero.                  |        |
                     +-------------------------+---------------------------+--------+
                     |                         | conjugate of the complex  |        |               
                     | ``c.conjugate()``       | number *c*                |        |            
                     +-------------------------+---------------------------+--------+
                     |                         | the pair                  | (2)    | 
                     | ``divmod(x, y)``        | ``(x // y, x % y)``       |        | 
                     +-------------------------+---------------------------+--------+
                     | ``pow(x, y)``           | *x* to the power *y*      | (5)    | 
                     |                         |                           |        | 
                     +-------------------------+---------------------------+--------+
                     | ``x ** y``              | *x* to the power *y*      | (5)    |                
                     +-------------------------+---------------------------+--------+

                  Notas:

                  #. El tipo de de este valor no es necesariamete un nu´mero entero
                  #. Indefinido en los números complejos

                  #. Ver las funciones
                     `math.floor() <https://docs.python.org/3/library/math.html#math.floor>`__ 
                     y
                     `math.ceil() <https://docs.python.org/3/library/math.html#math.ceil>`__

                  #. Los n'umeros decimales aceptan las variables de texto
                     ``nan`` e``inf`` con el prefijo de signo opcional
                     “+” or “-” para ``nan`` and positive or negative infinity.

                  #. Se cumple :math:`0^0=1`

                  #. `Lista completa de notaciones (**code points**) con la propiedad Nd
                     <https://www.unicode.org/Public/13.0.0/ucd/extracted/DerivedNumericType.txt>`__.


   .. container:: responsive-table__container

                     +---------------------+------------------------------------------------+
                     | Operation           | Result                                         |
                     +=====================+================================================+
                     |                     | *x* truncated to                               |
                     | `math.trunc(x) <h   | `Integral <https://docs.python.o               |
                     | ttps://docs.python. | rg/3/library/numbers.html#numbers.Integral>`__ |
                     | org/3/library/math. |                                                |
                     | html#math.trunc>`_  |                                                |
                     +---------------------+------------------------------------------------+
                     |                     | *x* rounded to *n* digits, rounding half to    |
                     | `round(x[, n]) <h   | even. If *n* is omitted, it defaults to 0.     |
                     | ttps://docs.python. |                                                |
                     | org/3/library/funct |                                                |
                     | ions.html#round>`__ |                                                |
                     +---------------------+------------------------------------------------+
                     |                     | the greatest                                   |
                     | `math.floor(x) <h   | `Integral <https://docs.python.o               |
                     | ttps://docs.python. | rg/3/library/numbers.html#numbers.Integral>`__ |
                     | org/3/library/math. | <= *x*                                         |
                     | html#math.floor>`__ |                                                |
                     +---------------------+------------------------------------------------+
                     | `math.ceil(x) <h    | the least                                      |
                     | ttps://docs.python  | `Integral <https://docs.python.o               |
                     | .org/3/library/math | rg/3/library/numbers.html#numbers.Integral>`__ |
                     | .html#math.ceil>`__ | >= *x*                                         |
                     +---------------------+------------------------------------------------+

For additional numeric operations see the
`math <https://docs.python.org/3/library/math.html#module-math>`__
and
`cmath <https://docs.python.org/3/library/cmath.html#module-cmath>`__
modules.


.. container:: subsection
   :name: Bitwise Operations on Integers

   .. rubric:: operadores Binarios sobre enteros
               Types\ `¶ <#bitwise-operations-on-integer-types>`__
      :name: bitwise-operations-on-integer-types


   Estos operadores solo funcionan con enteros.
   Su prioridad se encuentra entre los operadores numericos 
   y los operadores de ; the unary operation ``~`` has
   the same priority as the other unary numeric
   operations (``+`` and ``-``).

   This table lists the bitwise operations sorted in
   ascending priority:


                     
   .. container:: responsive-table__container

                        +--------------+-----------------------------------------+------------+
                        | Operador     | Resultado                               | Notas      |
                        +==============+=========================================+============+
                        | ``x | y``    | *bitwise o* de *x* e *y*                |            |
                        +--------------+-----------------------------------------+------------+
                        | ``x ^ y``    | *bitwise o exclusivo*                   |            |
                        +--------------+-----------------------------------------+------------+
                        | ``x & y``    | *bitwise y*                             |            |
                        +--------------+-----------------------------------------+------------+
                        | ``x << n``   | Desplazamiento de *x* a la              | (1) (2)    |                                                        
                        |              | izquierda po n bits                     |            |
                        +--------------+-----------------------------------------+------------+
                        | ``x >> n``   | Desplazamiento de *x* a la              | (1) (3)    |                                                        
                        |              | izquierda po n bits                     |            |
                        +--------------+-----------------------------------------+------------+
                        | ``~x``       | the bits of *x* inverted                |            |
                        +--------------+-----------------------------------------+------------+

                     Notes:

                     #. Los desplazamientos negativos causan un
                        `error de valor <https://docs.python.org/3/library/exceptions.html#ValueError>`__.

                     #. Equivalente a ``pow(2, n)``.

                     #.Equivalente a ``x//pow(2, n)``.


.. container:: subsection
   :name: ejemplos
   
   .. rubric:: Ejemplos
      :name: ejemplo

   .. container:: highlight
      
      >>> a, b, c = 2, 2.0, complex(1,-1)
      ... d, e  = 2 < 2.1, 2J==2j
      ... lista = [a,b,c,d,e]
      ... for l in lista:
      ...     print(l, type(l))
      

