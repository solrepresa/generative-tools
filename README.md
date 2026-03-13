# generative-tools

Colección de herramientas pequeñas para generación visual en el navegador.  
Sin instalación, sin dependencias, sin servidor. Abrís el archivo y funciona.

---

## Herramientas

### 🎞 Glitch Orgánico — `flujo-glitch.html`

Procesador de video en tiempo real usando [Hydra Synth](https://hydra.ojack.xyz).  
Cargás cualquier video local y lo transforma con efectos generativos.

**Efectos incluidos:**
- Glitch fluido — noise orgánico con feedback suave
- Membrana líquida — deformación que respira
- Corrosión cromática — separación RGB por canal
- Pulso orgánico — el video late y se expande
- Deriva fractal — capas superpuestas en espiral

**Cómo usar:**
1. Descargá el archivo `flujo-glitch.html`
2. Abrilo en Chrome o Firefox
3. Arrastrá un video `.mp4` a la pantalla o usá el botón para elegir archivo
4. Usá los controles de abajo para cambiar el modo, velocidad o pausar

---

## Stack

- Canvas 2D API
- [Hydra Synth](https://github.com/hydra-synth/hydra-synth) — video synth en WebGL
- Web Audio API
- JavaScript vanilla — sin frameworks

---

## Filosofía

Herramientas de una sola página. Todo en un `.html`.  
Fáciles de compartir, fáciles de modificar, fáciles de entender.

---

## Próximamente

- [ ] Reactividad al audio del video
- [ ] Más modos de efecto
- [ ] Exportación de frames

---

*Hecho con curiosidad.*
