Póster en LaTeX sobre Fractales

Este proyecto tiene como objetivo crear un póster académico en LaTeX dedicado al estudio y visualización de fractales. La idea principal es presentar de forma clara y visual algunos conceptos fundamentales de geometría fractal, junto con ejemplos clásicos y una breve explicación de cómo pueden construirse mediante procesos iterativos.

Objetivo

El póster busca mostrar cómo estructuras aparentemente complejas pueden generarse a partir de reglas matemáticas simples y repetitivas. Entre los ejemplos que pueden incluirse se encuentran:

Conjunto de Cantor.

Triángulo de Sierpiński.

Alfombra de Sierpiński.

Esponja de Menger.

Otros fractales generados mediante algoritmos iterativos.

Herramientas utilizadas

El póster se desarrolla utilizando:

LaTeX para la composición del documento.

TikZ para figuras y diagramas.

PGFPlots cuando se requieren gráficas.

beamerposter o tikzposter para la estructura del póster.

Imágenes generadas mediante Python, Manim u otros programas cuando sea necesario.

Estructura del proyecto

Una posible organización de archivos es:

poster-fractales/
│
├── main.tex
├── README.md
│
├── imagenes/
│   ├── sierpinski.png
│   ├── menger.png
│   └── mandelbrot.png
│
├── figuras/
│   └── fractales.tex
│
└── referencias.bib

Creación del póster

El archivo principal puede comenzar con una estructura similar a la siguiente:

\documentclass[final]{beamer}

\usepackage[size=a0,scale=1.2]{beamerposter}
\usepackage{graphicx}
\usepackage{tikz}
\usepackage{amsmath}
\usepackage{amssymb}

\title{Fractales: geometría, iteración y autosimilitud}
\author{Autor}
\institute{Universidad}

\begin{document}

\begin{frame}[t]

\begin{columns}[t]

\begin{column}{0.32\textwidth}

\begin{block}{Introducción}
Los fractales son objetos geométricos caracterizados por presentar
estructuras complejas que pueden surgir a partir de reglas iterativas simples.
\end{block}

\end{column}

\begin{column}{0.32\textwidth}

\begin{block}{Autosimilitud}
Muchos fractales presentan autosimilitud, es decir, partes de la figura
mantienen una estructura semejante a la figura completa.
\end{block}

\end{column}

\begin{column}{0.32\textwidth}

\begin{block}{Ejemplos}
Aquí pueden incluirse imágenes del triángulo de Sierpiński,
la esponja de Menger o el conjunto de Mandelbrot.
\end{block}

\end{column}

\end{columns}

\end{frame}

\end{document}

Conceptos matemáticos

Autosimilitud

Una de las características más importantes de muchos fractales es que una parte del objeto conserva una estructura semejante al objeto completo.

Iteración

Los fractales suelen construirse aplicando repetidamente una misma regla. Si una transformación se representa mediante una función

x_{n+1}=f(x_n),

el comportamiento del sistema después de muchas iteraciones puede producir estructuras de gran complejidad.

Dimensión fractal

A diferencia de los objetos geométricos tradicionales, algunos fractales poseen una dimensión no entera.

Para un fractal autosimilar formado por (N) copias reducidas por un factor (r), la dimensión de Hausdorff puede expresarse como

D=\frac{\ln N}{\ln(1/r)}.

Por ejemplo, para el triángulo de Sierpiński:

D=\frac{\ln 3}{\ln 2}\approx 1.585.

Para la esponja de Menger:

D=\frac{\ln 20}{\ln 3}\approx 2.727.

Esponja de Menger

La esponja de Menger se construye a partir de un cubo.

Se divide el cubo en (27) cubos pequeños.

Se eliminan el cubo central y los cubos centrales de cada cara.

Permanecen (20) cubos.

El proceso se repite sobre cada uno de los cubos restantes.

Después de (n) iteraciones, el número de cubos es

N_n = 20^n.

Si el cubo inicial tiene lado (L), cada cubo después de (n) iteraciones tendrá lado

L_n=\frac{L}{3^n}.

Este fractal es especialmente interesante porque su volumen tiende a cero mientras que su superficie crece indefinidamente.

Compilación

Si se utiliza pdflatex:

pdflatex poster.tex

Si el proyecto contiene bibliografía:

pdflatex poster.tex
bibtex poster
pdflatex poster.tex
pdflatex poster.tex

También puede compilarse directamente en Overleaf.

Recomendaciones para el diseño

Para que el póster sea fácil de leer:

Utilizar poco texto y priorizar figuras.

Mantener títulos grandes y visibles.

Dividir la información en bloques.

Evitar ecuaciones demasiado largas.

Utilizar imágenes de alta resolución.

Mantener una estructura visual consistente.

Incluir referencias para las definiciones y resultados matemáticos utilizados.

Posible organización del contenido

El póster puede dividirse en las siguientes secciones:

Introducción a los fractales.

Autosimilitud e iteración.

Dimensión fractal.

Construcción del triángulo o alfombra de Sierpiński.

Construcción de la esponja de Menger.

Visualizaciones generadas computacionalmente.

Aplicaciones de los fractales.

Conclusiones.

Referencias.

Propósito del proyecto

Además de presentar los conceptos matemáticos, este proyecto puede servir para explorar la relación entre matemáticas, programación y visualización científica, utilizando algoritmos para generar las figuras que posteriormente se incorporan al póster elaborado en LaTeX.