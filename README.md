# cuerpo-ar-modelos

Modelos 3D (GLB) de los sillones de la demo **Cuerpo** (Palta Solutions) para la función "Ver en tu espacio" (AR).
Se sirven con versión fija desde jsDelivr:

```
https://cdn.jsdelivr.net/gh/hysmarcos/cuerpo-ar-modelos@<versión>/<ruta>
```

- `modelos/<modelo>-<medida>/`: un glTF por tela y color (`<tela>-<color>.gltf`) que comparte la geometría (`.bin`). Desde v0.9 la tela se repite sobre el sillón a escala real (`base_<tela>.jpg` gris teñido por el color, relieve y rugosidad por tela) y la sombra, la variación de tono y los pliegues van en el color de los vértices; hasta v0.8, `base_<tela>.jpg` era el color horneado. Es lo que abren Scene Viewer (Android), Quick Look (iPhone) y la AR de Chrome. Se arma con `.tools/blender/exportar_modelo.py` (realismo: hundimientos, inclinaciones, pliegues y vivos) y `.tools/scripts/variantes-ar.mjs`. Nórdico tiene 2, 3 y 4 cuerpos y con chaise (módulo largo a la derecha mirándolo de frente); las otras medidas salen del modelo de 3 cuerpos con `.tools/blender/medidas.py`.
- `prototipo/` (hasta v0.5): versiones anteriores en GLB.
- `texturas/<tela>/`: mapas de tela (`base.jpg` gris para teñir, `nor_ar.jpg` con el relieve calibrado por tela, `rough_ar.jpg`; `foto.json` con el tamaño real cuando salen de una foto, `.tools/scripts/telas-foto.mjs`).

Los modelos se generan con `.tools/blender/sillon.py` del repo de la tienda; no se editan a mano.

## Texturas

Pana y lino (desde v0.9): imágenes propias de Palta Solutions (muestras de tela de 20 cm), procesadas con `telas-foto.mjs`.

Chenille y cuero, y las versiones anteriores de pana y lino (`diff.jpg`, `nor.jpg`, `rough.jpg`): CC0, Poly Haven.

| Tela | Textura | Autor |
|---|---|---|
| Pana (hasta v0.8) | [Velour Velvet](https://polyhaven.com/a/velour_velvet) | Rico Cilliers / colormass |
| Lino (hasta v0.8) | [Rough Linen](https://polyhaven.com/a/rough_linen) | Rico Cilliers / colormass |
| Chenille | [Curly Teddy Natural](https://polyhaven.com/a/curly_teddy_natural) | Rico Cilliers / colormass |
| Cuero | [Leather White](https://polyhaven.com/a/leather_white) | Rob Tuytel |
