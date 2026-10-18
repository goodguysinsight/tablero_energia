# Tablero de Energía en Viviendas — Censo Nacional 2025 (Perú)

Tablero dinámico e interactivo del acceso a energía en los hogares del Perú, a partir de los **Censos Nacionales 2025 (INEI)**: combustible utilizado para cocinar y acceso a energía eléctrica, con mapa coroplético a nivel departamental, provincial y distrital. Elaboración: **Good Guys Insight**.

## Demo

El tablero es una única página autocontenida (`index.html`). Para publicarla:

1. En este repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`.
2. La página quedará disponible en `https://goodguysinsight.github.io/tablero_energia/`.

También puede abrirse descargando `index.html` y abriéndolo en el navegador.

## Funcionalidades

- **Selector de indicador:**
  - **Combustible para cocinar** — distribución de hogares por tipo de combustible.
  - **Energía eléctrica** — acceso a alumbrado eléctrico por red pública en la vivienda.
  - **Pobreza energética (Censo)** — indicador de hogares en situación de carencia de acceso a energía.
- **Categorías** (para combustible de cocina): Gas (balón GLP), Gas natural (red de tuberías), Electricidad, Leña, Carbón, Bosta/estiércol, Otro, y hogares que no cocinan.
- **Tres niveles territoriales:** Departamental, Provincial y Distrital, con **filtros en cascada** (Departamento → Provincia → Distrito).
- **Medida:** porcentaje de hogares (**% de hogares**) o número absoluto (**N° de hogares**).
- **Mapa coroplético** coloreado por el indicador y la categoría elegidos.
- **Panel de resumen** por zona: total de hogares censados y participación de cada categoría.
- **Clic en una zona** la fija en el panel; el botón **"Ver todo"** regresa a la vista nacional.
- Diseño **responsive** para escritorio y celular.

## Fuente de datos

- **Indicadores de energía en viviendas:** **Censos Nacionales 2025: XIII de Población, VIII de Vivienda y IV de Comunidades Indígenas** — Instituto Nacional de Estadística e Informática (**INEI**).
- **Cartografía (límites distritales y provinciales):** Registro Nacional de Límites (**RENLIM**) — Secretaría de Demarcación y Organización Territorial (**SDOT – PCM**), vigencia 2023 (referenciales).

### Cobertura

Cobertura nacional a los tres niveles territoriales (25 departamentos). Las cifras corresponden a hogares censados en 2025 (~10,6 millones de hogares a nivel nacional).

## Datos

`energia_censo2025.csv` — dataset en formato largo (*tidy*), una fila por indicador × nivel × territorio × categoría:

| Columna | Descripción |
|---|---|
| `indicador` | Combustible para cocinar, Energía eléctrica o Pobreza energética (Censo) |
| `nivel` | `dep`, `prov` o `dist` |
| `ubigeo` | Código UBIGEO (2, 4 o 6 dígitos según el nivel) |
| `departamento`, `provincia`, `distrito` | Nombres territoriales |
| `total_hogares` | Total de hogares de la zona |
| `categoria` | Categoría del indicador (p. ej. Leña, Gas balón GLP, Red pública…) |
| `hogares` | Número de hogares en esa categoría |
| `porcentaje` | Participación (%) sobre el total de la zona |

## Limitaciones y notas

- Los valores son **referenciales** y pueden ajustarse según las publicaciones oficiales definitivas del INEI.
- Los límites distritales/provinciales son de vigencia 2023 (RENLIM); distritos creados con posterioridad pueden no estar representados.
- La categoría "No cocinan" agrupa a los hogares que declararon no cocinar en la vivienda.

## Créditos

Elaboración: **Good Guys Insight**. Datos: INEI (Censos Nacionales 2025; ENAHO). Límites: SDOT–PCM (RENLIM). 
