# NAHAR — Autoconsumo solar industrial

Sitio corporativo de **diecinueve páginas** en español, inglés y árabe con RTL real,
para una ingeniería de autoconsumo fotovoltaico industrial.

**Ver online:** https://2troll.github.io/nahar-solar/

Un solo archivo HTML: sin compilar, sin dependencias, sin claves de API.

## Las dieciséis páginas

`Inicio` · `Servicios` · `Proceso` · `Rendimiento` · `Amortización` ·
**`Simulador`** · **`Equipos`** · **`La obra`** · **`Glosario`** ·
**`Antes de la visita`** · **`Ficha`** · `Proyectos` · `Mantenimiento` ·
`Empresa` · `Preguntas` · `Contacto`

Las seis en negrita son nuevas, y cada una trae un **formato distinto**, no
más texto:

| Página | Formato | Qué hace |
|---|---|---|
| **Curva horaria** | Áreas superpuestas con solape calculado | Tu consumo hora a hora contra la producción solar: el área verde es lo que de verdad se aprovecha. La producción sale de la duración del día por mes a 40° N, no de un dibujo |
| **Comparar ofertas** | Tabla editable con veredicto | Metes tres presupuestos y calcula el coste por kWh producido a 25 años con degradación. Avisa si la más barata no lleva garantía de producción |
| **Simulador** | Formulario con panel de resultados en vivo | Dimensiona la instalación con los datos del visitante y explica **cuál de los dos techos manda**: la cubierta o el consumo |
| **Equipos** | Tabla ordenable y filtrable | Se ordena pulsando cualquier columna, también con teclado; el filtro compara con el tipo de la primera fila, así que funciona en los tres idiomas |
| **La obra** | Diagrama de Gantt | Tres tamaños de instalación reescalan las duraciones y desplazan las tareas conservando los solapes; la ruta crítica va marcada |
| **Glosario** | Búsqueda que filtra al teclear | Catorce términos, con la coincidencia resaltada y aviso cuando no hay ninguna |
| **Antes de la visita** | Lista con progreso guardado | Ocho comprobaciones que se recuerdan en `localStorage`; el texto de abajo cambia según cuánto lleves |
| **Ficha** | Documento imprimible A4 | Recoge el resultado del simulador y se imprime con `@media print`, que oculta menú, pie y el resto de rutas |

## Lo que no es decorativo

- **Gráfica de producción mensual.** Barras de doce meses con selector de
  orientación (sur / este-oeste / ambas). Los datos salen de un perfil de
  irradiancia para latitud ~40° N; el este-oeste no es el sur multiplicado por
  una constante, sino con un factor que sube en invierno y baja en verano,
  que es lo que hace la geometría de verdad.
- **Calculadora de amortización.** Dos deslizadores (potencia instalada y
  autoconsumo directo) que recalculan el flujo de caja acumulado a 25 años,
  con degradación del panel del 0,5 % anual. La línea cruza el cero en el año
  de amortización, marcado.
- **Lámina isométrica** de la instalación, generada con trigonometría en SVG.
  No es una imagen: se redibuja con el tema y no se pixela.

Todos los supuestos del modelo económico están escritos en la propia página,
y las cifras del cálculo cuadran con las que anuncia la portada.

## Traducción

- 139 claves × 3 idiomas, paridad exacta, 0 sin traducir.
- Las estructuras (pasos, proyectos, planes, preguntas) son arrays paralelos:
  6/6/6, 3/3/3, 6/6/6 en los tres idiomas.
- Dígitos árabe-índicos pedidos explícitamente (`ar-u-nu-arab`): `ar` a secas
  devuelve dígitos latinos.
- Las gráficas se repintan al cambiar de idioma: ejes, leyenda y tabla incluidos.
- `letter-spacing: 0` en todos los rótulos árabes — espaciar las letras rompe
  las ligaduras.
- `background-position` del desplegable reflejada a mano: es la única propiedad
  del formulario sin versión lógica.

## Fotografía

3 fotografías reales de **Wikimedia Commons**, todas con licencia libre
(CC0, CC BY o CC BY-SA), descargadas al repositorio y no enlazadas a un
tercero: si mañana desaparecen de Commons, el sitio sigue igual.

- Cada una lleva **texto alternativo traducido a los tres idiomas**, no un
  `alt` en español dentro de la versión árabe.
- Los créditos —título, autor y licencia con enlace— se muestran dentro del
  propio sitio y también cambian de idioma.
- Se redimensionaron a 1400 px de ancho; ninguna pasa de 500 KB.

Se descartó una candidata de fisioterapia que la licencia permitía usar pero
que retrataba a **un menor identificable**. En una maqueta comercial eso no se
publica aunque sea legal.

## Comprobado

```
217 claves × 3 idiomas       paridad ✔ · 0 sin traducir
16 rutas × 3 idiomas         0 fugas de idioma
16 enlaces del menú          los 16 navegan
desborde horizontal          0 px en las 16 rutas
3 orientaciones              12 / 12 / 24 barras
calculadora                  6–7 años, coherente con el «5–8» de portada
formulario en árabe          3 estados
paleta de las gráficas       los 6 controles, en claro y en oscuro
```

---

**Maqueta de demostración.** Empresa ficticia; las cifras son de modelo y no
de cliente. Las gráficas son reales, los datos de ejemplo.
