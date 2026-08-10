# rutina.ginproducts.com — sitio publicado

Este repositorio es el **sitio en vivo** del corner SO YOUNG (BHermanos, México).
La página oficial es **`/tienda`**; la raíz y `/k` solo redirigen ahí.

## Si vas a editar el diseño aquí (ChatGPT / Codex)

Adelante: el diseño que se publica aquí **es el definitivo**, y el pipeline de
datos lo adopta tal cual. Pero hay piezas que **se regeneran a máquina** con cada
alta o baja de producto — lo que edites ahí se pierde en la siguiente
reconstrucción:

- los `<meta name="x-…">` del `<head>` (sellos de contenido),
- los `<section class="panel">` de `/tienda` y `/piel` (fichas de colecciones)
  — con una excepción: su encabezado `<div class="ptit">` sí es de diseño y se respeta,
- los `<details class="marca">` del catálogo de `/buscar`,
- **todo `const X = <JSON>`** dentro de los scripts (productos, precios, rutinas,
  instrucciones). Dentro de esos datos solo se respetan los iconos: `PI` y el
  campo `i` de `N`/`NEC`.

Todo lo demás — estilos, scripts, marcado, textos — se respeta byte a byte.

No borres el script de datos (el `const D`/`const B` grande): sin él la página
se queda sin productos y la reconstrucción se detiene con error.

## Reglas del negocio (no son estilo)

1. Nada de envíos: es un corner dentro de una tienda física.
2. Crédito = +40 % sobre contado, mostrando siempre contado, número de pagos y
   diferencia (LFPC art. 66).
3. Nada de diagnóstico médico.
4. La promesa de privacidad de la selfie en `/piel` (todo local, nada se sube)
   tiene que seguir siendo cierta y visible.
5. **Sin modismos mexicanos** en ningún texto que se pinte («te late», «apantalla»,
   «ahorita», «checa»…): la página servirá también para otros países. Hay un
   auditor que detiene la publicación si aparece uno.
6. **La ficha de producto siempre CIERRA con `⚖️ Comparar este producto`**
   (`.mcompbtn`): en `/buscar` mete el producto al duelo del comparador; en
   `/tienda` y `/piel` es un enlace a `../buscar/#comparar=N` (deep-link que
   precarga el duelo). Los auditores lo exigen en las tres páginas.
7. Los bloques `.rutina` que **no** son rutinas (los regalos armados) traen
   `data-todo="…"` con su propio verbo; el carrito lo lee (`dataset.todo`) para
   el botón de agregar-todo. No quitar ni el atributo ni la lectura.
