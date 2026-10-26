# La imagen perfecta en 12 GB de VRAM · workflows de ComfyUI

Los workflows de imagen del vídeo **«Tu PC hace imágenes como ChatGPT (si se lo pides bien)»** de [Capitán Tokn](https://www.youtube.com/@CapitanTokn), tal cual los uso.
Probados en una RTX 4070 de 12 GB con 32 GB de RAM.

**[Descargar todo en un .zip](https://github.com/Capitan-Tokn/imagen-perfecta-12gb/raw/main/CapitanTokn_imagen_perfecta_12GB.zip)**

## Lo más rápido

Arrastra cualquier imagen de [`ejemplos/`](ejemplos) encima de ComfyUI: se monta el workflow con el que se hizo, con su prompt y su semilla.

## Qué hay aquí

| Archivo | Para qué | Medido en mi PC |
| --- | --- | --- |
| [`1_flux2_klein_4b.json`](1_flux2_klein_4b.json) | Probar ideas: muchas versiones muy rápido | 2,5 s por imagen · 9 de 18 contando |
| [`2_z_image_turbo.json`](2_z_image_turbo.json) | Cuando la imagen tiene que llevar algo exacto | 14,7 s por imagen · 9 de 18 contando (el mejor con el calendario) |
| [`RECETA_PROMPT.md`](RECETA_PROMPT.md) | La receta del prompt en 7 partes y la plantilla para pedírselo a una IA | |
| [`ejemplos/`](ejemplos) | Las imágenes del vídeo, con el workflow guardado dentro | |

Cada workflow lleva una nota arriba con los ajustes y por qué. Los dos son imagen a 1344×768 (16:9), lista para animar con el
[workflow de vídeo del canal](https://github.com/Capitan-Tokn/wan22-12gb-vram).

«Contando» = calendario con 2 días tachados, 3 manzanas y una mano con 4 dedos, 6 semillas de cada (18 imágenes). Ningún modelo local pasó del 50 %: genera varias semillas y cuéntalo tú.

## Modelos

No hacen falta nodos extra: todo es de ComfyUI de serie.

| Carpeta de ComfyUI | Archivo | Descarga | Tamaño | Lo usa |
| --- | --- | --- | --- | --- |
| `models/diffusion_models` | `flux-2-klein-4b-fp8.safetensors` | [black-forest-labs/FLUX.2-klein-4b-fp8](https://huggingface.co/black-forest-labs/FLUX.2-klein-4b-fp8/blob/main/flux-2-klein-4b-fp8.safetensors) | 4,07 GB | klein |
| `models/diffusion_models` | `z_image_turbo_bf16.safetensors` | [Comfy-Org/z_image_turbo](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/diffusion_models/z_image_turbo_bf16.safetensors) | 12,31 GB | Z-Image |
| `models/text_encoders` | `qwen_3_4b_fp8_mixed.safetensors` | [Comfy-Org/z_image_turbo](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/text_encoders/qwen_3_4b_fp8_mixed.safetensors) | 5,63 GB | los dos |
| `models/vae` | `flux2-vae.safetensors` | [Comfy-Org/flux2-dev](https://huggingface.co/Comfy-Org/flux2-dev/blob/main/split_files/vae/flux2-vae.safetensors) | 0,34 GB | klein |
| `models/vae` | `ae.safetensors` | [Comfy-Org/z_image_turbo](https://huggingface.co/Comfy-Org/z_image_turbo/blob/main/split_files/vae/ae.safetensors) | 0,34 GB | Z-Image |

Solo klein: unos 10 GB. Los dos: unos 23 GB. FLUX.2 klein 4B y Z-Image Turbo tienen licencia **Apache 2.0**.

## Lo que más cambia el resultado

1. **El prompt.** Con una frase corta, cualquier modelo local se ve pobre al lado de ChatGPT. Con la [receta](RECETA_PROMPT.md), klein y Z-Image se acercan muchísimo.
2. **Lo que importa, grande; con fondo; en 16:9.** La imagen decide el vídeo.
3. **Cuenta tú** antes de animar. En el vídeo ya no se arregla.

Y lo más importante: dale este repositorio a tu IA, dile qué gráfica y cuánta memoria tienes, y pídele que te lo adapte.

Úsalos como quieras.

— [Capitán Tokn](https://www.youtube.com/@CapitanTokn)
