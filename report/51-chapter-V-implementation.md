# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

### 5.1.1. Software Development Environment Configuration

En esta sección se describen todas las herramientas, plataformas y tecnologías utilizadas por el equipo durante el desarrollo del proyecto InfraTrack. Cada integrante configuró su entorno local siguiendo estas especificaciones para garantizar consistencia en el desarrollo colaborativo.
 
| Herramienta | Propósito | URL / Versión |
|---|---|---|
| Web Storm | Editor de código principal para HTML, CSS, JavaScript y Markdown | https://www.jetbrains.com/webstorm/ |
| Git | Sistema de control de versiones distribuido | https://git-scm.com/ v2.43+ |
| GitHub | Plataforma de repositorios remotos, gestión de ramas y colaboración | https://github.com |
| Node.js | Entorno de ejecución para herramientas de frontend y scripts | v18.x LTS |
| Bootstrap 5.3 | Framework CSS para diseño responsivo de la landing page | https://getbootstrap.com v5.3 |
| Bootstrap Icons 1.11 | Librería de íconos SVG para la interfaz | https://icons.getbootstrap.com |
| Google Fonts (Outfit) | Tipografía principal del proyecto | https://fonts.google.com |
| Figma | Diseño colaborativo de wireframes, mockups y prototipos | https://figma.com |
| Vercel | Plataforma de despliegue continuo para la landing page | https://vercel.com |
| Postman | Testing y documentación de endpoints de la API REST | https://postman.com |
| draw.io / Mermaid | Elaboración de diagramas de arquitectura y flujos | https://draw.io |

Para clonar y ejecutar la landing page localmente:
 
```bash
# Clonar el repositorio desde el mismo WebStorm creando un nuevo proyecto
y pegando el link de la lading: https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot/InfraTrack-Landing-Page.git
```

### 5.1.2. Source Code Management
El equipo gestiona el código fuente a través de la organización pública de GitHub: 
**Organización:** [https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot](https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot)
 
**Repositorios del proyecto:**
 
| Repositorio | URL | Descripción |
|---|---|---|
| InfraTrack-Landing-Page | https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot/InfraTrack-Landing-Page | Landing page institucional desplegada en Vercel |
| InfraTrack-Report | https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot/InfraTrack-Report | Informe del proyecto en formato Markdown (este documento) |
 
**Estrategia de Branching — GitFlow:**
 
El equipo aplica GitFlow como estrategia de control de versiones. Las ramas son:
 
```
main          → Versión estable de producción. Solo recibe merges desde release/ o hotfix/.
develop       → Rama de integración. Recibe merges de todas las ramas feature/.
feature/[nombre] → Desarrollo de nuevas funcionalidades o secciones. Ej: feature/hero-section
release/[v]   → Preparación de la entrega. Ej: release/tb1
```
 
**Flujo de trabajo del equipo:**
 
```
1. El desarrollador crea su rama: git checkout -b feature/nombre-tarea develop
2. Desarrolla y hace commits con Conventional Commits
3. Hace push: git push origin feature/nombre-tarea
4. Abre un Pull Request hacia develop
5. El equipo revisa y aprueba
6. Se hace merge a develop
7. Para la entrega: se crea release/tb1 desde develop → merge a main → tag de versión
```
 
### 5.1.3. Source Code Style Guide & Conventions
**Conventional Commits:**
 
