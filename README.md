# generative-tools

Colección de herramientas pequeñas para generación visual en el navegador.  
Sin instalación, sin dependencias, sin servidor. Abrís el archivo y funciona.

---

## Herramientas

### 🎞 Glitch sobre video — `glitch sobre video v2.html`

Procesador de video en tiempo real usando [Hydra Synth](https://hydra.ojack.xyz).  
Cargás cualquier video local y lo transforma con efectos generativos.

**Efectos incluidos:**
- Glitch fluido — noise orgánico con feedback suave
- Membrana líquida — deformación que respira
- Corrosión cromática — separación RGB por canal
- Pulso orgánico — el video late y se expande
- Deriva fractal — capas superpuestas en espiral

**Cómo usar:**
1. Descargá el archivo
2. Abrilo en Chrome o Firefox
3. Arrastrá un video `.mp4` a la pantalla o usá el botón para elegir archivo
4. Los controles de abajo permiten cambiar el modo, la velocidad o pausar

---

### ✦ Hydra Editor — `hydra-editor.html`

Editor en vivo para [Hydra Synth](https://hydra.ojack.xyz) con soporte de audio reactivo y sistema de presets.  
Escribís código Hydra directamente en el navegador y lo ves ejecutarse en tiempo real.

**Funcionalidades:**
- Editor de código con resaltado de errores
- `Ctrl+Enter` para ejecutar sin usar el mouse
- Guardar y cargar presets con nombre (persisten entre sesiones)
- Activar audio reactivo — usá `a.fft[0]`, `a.fft[1]`, etc. en tu código
- Modo pantalla completa para performance o instalación

**Cómo usar:**
1. Descargá el archivo
2. Abrilo en Chrome o Firefox
3. Escribí código Hydra en el panel derecho
4. `Ctrl+Enter` o el botón ▶ para ejecutar
5. Guardá tus efectos favoritos como presets

**Ejemplo mínimo:**
```javascript
osc(6, 0.05, 1.4)
  .rotate(0.3)
  .modulateScale(noise(3), 0.3)
  .color(1.1, 0.8, 1.3)
  .out()
```

**Ejemplo con audio reactivo:**
```javascript
// primero activá el audio desde el panel
osc(() => a.fft[0] * 20, 0.05, 1.4)
  .modulate(noise(3), () => a.fft[1] * 0.3)
  .out()
```

---

## Stack

- [Hydra Synth](https://github.com/hydra-synth/hydra-synth) — video synth en WebGL
- Canvas 2D API
- Web Audio API
- JavaScript vanilla — sin frameworks

---

## Filosofía

Herramientas de una sola página. Todo en un `.html`.  
Fáciles de compartir, fáciles de modificar, fáciles de entender.

---

## Próximamente

- [ ] Exportación de frames / grabación de video
- [ ] Soporte para cargar video local desde el editor Hydra
- [ ] Más modos de efecto en el procesador de video

---

*Hecho con curiosidad.*
