# 📦 Instrucciones para Subir el Portfolio a GitHub

Guía paso a paso para crear un nuevo repositorio en GitHub y subir el portfolio profesional.

## 🚀 Pasos para Desplegar

### Paso 1: Crear un nuevo repositorio en GitHub

1. **Ve a GitHub.com** y haz login
2. **Click en el botón "+"** (arriba a la derecha) → **"New repository"**
3. **Configura el repositorio**:
   - **Repository name**: `portfolio` (o el nombre que prefieras, ej: `franco-cardozo-portfolio`)
   - **Description**: "Portfolio profesional - DevOps Engineer (in progress) | Automation & Cloud"
   - **Visibility**: Público (recomendado) o Privado
   - **NO marques** "Initialize this repository with a README" (ya tenemos archivos)
   - **NO agregues** .gitignore ni license (ya están incluidos)
4. **Click en "Create repository"**

### Paso 2: Preparar el repositorio localmente

Abre tu terminal en la carpeta del proyecto (`C:\Cursor\Portfolio`) y ejecuta:

```bash
# Inicializar git (si no está ya inicializado)
git init

# Verificar que estás en la carpeta correcta
pwd
# Debería mostrar: C:\Cursor\Portfolio
```

### Paso 3: Agregar todos los archivos

```bash
# Agregar todos los archivos al staging
git add .

# Verificar qué archivos se agregaron
git status
```

Deberías ver:
- `index.html`
- `styles.css`
- `script.js`
- `README.md`
- `DEPLOY_INSTRUCTIONS.md`
- `.gitignore`
- `.github/workflows/deploy.yml`

### Paso 4: Hacer el primer commit

```bash
# Crear el commit inicial
git commit -m "Initial commit: Portfolio DevOps Engineer"

# O si prefieres un mensaje más detallado:
git commit -m "Initial commit: Portfolio DevOps Engineer | Automation & Cloud | Product Tech Specialist"
```

### Paso 5: Conectar con GitHub y hacer push

```bash
# Agregar el remote (reemplaza TU-USUARIO y TU-REPOSITORIO con tus valores)
git remote add origin https://github.com/TU-USUARIO/TU-REPOSITORIO.git

# Verificar que el remote se agregó correctamente
git remote -v

# Cambiar a la rama main (si estás en otra rama)
git branch -M main

# Hacer push al repositorio
git push -u origin main
```

**Ejemplo real:**
Si tu usuario es `francocardozo` y tu repo se llama `portfolio`, sería:
```bash
git remote add origin https://github.com/francocardozo/portfolio.git
git push -u origin main
```

### Paso 6: Configurar GitHub Pages con CI/CD

1. **Ve a tu repositorio en GitHub** (ej: `https://github.com/TU-USUARIO/TU-REPOSITORIO`)
2. **Click en "Settings"** (en el menú superior del repo)
3. **En el menú lateral, busca "Pages"** (dentro de Code and automation)
4. **En "Source"**:
   - Selecciona **"GitHub Actions"** (NO "Deploy from a branch")
5. **Guarda los cambios** (no hay botón, se guarda automáticamente)

### Paso 7: Activar el workflow de GitHub Actions

1. **Ve a la pestaña "Actions"** en tu repositorio
2. Si el workflow no se ejecutó automáticamente, haz un pequeño cambio y haz push:
   ```bash
   # Hacer un pequeño cambio (opcional)
   echo "# Portfolio DevOps" >> README.md
   git add README.md
   git commit -m "Trigger CI/CD pipeline"
   git push
   ```
3. **Espera a que el pipeline termine** (verás un check verde ✓ cuando termine)
4. **Tu sitio estará disponible en**:
   ```
   https://TU-USUARIO.github.io/TU-REPOSITORIO/
   ```

## ✅ Verificación Post-Deploy

Después de configurar todo, verifica:

