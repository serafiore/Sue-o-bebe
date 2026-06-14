# Guia: Publicar Sueño Baby en GitHub Pages (Online)

## QUE VAS A LOGRAR

Al terminar esta guia vas a tener:
- Tu app accesible desde un link tipo: `https://tuusuario.github.io/sueno-baby/`
- Las madres pueden abrirla desde cualquier celular o computadora
- Pueden guardarla como app en su pantalla de inicio
- Funciona sin internet despues de la primera carga

---

## PARTE 1: CREAR CUENTA EN GITHUB (5 minutos)

### Paso 1: Ir a GitHub
1. Abri tu navegador y anda a **https://github.com**
2. Toca el boton verde **"Sign up"** (Registrate)
3. Segui los pasos:
   - Escribe tu email
   - Crea una contrasena
   - Elige un nombre de usuario (esto sera tu link: github.com/TU-USUARIO)
4. Verifica tu email cuando te llegue el codigo

**Listo, ya tenes cuenta en GitHub.**

---

## PARTE 2: CREAR EL REPOSITORIO (3 minutos)

### Paso 2: Crear un nuevo repositorio
1. Una vez logueado en GitHub, toca el **"+"** arriba a la derecha
2. Selecciona **"New repository"**
3. Completa estos campos:
   - **Repository name**: `sueno-baby` (asi sera tu link)
   - **Description**: `App de seguimiento de sueno para bebes`
   - Selecciona **"Public"** (importante para que sea gratis)
   - Marca la casilla **"Add a README file"**
4. Toca el boton verde **"Create repository"**

**Listo, ya tenes tu repositorio.**

---

## PARTE 3: SUBIR LOS ARCHIVOS (10 minutos)

### Paso 3: Subir los archivos de la app
1. En tu repositorio, toca el boton **"Add file"** > **"Upload files"**
2. Arrastra estos archivos desde tu carpeta:
   - `rutina-sueno.html`
   - `sw.js`
   - `manifest.json`
   - `guia-instalacion.html`
3. Toca **"Commit changes"**

### Paso 4: Crear la carpeta de iconos
1. Toca **"Add file"** > **"Create new file"**
2. En el campo del nombre escribe: `icons/icon-192.png`
3. Toca **"choose your files"** y sube `icon-192.png` desde tu carpeta `icons`
4. Toca **"Commit changes"**
5. Repite este paso para estos archivos (uno por uno):
   - `icons/icon-512.png`
   - `icons/icon-128.png`
   - `icons/icon-144.png`
   - `icons/icon-152.png`
   - `icons/icon-72.png`
   - `icons/icon-96.png`
   - `icons/icon-384.png`

**Alternativa mas rapida:** Si tenes Git instalado, podes subir todo de una vez (ver nota al final).

---

## PARTE 4: ACTIVAR GITHUB PAGES (2 minutos)

### Paso 5: Activar la pagina
1. En tu repositorio, toca la pestana **"Settings"** (arriba)
2. En el menu de la izquierda, toca **"Pages"**
3. En **"Source"** selecciona:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Toca **"Save"**
5. Espera 1-2 minutos

### Paso 6: Obtener tu link
1. Despues de unos minutos, recarga la pagina de Settings > Pages
2. Veras un mensaje verde que dice: **"Your site is live at..."**
3. Copia ese link. Sera algo como:
   ```
   https://tuusuario.github.io/sueno-baby/
   ```

**Listo, tu app ya esta online!**

---

## PARTE 5: COMO COMPARTIR CON LAS MADRES

### Por WhatsApp
1. Copia el link de tu app
2. Envia el mensaje algo como:
   ```
   Hola! Te comparto la app para trackear el sueno del bebe:
   https://tuusuario.github.io/sueno-baby/
   
   Abri el link en Chrome (Android) o Safari (iPhone)
   y guardala en tu pantalla de inicio para usarla como app.
   ```
3. Tambien podes enviarles el `guia-instalacion.html` para que tengan las instrucciones

### Por Instagram/Facebook
Pega el link en tu bio o en un post con una captura de la app.

---

## PARTE 6: GUARDAR EN LA PANTALLA DE INICIO

### En Android (Chrome)
1. Abri el link en **Google Chrome**
2. Toca los **tres puntos** (arriba a la derecha)
3. Selecciona **"Instalar app"** o **"Agregar a pantalla de inicio"**
4. Toca **"Instalar"**
5. La app aparecera en tu pantalla de inicio como un icono

### En iPhone (Safari)
1. Abri el link en **Safari**
2. Toca el boton de **compartir** (cuadro con flecha hacia arriba)
3. Desliza y toca **"Agregar a pantalla de inicio"**
4. Toca **"Agregar"** arriba a la derecha
5. La app aparecera en tu pantalla de inicio

### En Windows (Chrome o Edge)
1. Abri el link en **Chrome** o **Edge**
2. En Chrome: toca los tres puntos > **"Instalar app"**
3. En Edge: toca los tres puntos > **"Aplicaciones"** > **"Instalar este sitio como app"**
4. Toca **"Instalar"**
5. Podes fijarla en la barra de tareas

---

## NOTA: SUBIR TODO DE UNA VEZ CON GIT

Si tenes Git instalado en tu computadora, podes subir todo de una vez:

```bash
# 1. Abri una terminal en tu carpeta del proyecto
cd "C:\Users\Bernabe\Desktop\Open code Proyectos\Recurso curso"

# 2. Inicializar git
git init
git add .
git commit -m "Primea version de Sueño Baby"

# 3. Conectarse a GitHub
git remote add origin https://github.com/TU-USUARIO/sueno-baby.git
git branch -M main
git push -u origin main
```

---

## SOLUCION DE PROBLEMAS

### "No me deja activar Pages"
- Asegurate de que el repositorio sea **Public**
- Verifica que exista al menos un archivo `index.html` o que hayas configurado el HTML principal

### "La app no carga los graficos"
- La primera vez necesita internet para cargar Chart.js
- Despues de la primera carga, funciona offline

### "No se puede guardar como app en iPhone"
- Asegurate de usar **Safari**, no Chrome en iPhone
- En iPhone, Chrome no permite guardar como app

### "Los iconos no se ven"
- Verifica que la carpeta `icons/` este dentro del repositorio
- Los archivos deben estar en `icons/icon-192.png`, etc.

---

## RESUMEN RAPIDO

1. Crear cuenta en **github.com**
2. Crear repositorio **publico** llamado `sueno-baby`
3. Subir los archivos: `rutina-sueno.html`, `sw.js`, `manifest.json`, `guia-instalacion.html`
4. Crear carpeta `icons/` y subir los PNG
5. Ir a **Settings > Pages** y activar desde `main`
6. Copiar el link y compartirlo

**Tu link sera:** `https://tuusuario.github.io/sueno-baby/`