GOSPIN - CALCULADORA DE ZONAS (v1.4-fix)
=========================================

Si ves el mensaje:
" Todavía se están cargando los datos de localidades... "
es casi seguro que:
- El archivo zonas.dat no está en la MISMA carpeta que index.html, o
- Subiste solo index.html a GitHub Pages pero no zonas.dat, o
- zonas.dat se dañó al copiarlo.

Solución:
---------
1. Asegurate de que estos archivos estén juntos:
   - index.html
   - zonas.dat

2. Si es en tu PC:
   - Descomprimí el ZIP en una carpeta nueva.
   - Abrí index.html desde esa carpeta (donde se vea también zonas.dat).

3. Si es en GitHub Pages:
   - Subí index.html y zonas.dat al mismo repositorio y misma rama.
   - Volvé a publicar (o esperá a que GitHub regenere la página).

Esta versión es igual a la 1.4 pero con un pequeño ajuste en el mensaje
de error para ayudarte a detectar si falta zonas.dat.

Config. de zonas:
-----------------
- Zona 1  -> CABA (columna B)
- Zona 2  -> Zona media (columnas D y E)
- Zona 3  -> TODO lo pintado de celeste (columnas G, H, J y K)

Hecho para GoSpin Logística.
