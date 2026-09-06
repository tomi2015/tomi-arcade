# Tomi Arcade

Página web con los juegos de [tomi2015](https://github.com/tomi2015).
Sitio estático (un solo `index.html`), desplegado en Vercel.

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

3. Guarda, y publica:

```bash
git add index.html
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