Todos los mensajes de commit siguen el estándar [Conventional Commits v1.0.0](https://www.conventionalcommits.org/). El formato es:
 
```
<tipo>[ámbito opcional]: <descripción corta en inglés>
 
[cuerpo opcional]
 
[footer opcional]
```
 
**Tipos de commit utilizados:**
 
| Tipo | Uso |
|---|---|
| `feat` | Nueva funcionalidad o sección |
| `fix` | Corrección de bug o error |
| `docs` | Cambios en documentación o README |
| `style` | Cambios de formato, CSS, sin afectar lógica |
| `refactor` | Reestructuración de código sin cambiar funcionalidad |
| `test` | Adición o modificación de pruebas |
| `chore` | Tareas de configuración, despliegue o dependencias |
 
**Ejemplos de commits del proyecto:**
 
```bash
feat(landing): add hero section with typing animation effect
feat(landing): add IoT operations dashboard with real-time KPI cards
feat(landing): add pricing plans section with three tiers
fix(landing): fix team photo path with spaces in filename
docs(report): add chapter I lean ux problem statements
chore(deploy): configure vercel deployment from main branch
style(landing): adjust color palette to match brand guidelines
```
 
**Convenciones de código HTML/CSS:**
 
- Indentación: 4 espacios
- Clases CSS: kebab-case (ej: `hero-section`, `floating-card-horizontal`)
- IDs: camelCase (ej: `typingTitle`, `iotTemp`)
- Comentarios de sección: `<!-- Section N: Nombre -->` para marcar bloques principales
- Imágenes: formato WebP cuando sea posible, con atributo `alt` descriptivo obligatorio
**Convenciones de JavaScript:**
 
- Variables y funciones: camelCase
- Constantes: UPPER_SNAKE_CASE
- Funciones: declarativas con `function` o arrow functions según contexto
- Sin `var`, usar `const` y `let`
**Convenciones de base de datos (SQL):**
 
- Palabras reservadas: UPPER_CASE (`SELECT`, `FROM`, `WHERE`)
- Nombres de tablas: camelCase (`telemetryData`, `iotNodes`)
- Nombres de columnas: camelCase (`fuelLevel`, `recordedAt`)
- Claves primarias: siempre `id` con tipo `BIGINT`
- Claves foráneas: `[tabla]Id` (ej: `assetId`, `nodeId`)

### 5.1.4. Software Deployment Configuration
**Landing Page — Vercel:**
 
La landing page de InfraTrack está desplegada en Vercel con integración continua desde GitHub.
 
| Parámetro | Valor |
|---|---|
| **Plataforma** | Vercel |
| **Repositorio fuente** | https://github.com/1ASI0729-2610-20262-TBL-InfraTrackIot/InfraTrack-Landing-Page |
| **Rama de producción** | `main` |
| **URL de producción** | https://infratrack-iot-inky.vercel.app/ |
| **Despliegue automático** | Activado — cada push a `main` genera un nuevo despliegue |
| **Framework detectado** | Other (HTML estático) |
 
**Proceso de despliegue paso a paso:**
 
```
1. El desarrollador trabaja en su rama feature/[nombre]
2. Hace commits con conventional commits
3. Abre Pull Request hacia develop
4. El equipo revisa y aprueba el PR
5. Se hace merge a develop (genera preview deployment en Vercel)
6. Para la entrega: se hace merge de develop a main
7. Vercel detecta el push a main automáticamente
8. Vercel construye y despliega en producción en < 60 segundos
9. La URL de producción queda disponible
```
---

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1
| Sprint # | Sprint 1 |
| :--- | :--- |
| Sprint Planning Background | |
| Date | 2025-04-20 |
| Time | 10:30 AM |
| Location | Universidad Peruana de Ciencias Aplicadas(Campus San Isidro), Reunión física |
| Prepared By | Jefferson Morales |
| Attendees (to planning meeting) | Jefferson Morales / Carlos Mansilla / Dhilsen Malqui / David Calixto / Aldair Ramos |
| Sprint Goal & User Stories | |
| Sprint 1 Goal | Nuestro enfoque está en desarrollar y desplegar una landing page funcional que presente eficazmente nuestro producto. Creemos que esto genera una primera interacción positiva y clara con potenciales clientes, facilitando su comprensión y conexión inicial con la propuesta de valor. Esto se confirmará cuando recibamos las primeras visitas y observemos señales básicas de interés, como clics en elementos clave, navegación dentro de la página y comentarios iniciales de usuarios o colegas. |
| Sprint 1 Velocity | 7 |
| Sum of Story Points | 45 |
#### 5.2.1.2. Aspect Leaders and Collaborators

#### 5.2.1.3. Sprint Backlog 1

#### 5.2.1.4. Development Evidence for Sprint Review

#### 5.2.1.5. Execution Evidence for Sprint Review

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

#### 5.2.1.8. Team Collaboration Insights during Sprint

---

## 5.3. Validation Interviews

### 5.3.1. Diseño de Entrevistas

### 5.3.2. Registro de Entrevistas

### 5.3.3. Evaluaciones según heurísticas

---

## 5.4. Video About-the-Product

---

# Conclusiones

## Conclusiones y recomendaciones

## Video About-the-Team
