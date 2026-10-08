# El binomio de Newton · de los exponentes a la combinatoria

[![Licencia: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)

Actividad web interactiva para el tema **binomio de Newton**, pensada para la unidad 2 de
*Tópicos de Matemáticas* (Licenciatura en Matemáticas, Universidad Autónoma de Nayarit).

La idea que organiza toda la página es una sola: **desarrollar (a + b)ⁿ no es aplicar una
fórmula, es contar**. Multiplicar (a + b) por sí mismo n veces equivale a elegir, en cada
paréntesis, uno de los dos términos; cada elección produce una «palabra», y el coeficiente de
cada término es simplemente **cuántas palabras hay de ese tipo**. De ahí salen los números
combinatorios, y de ahí salen también sus aplicaciones fuera del álgebra.

---

## Contenido

| Pestaña | Tema | Qué puede hacer el estudiante |
|---|---|---|
| ① | **Desarrollo** | Mover n y escribir cualquier par de términos —`a` y `b`, `2x` y `−3`, `x²` y `1/x`— para ver el desarrollo completo. Al tocar un término se descompone en sus tres piezas: coeficiente, potencia del primero y potencia del segundo, con el cálculo de C(n,k) desarrollado |
| ② | **Los exponentes** | Avanzar término por término —o dejar que la página los recorra sola— y ver en dos barras cómo un exponente baja de n a 0 mientras el otro sube de 0 a n, y cómo la suma nunca cambia |
| ③ | **Triángulo de Pascal** | Tocar cualquier casilla: se marcan sus dos «padres», se muestra la regla de Pascal con números, el término que acompaña, la suma de la fila (2ⁿ) y el simétrico. Dos botones: **Resaltar los impares**, que deja los números a la vista y atenúa los pares, y **Ver el triángulo de Sierpiński**, que abre un recorrido guiado de cinco pasos —4, 8, 16 y 32 filas— en el que las casillas se vuelven cuadritos pintados por paridad, con el conteo de impares en cada paso (9 → 27 → 81 → 243) y la explicación por el teorema de Lucas al final. Los cuadritos siguen siendo clicables y el panel dice el valor y la paridad |
| ④ | **Término k-ésimo** | Calcular un término concreto sin desarrollar todo, con n hasta 60. Admite coeficientes fraccionarios y exponentes negativos, de modo que casos como (x² + 1/x)⁶ se resuelven igual que los sencillos |
| ⑤ | **Por qué C(n,k)** | Elegir a mano, paréntesis por paréntesis, qué término se toma de cada factor; ver todas las palabras posibles agrupadas por cuántas b contienen, y comprobar que el tamaño de cada grupo es exactamente el coeficiente binomial. Incluye seis aplicaciones de conteo y probabilidad |
| ⑥ | **Pirámide 3D** | Girar con el ratón, con el dedo, con los botones o con las flechas del teclado una **pirámide de Sierpiński** (tetraedro de Sierpiński) dibujada en tres dimensiones. Se elige el nivel de 0 a 5 —de 1 a 1 024 tetraedros—, se acerca o se aleja, se activa o se pausa el giro automático y se muestran u ocultan las aristas. Un panel actualiza en cada nivel el número de tetraedros, los huecos quitados, el volumen restante y la dimensión (log 4 / log 2 = 2), y explica el puente con el **tetraedro de Pascal**: los coeficientes de (a + b + c)ⁿ y el criterio de paridad de Kummer |
| ⑦ | **Práctica** | Diez reactivos generados al azar, con marcador y racha |

En la práctica **cada distractor corresponde a un error frecuente identificado** —confundir n
con n + 1 términos, usar el índice k como posición, equivocar la paridad que decide el signo en
(a − b)ⁿ, sumar las filas equivocadas del triángulo—. La retroalimentación dice qué se hizo mal,
no sólo que la respuesta es incorrecta.

---

## Lo que la actividad quiere que quede claro

1. **Hay n + 1 términos, no n.** El índice k empieza en 0, y de ahí viene el desfase entre el índice y el número de término, que es el error más común al pedir «el séptimo término».
2. **Los dos exponentes suman n en todos los términos.** Es la verificación más rápida de un desarrollo: si no suman n, hay un error.
3. **Los coeficientes son simétricos** porque elegir k para llevar es lo mismo que elegir n − k para dejar.
4. **La fila n del triángulo suma 2ⁿ** porque es el desarrollo de (1 + 1)ⁿ, y 2ⁿ es el número de subconjuntos de un conjunto de n elementos.
5. **El coeficiente C(n,k) cuenta**: de cuántas maneras se eligen los k paréntesis que aportan la b. Es la misma pregunta que «¿de cuántas formas elijo k objetos de n?».
6. **La paridad de los coeficientes tiene forma.** Marcar los impares del triángulo dibuja el triángulo de Sierpiński; pasar de dos letras a tres convierte el triángulo de números en un tetraedro y la figura en una pirámide. El número de letras del binomio —o trinomio— es la dimensión de la figura que aparece.

## Aplicaciones que aparecen en la pestaña ⑤

| Situación | Cálculo | Resultado |
|---|---|---|
| Comité de 3 personas entre 10 | C(10, 3) | 120 comités |
| Menú con 8 ingredientes opcionales | 2⁸, la suma de la fila 8 | 256 combinaciones |
| Rutas en una cuadrícula de 4 × 3 | C(7, 3) | 35 rutas |
| Exactamente 6 águilas en 10 volados | C(10, 6) de 2¹⁰ | 210 de 1 024 ≈ 20.5 % |
| Muestra de 4 piezas de un lote de 12 | C(12, 4) | 495 muestras |
| Interés compuesto a dos periodos | (1 + i)² = 1 + 2i + i² | con i = 8 %, el término i² aporta 0.64 % |

La pestaña incluye además una calculadora de C(n, k) que muestra la fórmula con factoriales, el
valor y la lectura de conteo.

---

## Cómo publicarla en GitHub Pages

1. Cree un repositorio nuevo en GitHub llamado `binomio-de-newton`.
2. Suba los archivos de esta carpeta a la raíz del repositorio (`index.html`, `README.md`,
   `CITATION.cff`, `LICENSE`).
   Desde la web: **Add file → Upload files**, arrastrar y **Commit changes**.
3. Entre a **Settings → Pages**.
4. En *Source* elija **Deploy from a branch**; en *Branch* elija `main` y la carpeta `/ (root)`.
   Guarde con **Save**.
5. Espere un minuto. La página quedará publicada en:

   ```
   https://daliacastillo.github.io/binomio-de-newton/
   ```

Desde la terminal, el equivalente es:

```bash
git init
git add .
git commit -m "Actividad interactiva del binomio de Newton"
git branch -M main
git remote add origin https://github.com/daliacastillo/binomio-de-newton.git
git push -u origin main
```

---

## Sugerencias de uso en clase

- **Empiece por la pestaña ⑤, no por la ①.** Si los estudiantes ven primero que el coeficiente
  cuenta palabras, la fórmula deja de ser arbitraria. Proyecte n = 3 y pida que enumeren a mano
  las ocho palabras antes de mostrar el agrupamiento.
- **La pestaña ② como criterio de autocorrección.** Pida que, antes de entregar cualquier
  desarrollo, verifiquen que los exponentes suman n en todos los términos. Es la revisión más
  rentable del tema.
- **La pestaña ④ para justificar la fórmula del término general.** Proponga «el término que
  contiene x⁶ en (2x − 3)¹⁰» y deje que intenten desarrollarlo completo; la fórmula se vuelve
  necesaria por economía, no por autoridad.
- **El desfase k ↔ posición.** Vale la pena dedicarle un momento explícito: pida «el séptimo
  término» y observe cuántos usan k = 7.
- **El recorrido de Sierpiński de la pestaña ③** funciona bien como cierre. Use primero *Resaltar
  los impares* con pocas filas, para que vean la paridad sin perder los números; después abra el
  recorrido y avance paso a paso. Deténgase en el conteo —9, 27, 81, 243— y pregunte qué pasará al
  llegar a 64 filas antes de mostrar el último paso. La explicación por el teorema de Lucas conecta
  el tema con aritmética modular y con autosemejanza sin salirse del programa.
- **La pirámide de la pestaña ⑥ para cerrar la unidad.** Proyecte el nivel 1 y pregunte qué se
  quitó: la respuesta —un octaedro en el centro— rara vez se adivina. Suba al nivel 3 con el giro
  automático encendido y plantee la paradoja: la superficie no cambia nunca y el volumen tiende a
  cero. Sirve para introducir, sin tecnicismos, la idea de dimensión fraccionaria y la de límite.
- **Tarea.** La serie de práctica puede pedirse como evidencia: captura de pantalla del marcador
  final con 8 o más aciertos.

---

## Notas técnicas

- **Un solo archivo.** Todo (HTML, CSS y JavaScript) está en `index.html`. No hay dependencias,
  no se carga nada de internet y funciona sin conexión: basta abrir el archivo en cualquier navegador.
- **Sin build ni instalación.** No requiere Node, npm ni ningún compilador.
- **Aritmética exacta con enteros grandes.** Los coeficientes binomiales se calculan con `BigInt`,
  de modo que C(60, 30) o el término 31 de (x + 1)⁶⁰ se muestran con todas sus cifras, sin
  notación científica ni errores de redondeo. Los coeficientes de los monomios se manejan como
  fracciones exactas.
- **Analizador de monomios propio.** Los campos de entrada aceptan `3`, `-5`, `2/3`, `x`, `2x`,
  `2x^3`, `x²`, `x/2` y `1/x`; no se usa `eval` en ningún punto.
- **Trazo 3D propio, sin bibliotecas.** La pirámide de la pestaña ⑥ se dibuja sobre un `<canvas>`
  2D con código escrito a mano: rotación por dos ángulos, proyección en perspectiva, descarte de
  caras ocultas, ordenamiento por profundidad (algoritmo del pintor) y sombreado lambertiano. No
  usa WebGL ni `three.js`, de modo que el archivo sigue siendo uno solo y funciona sin conexión.
  En el nivel 5 dibuja 1 024 tetraedros —4 096 caras— y se mantiene fluida.
- **Responsiva.** Funciona en computadora, tableta y teléfono (probada hasta 390 px de ancho).
- **Tema claro y oscuro**, con botón de cambio y respeto a la preferencia del sistema.
- **Sin almacenamiento.** No guarda datos, no usa cookies ni `localStorage` y no envía nada a
  ningún servidor; el marcador vive sólo mientras la pestaña está abierta.
- **Citable.** Lleva metadatos de citación en el `<head>` (Dublin Core, etiquetas `citation_*` de
  Google Académico y `JSON-LD` de schema.org) y un archivo `CITATION.cff` en la raíz.

### Cómo modificarla

- `S1`, `S2`, `S3`, `S5`, `S7` guardan el estado inicial de cada apartado.
- `construye7(m)` genera la pirámide: cada tetraedro se parte en cuatro, y el hijo `i` conserva el
  vértice `i` y cambia los otros tres por los puntos medios de las aristas que salen de él.
  Subir el máximo del control `niv7` por encima de 5 es posible, pero el número de caras se
  cuadruplica en cada nivel.
- `leeMono()` es el analizador de los campos de entrada; ampliarlo permite admitir más formas.
- `APPS` es la lista de aplicaciones de la pestaña ⑤: cada entrada es un objeto con título,
  descripción, fórmula y una función que devuelve el resultado calculado.
- `generadores()` contiene los siete tipos de reactivo de la práctica. Para agregar uno nuevo
  basta añadir una función que devuelva `{ q, ops, exp }`, con la respuesta correcta en la
  posición 0; el programa baraja las opciones por sí mismo.
- La paleta completa son variables CSS en `:root` (`--c-a`, `--c-b`, `--c-coef`, `--brand`).

---

## Cómo citar

Este repositorio incluye un archivo `CITATION.cff`, de modo que GitHub muestra el botón
**Cite this repository** en la columna derecha de la página del repositorio y genera
automáticamente la cita en APA y en BibTeX. La propia actividad lleva un bloque de créditos
al pie, con botones para copiar la cita.

**APA (7.ª edición)**

> Castillo Márquez, D. I. (2026). *El binomio de Newton: de los exponentes a la combinatoria*
> (Versión 1.0) [Material didáctico interactivo]. Universidad Autónoma de Nayarit,
> Unidad Académica de Ciencias Básicas e Ingenierías. https://daliacastillo.github.io/binomio-de-newton/

**BibTeX**

```bibtex
@misc{castillo2026binomionewton,
  author       = {Castillo Márquez, Dalia Imelda},
  title        = {{El binomio de Newton: de los exponentes a la combinatoria}},
  year         = {2026},
  version      = {1.0},
  howpublished = {Material didáctico interactivo},
  institution  = {Universidad Autónoma de Nayarit, Unidad Académica de Ciencias Básicas e Ingenierías},
  url          = {https://daliacastillo.github.io/binomio-de-newton/},
  note         = {ORCID: 0000-0002-5890-0437. Licencia CC BY-NC-SA 4.0}
}
```

### Obtener un DOI con Zenodo

1. Entre a [zenodo.org](https://zenodo.org) e inicie sesión **con su cuenta de GitHub**.
2. Vaya a *Settings → GitHub* y encienda el interruptor del repositorio `binomio-de-newton`.
   Tiene que estar encendido **antes** de crear la release.
3. En GitHub, cree una **release** (*Releases → Create a new release*) con la etiqueta `v1.0.0`
   y el título `Versión 1.0`.
4. Zenodo archiva esa release y emite dos DOI en unos minutos: el **de concepto** (el de uso
   general, que siempre resuelve a la versión más reciente) y el **de esta versión**. Escriba el
   de concepto en la línea `doi:` de `CITATION.cff`, en la constante `OBRA` de `index.html` y en
   la insignia de este README.
5. Asocie el DOI a su ORCID desde [orcid.org](https://orcid.org) → *Works → Add works →
   Search & link* → **DataCite**.

## Metadatos incluidos

- `CITATION.cff` — citación legible por máquina (botón *Cite this repository* de GitHub).
- Etiquetas `citation_*` y `DC.*` en el `<head>` — las usan Google Académico y los recolectores
  de repositorios institucionales.
- `JSON-LD` con `schema.org/LearningResource` — describe la obra como recurso educativo:
  autoría, ORCID, afiliación, nivel educativo, licencia y versión.

## Material relacionado

- [*Productos notables: la demostración que se ve*](https://doi.org/10.5281/zenodo.23195334) —
  las identidades (a + b)², (a − b)², (a + b)(a − b) y (a + b)³ demostradas con áreas y
  volúmenes. El cubo de un binomio de esa actividad es el caso n = 3 de ésta, y sus coeficientes
  1, 3, 3, 1 son la fila 3 del triángulo de Pascal.

## Créditos y licencia

Dra. Dalia Imelda Castillo Márquez · Docente investigadora
ORCID: [0000-0002-5890-0437](https://orcid.org/0000-0002-5890-0437)
Universidad Autónoma de Nayarit · Unidad Académica de Ciencias Básicas e Ingenierías

Versión 1.0 · octubre de 2026

Obra bajo licencia
[Creative Commons Atribución-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es).
Puede compartirse y adaptarse con fines no comerciales, dando crédito a la autora y distribuyendo
las obras derivadas bajo la misma licencia. Véase `LICENSE`.
