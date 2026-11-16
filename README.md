<p align="center">

<img src="img/banner.jpg" alt="El lado invisible del progreso urbano" width="100%"/>

</p>

<p align="center">

<img src="https://img.shields.io/badge/R-276DC3?logo=r&amp;logoColor=white" alt="R"/> <img src="https://img.shields.io/badge/R%20Markdown-512A75?logo=rstudioide&amp;logoColor=white" alt="R Markdown"/> <img src="https://img.shields.io/badge/mapas-leaflet-76509A" alt="leaflet"/> <img src="https://img.shields.io/badge/gr%C3%A1ficos-ggplot2-9475B5" alt="ggplot2"/> <img src="https://img.shields.io/badge/curso-2026--2027-B5418A" alt="Curso 2026-2027"/>

</p>

::: {align="center"}
# El lado invisible del progreso urbano

**Análisis territorial de la contaminación atmosférica, la exposición a luz nocturna y los indicadores de salud mental en España.**

Seminario de la asignatura **Fuentes de Datos Biomédicos y Web Semántica** Curso **2026-2027**

**Autoras:** Claudia Fernández Ruiz y Nieves García Morquillas
:::

------------------------------------------------------------------------

::: {align="center"}
## DE QUÉ TRATA
:::

::: {style="text-align: justify"}
Las ciudades se diseñan pensando en la salud física *(calidad del aire, del agua, radiación...)*, pero ¿qué ocurre con la **salud mental**?

En este seminario se explora, con **datos oficiales** y a escala de **comunidad autónoma**, si la **luz nocturna**, el **ruido** y la **contaminación atmosférica** *(NO2 y O3)* se relacionan con los **trastornos mentales**, la **depresión**, las **horas de sueño** y el **consumo de psicofármacos** en España.
:::

::: {align="center"}
## OBJETIVOS

### Objetivo general
:::

::: {style="text-align: justify"}
Analizar, a escala de Comunidad Autónoma, si la exposición lumínica, acústica y atmosférica se relaciona con peores indicadores de salud en España.

### Objetivos específicos

1.  Estudiar el impacto que tiene la presencia de luz artificial durante la noche sobre nuestro ritmo circadiano. Pretende buscar el impacto que tiene la no presencia de oscuridad en las horas nocturnas y el impacto en la conciliación del sueño.

2.  Vincular los factores contaminantes con el deterioro del estado de salud mental. Observar el efecto de estos contaminantes en la prevalencia del deterioro del estado de la salud mental y, en consecuencia, con el desarrollo de trastornos mentales.

3.  Comprobar la percepción pública con los datos reales de percepción acústica. Establecer si el ruido es un factor influyente en el desarrollo de cuadros depresivos y, por tanto, una ciudad con peor índice de esta contaminación se ve condicionada a un mayor consumo de fármacos antidepresivos en su población.
:::

::: {align="center"}
## PREGUNTAS DE INVESTIGACIÓN
:::

::: {style="text-align: justify"}
**1.** ¿Una mayor **contaminación lumínica** se vincula con menos **horas de sueño** y más consumo de **fármacos para dormir**?

**2.** ¿La exposición simultánea a **ruido y luz nocturna** se correlaciona con una peor **salud mental**?

**3.** ¿La **molestia por ruido** que percibe la población coincide con el **NO2** (tráfico) y se relaciona con la **depresión** y el consumo de **antidepresivos**?
:::

::: {align="center"}
## RESULTADOS EN UN VISTAZO

<img src="img/mapa_exposicion.png" alt="Mapa del índice de exposición combinada" width="49%"/> <img src="img/mapa_depresion.png" alt="Mapa de la población con cuadro depresivo mayor" width="49%"/>

| Pregunta | Relación estudiada | rho de Spearman | p-valor | Resultado |
|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| 1 | Luz nocturna – Horas de sueño | -0,04 | 0,881 | Sin relación |
| 1 | Luz nocturna – Tranquilizantes | 0,12 | 0,649 | Sin relación |
| 2 | Exposición combinada – Depresión | **0,70** | **0,002** | **Asociación fuerte y significativa** |
| 2 | Exposición combinada – Trastornos mentales | 0,39 | 0,117 | Moderada, no significativa |
| 3 | Ruido molesto – NO2 | 0,16 | 0,541 | No coinciden |
| 3 | Ruido molesto – Depresión | **0,62** | **0,008** | **Asociación fuerte y significativa** |
| 3 | Ruido molesto – Antidepresivos | 0,49 | 0,057 | Moderada, casi significativa |

