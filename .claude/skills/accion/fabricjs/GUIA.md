# Fabric.js — guía rápida (basada en el README del repo fabricjs/fabric.js)

Librería JavaScript para canvas HTML5: interacción lista para usar (mover, escalar, rotar, sesgar, agrupar), formas, controles, animaciones, filtros de imagen, degradados, patrones, pinceles; entrada/salida en JPG, PNG, JSON y SVG; tipada y modular.

## Instalación
- Navegador (apps nuevas): `npm install @fabricjs/browser`
- Node.js (apps nuevas, mínimo Node 20): `npm install @fabricjs/node` (depende de node-canvas y jsdom)
- Paquete heredado compatible: `npm install fabric` (reexporta `@fabricjs/browser`)
- Mantener `fabric` y todos los `@fabricjs/*` en **la misma versión**; mezclar versiones carga runtimes separados.
- Extensiones opcionales, p. ej. `@fabricjs/aligning-guidelines`.

## Uso mínimo
```html
<canvas id="canvas" width="300" height="300"></canvas>
<script src="https://cdn.jsdelivr.net/npm/fabric@6.4.3/dist/index.js"></script>
<script>
  const canvas = new fabric.Canvas('canvas');
  canvas.add(new fabric.Rect({ top: 100, left: 100, width: 60, height: 70, fill: 'red' }));
</script>
```
```js
import { Canvas } from '@fabricjs/browser';   // apps nuevas
import { Canvas } from 'fabric';               // compatibilidad
```

## React
Crear el `Canvas` en `useEffect` sobre un `<canvas ref>` y **llamar `canvas.dispose()` en la limpieza** del efecto.

## Notas
- Navegadores mínimos aprox.: Chrome 64, Firefox 58, Safari 11; sin IE11 ni Edge Legacy.
- Antes de usar APIs concretas, verifica la versión instalada y la documentación oficial (sitio fabricjs.com, sección GOTCHAS); no asumas firmas de memoria.
- `fabricjs-open-pr/` es una skill del propio repo para abrir PRs **en fabric.js**; solo aplica si contribuyes a esa librería.
