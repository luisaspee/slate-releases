<div align="center">

# SLATE

### Motor Documental para Ingeniería

_Escribe como ingeniero. Exporta como profesional._

---

![Version](https://img.shields.io/badge/versión-0.1.0--alpha-f38ba8?style=flat-square)
![Platform](https://img.shields.io/badge/plataforma-Windows-89b4fa?style=flat-square)
![License](https://img.shields.io/badge/licencia-Non--Commercial-a6e3a1?style=flat-square)
![Built with](https://img.shields.io/badge/motor-Typst-cba6f7?style=flat-square)

</div>

---

## ¿Qué es SLATE?

SLATE es un entorno documental **local-first** diseñado específicamente para ingeniería, ciencias y el mundo académico. Combina la fluidez visual de un editor de texto moderno (basado en Lexical) con el poder de compilación tipográfica de **Typst**, generando PDFs de calidad profesional sin requerir programación por parte del usuario.

A diferencia de editores genéricos, SLATE está construido alrededor de un **Sistema Vault** que garantiza la portabilidad de tus proyectos, datos y tablas vinculadas en cualquier computador o pendrive.

---

## Arquitectura y Características de Alto Impacto

### 🗄️ Sistema Vault (Portabilidad Absoluta)

SLATE no guarda archivos de forma caótica. Todo se organiza en un **Vault** (una bóveda de proyecto).

- **Dual-Path Resolver:** Las referencias a archivos externos (como planillas Excel) usan rutas relativas. Si mueves tu Vault a un pendrive o a OneDrive, los enlaces de tus documentos `.slt` no se rompen.
- **Portable por Diseño:** Modo centinela (`.slateroot`) que aísla toda la configuración (`registry.json`, cachés) en la misma carpeta del ejecutable, logrando un uso 100% portable y Cero-Huella.

### 📊 Data Anchor & Grillas Interactivas

Los ingenieros trabajan con datos. SLATE integra herramientas nativas para ello:

- **Tablas Vinculadas (.xlsx):** Conecta rangos de Excel directo a tu documento, permitiendo la actualización automática de datos a raíz del archivo .xlsx enlazado. Si el archivo original no se encuentra, SLATE utiliza la caché local incrustada sin colapsar el documento (`embedded: true`).

### 🔗 Sistema de Referencias Cruzadas y Variables

Más allá de figuras y tablas, SLATE automatiza toda la estructura cruzada con _typeahead_ inteligente:

- **Elementos de documento:** Figuras (`@fig:`), Tablas (`@tbl:`), Ecuaciones (`@eq:`), Anexos PDF (`@apx:`)
- **Gestor Bibliográfico:** Referencias bibliográficas automáticas (`@cite:`) con lectura de archivos `.bib`.
- **Variables Dinámicas:** Inyección directa de variables de proyecto y configuración (`@var:`) dentro del flujo de texto.

### 🛠️ Inyección "Raw Typst" y Plantillas (Scaffolding)

Para _power users_ que necesitan ir más allá del editor visual:

- **Raw Typst Nodes:** Inyecta código nativo de Typst directamente en el flujo del documento Lexical (ideal para algoritmos complejos, layouts custom o macros).
- **ScaffoldBuilder:** Sistema de plantillas dinámicas separadas (`theme.typ`, `schema.json`, `theme_values.json`). Cambia la apariencia entera del PDF (portadas, tipografías, variables institucionales) sin alterar una sola línea del contenido del documento.
- **ScaffoldIDE:** Entorno de desarrollo completo incrustado en SLATE. Un editor CodeMirror con soporte nativo LSP para Typst (vía Tinymist), que proporciona autocompletado semántico, resaltado avanzado y _live preview_ del PDF ("Ghost Rendering") mientras editas el código de la plantilla.

### 📐 Herramientas Visuales Integradas

- **Editor de Ecuaciones (KaTeX):** Más de 292 expresiones matemáticas integradas con búsqueda semántica en español.
- **Excalidraw Integrado:** Crea sketches y diagramas de ingeniería directamente dentro del editor. Los diagramas se inyectan como vectores escalables en el PDF compilado.
- **MediaBuilderModal (Gestor Unificado de Medios):** Un centro de recursos visuales con bóvedas locales.
  - **ChartBuilder:** Motor de gráficos nativo impulsado por **Apache ECharts**. Soporta 9 tipos de visualización interactiva (Barras, Líneas, Dispersión, Torta, Radar, Heatmap, Velas, Gauge y Boxplot) con importación directa desde CSV o pegapapeles.
  - **FigureBuilder:** Gestor de imágenes con una "Bóveda" exclusiva por proyecto (Workspace Vault), asegurando que todas las imágenes insertadas estén portables y centralizadas.

---

## Requisitos

- Windows 10 / Windows 11 (64-bit)
- WebView2 — se instala automáticamente si no está presente

---

## Instalación

### Estándar (recomendada)

1. Descarga `SLATE_0.1.0_x64-setup.exe` desde la sección **Releases**.
2. Ejecuta el instalador y sigue las instrucciones.
3. Abre SLATE desde el menú de inicio.

### Portable (pendrive / sin instalación)

1. Instala SLATE en tu computador y copia la carpeta completa de instalación a tu pendrive.
2. Crea un archivo vacío llamado `.slateroot` en la misma carpeta que `slate-app.exe`.
3. Ejecuta `slate-app.exe` directamente. SLATE detectará el centinela y aislará sus datos localmente.
*(Tip: Recomendamos llevar también el instalador `SLATE_0.1.0_x64-setup.exe` en tu pendrive. Si pruebas SLATE en un computador que no tenga el motor WebView2, ejecutar el instalador lo descargará e instalará automáticamente).*

---

## Estado Alpha

SLATE se encuentra en fase **Alpha** (lanzamiento inicial comunidad FCFM). Las funcionalidades core están implementadas y probadas, pero pueden existir comportamientos inesperados. Se recomienda mantener copias de seguridad de los documentos importantes.

El feedback es bienvenido — abre un **Issue** en este repositorio para reportar problemas o sugerencias.

---

## Licencia y Uso (TECTONIC Fortress)

SLATE es **gratuito exclusivamente para uso personal y académico**.

Como medida de protección, los documentos generados con la versión gratuita incluyen metadatos invisibles a nivel binario (`non-commercial-use-only`) para auditoría de licenciamiento.

El uso comercial, institucional o empresarial requiere adquirir una licencia comercial de **TECTONIC**. Consulta el archivo `LICENSE` para más detalles.

© 2026 Luis Aspee — TECTONIC. Todos los derechos reservados.

</div>
