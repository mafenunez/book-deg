# R/tema.R
# Configuración de estilo compartida por todos los capítulos del libro.
# Se carga con: source("R/tema.R") en el primer chunk de cada .qmd

# --- Tipografía ---
sysfonts::font_add_google("Poppins", "poppins")
showtext::showtext_auto()
showtext::showtext_opts(dpi = 300)

fuente_regular <- "poppins"
fuente_bold    <- "poppins"

# --- Paleta de colores ---
color_primario   <- "#DD5C61"  # rojo coral — color de marca / series únicas
color_secundario <- "#1B2740"  # azul marino — texto, ejes, líneas de referencia
color_fondo      <- "#FFFFFF"
color_texto      <- "#1B2740"
color_texto_sec  <- "#5B6472"  # gris azulado — subtítulos y notas al pie
color_grid       <- "#E7E2DF"

# --- Tema ggplot2 reutilizable ---
tema_libro <- function(base_size = 12) {
  ggplot2::theme_minimal(base_size = base_size) +
    ggplot2::theme(
      text = ggplot2::element_text(family = fuente_regular, color = color_texto),
      plot.title = ggplot2::element_text(family = fuente_bold, face = "bold",
                                          color = color_secundario, size = base_size * 1.3),
      plot.subtitle = ggplot2::element_text(color = color_texto_sec, size = base_size * 1.0),
      plot.caption = ggplot2::element_text(color = color_texto_sec, size = base_size * 0.75,
                                            hjust = 0),
      axis.title = ggplot2::element_text(color = color_secundario),
      axis.text = ggplot2::element_text(color = color_texto_sec),
      panel.grid.major = ggplot2::element_line(color = color_grid, linewidth = 0.3),
      panel.grid.minor = ggplot2::element_blank(),
      plot.background = ggplot2::element_rect(fill = color_fondo, color = NA),
      panel.background = ggplot2::element_rect(fill = color_fondo, color = NA),
      legend.position = "bottom",
      legend.title = ggplot2::element_blank()
    )
}

# Paleta discreta de apoyo (por si necesitas más de una serie)
paleta_libro <- c(color_primario, color_secundario, "#E8A87C", "#8AA6A3", color_texto_sec)
