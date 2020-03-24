Entradas
===========

.. toctree::
   :maxdepth: 2
   :caption: Contenido:

   capas
   funciones
   supermatrices
   escorrentias


Los insumos de datos para correr el modelo megadaptr se dividen en capas geográficas, funciones de valor, datos provenientes de modelos desacoplados (crecimiento urbano y escorrentías) y supermatrices para simular la toma de decisiones de los agentes

Las **capas geográficas** representan el estado inicial de las unidades geográficas del modelo en este caso AGEBS. El estado inicial se conforma de los distintos criterios que los agentes necesitan para tomar sus decisiones en cada ciclo del modelo.

Las **funciones de valor** se aplican a cada uno de los criterios del estado inicial o capas geográficas para transformar los valores de una escala natural a una escala de cociente. Las funciones específicas que se aplican a cada criterio representan la connotación que los distintos valores de los criterios tienen para los agentes del modelo.

Las **supermatrices** representan las valoraciones especificas que cada agente le da a cada criterio y se dividen en matrices no ponderadas y matrices de clusters.

Estos tres insumos están estrechamente ligados y es necesario que exista una correspondencia entre cada criterio de las supermatrices con las capas geograficas y una funcion de valor para cada una de ellas. Dada la estrecha relación de estos tres insumos se recomienda crear tablas que permitan verificar la correspondencia y consistencia de de estos tres insumos básicos.

Adicionalmente, entran al modelo datos provenientes de otros modelos que funcionan como forzantes externos en este caso las escorrentías y presiitaciones esperadas para cada escenario de cambio climático y cada escenario de crecimiento urbano.
