# Portfolio Profesional - Franco Sebastián Cardozo

Portfolio web profesional y moderno para Franco Sebastián Cardozo, DevOps Engineer (in progress) | Automation & Cloud | Product Tech Specialist.

> 📦 **¿Primera vez desplegando?** Consulta las [Instrucciones de Deployment](./DEPLOY_INSTRUCTIONS.md) para una guía paso a paso completa.

## 🚀 Características

- **Diseño moderno y profesional**: Paleta de colores azul profundo y naranja cálido
- **Totalmente responsive**: Optimizado para dispositivos móviles, tablets y desktop
- **Animaciones suaves**: Microinteracciones y efectos visuales elegantes
- **Tipografía limpia**: Inter y Poppins de Google Fonts
- **CI/CD automatizado**: Pipeline con GitHub Actions para build y deploy automático
- **Optimizado para GitHub Pages**: Listo para desplegar

## 📋 Estructura

```
Portfolio/
├── index.html                    # Página principal
├── styles.css                    # Estilos y animaciones
├── script.js                     # Interactividad y efectos
├── .github/
│   └── workflows/
│       └── deploy.yml           # Pipeline CI/CD con GitHub Actions
└── README.md                     # Este archivo
```

## 🎨 Secciones

1. **Hero**: Presentación principal con headline inspiracional y CTA
2. **Sobre mí**: Transición a DevOps y propósito personal
3. **Experiencia destacada**: Product Tech Specialist con foco en automatización
4. **Skills**: Technical (CI/CD, Git, Linux, Cloud, Python) y Soft/Product
5. **Proyectos**: Bots de automatización, dashboards, CI/CD pipeline del portfolio
6. **Contacto**: Links sociales y CTA motivador

## 🚀 Despliegue en GitHub Pages con CI/CD

Este portfolio incluye un pipeline automatizado con GitHub Actions que valida y despliega automáticamente en cada push a la rama `main`.

### Configuración Inicial

1. **Crea un repositorio en GitHub** (puede ser público o privado)

2. **Sube los archivos al repositorio**:
   ```bash
   git clone https://github.com/tuusuario/tu-repositorio.git
   cd tu-repositorio
   # Copia todos los archivos del portfolio aquí
   git add .
   git commit -m "Initial commit: Portfolio DevOps"
   git push origin main
   ```

3. **Habilita GitHub Pages con GitHub Actions**:
   - Ve a **Settings** > **Pages**
   - En **Source**, selecciona **GitHub Actions** (no Branch)
   - Guarda los cambios

4. **El pipeline se ejecutará automáticamente**:
   - En cada push a `main`, GitHub Actions:
     - Valida la estructura HTML
     - Verifica que existan los archivos CSS y JS
     - Despliega automáticamente a GitHub Pages
   - Verás el progreso en la pestaña **Actions** de tu repositorio

5. **Tu sitio estará disponible en**: 
   `https://tuusuario.github.io/nombre-repo/`

### CI/CD Pipeline

El pipeline (`.github/workflows/deploy.yml`) incluye:

- ✅ Validación de HTML
- ✅ Verificación de archivos CSS y JS
- ✅ Build automático (sin build step para sitio estático)
- ✅ Deploy automático a GitHub Pages
- ✅ Notificación de estado de deployment

**Ventajas del CI/CD**:
- Deploy automático en cada cambio
- Validación antes de publicar
- Historial de deployments
- Rollback fácil si algo falla

## 🔧 Personalización

### Cambiar la foto de perfil

Reemplaza la imagen placeholder en `index.html` (línea ~44):
```html
<img src="tu-foto.jpg" alt="Franco Sebastián Cardozo" class="profile-img">
```

### Actualizar enlaces sociales

Modifica los enlaces en la sección de contacto (línea ~214):
```html
<a href="https://github.com/tu-usuario" target="_blank" rel="noopener noreferrer">
<a href="https://linkedin.com/in/tu-perfil" target="_blank" rel="noopener noreferrer">
<a href="mailto:tu-email@ejemplo.com">
```

### Cambiar colores

Edita las variables CSS en `styles.css` (líneas 5-12):
```css
--color-primary-blue: #4A90E2;
--color-primary-orange: #FF8C42;
```

## 📱 Responsive

El sitio está optimizado para:
- 📱 Móviles (320px+)
- 📱 Tablets (768px+)
- 💻 Desktop (1024px+)
- 🖥️ Pantallas grandes (1440px+)

## 🎯 Tecnologías Utilizadas

### Frontend
- **HTML5**: Estructura semántica
- **CSS3**: Animaciones, gradientes, responsive design, variables CSS
- **JavaScript**: Interactividad y efectos
- **Google Fonts**: Inter y Poppins
- **Font Awesome**: Íconos

### DevOps & CI/CD
- **GitHub Actions**: Pipeline de CI/CD automatizado
- **Git**: Control de versiones
- **GitHub Pages**: Hosting estático

## 📝 Notas

- Asegúrate de actualizar el email de contacto antes de desplegar
- Reemplaza las imágenes placeholder con tus fotos reales
- Personaliza los proyectos y experiencia según tu caso
- Los enlaces sociales (GitHub, LinkedIn) deben actualizarse con tus perfiles reales
- El pipeline de GitHub Actions está configurado y funcionará automáticamente al hacer push

## 🔧 Tecnologías DevOps Mostradas

Este portfolio demuestra conocimientos en:
- **CI/CD**: Pipeline automatizado con GitHub Actions
- **Git**: Control de versiones y workflow colaborativo
- **Infraestructura como Código**: Pipeline definido en YAML
- **Automatización**: Deploy sin intervención manual
- **Monitoreo**: Status de deployments en GitHub Actions

## 📄 Licencia

Este proyecto está disponible para uso personal y profesional.

---

**Desarrollado con ❤️ y propósito**