<img src="img/dispersion_depresion.png" alt="Relación entre la exposición combinada y la depresión" width="75%"/>
:::

::: {style="text-align: justify"}
**Importante:** son asociaciones a nivel de comunidad autónoma *(estudio ecológico con 17 comunidades)*, no relaciones causa-efecto. Las limitaciones se detallan en el apartado de conclusiones del seminario.
:::

::: {align="center"}
## EL SEMINARIO EN UNA IMAGEN

<img src="img/nube_palabras.png" alt="Nube de palabras con los conceptos clave del seminario" width="70%"/>
:::

::: {align="center"}
## FUENTES DE DATOS

| Variable | Año | Fuente |
|:----------------------:|:----------------------:|:----------------------:|
| Luz nocturna, NO2 y O3 | 2023 | [Google Earth Engine](https://earthengine.google.com/) |
| Ruido exterior molesto y trastornos mentales | 2023 | [INCLASNS – Ministerio de Sanidad](https://inclasns.sanidad.gob.es/main.html) |
| Cuadro depresivo mayor | 2022 | [Instituto Nacional de Estadística](https://www.ine.es/) |
| Horas de sueño | 2011 | [Instituto Nacional de Estadística](https://www.ine.es/) |
| Consumo de tranquilizantes y antidepresivos | 2001 | [Ministerio de Sanidad – Encuesta Nacional de Salud](https://www.sanidad.gob.es/estadEstudios/sanidadDatos/home.htm) |
| Población por comunidad autónoma | 2022 | [INE – Padrón a 1 de enero de 2022](https://www.boe.es/eli/es/rd/2022/12/20/1037) |
:::

::: {align="center"}
## ESTRUCTURA DEL REPOSITORIO
:::

```         
Seminario-Fuentes-de-Datos/
├── README.md                          <- Esta página
├── Seminario-Fuentes-de-Datos.Rmd     <- Cuaderno de R (texto + código)
├── Seminario-Fuentes-de-Datos.html    <- Seminario renderizado
├── Seminario-Fuentes-de-Datos.Rproj   <- Proyecto de RStudio
├── data/
│   ├── ambientales/                   <- GeoJSON de luz nocturna, NO2 y O3 (2023)
│   └── sanitarios/                    <- Excel y CSV de salud mental, sueño y fármacos
├── bibliografia/
│   ├── referencias.bib                <- Referencias 
│   └── apa.csl                        <- Estilo de citas APA
├── estilos/
│   ├── estilos.css                    <- Diseño del HTML
│   └── fondo_seminario.png            <- Imagen de fondo del HTML
└── img/                               <- Imágenes de este README
```

::: {align="center"}
## CÓMO REPRODUCIRLO
:::

::: {style="text-align: justify"}
**1.** Clona el repositorio y abre `Seminario-Fuentes-de-Datos.Rproj` en RStudio.

**2.** Instala los paquetes necesarios (solo la primera vez):
:::

``` r
install.packages(c("sf", "dplyr", "readr", "readxl", "knitr", "kableExtra",
                   "leaflet", "ggplot2", "wordcloud2", "rmarkdown"))
```

::: {style="text-align: justify"}
**3.** Abre `Seminario-Fuentes-de-Datos.Rmd` y pulsa **Knit**. Se generan el HTML y las figuras de la carpeta `img/`.
:::

::: {align="center"}
## ORIGEN DE LAS IMÁGENES
:::

| Imagen | Origen |
|:----------------------------------:|:----------------------------------:|
| `img/banner.jpg` | Recorte de la imagen de fondo del seminario *(generada por las autoras con Microsoft Copilot)* con el título superpuesto |
| `img/mapa_exposicion.png`<br>`img/mapa_depresion.png`<br>`img/dispersion_depresion.png` | Elaboración propia con `ggplot2` a partir de los datos del seminario *(bloque `figuras-readme` del Rmd)* |
| `img/nube_palabras.png` | Captura de la nube de palabras creada con `wordcloud2` en el Rmd |
| Insignias de la parte superior | [shields.io](https://shields.io/) |
| Estilo de citas `apa.csl` | [Citation Style Language](https://github.com/citation-style-language/styles) *(licencia CC BY-SA 3.0)* |

::: {align="center"}
## USO DE INTELIGENCIA ARTIFICIAL
:::

::: {style="text-align: justify"}
En el seminario se declara el uso de **Microsoft Copilot** *(imagen de fondo)* y **ChatGPT** *(apoyo con el CSS)*.

Todo el contenido ha sido revisado por las autoras.
:::
