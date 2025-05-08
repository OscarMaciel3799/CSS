# 📦 Posicionamiento y Display en CSS

Como se **controla la ubicación y el comportamiento visual de los elementos en la página** ?. Esto se logra principalmente con dos propiedades CSS:

- `position`: permite mover elementos del flujo normal del documento.
- `display`: define cómo se comportan visualmente en el flujo.

---

## 🎯 Propiedad `position`

La propiedad `position` define **cómo se posiciona un elemento respecto a su contenedor o al viewport (pantalla)**.

| Valor        | ¿Afecta el flujo? | ¿Se puede mover? | ¿Ocupa espacio? |
|--------------|-------------------|------------------|------------------|
| `static`     | ✅ Sí             | ❌ No            | ✅ Sí            |
| `relative`   | ✅ Sí             | ✅ Sí            | ✅ Sí            |
| `absolute`   | ❌ No             | ✅ Sí            | ❌ No            |
| `fixed`      | ❌ No             | ✅ Sí            | ❌ No            |

---

### 🔹 `static` (por defecto)

- Es el valor por defecto.
- El elemento se posiciona según el flujo natural del documento.
- **No se puede mover** usando `top`, `left`, etc.

```css
.caja {
  position: static;
}
```

---
### 🔹 `relative`
El elemento se mueve desde su posición original.

Sigue ocupando su espacio original en el flujo del documento.

```
.caja {
  position: relative;
  top: 10px;
  left: 20px;
}
```
---
###  🔹 `absolute`
El elemento se ubica respecto al primer ancestro que tenga position: relative, absolute o fixed.

Sale del flujo del documento, no empuja a los otros elementos.

```
.padre {
  position: relative;
}

.hijo {
  position: absolute;
  top: 0;
  right: 0;
}
```
---
###  🔹 `fixed`
Se posiciona respecto al viewport (pantalla).

Permanece fijo aunque se haga scroll.

Común en botones flotantes o menús fijos.

```
.fixed {
  position: fixed;
  bottom: 10px;
  right: 10px;
}
```
---
###   🧱 Propiedad display
La propiedad display determina cómo se muestran los elementos y cómo ocupan espacio en el documento.


| Valor          |    ¿Rompe línea?  | ¿Acepta width/height? | Uso típico                   |
|----------------|-------------------|-----------------------|------------------------------|
| `block`        | ✅ Sí             | ✅ Sí                | Contenedores, secciones      |
| `inline`       | ❌ No             | ❌ No                | Texto, enlaces               |
| `inline-block` | ❌ No             | ✅ Sí                | 	Botones, etiquetas flexibles|
| `none`         | ❌ No             | ❌ No                | Ocultar elementos            |



---
###   🔹 `block`
Ocupa todo el ancho disponible.

Empuja otros elementos hacia abajo.

```
.block {
  display: block;
}
```
---
###   🔹`inline`
Solo ocupa el ancho de su contenido.

No se pueden usar width, height, margin-top, ni margin-bottom.

```
.inline {
  display: inline;
}
```
---
###   🔹 `inline-block`
Se comporta como inline, pero permite definir dimensiones y márgenes.

Muy útil para botones y elementos alineados horizontalmente.

```
.inline-block {
  display: inline-block;
  width: 100px;
}
```
---
###   🔹 `none`
El elemento no se muestra ni ocupa espacio.

```
.none {
  display: none;
}
```
