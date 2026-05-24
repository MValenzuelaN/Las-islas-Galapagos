# Especies de las Islas Galápagos

> Presentación académica sobre **Modelos Lineales** aplicados al estudio de la diversidad de especies del archipiélago de Galápagos, elaborada en formato **LaTeX Beamer**.

---

## Descripción

Esta presentación fue desarrollada como trabajo del **Laboratorio de Modelos Lineales** en la Universidad Católica del Maule. Se analiza un conjunto de datos de 25 islas del archipiélago de Galápagos con el objetivo de identificar patrones ecológicos que permitan predecir la diversidad de especies a partir de variables físicas del nicho (área, elevación y distancia a la isla más cercana).

El análisis cubre desde la exploración preliminar de los datos hasta el ajuste de un modelo de **regresión lineal múltiple** por mínimos cuadrados ordinarios (OLS), incluyendo la estimación de coeficientes y su matriz de covarianzas.

**Autor:** Matías Valenzuela Nuche  
**Profesor:** José Zúñiga Núñez  
**Institución:** Universidad Católica del Maule  
**Fecha:** Octubre 2024

---

## Contenido de la presentación

| Sección | Descripción |
|---|---|
| **Introducción** | Contexto geográfico y ecológico del archipiélago de Galápagos |
| **Descripción** | Variables del conjunto de datos (25 islas) y su tipología estadística |
| **Análisis preliminar** | Gráfico de pares y mapa de calor de correlaciones de Pearson |
| **Modelado** | Regresión lineal múltiple: formulación matricial, estimación OLS y diagnóstico |
| **Conclusión** | Síntesis e implicancias del modelo ajustado |
| **Bibliografía** | Referencias utilizadas |

### Modelo estadístico central

El modelo ajustado sigue la especificación matricial clásica:

$$Y = X\beta + \varepsilon, \quad \varepsilon \sim \mathcal{N}(0, \sigma^2 I)$$

donde $Y$ es el vector de número de especies, $X$ la matriz de diseño con las variables ecológicas, $\beta$ el vector de coeficientes y $\varepsilon$ el término de error. Los estimadores OLS obtenidos son:

$$\hat{\beta}_0 = 11.09, \quad \hat{\beta}_1 = 0.79 \text{ (área)}, \quad \hat{\beta}_2 = 0.13 \text{ (elevación)}, \quad \hat{\beta}_3 = -0.91 \text{ (distancia)}$$

con una correlación entre valores observados y predichos de $r = 0.87$.

---

## Estructura del repositorio

```
Las-islas-Galapagos/
├── presentazione.tex          # Fuente LaTeX principal (414 líneas)
├── presentazione.pdf          # Presentación compilada
├── otherResources/            # Logos institucionales y configuración del tema
├── _minted/                   # Caché de resaltado de código (minted)
├── tabla_base_datos.png       # Tabla con el conjunto de datos
├── mapa-galapagos-scaled.jpeg # Mapa del archipiélago
├── 1200px-Ernst_Haeckel_5.jpg # Imagen de Ernst Haeckel
├── big-15-galapagos-iconic-species.jpg
├── Rplot01.png                # Gráficos generados en R
├── Rplot03.png
├── Rplot04.jpeg
├── Rplot05.jpeg
├── Rplot06.jpeg
└── .gitignore
```

---

## Uso como plantilla

Este repositorio está marcado como **plantilla pública** en GitHub. Para usarlo como base para una nueva presentación Beamer:

1. Haz clic en **"Use this template"** en la página del repositorio.
2. Reemplaza el contenido de `presentazione.tex` con tu propio material.
3. Actualiza los metadatos del documento (título, autor, institución, fecha) en el preámbulo del `.tex`.
4. Sustituye los logos en `otherResources/` por los de tu institución.
5. Compila con `pdflatex` habilitando el flag `-shell-escape` (requerido por el paquete `minted`):

```
pdflatex -shell-escape presentazione.tex
```

> [!NOTE]
> El paquete `minted` requiere **Python** y la librería **Pygments** instalados en el sistema. Asegúrate de ejecutar `pip install Pygments` antes de compilar.

> [!TIP]
> La plantilla está basada en un trabajo previo de 2022 de Isac Pasianotto. La configuración del tema Beamer se encuentra en `otherResources/presentazione_myThemeSetting.tex`.

---

## Requisitos

- **LaTeX** (TeX Live, MiKTeX o MacTeX)
- **Python ≥ 3.x** con `Pygments` (para el paquete `minted`)
- Paquetes LaTeX utilizados: `beamer`, `amsmath`, `mathtools`, `tikz`, `booktabs`, `minted`, `graphicx`, `hyperref`, entre otros.

---

## Licencia

Distribuido bajo la licencia **MIT**. Consulta el archivo [LICENSE](LICENSE) para más detalles.
