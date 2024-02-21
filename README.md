# Vite

En este proyecto base vemos como Vite se encarga de todo. Vite, usa el index.html como punto de entrada de nuestra aplicación y detecta que estamos cargando código typescript desde el tag script:

```html
<script type="module" src="/src/main.ts"></script>
```

Esta linea no podría funcionar en el navegador sin que Vite detecte esto y automáticamente transpile todos los archivos typescript a javascript y los combine en un solo archivo (bundle).

Esto además de mejorar los tiempos de carga ya que el bundle es un solo archivo js con todo incluido, nos permite ocuparnos de la lógica de nuestra app y no tanto de como procesar estos archivos para que funcionen en la web. Más adelante veremos como usar Vite y otros bundlers de forma más "manual" y entenderemos como funcionan estas herramientas.

## CSS

Otra enorme ventaja es poder importar archivos CSS desde TypeScript como podemos observar en `main.ts` donde hacemos este import:

```ts
import "./style.css";
```

Y esto genera un archivo css en el bundle. que luego es importado por el index.html sin que tengamos que preocuparnos de nada.
