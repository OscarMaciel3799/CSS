# Efectos y Transiciones en CSS

CSS permite crear efectos visuales atractivos que mejoran la experiencia del usuario. En esta sección aprenderás a aplicar:

---

## 🎯 Transiciones (`transition`)

Permiten animar cambios suaves entre valores de propiedades CSS.

**Sintaxis básica:**
```css
selector {
  transition: propiedad duración función;
}
```
Ejemplo:

```
button {
  background-color: blue;
  transition: background-color 0.3s ease;
}
button:hover {
  background-color: green;
}
```
---

## 🔁 Transformaciones (`transform`)
Cambian visualmente un elemento sin modificar su flujo en el documento.

Ejemplos:

Escalar
```
transform: scale(1.2);
```

Rotar
```
transform: rotate(15deg);
```
Mover
```
transform: translateX(50px);
```

---

## 🎬 Animaciones con `@keyframes`
Permiten definir una secuencia de pasos con cambios en propiedades CSS.

Ejemplo:

```@keyframes girar {
from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

img {
  animation: girar 2s linear infinite;
}
```
---

## 🧪 `Pseudoclases` para interacción
:hover: cuando el mouse está sobre un elemento.

:active: cuando se está haciendo clic.

:focus: cuando el elemento recibe foco (teclado o mouse).

```
input:focus {
  border-color: blue;
}
```