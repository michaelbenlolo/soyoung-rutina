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
