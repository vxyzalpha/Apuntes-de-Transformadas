# Señales, Fourier y muestreo digital

Material interactivo de apoyo para Electrónica e Instrumentación (UPM): tres páginas HTML autocontenidas (sin dependencias externas) que explican, con herramientas interactivas y ejercicios, la Serie de Fourier, la Transformada de Fourier y el teorema de muestreo de Nyquist-Shannon.

## Contenido

- `index.html` — página de inicio, con acceso a los tres temas.
- `fourier-series.html` — la Serie de Fourier (señales periódicas, espectro de líneas).
- `fourier-transform.html` — la Transformada de Fourier (señales aperiódicas, espectro continuo).
- `nyquist.html` — teorema de muestreo de Nyquist-Shannon (muestreo y aliasing).

Cada página incluye:
- una explicación conceptual breve,
- una herramienta interactiva (canvas + sliders) que dibuja la señal en el tiempo y su espectro en frecuencia,
- una tabla de fórmulas y propiedades,
- una batería de ejercicios con solución oculta (botón "Ver solución") para autoevaluación.

Los ejes de ordenadas de las gráficas se mantienen **fijos** dentro de cada forma de señal: al mover un slider se ve el efecto real (crecimiento/estrechamiento de la curva), en vez de que la gráfica se reescale automáticamente para llenar siempre el mismo espacio.

## Ver el sitio localmente

No hace falta ningún servidor ni build: son archivos HTML con CSS y JavaScript embebidos. Basta con abrir `index.html` en el navegador (doble clic, o `Abrir con` → tu navegador).

## Publicar con GitHub Pages

1. Sube estos archivos a un repositorio de GitHub (todos en la raíz del repo, tal como están aquí).
2. En el repositorio, ve a **Settings → Pages**.
3. En "Build and deployment", elige **Deploy from a branch**, rama `main` (o la que uses) y carpeta `/ (root)`.
4. Guarda. GitHub publicará el sitio en `https://<tu-usuario>.github.io/<nombre-del-repo>/` en un par de minutos, con `index.html` como página de inicio.

## Notas técnicas

- No hay dependencias externas (sin librerías de terceros, sin fuentes externas): todo el CSS y JS está embebido en cada archivo, y las fórmulas matemáticas se maquetan con HTML/CSS puro.
- Los espectros se calculan numéricamente en el propio navegador (DFT/integral discreta), en tiempo real, cada vez que se cambia un parámetro.
