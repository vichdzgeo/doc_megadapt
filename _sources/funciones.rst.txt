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





.. |g_escasez_cz| image:: /fv_images/g_escasez_cz.png
       :width: 100pt
       :height: 100pt

.. |m_escasez_cz| image:: /fv_images/m_escasez_cz.png
        :width: 100pt
        :height: 100pt

.. |g_escasez_ph| image:: /fv_images/g_escasez_ph.png
       :width: 100pt
       :height: 100pt

.. |m_escasez_ph| image:: /fv_images/m_escasez_ph.png
        :width: 100pt
        :height: 100pt

.. |g_escasez_fd| image:: /fv_images/g_escasez_fd.png
       :width: 100pt
       :height: 100pt

.. |m_escasez_fd| image:: /fv_images/m_escasez_fd.png
        :width: 100pt
        :height: 100pt

.. |g_escasez_dsa| image:: /fv_images/g_escasez_dsa.png
       :width: 100pt
       :height: 100pt

.. |m_escasez_dsa| image:: /fv_images/m_escasez_dsa.png
        :width: 100pt
        :height: 100pt

.. |g_escasez_ant| image:: /fv_images/g_escasez_ant.png
       :width: 100pt
       :height: 100pt

.. |m_escasez_ant| image:: /fv_images/m_escasez_ant.png
        :width: 100pt
        :height: 100pt





Las funciones de valor se aplican a cada uno de los criterios del estado inicial o capas geográficas para transformar los valores de una escala natural a una escala de cociente. Las funciones específicas que se aplican a cada criterio representan la connotación que los distintos valores de los criterios tienen para los agentes del modelo.

Funciones de valor para el agente SACMEX:

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
|   falta_dist        | value_funtions.R 126   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   salud             | value_funtions.R 136   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   presion_medios    | value_funtions.R 152   |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   edad_infra_p(m)   |   sacmex_dtss.R 65     |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|   edad_infra_p(n)   |   sacmex_dtss.R 74     |                  |                  |  capa de 1s   |
+---------------------+------------------------+------------------+------------------+---------------+
|   capcidad_p        |   sacmex_dtss.R 77     |                  |                  |  capa de 1s   |
+---------------------+------------------------+------------------+------------------+---------------+
|   falla_dist        |   sacmex_dtss.R 80     |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|      monto          |   sacmex_dtss.R 104    |                  |                  |  capa de 1s   |
+---------------------+------------------------+------------------+------------------+---------------+
|      escesez        |   sacmex_dtss.R 127    |                  |                  | | directo     |
|                     |                        |                  |                  | | el indice de|
|                     |                        |                  |                  | | escasez     |
+---------------------+------------------------+------------------+------------------+---------------+

Funciones de valor para residentes:

+---------------------+------------------------+------------------+------------------+---------------------+
|       capa          |         función        |   gráfica        |      mapa        | observación         |
+=====================+========================+==================+==================+=====================+
|   calidad_agua      |  resident_fnss.R 10    |                  |                  | sin función         |
+---------------------+------------------------+------------------+------------------+---------------------+
| crecimiento_urbano  |  resident_fnss.R 12    |                  |                  | es discreta (wf)    |
+---------------------+------------------------+------------------+------------------+---------------------+
|  agua_insuficente   |  resident_fnss.R 21    |                  |                  | convexa_creciente   |
+---------------------+------------------------+------------------+------------------+---------------------+
|  desperdicio_agua   |  resident_fnss.R 30    |                  |                  | es discreta (wf)    |
+---------------------+------------------------+------------------+------------------+---------------------+
|     fugas           |  resident_fnss.R 42    |                  |                  | | es discreta (wf)  |
|                     |                        |                  |                  | | usa la capa de    |
|                     |                        |                  |                  | | falta_dist        |
+---------------------+------------------------+------------------+------------------+---------------------+
|  agua_insuficente   | | resident_fnss.R 55   |                  |                  |                     |
|                     | | value_funtions.R 126 |                  |                  |                     |
+---------------------+------------------------+------------------+------------------+---------------------+
|     basura          | | resident_fnss.R 63   |                  |                  |                     |
|                     | | value_funtions.R 110 |                  |                  |                     |
+---------------------+------------------------+------------------+------------------+---------------------+
|  encharcamientos    |  resident_fnss.R 70    |                  |                  | | se usa la         |
|                     |                        |                  |                  | | vulnerabilidad    |
|                     |                        |                  |                  | | a inundaciones    |
+---------------------+------------------------+------------------+------------------+---------------------+
|     salud           | | resident_fnss.R 73   |                  |                  |                     |
|                     | | value_funtions.R 136 |                  |                  |                     |
+---------------------+------------------------+------------------+------------------+---------------------+

Funciones de valor para los índices de escasez:

+---------------------+------------------------+------------------+------------------+---------------+
|       capa          |         función        |   gráfica        |      mapa        | observación   |
+=====================+========================+==================+==================+===============+
|                     | | logistica_invertida  | |g_escasez_cz|   | |m_escasez_cz|   |               |
|   critical_zones    | | center=0.2           |                  |                  |               |
|                     | | k=0.255              |                  |                  |               |
|                     | | max=1                |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica            | |g_escasez_ph|   | |m_escasez_ph|   |               |
| hydraulic_pressure  | | center=0.3           |                  |                  |               |
|                     | | k=0.1815             |                  |                  |               |
|                     | | max=0.9405           |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica_invertida  | |g_escasez_ant|  | |m_escasez_ant|  |               |
| infrastructure_age  | | center=34            |                  |                  |               |
|                     | | k=0.1325             |                  |                  |               |
|                     | | max=64               |                  |                  |               |
|                     | | min=4                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica_invertida  | |g_escasez_fd|   | |m_escasez_fd|   |               |
|   potable_lacking   | | center=0.17          |                  |                  |               |
|                     | | k=0.083              |                  |                  |               |
|                     | | max=1                |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+
|                     | | logistica_invertida  | |g_escasez_dsa|  | |m_escasez_dsa|  |               |
|  fix_failure_days   | | center=0             |                  |                  |               |
|                     | | k=0.1325             |                  |                  |               |
|                     | | max=167              |                  |                  |               |
|                     | | min=0                |                  |                  |               |
+---------------------+------------------------+------------------+------------------+---------------+

`critical_zones <http://gvf.magrat.mine.nu/critical_zones/logistica_invertida/?center=0.2&k=0.255&show_map=True&max=1&min=0>`_
