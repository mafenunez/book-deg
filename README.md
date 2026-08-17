# Libro Quarto

## Estructura
```
quarto-book/
├── _quarto.yml        # configuración del libro (título, capítulos, cover-image)
├── styles.scss         # tema de color (#DD5C61 / #1B2740 / etc.) + fuente Poppins
├── R/
│   └── tema.R           # colores, fuente y tema ggplot2 compartidos por los capítulos
├── images/
│   └── banner.jpg        # << REEMPLAZA por tu imagen de portada
├── index.qmd            # portada / prefacio (incluye el banner)
├── 01-seccion1.qmd
├── 02-seccion2.qmd
└── 03-seccion3.qmd
```

## Para poner tu banner
1. Copia tu imagen dentro de `images/`, reemplazando `banner.jpg`
   (o usa otro nombre, pero actualízalo en dos lugares):
   - `_quarto.yml` → campo `cover-image:`
   - `index.qmd` → dentro del bloque `.portada-banner`
2. Se recomienda una imagen horizontal (ej. 1600×500 px) para que se vea bien
   como banner ancho.

## Paquetes de R necesarios
```r
install.packages(c("sysfonts", "showtext", "ggplot2", "gt"))
```

## Renderizar el libro
Desde la carpeta del proyecto, en la terminal:
```bash
quarto render
```
Esto genera el libro en `_book/` (HTML por defecto; PDF también está
configurado en `_quarto.yml` si tienes LaTeX instalado).

Para previsualizar mientras editas:
```bash
quarto preview
```

## Personalizar
- **Colores y fuente**: edita `R/tema.R` (para gráficos) y `styles.scss`
  (para el sitio web) — ambos ya están alineados con tu paleta original.
- **Añadir más capítulos**: crea un nuevo `.qmd` y agrégalo a la lista
  `chapters:` en `_quarto.yml`.
