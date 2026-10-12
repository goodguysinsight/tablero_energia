# Tablero Censo 2025 — Energía

Tablero interactivo de los **Censos Nacionales 2025 (INEI)** con tres indicadores
a tres niveles (departamental, provincial y distrital):

- **Combustible para cocinar** en hogares.
- **Procedencia de la energía eléctrica** en viviendas particulares.
- **Pobreza energética** (estimación referencial): cruce combustible × electricidad.

## Características
- Selector de indicador (combustible · energía eléctrica · pobreza energética).
- Filtros en cascada: Departamento → Provincia → Distrito.
- Etiquetas regionales con nombre y valor (% o cantidad), sin superposición.
- Mapa coroplético con leyenda por categoría y panel de desglose nacional.

## Pobreza energética — nota metodológica
Es una **estimación referencial**, no un dato oficial. Se construye cruzando los
marginales de combustible (respuesta múltiple) y de fuente eléctrica (respuesta
única) bajo **supuesto de independencia** en cada unidad. Matriz 2×3:

| | Red pública | Alternativa (panel/generador/eólica/otro) | Sin acceso |
|---|---|---|---|
| **Sólidos** (leña, carbón, bosta, otro, no cocinan) | Pobre | Pobre | Extremo pobre |
| **Limpios** (electricidad, GLP, GN) | No pobre | Depende de la suficiencia eléctrica | Pobre |

El cálculo exacto requiere microdatos del Censo 2025 (cruce a nivel de hogar).

## Uso
Página autocontenida. Abre `index.html` o publícala con **GitHub Pages**
(Settings → Pages → Branch: `main` / carpeta raíz).

## Datos
- Fuente: Instituto Nacional de Estadística e Informática — Censos Nacionales 2025:
  XIII de Población, VIII de Vivienda y IV de Comunidades Indígenas.
- Datos censales al 15 de julio de 2026 (límites vigentes RENLIM).
- Elaboración: **Good Guys Insight**.
