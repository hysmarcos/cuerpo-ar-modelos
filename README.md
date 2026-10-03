# cuerpo-ar-modelos

Modelos 3D (GLB) de los sillones de la demo **Cuerpo** (Palta Solutions) para la función "Ver en tu espacio" (AR).
Se sirven con versión fija desde jsDelivr:

```
https://cdn.jsdelivr.net/gh/hysmarcos/cuerpo-ar-modelos@<versión>/<ruta>
```

- `modelos/<modelo>-<medida>/`: un glTF por tela y color (`<tela>-<color>.gltf`) que comparte la geometría (`.bin`), con la textura de color horneada por tela (`base_<tela>.jpg`, 2K, con sombras, variación de tono y desgaste), relieve y rugosidad por tela. Es lo que abren Scene Viewer (Android), Quick Look (iPhone) y la AR de Chrome. Se arma con `.tools/blender/exportar_modelo.py` (realismo: hundimientos, inclinaciones y pliegues por simulación de tela) y `.tools/scripts/variantes-ar.mjs`.
- `prototipo/` (hasta v0.5): versiones anteriores en GLB.
- `texturas/<tela>/`: mapas de tela (`base.jpg` gris para teñir, `nor.jpg`, `nor_ar.jpg` con el relieve calibrado por tela, `rough.jpg`).

Los modelos se generan con `.tools/blender/sillon.py` del repo de la tienda; no se editan a mano.

## Créditos de texturas (CC0, Poly Haven)

| Tela | Textura | Autor |
|---|---|---|
| Pana | [Velour Velvet](https://polyhaven.com/a/velour_velvet) | Rico Cilliers / colormass |
| Lino | [Rough Linen](https://polyhaven.com/a/rough_linen) | Rico Cilliers / colormass |
| Chenille | [Curly Teddy Natural](https://polyhaven.com/a/curly_teddy_natural) | Rico Cilliers / colormass |
| Cuero | [Leather White](https://polyhaven.com/a/leather_white) | Rob Tuytel |
