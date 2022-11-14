Iteraciones y Condicionales
===========================

Iterables
---------

Hasta el momento, hemos investigado algunos recursos básicos de Python. 
En este capítulo vamos a tomar el camino inverso. Supongamos que en nuestra mente está 
definir un triángulo en el plano euclidiano. Para ello necesitamos previamente tener definido un punto
en un plano; o lo que es lo mismo, definir dos coordenadas para cada punto. Resulta más práctica la posibilidad de agrupar ambas coordenadas en una sola variable. Posteriormente, podemos crear una **función** definida en tres puntos para caracterizar ese triángulo. No obstante, puede resultar más interesante la posibilidad de construir una **clase** con el objetivo de trasladarlo, modificarlo, calcular su aŕea, su perímetro, representarlo geométricamente, pintarlo, escalarlo para formar polígonos con triángulos adicionales, etc. Funciones y clases merecen un capítulo separado para cada categoría. En todo caso, tal y como nos ilustra el ejemplo precedente, para dotarlas de una utilidad práctica, nos resulta conveniente indagar en la noción de **objeto iterable** en la nomenclatura de Python.

Un objeto iterable puede ser analizado recursivamente, elemento a elemento. Para convertir un objeto en iterable, basta añadir los métodos __iter__() o  __getitem(). Ejemplos de iterables son las variables de texto. Otros iterables permitidos por Python son las listas, las tuplas, los diccionarios y los conjuntos. 

Listas
------

Las **listas** son grupos de objetos mutables formados por elementos arbitrarios, que sde denotan por medio de corchetes ``[]``. La diferencia de las listas con las **tuplas**, es que estas  últimas son objetos inmutables, y se denotan por medio de paréntesis ``()``.


.. container:: highlight

   >>> lista = ['adan', 'eva']
   ... for i in lista:
   ...     print(i, len(i))
   ...
   adan 4
   eva 3

En la nueva lista que vamos a definir a continuación, vamos a repasar algunos de los contenidos del tema anterior, haciendo uso de las técnicas adquiridas en este tema.

.. container:: highlight
   
   >>> tupla = (2, 2.0, complex(1,-1), 2>2.1, 2J == 2j])
   ... tipos = ()
   ... for l in tupla:
   ...     tipos.append(type(l))
   ... for l in zip(tupla, tipos):
   ...     print("El tipo de {0} es {1}".format(l[0], l[1]))
   ... 
   El tipo de 2 es int
   El tipo de 2.0 es float
   El tipo de (1-1j) es complex
   El tipo de False es bool
   El tipo de True es bool

