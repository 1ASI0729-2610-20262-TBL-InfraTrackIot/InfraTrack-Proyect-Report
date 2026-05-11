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
| Date | 2026-04-20 |
| Time | 10:30 AM |
| Location | Universidad Peruana de Ciencias Aplicadas(Campus San Isidro), Reunión física |
| Prepared By | Jefferson Morales |
| Attendees (to planning meeting) | Jefferson Morales / Carlos Mansilla / Dhilsen Malqui / David Calixto / Aldair Ramos |
| Sprint Goal & User Stories | |
| Sprint 1 Goal | Nuestro enfoque está en desarrollar y desplegar una landing page funcional que presente eficazmente nuestro producto. Creemos que esto genera una primera interacción positiva y clara con potenciales clientes, facilitando su comprensión y conexión inicial con la propuesta de valor. Esto se confirmará cuando recibamos las primeras visitas y observemos señales básicas de interés, como clics en elementos clave, navegación dentro de la página y comentarios iniciales de usuarios o colegas. |
| Sprint 1 Velocity | 7 |
| Sum of Story Points | 45 |
#### 5.2.1.2. Aspect Leaders and Collaborators
| Team Member (Last Name, First Name) | GitHub Username | UI/UX Design (L/C) | Landing Page Development (L/C) | Quality Control (L/C) | Documentation (L/C) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Jefferson Morales | Fenfito | L | C | C | C |
| Carlos Mansilla | c3sv | C | C | C | L |
| Dhilsen Malqui | Dhilsen18 | C | L | C | C |
| David Calixto | DavidCalixto99 | C | C | C | C |
| Aldair Ramos | AldairRamos13 | C | C | L | C |
#### 5.2.1.3. Sprint Backlog 1

**Objetivo:** Crear y poner en producción una landing page operativa que satisfaga todas las historias de usuario definidas, sirviendo como el primer punto de contacto con los clientes y como vitrina para presentar el producto.

**Alcance:**

* Implementar barra de navegación responsive
* Crear componentes de llamada a la acción (CTA)
* Desarrollar sección de beneficios del servicio
* Construir tarjetas interactivas de servicios
* Implementar funcionalidad de preguntas frecuentes (FAQ)
* Colocar los nuevos puntos a la documentación del trabajo

**Duración:** 20 de Abril - 01 de Mayo 2026

**Capacidad de equipo:** 120 horas totales - 5 integrantes

**Requisitos técnicos:** Google Docs, GitHub, HTML, CSS, JS

<table>
  <thead>
    <tr>
      <th colspan="1" style="text-align:left; border: 1px solid black; padding: 8px;">Sprint #</th>
      <th colspan="7" style="text-align:left; border: 1px solid black; padding: 8px;">Sprint 1</th>
    </tr>
    <tr>
      <th colspan="2" style="text-align:left; border: 1px solid black; padding: 8px;">User Story</th>
      <th colspan="6" style="text-align:left; border: 1px solid black; padding: 8px;">Work-Item / Task</th>
    </tr>
    <tr>
      <th style="border: 1px solid black; padding: 8px;">Id</th>
      <th style="border: 1px solid black; padding: 8px;">Title</th>
      <th style="border: 1px solid black; padding: 8px;">Id</th>
      <th style="border: 1px solid black; padding: 8px;">Title</th>
      <th style="border: 1px solid black; padding: 8px;">Description</th>
      <th style="border: 1px solid black; padding: 8px;">Estimation (Hours)</th>
      <th style="border: 1px solid black; padding: 8px;">Assigned To</th>
      <th style="border: 1px solid black; padding: 8px;">Status (To-do / In-Process / To-Review / Done)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-35</td>
      <td style="border: 1px solid black; padding: 12px;">Propuesta de valor</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Diseñar sección informativa del producto en la landing page.</td>
      <td style="border: 1px solid black; padding: 12px;">Crear una sección visual e informativa dentro de la landing page que explique los beneficios, funcionalidades y propuesta de valor del sistema.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-36</td>
      <td style="border: 1px solid black; padding: 12px;">Formulario contacto</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar formulario de contacto</td>
      <td style="border: 1px solid black; padding: 12px;">Desarrollar un formulario interactivo que permita a los visitantes enviar consultas, solicitudes de información o solicitudes de demostración.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-37</td>
      <td style="border: 1px solid black; padding: 12px;">Recepción de datos IoT</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar recepción de telemetría</td>
      <td style="border: 1px solid black; padding: 12px;">Crear endpoints y lógica backend para recibir, procesar y almacenar correctamente la información enviada por los sensores IoT.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-38</td>
      <td style="border: 1px solid black; padding: 12px;">Acceso a la app</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Crear acceso directo a la plataforma</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar botones y accesos rápidos que permitan redirigir a los usuarios desde la landing page hacia la aplicación principal.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-39</td>
      <td style="border: 1px solid black; padding: 12px;">Consulta de datos API</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar API de consulta</td>
      <td style="border: 1px solid black; padding: 12px;">Desarrollar una API REST que permita consultar información del sistema y facilitar integraciones externas con otras plataformas.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-40</td>
      <td style="border: 1px solid black; padding: 12px;">Validación de datos</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Validar datos recibidos de sensores</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar validaciones automáticas para detectar datos inválidos, inconsistentes o fuera de rango enviados por sensores IoT.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-46</td>
      <td style="border: 1px solid black; padding: 12px;">Calibración de sensores</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Ajustar parámetros de sensores IoT</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar herramientas que permitan modificar parámetros y factores de corrección de sensores desde la plataforma web.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-47</td>
      <td style="border: 1px solid black; padding: 12px;">Modo Offline</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Implementar funcionamiento sin conexión</td>
      <td style="border: 1px solid black; padding: 12px;">Desarrollar almacenamiento en caché para permitir la visualización de los últimos datos registrados aun cuando no exista conexión a internet.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-48</td>
      <td style="border: 1px solid black; padding: 12px;">Dashboard de Hardware</td>
      <td style="border: 1px solid black; padding: 12px;">EP-08</td>
      <td style="border: 1px solid black; padding: 12px;">Diseñar panel de monitoreo técnico</td>
      <td style="border: 1px solid black; padding: 12px;">Crear un dashboard especializado para visualizar el estado técnico, batería y telemetría de los nodos IoT conectados.</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
  </tbody>
