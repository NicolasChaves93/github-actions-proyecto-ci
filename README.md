# Proyecto CI/CD con GitHub Actions

![GitHub Actions](https://img.shields.io/github/actions/workflow/status/NicolasChaves93/github-actions-proyecto-ci/deploy.yml?branch=master&label=CI/CD)

Este proyecto es un ejemplo práctico del uso de GitHub Actions para implementar un pipeline de Integración Continua y Despliegue Continuo (CI/CD) de una aplicación web estática basada en Node.js.

## 📋 Descripción

Este proyecto forma parte del Bootcamp de GitHub Actions en Código Facilito y demuestra:

- Creación de un servidor web simple con Express.js
- Generación de páginas estáticas a partir de un servidor dinámico
- Implementación de pruebas automatizadas con Jest
- Configuración de un workflow de GitHub Actions para CI/CD
- Despliegue automático a GitHub Pages

## 🚀 Estructura del Proyecto

```
.
├── .github/workflows    # Configuraciones de GitHub Actions
│   └── deploy.yml       # Workflow de CI/CD
├── public/              # Archivos estáticos generados
│   └── index.html       # HTML generado para despliegue
├── src/                 # Código fuente
│   ├── app.js           # Servidor Express
│   ├── build.js         # Script para generar HTML estático
│   └── public/          # Archivos estáticos para desarrollo
│       └── index.html   # Plantilla HTML original
├── test/                # Tests
│   └── app.test.js      # Pruebas del servidor
├── package.json         # Dependencias y scripts
└── README.md            # Este archivo
```

## 🛠️ Tecnologías Utilizadas

- **Node.js**: Entorno de ejecución para JavaScript
- **Express.js**: Framework para aplicaciones web
- **Jest**: Framework de pruebas
- **SuperTest**: Librería para pruebas HTTP
- **GitHub Actions**: Plataforma de CI/CD
- **GitHub Pages**: Hosting para la página web estática
- **TailwindCSS**: Framework CSS para estilizar la interfaz

## ⚙️ Configuración del Workflow

El archivo `.github/workflows/deploy.yml` define un workflow que:

1. **Construye la aplicación**:
   - Hace checkout del código
   - Configura Node.js v18
   - Instala dependencias
   - Ejecuta pruebas
   - Genera la página estática
   - Sube los artefactos generados

2. **Despliega a GitHub Pages**:
   - Toma los artefactos generados
   - Los despliega a GitHub Pages
   - Proporciona la URL de la página desplegada

## 🔧 Uso Local

### Requisitos Previos

- Node.js (versión 18 o superior)
- npm (incluido con Node.js)

### Instalación

```powershell
# Clonar el repositorio
git clone https://github.com/NicolasChaves93/github-actions-proyecto-ci.git
cd github-actions-proyecto-ci

# Instalar dependencias
npm install
```

### Comandos Disponibles

```powershell
# Iniciar servidor de desarrollo
npm start

# Ejecutar pruebas
npm test

# Generar página estática
npm run build
```

## 📊 Flujo de Trabajo

1. Desarrolla nuevas características o correcciones
2. Realiza pruebas locales con `npm test`
3. Haz commit y push de tus cambios a GitHub
4. El workflow de GitHub Actions se ejecutará automáticamente
5. Verifica el estado de la ejecución en la pestaña "Actions" de tu repositorio
6. Si todas las pruebas pasan, tu página será desplegada automáticamente en GitHub Pages

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 🙏 Agradecimientos

- [Código Facilito](https://codigofacilito.com/) por el Bootcamp de GitHub Actions
- La comunidad de GitHub por las excelentes herramientas de CI/CD
