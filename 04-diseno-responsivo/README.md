# 📱 Diseño Responsivo con CSS

El **Diseño Responsivo** permite que un sitio web se adapte a diferentes tamaños de pantalla: computadoras, tablets y celulares. Es esencial para una buena experiencia de usuario.

---

## 🧱 Principales técnicas

### 1. **Unidades relativas**

Evitar usar píxeles (`px`) fijos en favor de unidades que se adapten:

| Unidad | Se adapta | Uso común |
|--------|-----------|------------|
| `%`    | ✅         | Anchuras relativas |
| `em`   | ✅         | Tamaño relativo al elemento padre |
| `rem`  | ✅         | Tamaño relativo al `html` (raíz) |
| `vh/vw`| ✅         | Porcentaje del alto o ancho del viewport |

```css
.container {
  width: 80%;
  font-size: 1.2rem;
}
```
---

## 2. **Media Queries**
Permiten aplicar estilos específicos según el ancho del dispositivo.


Estilo general
```
body {
  background: white;
}
```
Estilo para pantallas de 600px o menos
```
@media (max-width: 600px) {
  body {
    background: lightgray;
  }
}
```
Puedes combinar condiciones:

```
@media (min-width: 768px) and (max-width: 1024px) {
  /* Tablets */
}
```
---

## 3. **Diseños flexibles con Flexbox o Grid**
Estas técnicas permiten que los elementos se acomoden automáticamente sin necesidad de usar flotantes (float) ni posiciones absolutas.

Ejemplo con Flexbox:
```
.contenedor {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
```

---

## 4. **Imágenes responsivas**
Las imágenes deben adaptarse al ancho del contenedor:

```
img {
  max-width: 100%;
  height: auto;
}
```
También se puede usar el atributo HTML srcset para cargar imágenes diferentes según la resolución.

---

## 5. Diseño Mobile First
Se basa en escribir primero los estilos para pantallas pequeñas (como móviles) y luego usar media queries para mejorar la visualización en pantallas más grandes.

Estilos para móviles
```
.menu {
  display: none;
}
```
Agregar visibilidad en pantallas más grandes
```
@media (min-width: 768px) {
  .menu {
    display: flex;
  }
}
```
