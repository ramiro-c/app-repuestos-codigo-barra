# Buscador de Códigos de Barras

Aplicación web para buscar códigos de barras en archivos Excel. Permite cargar un archivo Excel y buscar información de repuestos mediante su código de barras.

## Características

- 📤 **Carga de archivos Excel**: Soporta archivos `.xlsx` y `.xls`
- 🔍 **Búsqueda inteligente**: Busca el código de barras en todas las columnas del archivo
- 📊 **Visualización de resultados**: Muestra información detallada del repuesto encontrado:
  - Código
  - Código de Barras
  - Nombre del Repuesto
  - Precio
- 🎨 **Interfaz moderna**: Diseño limpio y responsivo con gradientes y animaciones
- ⚡ **Búsqueda parcial**: Encuentra coincidencias incluso si el código está contenido dentro de otro valor

## Cómo usar

1. **Cargar archivo Excel**: Haz clic en "Elegir archivo" y selecciona tu archivo Excel
2. **Ingresar código**: Pega o escribe el código de barras en el campo de búsqueda
3. **Buscar**: Haz clic en el botón "Buscar" o presiona Enter
4. **Ver resultados**: La aplicación mostrará la información del repuesto si se encuentra

## Requisitos

- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Archivo Excel con formato válido (.xlsx o .xls)

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla)
- [SheetJS (xlsx.js)](https://sheetjs.com/) - Biblioteca para leer archivos Excel

## Estructura del proyecto

```
app-repuestos-codigo-barra/
├── index.html          # Aplicación completa (HTML, CSS y JavaScript)
└── README.md          # Este archivo
```

## Notas técnicas

- La aplicación busca en todas las columnas del archivo Excel
- La búsqueda es parcial (no requiere coincidencia exacta)
- Los espacios en blanco se eliminan automáticamente durante la búsqueda
- La aplicación procesa solo la primera hoja del archivo Excel
- Los datos se procesan completamente en el cliente (no se envían a ningún servidor)

## Formato esperado del Excel

El archivo Excel debe tener una estructura similar a:

| Código | Código de Barras | Repuesto | ... | Precio |
|--------|------------------|----------|-----|--------|
| 001    | 1234567890123    | Filtro   | ... | 25.50  |
| 002    | 9876543210987    | Aceite   | ... | 15.75  |

La aplicación mostrará las columnas en las posiciones 0, 1, 2 y la última columna como: Código, Código de Barras, Repuesto y Precio respectivamente.
