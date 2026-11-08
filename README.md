# La Mesa Abierta — Registro Público de Pruebas y Enmiendas

Aplicación web interactiva (`HTML/CSS/JS` en un único archivo autónomo) diseñada para acompañar las ediciones impresa y digital de ***Hechos, no nacidos*** (*Made, Not Born*), de **Sergio Fontestad Gómez**.

- **Edición en español:** `index.html` (o `?lang=es`)
- **Edición en inglés:** `index.html?lang=en`

---

## Despliegue en GitHub Pages

1. Suba el contenido de este repositorio (o únicamente la carpeta `/docs`) a su repositorio de GitHub (`https://github.com/sefontier/hechos-no-nacidos`).
2. En **Settings → Pages**, seleccione **Deploy from a branch**, elija la rama `main` y la carpeta **`/docs`**.
3. La aplicación quedará publicada en `https://sefontier.github.io/hechos-no-nacidos/` (y en inglés en `https://sefontier.github.io/hechos-no-nacidos/?lang=en`), coincidiendo con los códigos QR de alta resolución integrados al final del libro.

---

## Conexión opcional con Supabase ( en 3 pasos)

La aplicación funciona desde el primer segundo en modo autónomo con persistencia local (`localStorage`). Si desea centralizar los votos y comentarios de todos los lectores en una base de datos gratuita de **Supabase**:

1. Cree un proyecto gratuito en [supabase.com](https://supabase.com) y ejecute el contenido de [`supabase_schema.sql`](./supabase_schema.sql) en el **SQL Editor**.
2. En **Project Settings → API**, copie su `Project URL` y su clave pública `anon public`.
3. Pegue ambos valores en el bloque `BACKEND_CONFIG` de [`index.html`](./index.html) (`SUPABASE_URL` y `SUPABASE_ANON_KEY`).
