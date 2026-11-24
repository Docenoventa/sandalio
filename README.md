# Cómo subir el sitio a GitHub y conectar tu dominio

## Archivos
- `index.html`: la página completa.
- `logo.svg`: el logo provisional con las iniciales. Abre el archivo con un editor de texto y el logo provisional usa las iniciales "SSM".
- `CNAME`: aquí va tu dominio. Ábrelo y escribe solo el dominio, por ejemplo `www.tudominio.com`.

Los textos que dicen **[ ... ]** y tienen fondo amarillo son los que faltan por llenar. Cuando pongas el texto real, quita también el `<span class="ph">`, que es lo que pinta el fondo amarillo.

## 1. Subir a GitHub
1. Entra a github.com y crea un repositorio nuevo (botón **New**). Puede ser público.
2. En el repositorio entra a **Add file → Upload files** y arrastra `index.html`, `logo.svg` y `CNAME`. Luego da clic en **Commit changes**.
3. Ve a **Settings → Pages**. En "Branch" elige `main` y la carpeta `/ (root)`, y luego da clic en **Save**.
4. En uno o dos minutos la página queda publicada en `tuusuario.github.io/nombre-del-repo`.

## 2. Conectar el dominio
En el panel donde compraste el dominio (GoDaddy, Namecheap, Hostinger, etc.) busca **DNS** y agrega estos registros:

| Tipo  | Nombre / Host | Valor |
|-------|---------------|-------|
| A     | @             | 185.199.108.153 |
| A     | @             | 185.199.109.153 |
| A     | @             | 185.199.110.153 |
| A     | @             | 185.199.111.153 |
| CNAME | www           | tuusuario.github.io |

Después regresa a GitHub, entra a **Settings → Pages → Custom domain**, escribe tu dominio y da clic en **Save**. Cuando aparezca la opción, marca **Enforce HTTPS**.

Los cambios de DNS pueden tardar de unos minutos a 24 horas en funcionar.

## Formulario de contacto
Por ahora, el formulario abre el programa de correo de quien lo usa. Si quieres que los mensajes lleguen solos a tu bandeja, se puede conectar a Formspree, que es gratis.
