# NAHAR — Autoconsumo solar industrial

Sitio corporativo de **diez páginas** en español, inglés y árabe con RTL real,
para una ingeniería de autoconsumo fotovoltaico industrial.

**Ver online:** https://2troll.github.io/nahar-solar/

Un solo archivo HTML: sin compilar, sin dependencias, sin claves de API.

## Las diez páginas

`Inicio` · `Servicios` · `Proceso` · `Rendimiento` · `Amortización` ·
`Proyectos` · `Mantenimiento` · `Empresa` · `Preguntas` · `Contacto`

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
139 claves × 3 idiomas       paridad ✔ · 0 sin traducir
10 rutas × 3 idiomas         0 fugas de idioma
3 orientaciones              12 / 12 / 24 barras
calculadora                  6–7 años, coherente con el «5–8» de portada
formulario en árabe          3 estados
paleta de las gráficas       los 6 controles, en claro y en oscuro
```

---

**Maqueta de demostración.** Empresa ficticia; las cifras son de modelo y no
de cliente. Las gráficas son reales, los datos de ejemplo.