- [ ] El repositorio existe en GitHub
- [ ] Todos los archivos están subidos (index.html, styles.css, script.js, etc.)
- [ ] El workflow de GitHub Actions está activo en la pestaña "Actions"
- [ ] El pipeline ejecutó correctamente (check verde ✓)
- [ ] El sitio está accesible en GitHub Pages
- [ ] El sitio carga correctamente y se ve bien

## 🔧 Personalización Antes de Subir (Opcional)

### Actualizar enlaces sociales

Antes de hacer push, puedes actualizar los enlaces en `index.html`:

**Línea ~306-314** (sección de contacto):
```html
<a href="https://github.com/TU-USUARIO" target="_blank" rel="noopener noreferrer" class="social-link">
    <i class="fab fa-github"></i>
    <span>GitHub</span>
</a>
<a href="https://linkedin.com/in/TU-PERFIL" target="_blank" rel="noopener noreferrer" class="social-link">
    <i class="fab fa-linkedin-in"></i>
    <span>LinkedIn</span>
</a>
<a href="mailto:TU-EMAIL@ejemplo.com" class="social-link">
    <i class="fas fa-envelope"></i>
    <span>Mail</span>
</a>
```

Y también en el botón de contacto (línea ~319):
```html
<a href="mailto:TU-EMAIL@ejemplo.com" class="cta-button secondary">
```

### Actualizar foto de perfil

**Línea ~48** de `index.html`:
```html
<img src="ruta-a-tu-foto.jpg" alt="Franco Sebastián Cardozo" class="profile-img">
```

Puedes subir una foto a una carpeta `images/` y referenciarla como:
```html
<img src="images/profile.jpg" alt="Franco Sebastián Cardozo" class="profile-img">
```

## 📝 Comandos Útiles para el Futuro

### Hacer cambios y actualizar el sitio

Cada vez que hagas cambios:

```bash
# Ver qué archivos cambiaron
git status

# Agregar los cambios
git add .

# O agregar archivos específicos
git add index.html styles.css

# Hacer commit
git commit -m "Descripción de los cambios"

# Subir a GitHub (el CI/CD se ejecutará automáticamente)
git push
```

### Ver el historial

```bash
# Ver commits recientes
git log --oneline

# Ver qué cambió en un archivo
git diff index.html
```

## 🐛 Solución de Problemas

### Error: "remote origin already exists"

Si ya tienes un remote configurado, elimínalo primero:
```bash
git remote remove origin
git remote add origin https://github.com/TU-USUARIO/TU-REPOSITORIO.git
```

### Error: "failed to push some refs"

Asegúrate de haber hecho commit primero:
```bash
git add .
git commit -m "Mensaje del commit"
git push -u origin main
```

### El pipeline no se ejecuta

1. Verifica que el archivo `.github/workflows/deploy.yml` existe
2. Ve a Settings > Actions > General
3. Asegúrate de que "Allow all actions and reusable workflows" está habilitado
4. Haz un pequeño cambio y haz push para activar el workflow

### El sitio no carga

1. Verifica que GitHub Pages está configurado con "GitHub Actions" (no "branch")
2. Revisa la pestaña "Actions" para ver si hay errores en el pipeline
3. Espera unos minutos después del deploy (puede tardar hasta 10 minutos en propagarse)

## 📚 Recursos Útiles

- [Documentación de GitHub Pages](https://docs.github.com/en/pages)
- [Documentación de GitHub Actions](https://docs.github.com/en/actions)
- [Guía rápida de Git](https://guides.github.com/introduction/git-handbook/)

---

## 🎯 Checklist Final

Cuando hayas completado todos los pasos:

- [ ] Repositorio creado en GitHub
- [ ] Archivos subidos correctamente
- [ ] Primer commit realizado
- [ ] GitHub Pages configurado con GitHub Actions
- [ ] Pipeline ejecutado exitosamente
- [ ] Sitio accesible en la URL de GitHub Pages
- [ ] Enlaces sociales actualizados
- [ ] Foto de perfil actualizada (opcional)

**¡Listo! Tu portfolio está en línea y se actualizará automáticamente con cada push. 🚀**

---

*Creado el: $(date)*
*Última actualización: Cuando completes el deploy*

