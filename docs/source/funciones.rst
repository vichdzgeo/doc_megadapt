Funciones de valor
===============================

.. |g_antiguedad_d| image:: /fv_images/g_antiguedad_d.png
   :width: 100pt
   :height: 100pt

.. |m_antiguedad_d| image:: /fv_images/m_antiguedad_d.png
    :width: 100pt
    :height: 100pt

.. |g_antiguedad_p| image:: /fv_images/g_antiguedad_p.png
   :width: 100pt
   :height: 100pt

.. |m_antiguedad_p| image:: /fv_images/m_antiguedad_p.png
    :width: 100pt
    :height: 100pt

.. |g_calidad_agua| image:: /fv_images/g_calidad_agua.png
   :width: 100pt
   :height: 100pt

.. |m_calidad_agua| image:: /fv_images/m_calidad_agua.png
    :width: 100pt
    :height: 100pt

.. |g_pres_hid| image:: /fv_images/g_pres_hid.png
   :width: 100pt
   :height: 100pt

.. |m_pres_hid| image:: /fv_images/m_pres_hid.png
    :width: 100pt
    :height: 100pt

.. |g_subsidencia| image:: /fv_images/g_subsidencia.png
   :width: 100pt
   :height: 100pt

.. |m_subsidencia| image:: /fv_images/m_subsidencia.png
    :width: 100pt
    :height: 100pt

.. |g_falla_escasez| image:: /fv_images/g_falla_escasez.png
       :width: 100pt
       :height: 100pt

.. |m_falla_escasez| image:: /fv_images/m_falla_escasez.png
        :width: 100pt
        :height: 100pt


Las funciones de valor se aplican a cada uno de los criterios del estado inicial o capas geográficas para transformar los valores de una escala natural a una escala de cociente. Las funciones específicas que se aplican a cada criterio representan la connotación que los distintos valores de los criterios tienen para los agentes del modelo.


+---------------------+------------------------+------------------+------------------+---------------+
|       capa          |         función        |   gráfica        |      mapa        | observación   |
+=====================+========================+==================+==================+===============+
|                     | | logistica_invertida  | |g_antiguedad_d| | |m_antiguedad_d| |               |
| antiguedad_drenaje  | | center=38.5          |                  |                  |               |
|                     | | k=0.083              |                  |                  |               |
|                     | | max=70               |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | campana_invertida    | |g_antiguedad_p| | |m_antiguedad_p| | | es la misma |
| antiguedad_potable  | | center=60            |                  |                  | | capa para   |
|                     | | a=40                 |                  |                  | | drenaje y   |
|                     | | max=60               |                  |                  | | potable     |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica_invertida  | |g_calidad_agua| | |m_calidad_agua| | | en el gpk   |
|   calidad_agua      | | center=154           |                  |                  | | está entre  |
|                     | | k=0.1325             |                  |                  | | 0.7 y 1     |
|                     | | max=200              |                  |                  |               |
|                     | | min=20               |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica            | |g_pres_hid|     | |m_pres_hid|     |               |
| presion_hidraulica  | | center=0.3           |                  |                  |               |
|                     | | k=0.1815             |                  |                  |               |
|                     | | max=1                |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica_invertida  | |g_subsidencia|  | |m_subsidencia|  |               |
|   subsidencia       | | center=12.5475       |                  |                  |               |
|                     | | k=0.1325             |                  |                  |               |
|                     | | max=35.85            |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | convexa_creciente    | |g_falla_escasez|| |m_falla_escasez||               |
|   falla_escasez     | | gama=0.01975         |                  |                  |               |
|                     | | max=348.395          |                  |                  |               |
|                     | | min=0                |                  |                  |               |
|                     | |                      |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|peticion_delegaciones|         1 - x          |                  |                  |  capa de 1s   |
+---------------------+------------------------+------------------+------------------+---------------+
|   basura            | value_funtions.R 110   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   falla_dist        | value_funtions.R 126   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   salud             | value_funtions.R 136   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   salud             | value_funtions.R 136   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