.. container:: section middleContent
      :name: middleContent

      .. container:: container-fluid

         .. container:: row

            .. container:: col-md-12 pr-md-0 col-lg-12 col-xl-8

               .. rubric:: Built-in List Functions in Python
                  :name: built-in-list-functions-in-python

               The following table lists all the functions that can be
               used with the `list type in Python
               3 <https://www.tutorialsteacher.com/python/python-list>`__.

               .. container:: table-responsive

                  +----------------------------------------------+----------------------------------+
                  | List Method                                  | Description                      |
                  +==============================================+==================================+
                  | ``list.append()``                            | Adds a new item at the end of    |
                  |                                              | the list.                        |           
                  +----------------------------------------------+----------------------------------+
                  | ``list.clear()``                             | Removes all the items from the   |                                                                                            
                  |                                              | list and make it empty.          |
                  +----------------------------------------------+----------------------------------+
                  | ``list.copy()``                              | Returns a shallow copy of a      |
                  |                                              | list.                            |
                  +----------------------------------------------+----------------------------------+
                  | ``list.count()``                             | Returns the number of times an   |
                  |                                              | element occurs in the list.      |
                  +----------------------------------------------+----------------------------------+
                  | ``list.extend()``                            | Adds all the items of the        |
                  |                                              | specified iterable (list, tuple, |
                  |                                              | set, dictionary, string) to the  |
                  |                                              | end of the list.                 |
                  +----------------------------------------------+----------------------------------+
                  | ``list.index()``                             | Returns the index position of    |
                  |                                              | the first occurance of the       |
                  |                                              | specified item. Raises a         |
                  |                                              | ValueError if there is no item   |
                  |                                              | found.                           |
                  +----------------------------------------------+----------------------------------+
                  | ``list.insert()``                            | Inserts an item at a given       |
                  |                                              | position.                        |
                  +----------------------------------------------+----------------------------------+
                  | ``list.pop()``                               | Returns an item from the         |
                  |                                              | specified index position         |
                  |                                              | also removes it from the list.   |
                  |                                              | If no index is specified, the    |
                  |                                              | list.pop() method removes and    |
                  |                                              | returns the last item in the     |
                  |                                              | list.                            |
                  +----------------------------------------------+----------------------------------+
                  | ``list.remove()``                            | Removes the first occurance of   |
                  |                                              | the specified item from the      |
                  |                                              | list. It the specified item not  |
                  |                                              | found then throws a ValueError.  |
                  +----------------------------------------------+----------------------------------+
                  | ``list.reverse()``                           | Reverses the index positions of  |
                  |                                              | the elements in the list. The    |
                  |                                              | first element will be at the     |
                  |                                              | last index, the second element   |
                  |                                              | will be at second last index and |
                  |                                              | so on.                           |
                  +----------------------------------------------+----------------------------------+
                  | ``list.sort()``                              | Sorts the list items in          |
                  |                                              | ascending, descending, or in     |
                  |                                              | custom order.                    |
                  +----------------------------------------------+----------------------------------+


Compresión de Listas
---------------------

Combinan un bucle (*loop*) y la definici'on de una lista en una línea de código. Por ejemplo, si quisíermos calcular las potecias de orden 4 desde el 1 hasta el 10: 



Diccionarios y Conjuntos
------------------------

.. container:: w3-main w3-light-grey
   :name: belowtopnav

   .. container:: w3-row w3-white

      .. container:: w3-col l10 m12
         :name: main

         .. container::
            :name: mainLeaderboard

            .. rubric:: Python Dictionary Methods
               :name: python-dictionary-methods



         Python has a set of built-in methods that you can use on
         dictionaries.

         +----------------------------------+----------------------------------+
         | Method                           | Description                      |
         +----------------------------------+----------------------------------+
         | ``clear()``                      | Removes all the elements from    |
         |                                  | the dictionary                   |
         +----------------------------------+----------------------------------+
         | ``copy()``                       | Returns a copy of the dictionary |
         +----------------------------------+----------------------------------+
         | ``fromkeys()``                   | Returns a dictionary with the    |
         |                                  | specified keys and value         |
         +----------------------------------+----------------------------------+
         | ``get()``                        | Returns the value of the         |
         |                                  | specified key                    |
         +----------------------------------+----------------------------------+
         | ``items()``                      | Returns a list containing a      |
         |                                  | tuple for each key value pair    |
         +----------------------------------+----------------------------------+
         | ``keys()``                       | Returns a list containing the    |
         |                                  | dictionary's keys                |
         +----------------------------------+----------------------------------+
         | ``pop()``                        | Removes the element with the     |
         |                                  | specified key                    |
         +----------------------------------+----------------------------------+
         | ``popitem()``                    | Removes the last inserted        |
         |                                  | key-value pair                   |
         +----------------------------------+----------------------------------+
         | ``setdefault()``                 | Returns the value of the         |
         |                                  | specified key. If the key does   |
         |                                  | not exist: insert the key, with  |
         |                                  | the specified value              |
         +----------------------------------+----------------------------------+
         | ``update()``                     | Updates the dictionary with the  |
         |                                  | specified key-value pairs        |
         |                                  |                                  |
         +----------------------------------+----------------------------------+
         | ``values()``                     | Returns a list of all the values |
         |                                  | in the dictionary                |
         |                                  |                                  |
         +----------------------------------+----------------------------------+

         

1. 
