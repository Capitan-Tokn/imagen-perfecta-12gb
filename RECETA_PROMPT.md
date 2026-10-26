# La receta del prompt en 7 partes

ChatGPT y Gemini no dibujan tu frase tal cual: por dentro la convierten en una descripción mucho más larga.
Tu modelo local dibuja exactamente lo que le escribes. Si le escribes poco, te da poco.

| # | Parte | Ejemplo (el balcón del vídeo) |
| --- | --- | --- |
| 1 | **Estilo** | Semi-realistic cartoon illustration in a warm, detailed animated-film style, clean confident outlines |
| 2 | **Quién es y qué lleva** | A woman in her thirties with curly auburn hair tied in a loose bun, freckles, a mustard yellow linen shirt |
| 3 | **Qué hace** | She holds a small green metal watering can and pours water into the middle pot |
| 4 | **Cómo es el plano** | seen from the waist up, three-quarter view |
| 5 | **El sitio, con tres cosas concretas** | a black wrought-iron railing, exactly three terracotta flower pots, a small wooden stool |
| 6 | **La luz** | warm low sunlight from the left, golden rim light, pink and orange sunset sky |
| 7 | **El formato** | Horizontal 16:9 composition, no text. |

## Antes y después (medido en el vídeo)

**Solo la idea** → klein devolvió fotos realistas, ninguna con tres macetas:

```
A woman waters three flower pots on her balcony at sunset. Horizontal 16:9, no text.
```

**Con la receta** → el estilo que quería, en 53 s para 12 semillas (2 de 12 con exactamente tres macetas: hay que contar):

```
Semi-realistic cartoon illustration in a warm, detailed animated-film style, clean confident outlines, soft painterly shading and rich textures. A woman in her thirties with curly auburn hair tied in a loose bun, freckles and a calm focused expression, wearing a mustard yellow linen shirt with rolled-up sleeves. She holds a small green metal watering can with her right hand and pours water into the middle pot, seen from the waist up, three-quarter view. A narrow city balcony with a black wrought-iron railing: exactly three terracotta flower pots in a row on the railing ledge, red geraniums, a small wooden stool, string lights hanging above. Behind her, rooftops and a church tower of an old town under a pink and orange sunset sky. Warm low sunlight from the left, golden rim light on her hair and shoulders, soft depth of field on the background. Horizontal 16:9 composition, no text.
```

## Si te da pereza escribirlo: pídeselo a una IA

Pega esto en ChatGPT, Gemini, Claude o la que uses, cambiando la última línea:

```
Convierte mi idea en un prompt para un modelo de imagen local (FLUX o Z-Image), en inglés y en un solo párrafo.
Sigue este orden: estilo · quién es y qué lleva · qué hace · cómo es el plano · el sitio con tres cosas concretas · la luz · formato «Horizontal 16:9 composition, no text».
Si algo tiene que tener un número exacto, escribe «exactly» delante. No inventes texto ni carteles.
Mi idea: [ESCRIBE AQUÍ TU IDEA]
```

## Antes de animar la imagen

- **Lo que importa, grande.** Una cara pequeña en la imagen se deforma (o hace otra cosa) en el vídeo.
- **Dale un sitio.** Sobre un fondo vacío, el modelo de vídeo se inventa cosas: un vaso se convirtió en lata.
- **Horizontal desde el principio.** Una imagen cuadrada animada a 16:9 pierde la cabeza por arriba.
- **Cuenta tú.** Ningún modelo local pasó del 50 % contando dedos, manzanas o días tachados.
- **Que los objetos no se toquen.** Si la regadera toca la maceta, el vídeo las mezcla. Si un fallo se repite con otra semilla, no cambies la semilla: cambia la imagen.
