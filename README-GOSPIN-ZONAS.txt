GOSPIN - CALCULADORA DE ZONAS (v2.0)
====================================

Novedades importantes:
----------------------
1) Búsqueda por CÓDIGO POSTAL funcionando.
2) La app ahora lee:
   - Localidades / barrios desde: zonas.dat
   - Códigos postales desde: cp.dat

Definición de zonas por código postal:
--------------------------------------
- Zona 1:
  * TODOS los códigos postales entre 1000 y 1599 (rango completo).

- Zona 2:
  * Códigos puntuales:
    1602,1603,1604,1605,1606,1607,1609,1636,1637,1638,1640,1641,1642,1643,
    1644,1645,1646,1650,1651,1653,1655,1657,1672,1674,1676,1678,1682,1683,
    1684,1685,1686,1687,1688,1689,1690,1691,1692,1702,1703,1704,1706,1707,
    1708,1712,1713,1714,1715,1751,1752,1753,1754,1766,1768,1773,1778,1821,
    1822,1823,1824,1825,1826,1827,1828,1832,1833,1834,1836,1869,1870,1872,
    1873,1874,1875.

- Zona 3:
  * Códigos puntuales (lista larga que me pasaste, ya cargada en cp.dat).

Cómo funciona la búsqueda por CP:
---------------------------------
1) El usuario elige "Por código postal".
2) Escribe un CP (solo números, ej: 1704).
3) La app hace:
   - Si el CP está entre 1000 y 1599 -> ZONA 1.
   - Si está en la tabla de cp.dat -> ZONA 2 o ZONA 3 según corresponda.
   - Si no está en ninguna de las dos -> muestra mensaje de "CP no configurado".

Archivos:
---------
- index.html   -> App principal.
- zonas.dat    -> Localidades/barrio -> zona (codificado en base64).
- cp.dat       -> Código postal -> zona (codificado en base64).
- LAS ZONAS Y SUS DIVISIONES GOSPIN LOGISTICA.xlsx -> Referencia original.

Uso en GitHub Pages:
--------------------
1) Creá/actualizá tu repositorio.
2) Subí estos tres archivos a la raíz de la rama que uses para Pages:
   - index.html
   - zonas.dat
   - cp.dat
3) En Settings -> Pages, elegí esa rama y carpeta root.
4) Abrí la URL pública que te da GitHub y probá:

   - Modo localidad:
     * caballito, caba, la plata, ensenada, etc.
   - Modo código postal:
     * 1000..1599 -> Zona 1
     * 1704, 1754, 1878, 2800, etc. según tabla -> Zona 2 o Zona 3.

Recordatorio:
-------------
Si abrís index.html con doble clic (file://) en tu PC, los fetch() a
zonas.dat y cp.dat pueden fallar por restricciones del navegador.
Para pruebas locales "a lo bruto" se puede usar una versión embebida
como la que armamos antes, pero para producción en GitHub Pages esta
estructura con archivos externos está perfecta.

Hecho para GoSpin Logística.
