<div align="center">
<img src="assets/upc_logo.png" alt="UPC Logo" width="300"/>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS

### Carrera: Ingeniería de Software

### Periodo: 2026-10

### Nombre del curso: Desarrollo de Aplicaciones Open Source (1ASI0729)

### NRC: 20262

### Nombre del profesor: Angel Augusto Velasquez Nuñez

## Informe de Trabajo Final

## Nombre del startup: InfraTrack

## Nombre del producto: Digital Machine

### Relación de integrantes:

<div style="text-align: center;">

| Apellidos y Nombres | Código de Alumno |
|:-------------------:|:----------------:|
| Mallqui Vilca, Dhilsen Armil |    U202319440    |


</div>

### Abril, 2026

---

</div>

# Registro de Versiones del Informe

| Versión | Fecha | Autor        | Descripción de modificación |
|---------|-------|--------------|-----------------------------|
| 1.0 | 04/04/2026 | Mallqui Dhilsen | Creación del reporte en formato Markdown. |

---

# Project Report Collaboration Insights

Enlace al repositorio de GitHub:

# Student Outcome
    
# Tabla de contenidos

## [Registro de Versiones del Informe](#registro-de-versiones-del-informe-1)
## [Project Report Collaboration Insights](#project-report-collaboration-insights-1)

## [Contenido](#contenido-1)
## [Tabla de contenidos](#tabla-de-contenidos-1)
## [Student Outcome](#student-outcome-1)

