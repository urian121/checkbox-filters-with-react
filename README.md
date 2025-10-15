# 🛒 Sistema de Filtros con Checkboxes en React

[![React](https://img.shields.io/badge/React-18.3.1-blue.svg)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-7.1.10-purple.svg)](https://vitejs.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 Descripción

Aplicación web interactiva desarrollada en **React** que implementa un sistema de filtrado dinámico mediante checkboxes. Los usuarios pueden filtrar productos por múltiples categorías de forma simultánea, con una interfaz moderna y responsiva que consume datos de una API REST externa.

### ✨ Características Principales

- 🎯 **Filtrado Múltiple**: Selección simultánea de múltiples categorías mediante checkboxes
- 🔄 **Actualización en Tiempo Real**: Los productos se filtran dinámicamente sin recargar la página
- 📡 **Integración con API**: Consume datos de [FakeStore API](https://fakestoreapi.com/)
- ⚡ **Indicador de Carga**: Animación personalizada durante el proceso de filtrado
- 🎨 **Interfaz Moderna**: Diseño de tarjetas con efectos hover y animaciones suaves
- 💰 **Sistema de Precios**: Muestra precio original y precio con descuento
- 🛍️ **Acciones de Producto**: Iconos para agregar a favoritos y al carrito
- 📱 **Diseño Responsivo**: Adaptable a diferentes tamaños de pantalla

## 🚀 Tecnologías Utilizadas

| Tecnología          | Versión | Propósito                                        |
| ------------------- | ------- | ------------------------------------------------ |
| **React**           | 18.3.1  | Biblioteca principal para construir la UI        |
| **Vite**            | 7.1.10  | Build tool y dev server de alto rendimiento      |
| **Axios**           | 1.7.2   | Cliente HTTP para peticiones a la API            |
| **loading-request** | 2.21.0  | Animaciones de carga personalizadas              |
| **ESLint**          | 8.57.0  | Linter para mantener código limpio y consistente |

## 📁 Estructura del Proyecto

```
checkbox-filters-with-reactjs/
│
├── src/
│   ├── components/
│   │   ├── Filter.jsx           # Componente de filtros con checkboxes
│   │   ├── ApiProducts.jsx      # Manejo de peticiones y filtrado de datos
│   │   └── ProductCard.jsx      # Tarjeta individual de producto
│   │
│   ├── style/
│   │   └── cards.css            # Estilos personalizados para las tarjetas
│   │
│   ├── App.jsx                  # Componente principal
│   └── main.jsx                 # Punto de entrada de la aplicación
│
├── public/                      # Archivos estáticos
├── index.html                   # HTML base
├── vite.config.js              # Configuración de Vite
└── package.json                # Dependencias y scripts
```

## 🔧 Instalación y Uso

### Prerrequisitos

- Node.js (versión 16 o superior)
- npm o yarn

### Pasos de Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/urian121/checkbox-filters-with-reactjs.git
   cd checkbox-filters-with-reactjs
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Ejecutar en modo desarrollo**
   ```bash
   npm run dev
   ```

4. **Abrir en el navegador**
   ```
   http://localhost:5173
   ```

### Scripts Disponibles

```bash
npm run dev      # Inicia el servidor de desarrollo
npm run build    # Genera el build de producción
npm run preview  # Previsualiza el build de producción
npm run lint     # Ejecuta el linter para revisar el código
```

## 🎯 Funcionalidades Detalladas

### 1. Sistema de Filtrado

El componente `Filter.jsx` gestiona las categorías disponibles:
- **Electrónica** - Dispositivos y gadgets tecnológicos
- **Joyería** - Accesorios y joyas
- **Ropa de Hombre** - Prendas masculinas
- **Ropa de Mujer** - Prendas femeninas

### 2. Gestión de Estado

- Utiliza `useState` para mantener las categorías seleccionadas
- Implementa `useEffect` para cargar productos desde la API
- Filtrado reactivo que actualiza la vista automáticamente

### 3. Tarjetas de Producto

Cada tarjeta muestra:
- Imagen del producto
- Título y categoría
- Precio original (tachado)
- Precio con 30% de descuento
- Botones de acción (favoritos y carrito)

## 🎨 Personalización

### Modificar Categorías

Edita el array `categories` en `src/components/Filter.jsx`:

```javascript
const categories = [
  { value: "electronics", label: "Electrónica" },
  { value: "jewelery", label: "Joyería" },
  // Añade más categorías aquí
];
```

### Cambiar el Porcentaje de Descuento

Modifica el cálculo en `src/components/ProductCard.jsx`:

```javascript
const discountedPrice = product.price - product.price * 0.3; // 30% de descuento
```

### Personalizar Animación de Carga

Ajusta los parámetros en `src/components/Filter.jsx`:

```javascript
showLoading({
  message: "Cargando Filtro...",
  spinnerColor: "#f3752b",
  textLoadingColor: "#EE5E09",
  textLoadingSize: "35px",
});
```

## 📸 Resultado Final

![Demo del Proyecto](https://raw.githubusercontent.com/urian121/imagenes-proyectos-github/master/checkbox-filters-with-reactjs-loading-request.gif)

## 🔍 Conceptos Clave de React Aplicados

- **Hooks**: `useState`, `useEffect`
- **Props**: Paso de datos entre componentes
- **Renderizado Condicional**: Mostrar productos según filtros
- **Manejo de Eventos**: `onChange` para checkboxes
- **Peticiones Asíncronas**: `async/await` con Axios
- **Componentización**: Separación lógica de responsabilidades

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Haz fork del proyecto
2. Crea una rama para tu funcionalidad (`git checkout -b feature/NuevaFuncionalidad`)
3. Haz commit de tus cambios (`git commit -m 'Añade nueva funcionalidad'`)
4. Haz push a la rama (`git push origin feature/NuevaFuncionalidad`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT.

## 💬 Expresiones de Gratitud

Si este proyecto te fue útil, considera:

- ⭐ Dar una estrella al repositorio
- 📢 Compartir con otros desarrolladores
- 🍺 Invitar un café: [PayPal](mailto:iamdeveloper86@gmail.com)
- 📺 Suscribirte al canal para más contenido

## 👨‍💻 Autor

**Urian Viera**

- GitHub: [@urian121](https://github.com/urian121)
- Email: iamdeveloper86@gmail.com

---

⌨️ con ❤️ por [Urian Viera](https://github.com/urian121)
