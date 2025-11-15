# 📘 Demo CI/CD – Pipeline hasta la construcción del PACKAGE

Este repositorio (`deber7`) contiene un ejemplo práctico del ciclo **CI/CD** (Integración Continua / Entrega Continua) usando **GitHub Actions**, incluyendo:

- Pruebas unitarias básicas  
- Pipeline de CI/CD funcional  
- Construcción automática de un package (`npm pack`)  
- Generación de un artefacto descargable en GitHub Actions  

---

##  Contenido del repositorio

- `index.js` — Código simple del paquete.  
- `package.json` — Configuración del proyecto y scripts.  
- `test/index.test.js` — Pruebas unitarias con Jest.  
- `.github/workflows/ci.yml` — Pipeline CI/CD.  
- `README.md` — Documentación del proyecto.

---

## 🛠 Tecnologías Requeridas

- **Node.js** (v18 o superior)  
- **npm**  
- **Git**  
- GitHub Actions (automático al subir el repo)

---

##  Estructura del Proyecto

```
deber7/
├─ .github/
│  └─ workflows/
│     └─ ci.yml
├─ test/
│  └─ index.test.js
├─ index.js
├─ package.json
└─ README.md
```

---

#  CI/CD: ¿Qué hace este pipeline?

El archivo `.github/workflows/ci.yml` ejecuta automáticamente los siguientes pasos cada vez que haces un **push**:

1. **Descargar el código** (`actions/checkout`)  
2. **Configurar Node.js**  
3. **Instalar dependencias** (`npm ci`)  
4. **Ejecutar pruebas unitarias** (`npm test`)  
5. **Construir el paquete** usando `npm pack`  
6. **Subir el artefacto generado** (.tgz) para descargarlo desde GitHub Actions

Este ciclo asegura que cualquier cambio en el repositorio pase por pruebas y construcción antes de considerarse válido.

---

# 🧪 Ejecutar el proyecto localmente

### 1. Instalar dependencias

```bash
npm install
```

### 2. Ejecutar pruebas

```bash
npm test
```

Deberías ver algo como:

```
PASS  test/index.test.js
```

### 3. Construir el paquete

```bash
npm pack
```

Esto generará:

```
deber7-0.1.0.tgz
```

---

#  Comandos utilizados para crear este repositorio

Este repositorio fue creado y subido usando:

```bash
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/emssilva22/deber7.git
git push -u origin main
```

Luego se subieron los demás archivos y el pipeline comenzó a ejecutarse desde la pestaña **Actions**.

---


#  Extensiones recomendadas (opcional)

- Añadir **ESLint** y **Prettier**  
- Publicar el paquete en **npm**  
- Agregar despliegue automático  
- Usar cache de dependencias en CI/CD

---

#  Autoría

Este README y los archivos del proyecto fueron elaborados con fines educativos como ejercicio práctico de CI/CD.
