# Tomi Arcade

Página web con los juegos de [tomi2015](https://github.com/tomi2015).
Sitio estático, desplegado en Vercel.

```
index.html            → la portada (rejilla de juegos)
wonderland/index.html  → Wonderland: El Coma (el juego, autónomo)
```

Cada juego vive en su propia carpeta y se enlaza con una ruta relativa
(`/wonderland/`), así que todo es público y no pide iniciar sesión.

## Añadir un juego

1. Abre `index.html` y busca el array `GAMES` (dentro del `<script>`, está comentado).
2. Copia un bloque `{ ... }` y rellénalo:

```js
{
  title: "Nombre del juego",
  sub:   "Subtítulo corto",          // sale en la pantallita; "" si no hay
  tags:  ["terror", "plataformas"],  // géneros / palabras clave
  year:  2026,
  desc:  "Una o dos frases sobre el juego.",
  url:   "https://...",              // enlace para jugar
  motif: "👾",                        // emoji grande de fondo
  theme: { g1: "#1b1030", g2: "#3a1622", accent: "#f0a53a" }
}
```

3. Si el juego es un archivo HTML propio, mételo en su carpeta:
   `nuevojuego/index.html`, y pon `url: "/nuevojuego/"`.
   Si está en otra web, pon la URL completa.

4. Guarda y publica:

```bash
git add -A
git commit -m "Añadir <juego>"
git push
```

Vercel detecta el push y actualiza la web en unos segundos.

## Desarrollo local

Es HTML puro, no necesita build. Abre `index.html` en el navegador,
o levanta un servidor:

```bash
npx serve .
```