</table>

#### 5.2.1.4. Development Evidence for Sprint Review

#### 5.2.1.5. Execution Evidence for Sprint Review

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

#### 5.2.1.8. Team Collaboration Insights during Sprint

---

### 5.2.2. Sprint 2

#### 5.2.2.1. Sprint Planning 2
| Sprint # | Sprint 2 |
| :--- | :--- |
| Sprint Planning Background | |
| Date | 2025-05-02 |
| Time | 10:10 AM |
| Location | Universidad Peruana de Ciencias Aplicadas(Campus San Isidro), Reunión física |
| Prepared By | David Calixto |
| Attendees (to planning meeting) | Jefferson Morales / Carlos Mansilla / Dhilsen Malqui / David Calixto / Aldair Ramos |
| Sprint Goal & User Stories | |
| Sprint 2 Goal | Nuestro enfoque está en optimizar aspectos del proyecto referente a la experiencia de usuario y validar el interés real de los potenciales clientes mediante mejoras en la landing page y la incorporación de mecanismos de interacción. Creemos que esto permitirá aumentar el nivel de participación y obtener retroalimentación más precisa sobre nuestra propuesta de valor. Esto se confirmará cuando observemos un incremento en métricas como tiempo de permanencia, cantidad de clics en llamados a la acción, registros, formularios completados o comentarios positivos de usuarios.|
| Sprint 2 Velocity | 7 |
| Sum of Story Points | 0 |
#### 5.2.2.2. Aspect Leaders and Collaborators
| Team Member (Last Name, First Name) | GitHub Username | UI/UX Design (L/C) | Landing Page Development (L/C) | Quality Control (L/C) | Documentation (L/C) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Jefferson Morales | Fenfito | L | C | C | C |
| Carlos Mansilla | c3sv | C | C | C | L |
| Dhilsen Malqui | Dhilsen18 | C | L | C | C |
| David Calixto | DavidCalixto99 | C | C | C | C |
| Aldair Ramos | AldairRamos13 | C | C | L | C |
#### 5.2.2.3. Sprint Backlog 2

**Objetivo:** Mejorar la interacción y validación de la landing page mediante nuevas funcionalidades y optimizaciones visuales, permitiendo recopilar retroalimentación y medir el interés de los usuarios a través de registros, clics y navegación dentro de la plataforma..

**Alcance:**

* ...
* ...
* ...
* ...
* ...
* ...

**Duración:** 2 de Mayo - 12 de Mayo 2026

**Capacidad de equipo:** 140 horas totales - 5 integrantes

**Requisitos técnicos:** Google Docs, GitHub, HTML, CSS, JS

<table>
  <thead>
    <tr>
      <th colspan="1" style="text-align:left; border: 1px solid black; padding: 8px;">Sprint #</th>
      <th colspan="7" style="text-align:left; border: 1px solid black; padding: 8px;">Sprint 2</th>
    </tr>
    <tr>
      <th colspan="2" style="text-align:left; border: 1px solid black; padding: 8px;">User Story</th>
      <th colspan="6" style="text-align:left; border: 1px solid black; padding: 8px;">Work-Item / Task</th>
    </tr>
    <tr>
      <th style="border: 1px solid black; padding: 8px;">Id</th>
      <th style="border: 1px solid black; padding: 8px;">Title</th>
      <th style="border: 1px solid black; padding: 8px;">Id</th>
      <th style="border: 1px solid black; padding: 8px;">Title</th>
      <th style="border: 1px solid black; padding: 8px;">Description</th>
      <th style="border: 1px solid black; padding: 8px;">Estimation (Hours)</th>
      <th style="border: 1px solid black; padding: 8px;">Assigned To</th>
      <th style="border: 1px solid black; padding: 8px;">Status (To-do / In-Process / To-Review / Done)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-23</td>
      <td style="border: 1px solid black; padding: 12px;">Registrar maquinaria</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-11</td>
      <td style="border: 1px solid black; padding: 12px;">Generar alertas de mantenimiento</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-19</td>
      <td style="border: 1px solid black; padding: 12px;">Configurar umbrales</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-26</td>
      <td style="border: 1px solid black; padding: 12px;">Estado de conexión del Nodo</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-12</td>
      <td style="border: 1px solid black; padding: 12px;">Historial de mantenimiento</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-29</td>
      <td style="border: 1px solid black; padding: 12px;">Perfil de Operador</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
   <tr>
      <td style="border: 1px solid black; padding: 12px;">HU-22</td>
      <td style="border: 1px solid black; padding: 12px;">Configurar horario de operación</td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
      <td style="border: 1px solid black; padding: 12px;"></td>
    </tr>
  </tbody>
</table>
#### 5.2.2.4. Development Evidence for Sprint Review

#### 5.2.2.5. Execution Evidence for Sprint Review

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

#### 5.2.2.8. Team Collaboration Insights during Sprint

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