## [Capítulo I: Introducción](#capítulo-i-introducción-1)
- [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
- [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1 Antecedentes y problemática](#121-antecedentes-y-problemática)
    - [1.2.2 Lean UX Process](#122-lean-ux-process)
        - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
        - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
        - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
        - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
- [1.3. Segmentos objetivo](#13-segmentos-objetivo)

## [Capítulo II: Requirements Elicitation & Analysis](#capítulo-ii-requirements-elicitation--analysis-1)
- [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
- [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
- [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](#234-empathy-mapping)
- [2.4. Big Picture EventStorming](#24-big-picture-eventstorming)
- [2.5. Ubiquitous Language](#25-ubiquitous-language)

## [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification-1)
- [3.1. User Stories](#31-user-stories)
- [3.2. Impact Mapping](#32-impact-mapping)
- [3.3. Product Backlog](#33-product-backlog)

## [Capítulo IV: Product Design](#capítulo-iv-product-design-1)
- [4.1. Style Guidelines](#41-style-guidelines)
    - [4.1.1. General Style Guidelines](#411-general-style-guidelines)
    - [4.1.2. Web Style Guidelines](#412-web-style-guidelines)
- [4.2. Information Architecture](#42-information-architecture)
    - [4.2.1. Organization Systems](#421-organization-systems)
    - [4.2.2. Labeling Systems](#422-labeling-systems)
    - [4.2.3. SEO Tags and Meta Tags](#423-seo-tags-and-meta-tags)
    - [4.2.4. Searching Systems](#424-searching-systems)
    - [4.2.5. Navigation Systems](#425-navigation-systems)
- [4.3. Landing Page UI Design](#43-landing-page-ui-design)
    - [4.3.1. Landing Page Wireframe](#431-landing-page-wireframe)
    - [4.3.2. Landing Page Mock-up](#432-landing-page-mock-up)
- [4.4. Web Applications UX/UI Design](#44-web-applications-uxui-design)
    - [4.4.1. Web Applications Wireframes](#441-web-applications-wireframes)
    - [4.4.2. Web Applications Wireflow Diagrams](#442-web-applications-wireflow-diagrams)
    - [4.4.2. Web Applications Mock-ups](#443-web-applications-mock-ups)
    - [4.4.3. Web Applications User Flow Diagrams](#444-web-applications-user-flow-diagrams)
- [4.5. Web Applications Prototyping](#45-web-applications-prototyping)
- [4.6. Domain-Driven Software Architecture](#46-domain-driven-software-architecture)
    - [4.6.1. Design-Level EventStorming](#461-design-level-eventstorming)
    - [4.6.2. Software Architecture Context Diagram](#462-software-architecture-context-diagram)
    - [4.6.3. Software Architecture Container Diagrams](#463-software-architecture-container-diagrams)
    - [4.6.4. Software Architecture Components Diagrams](#464-software-architecture-components-diagrams)
- [4.7. Software Object-Oriented Design](#47-software-object-oriented-design)
    - [4.7.1. Class Diagrams](#471-class-diagrams)
    - [4.7.2. Class Dictionary](#472-class-dictionary)
- [4.8. Database Design](#48-database-design)
    - [4.8.1. Database Diagram](#481-database-diagram)

## [Capítulo V: Product Implementation, Validation & Deployment](#capítulo-v-product-implementation-validation--deployment-1)
- [5.1. Software Configuration Management](#51-software-configuration-management)
    - [5.1.1. Software Development Environment Configuration](#511-software-development-environment-configuration)
    - [5.1.2. Source Code Management](#512-source-code-management)
    - [5.1.3. Source Code Style Guide & Conventions](#513-source-code-style-guide--conventions)
    - [5.1.4. Software Deployment Configuration](#514-software-deployment-configuration)
- [5.2. Landing Page, Services & Applications Implementation](#52-landing-page-services--applications-implementation)
    - [5.2.1. Sprint 1](#521-sprint-1)
        - [5.2.1.1. Sprint Planning n](#5211-sprint-planning-n)
        - [5.2.1.2. Aspect Leaders and Collaborators](#5212-aspect-leaders-and-collaborators)
        - [5.2.1.3. Sprint Backlog n](#5213-sprint-backlog-n)
        - [5.2.1.4. Development Evidence for Sprint Review](#5214-development-evidence-for-sprint-review)
        - [5.2.1.5. Execution Evidence for Sprint Review](#5215-execution-evidence-for-sprint-review)
        - [5.2.1.6. Services Documentation Evidence for Sprint Review](#5216-services-documentation-evidence-for-sprint-review)
        - [5.2.1.7. Software Deployment Evidence for Sprint Review](#5217-software-deployment-evidence-for-sprint-review)
        - [5.2.1.8. Team Collaboration Insights during Sprint](#5218-team-collaboration-insights-during-sprint)

## [Conclusiones](#conclusiones-1)

## [Bibliografía](#bibliografía-1)

## [Anexos](#anexos-1)

# Capítulo I: Introducción
## 1.1. Startup Profile
### 1.1.1. Descripción de la Startup
### 1.1.2. Perfiles de integrantes del equipo
## 1.2. Solution Profile
### 1.2.1 Antecedentes y problemática
### 1.2.2 Lean UX Process
#### 1.2.2.1. Lean UX Problem Statements
#### 1.2.2.2. Lean UX Assumptions.
#### 1.2.2.3. Lean UX Hypothesis Statements
#### 1.2.2.4. Lean UX Canvas
## 1.3. Segmentos objetivo

# Capítulo II: Requirements Elicitation & Analysis
## 2.1. Competidores
### 2.1.1. Análisis competitivo
<table>
  <!-- Fila 1 (encabezado) -->
  <tr>
     <td colspan="6" align="center">
      Competitive Analysis Landscape 
    </td>
  </tr>

  <!-- Fila 2 -->
  <tr>
    <td>¿Por qué llevar a cabo este análisis? </td>
    <td colspan = "5" align="center">Este análisis nos permite identificar fortalezas, debilidades y oportunidades estratégicas de InfraTrack frente a soluciones existentes de monitoreo de flotas y maquinaria pesada, con el fin de definir una ventaja competitiva sostenible basada en tecnología open source, bajo costo operativo y especialización en control de combustible.</td>
  </tr>
 <tr>
   <td></td>
      <td></td>
    <td>InfraTrack</td>
    <td>Samsara</td>
    <td>Geotab</td>
    <td>Tenna</td>
  </tr>
  <!-- Fila 3 -->
  <tr>
    <td rowspan="2">Perfil</td>
      <td>Overview</td>
    <td>Plataforma open source IoT para monitoreo de maquinaria pesada, combustible y GPS con dashboard centralizado.</td>
    <td>Saas Empresarial de monitoreo de flotas basadas en IoT y analytics.</td>
    <td>Sistema telemático global para gestión de vehículos y análisis operacional.</td>
    <td>Plataforma especializada en tracking y gestión de equipos de construcción.</td>
  </tr>

  <!-- Fila 4 (continúa rowspan) -->
  <tr>
    <td>Ventaja competitiva ¿Qué valor ofrece a los clientes</td>
    <td>Bajo costo, open source, personalizable y orientado a detección de robo de combustible.</td>
    <td>Alta escalabilidad y analítica avanzada basada en datos masivos.</td>
    <td>Ecosistema consolidado e integración con múltiples fabricantes.</td>
      <td>Especialización directa en maquinaria pesada.</td>
  </tr>

  <!-- Fila 5 combinada horizontal -->
  <tr>
      <td rowspan="2">Perfil de Marketing</td>
      <td>Mercado objetivo</td>
      <td>Empresas ferreteras y pymes con maquinaria pesada.</td>
      <td>Grandes empresas logísticas y transporte.</td>
      <td>Corporaciones con grandes flotas vehiculares.</td>
      <td>Empresas de construcción y minería</td>

  </tr>

  <!-- Fila 6 -->
  <tr>
    <td>Estrategias de marketing</td>
    <td>Adopción open source, bajo costo e implementación flexible</td>
    <td>Modelo SaaS corporativo con ventas B2B.</td>
    <td>Alianzas estratégicas y partners certificados</td>
    <td>Marketing sectorial especializado.</td>
    
  </tr>

  <!-- Fila 7 -->
  <tr>
      <td rowspan="3">Perfil de Producto
<br>(vertical)</td>
    <td>Productos & Servicios</td>
    <td>Sensores IoT, monitoreo GPS, alertas de combustible, dashboard web.</td>
    <td>Tracking vehicular, cámaras, seguridad y analítica AI</td>
    <td>Gestión de flotas, mantenimiento predictivo y telemetría.</td>
    <td>Seguimiento de activos, mantenimiento y localización de maquinaria.</td>
  </tr>

  <!-- Fila 8 -->
  <tr>
    <td>Precios & Costos</td>
    <td>Bajo costo.</td>
    <td>Alto costo por suscripción mensual.</td>
    <td>Costos medios-altos + hardware certificado.</td>
    <td>Costos medios con licencias propietarias</td>
  </tr>
  <tr>
    <td>Canales de distribución (Web y/o Móvil) </td>
    <td>Plataforma web open source + despliegue propio. </td>
    <td>Web + apps móviles oficiales.</td>
    <td>Web + apps móviles </td>
     <td>Web + app móvil empresarial. </td>
  </tr>
  <tr>
    <td rowspan="4">Análisis SWOT
    <td>Fortalezas</td>
    <td>Open source, económico, adaptable, enfoque en robo de combustible.</td>
    <td>Escalabilidad global y analítica avanzada.</td>
    <td>Alta confiabilidad y experiencia en el mercado.</td>
      <td>Especialización en maquinaria pesada</td>
  </tr>
  <tr>
    <td>Debilidades</td>
    <td>Menor madurez tecnológica y ecosistema reducido.</td>
    <td>Alto costo y dependencia del proveedor.</td>
    <td>Complejidad de implementación.</d>
    <td>Menor flexibilidad tecnológica.</d>
  </tr>
  <tr>
    <td>Oportunidades</td>
    <td>Digitalización de pymes industriales y mercados emergentes.</td>
    <td>Expansión hacia IoT industrial.</td>
    <td>Integración con smart cities y AI.</td>
    <td>Crecimiento del sector construcción</td>
  </tr>
   <tr>
    <td>Amenazas</td>
    <td>Entrada de grandes empresas al segmento low-cost.</td>
    <td>Competidores open source emergentes.</td>
    <td>Nuevas startups IoT flexibles.</td>
    <td>Plataformas SaaS más completas.</td>
  </tr>
 
</table>

### 2.1.2. Estrategias y tácticas frente a competidores

A partir del análisis competitivo realizado, se identificó que el mercado de monitoreo de maquinaria pesada está dominado por soluciones propietarias orientadas a grandes corporaciones, caracterizadas por altos costos de licenciamiento, dependencia tecnológica del proveedor y baja flexibilidad de personalización.
En este contexto, InfraTrack define un conjunto de estrategias y tácticas orientadas a explotar oportunidades del mercado, mitigar amenazas competitivas y capitalizar su principal diferenciador: una plataforma open source especializada en monitoreo técnico de maquinaria pesada.

**Diferenciación basada en Open Source.**<br>
 InfraTrack emplea una estrategia de diferenciación tecnológica al ofrecer una plataforma de código abierto que elimina costos de licenciamiento y reduce la dependencia hacia proveedores externos. Esta estrategia permite a las empresas adaptar el sistema a sus necesidades operativas específicas, representando una alternativa flexible frente a soluciones cerradas ofrecidas por los competidores.<br>
**Enfoque en un nicho específico.**<br>
 En lugar de competir directamente con plataformas generalistas de gestión de flotas, InfraTrack centra su propuesta en el monitoreo técnico de maquinaria pesada y el control de combustible. Esta especialización permite atender problemas concretos como la detección de posibles robos o pérdidas operativas, generando mayor valor para empresas que requieren soluciones adaptadas a su realidad industrial.<br>
**Liderazgo en costos de adopción.**<br>
 InfraTrack aprovecha la oportunidad existente en pequeñas y medianas empresas que no pueden acceder a plataformas enterprise debido a sus altos costos. Mediante el uso de hardware IoT accesible y software libre, la startup reduce significativamente la inversión inicial requerida para iniciar procesos de digitalización operativa.<br>
**Construcción de comunidad open source.**<br>
 Como táctica complementaria, InfraTrack fomenta la participación de desarrolladores y colaboradores externos mediante repositorios abiertos y documentación accesible. Esto promueve la innovación continua, mejora la calidad del sistema y reduce costos de desarrollo a largo plazo.
**Implementación progresiva y rápida.**<br>
 InfraTrack busca disminuir las barreras de entrada mediante procesos de instalación simples y dashboards preconfigurados. Esta táctica facilita la adopción por parte de organizaciones con baja madurez tecnológica, permitiendo obtener beneficios operativos desde etapas tempranas.<br>
**Especialización en detección de anomalías operativas.**<br>
 La plataforma prioriza funcionalidades críticas como alertas en tiempo real ante variaciones bruscas de combustible y monitoreo constante de ubicación. Esta táctica responde directamente a necesidades detectadas en el sector industrial, diferenciando a InfraTrack de soluciones más generales.<br>
**Alianzas estratégicas locales.**<br>
 Finalmente, InfraTrack plantea establecer colaboraciones con proveedores de hardware IoT, técnicos de mantenimiento y empresas del sector industrial. Estas alianzas permiten ampliar el alcance del sistema sin requerir grandes inversiones comerciales, fortaleciendo su posicionamiento competitivo.

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
Para obtener informacion correspondiente con respecto a las necesidades que requieren cada segemento objetivo hemos realizado preguntas especificas para ellos.

#### Segmento Objetivo 1: Dueños de empresas ferreteras
- ¿Cuáles son actualmente los principales costos operativos que impactan la rentabilidad de su empresa?
- ¿Qué nivel de visibilidad tiene sobre el uso y estado de sus activos (vehículos, maquinaria, inventario)?
- ¿Qué herramientas o sistemas utiliza actualmente para monitorear sus operaciones logísticas?
- ¿Ha identificado pérdidas asociadas a ineficiencias, robos o mal uso de recursos? ¿Con qué frecuencia ocurren?
- ¿Qué tan importante es para usted contar con datos en tiempo real para la toma de decisiones?
- ¿Qué indicadores clave (KPIs) considera más relevantes para evaluar el desempeño de su empresa?
- ¿Cuáles son los principales desafíos que enfrenta en la gestión de su flota o activos?
- ¿Estaría dispuesto a invertir en una solución tecnológica que optimice costos y mejore la trazabilidad? ¿Bajo qué condiciones?
- ¿Qué características valoraría más en una plataforma de monitoreo (ej. alertas, reportes, integración, facilidad de uso)?
- ¿Cómo evalúa el retorno de inversión (ROI) al implementar nuevas tecnologías en su negocio?
  
#### Segmento Objetivo 2: Administradores logísticos
- ¿Cómo gestiona actualmente el seguimiento de rutas y ubicación de vehículos?
- ¿Qué dificultades enfrenta al coordinar las operaciones logísticas en tiempo real?
- ¿Con qué frecuencia se presentan desviaciones de ruta o uso no autorizado de vehículos?
- ¿Qué tipo de información le gustaría recibir automáticamente para mejorar su gestión diaria?
- ¿Qué herramientas digitales utiliza actualmente y qué limitaciones presentan?
- ¿Cómo controla el consumo de combustible y detecta posibles irregularidades?
- ¿Cuánto tiempo dedica a la generación de reportes y análisis de datos operativos?
- ¿Qué tan útil sería para usted recibir alertas automáticas ante incidencias (retrasos, desvíos, fallas)?
- ¿Qué funcionalidades considera indispensables en una plataforma de monitoreo logístico?
- ¿Qué tan fácil o difícil le resulta adoptar nuevas tecnologías en su trabajo diario?

### 2.2.2. Registro de entrevistas
## 2.3. Needfinding
### 2.3.1. User Personas
### 2.3.2. User Task Matrix
### 2.3.3. User Journey Mapping
## 2.4. Big Picture EventStorming
## 2.5. Ubiquitous Language

# Capítulo III: Requirements Specification
## 3.1. User Stories
## 3.2. Impact Mapping
## 3.3. Product Backlog

# Capítulo IV: Product Design
## 4.1. Style Guidelines
### 4.1.1. General Style Guidelines
### 4.1.2. Web Style Guidelines
## 4.2. Information Architecture
### 4.2.1. Organization Systems
### 4.2.2. Labeling Systems
### 4.2.3. SEO Tags and Meta Tags
### 4.2.4. Searching Systems
### 4.2.5. Navigation Systems
## 4.3. Landing Page UI Design
### 4.3.1. Landing Page Wireframe
### 4.3.2. Landing Page Mock-up
## 4.4. Web Applications UX/UI Design
### 4.4.1. Web Applications Wireframes
### 4.4.2. Web Applications Wireflow Diagrams
### 4.4.2. Web Applications Mock-ups
### 4.4.3. Web Applications User Flow Diagrams
## 4.5. Web Applications Prototyping
## 4.6. Domain-Driven Software Architecture
### 4.6.1. Design-Level EventStorming
### 4.6.2. Software Architecture Context Diagram
### 4.6.3. Software Architecture Container Diagrams
### 4.6.4. Software Architecture Components Diagrams
## 4.7. Software Object-Oriented Design
### 4.7.1. Class Diagrams
### 4.7.2. Class Dictionary
## 4.8. Database Design
### 4.8.1. Database Diagram

# Capítulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management
### 5.1.1. Software Development Environment Configuration
### 5.1.2. Source Code Management
### 5.1.3. Source Code Style Guide & Conventions
### 5.1.4. Software Deployment Configuration
## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1
#### 5.2.1.2. Aspect Leaders and Collaborators
#### 5.2.1.3. Sprint Backlog 1
#### 5.2.1.4. Development Evidence for Sprint Review
#### 5.2.1.5. Execution Evidence for Sprint Review
#### 5.2.1.6. Services Documentation Evidence for Sprint Review
#### 5.2.1.7. Software Deployment Evidence for Sprint Review
#### 5.2.1.8. Team Collaboration Insights during Sprint

# Conclusiones

# Bibliografía

# Anexos
