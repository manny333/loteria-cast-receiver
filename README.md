# Cast Receiver - Lotería Mexicana

Este es el Custom Receiver que se ejecuta en el Chromecast/Android TV.

## 📤 Cómo hospedar este archivo

### Opción 1: GitHub Pages (Recomendado - Gratis)

1. Crear un repositorio en GitHub (puede ser privado con GitHub Pro)
2. Subir el archivo `index.html` a la carpeta raíz o a una carpeta `docs/`
3. Ir a Settings → Pages
4. Seleccionar la rama y carpeta
5. Guardar y obtener la URL: `https://tu-usuario.github.io/tu-repo/index.html`

### Opción 2: Firebase Hosting (Gratis)

```bash
# Instalar Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Inicializar proyecto
firebase init hosting

# Deploy
firebase deploy --only hosting
```

URL resultante: `https://tu-proyecto.web.app/index.html`

### Opción 3: Netlify (Gratis)

1. Arrastrar la carpeta `cast-receiver` a netlify.com/drop
2. Obtener URL automática: `https://random-name.netlify.app/index.html`

### Opción 4: Vercel (Gratis)

```bash
# Instalar Vercel CLI
npm install -g vercel

# Deploy desde esta carpeta
cd cast-receiver
vercel
```

## 🔧 Después de hospedar

1. Copia la URL completa del archivo `index.html`
2. Ve a https://cast.google.com/publish/
3. Registra tu Custom Receiver con esa URL
4. Obtendrás un **Application ID** (formato: `XXXXXXXX`)
5. Ese ID lo necesitarás en la app React Native

## 📝 Notas

- La URL debe ser HTTPS
- El archivo debe ser públicamente accesible
- Google Cast tarda ~15 minutos en propagar cambios

## 🧪 Testing

Para probar localmente antes de hospedar:
1. Usa `npx serve cast-receiver` 
2. Usa ngrok para crear túnel HTTPS: `ngrok http 3000`
3. Usa la URL ngrok temporalmente para pruebas

---

**Next step:** Hospedar y obtener el Application ID de Google Cast Console
