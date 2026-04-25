# Capítulo III: Requirements Specification

## 3.1. User Stories

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
|-----------------|--------|-------------|------------------------|--------------------------|
| EP-01 | Gestión de Combustible | N/A | N/A | N/A |
| HU-01 | Ver nivel de combustible | **Como** administrador logístico, **quiero** visualizar el nivel de combustible en tiempo real **para** monitorear el consumo de cada unidad. | **Dado que** el usuario accede al dashboard, **cuando** selecciona una unidad, **entonces** el sistema muestra el nivel actual de combustible. | EP-01 |
| HU-02 | Detectar robo de combustible | **Como** administrador logístico, **quiero** recibir alertas ante caídas bruscas de combustible **para** detectar posibles robos. | **Dado que** el nivel disminuye abruptamente, **cuando** supera el umbral, **entonces** el sistema envía una alerta inmediata. | EP-01 |
| HU-03 | Historial de consumo | **Como** administrador logístico, **quiero** analizar consumo **para** identificar patrones. | **Dado que** selecciona una unidad, **cuando** consulta historial, **entonces** se muestran datos históricos. | EP-01 |
| HU-04 | Reporte de consumo | **Como** dueño, **quiero** generar reportes **para** evaluar gastos. | **Dado que** solicita reporte, **cuando** define fechas, **entonces** se descarga archivo. | EP-01 |
| HU-05 | Exportar historial | **Como** administrador, **quiero** exportar datos **para** reuniones. | **Dado que** visualiza tabla, **cuando** exporta, **entonces** descarga Excel/PDF. | EP-01 |
| EP-02 | Rastreo Satelital y Geocercas | N/A | N/A | N/A |
| HU-06 | Ubicación GPS | **Como** administrador, **quiero** ver ubicación en tiempo real **para** supervisar rutas. | **Dado que** entra al mapa, **cuando** carga datos, **entonces** muestra ubicación. | EP-02 |
| HU-07 | Historial de rutas | **Como** administrador, **quiero** ver rutas pasadas **para** auditoría. | **Dado que** define fechas, **cuando** consulta, **entonces** muestra recorrido. | EP-02 |
| HU-08 | Geocercas | **Como** administrador, **quiero** definir zonas **para** evitar uso indebido. | **Dado que** dibuja área, **cuando** se sale, **entonces** genera alerta. | EP-02 |
| HU-09 | Última ubicación | **Como** administrador, **quiero** ver último punto **para** recuperación. | **Dado que** pierde señal, **cuando** carga mapa, **entonces** muestra último punto. | EP-02 |
| EP-03 | Control de Uso y Mantenimiento | N/A | N/A | N/A |
| HU-10 | Horas de motor | **Como** sistema, **quiero** registrar uso **para** mantenimiento. | **Dado que** opera, **cuando** acumula horas, **entonces** registra. | EP-03 |
| HU-11 | Alertas mantenimiento | **Como** administrador, **quiero** alertas **para** prevenir fallas. | **Dado que** llega al límite, **cuando** se cumple, **entonces** alerta. | EP-03 |
| HU-12 | Historial mantenimiento | **Como** administrador, **quiero** registrar servicios **para** control. | **Dado que** guarda servicio, **cuando** registra, **entonces** almacena. | EP-03 |
| HU-13 | Ralentí excesivo | **Como** administrador, **quiero** detectar inactividad **para** ahorrar combustible. | **Dado que** velocidad 0, **cuando** pasa 15 min, **entonces** registra evento. | EP-03 |
| EP-04 | Business Intelligence | N/A | N/A | N/A |
| HU-14 | Dashboard | **Como** dueño, **quiero** ver KPIs **para** decisiones. | **Dado que** entra, **cuando** carga, **entonces** muestra indicadores. | EP-04 |
| HU-15 | Filtros | **Como** administrador, **quiero** filtrar datos **para** análisis. | **Dado que** aplica filtros, **cuando** selecciona, **entonces** actualiza info. | EP-04 |
| HU-16 | Comparativa | **Como** dueño, **quiero** comparar unidades **para** eficiencia. | **Dado que** selecciona varias, **cuando** analiza, **entonces** muestra gráfica. | EP-04 |
| HU-17 | Sostenibilidad | **Como** dueño, **quiero** ver emisiones **para** cumplimiento. | **Dado que** calcula, **cuando** procesa, **entonces** muestra CO2. | EP-04 |
| EP-05 | Notificaciones | N/A | N/A | N/A |
| HU-18 | Notificaciones | **Como** administrador, **quiero** alertas **para** reaccionar. | **Dado que** ocurre evento, **cuando** detecta, **entonces** notifica. | EP-05 |
| HU-19 | Umbrales | **Como** administrador, **quiero** configurar límites **para** personalizar alertas. | **Dado que** guarda config, **cuando** aplica, **entonces** registra. | EP-05 |
| HU-20 | Historial alertas | **Como** administrador, **quiero** revisar alertas **para** análisis. | **Dado que** consulta, **cuando** accede, **entonces** muestra historial. | EP-05 |
| HU-21 | Email | **Como** administrador, **quiero** recibir correos **para** seguimiento. | **Dado que** ocurre alerta, **cuando** procesa, **entonces** envía email. | EP-05 |
| HU-22 | Horario | **Como** administrador, **quiero** definir horarios **para** control. | **Dado que** configura, **cuando** se incumple, **entonces** alerta. | EP-05 |
| HU-41 | Prioridad | **Como** administrador, **quiero** clasificar alertas **para** priorizar. | **Dado que** ocurre evento, **cuando** categoriza, **entonces** muestra colores. | EP-05 |
| HU-42 | Tipo de combustible | **Como** administrador logístico, **quiero** registrar el tipo de combustible **para** calcular costos precisos. | **Dado que** se registra una unidad, **cuando** selecciona el carburante, **entonces** el sistema guarda el dato. | EP-06 |
| HU-43 | Galería de fotos | **Como** administrador logístico, **quiero** subir fotos de la maquinaria **para** tener un registro visual. | **Dado que** edita la unidad, **cuando** carga imágenes, **entonces** el sistema las almacena. | EP-06 |
| HU-44 | Cierre automático | **Como** sistema, **quiero** cerrar sesión por inactividad **para** proteger la información. | **Dado que** no hay actividad, **cuando** pasan 30 min, **entonces** redirige al login. | EP-07 |
| HU-45 | Verificación de correo | **Como** sistema, **quiero** validar el email **para** evitar cuentas falsas. | **Dado que** el usuario se registra, **cuando** completa el proceso, **entonces** envía código de verificación. | EP-07 |
| HU-46 | Calibración de sensores | **Como** técnico, **quiero** ajustar sensores **para** corregir mediciones. | **Dado que** ingresa parámetros, **cuando** guarda, **entonces** aplica el ajuste. | EP-08 |
| HU-47 | Modo offline | **Como** administrador logístico, **quiero** ver datos sin internet **para** consultas rápidas. | **Dado que** no hay conexión, **cuando** abre la app, **entonces** muestra datos en caché. | EP-08 |
| HU-48 | Dashboard de hardware | **Como** desarrollador, **quiero** monitorear nodos IoT **para** prevenir fallas. | **Dado que** recibe datos, **cuando** detecta batería baja, **entonces** genera alerta. | EP-08 |
| HU-49 | Modo oscuro/claro | **Como** usuario, **quiero** cambiar el tema **para** mejorar visibilidad. | **Dado que** cambia configuración, **cuando** activa opción, **entonces** actualiza interfaz. | EP-09 |
| HU-50 | Selección de idioma | **Como** usuario, **quiero** cambiar idioma **para** facilitar uso. | **Dado que** selecciona idioma, **cuando** confirma, **entonces** traduce interfaz. | EP-09 |


## 3.2. Impact Mapping

### Beto Mendoza (Dueño)

<p align="center">
  <img src="../assets/Impact-Map Roberto.png" width="600"/>
</p>

### Carlos Vizcarra (Gestor de Flota)

<p align="center">
  <img src="../assets/Impact-Map Carlos.png" width="600"/>
</p>

## 3.3. Product Backlog

| # Orden | User Story Id | Título | Descripción | Story Points (1 / 2 / 3 / 5 / 8) |
|---------|--------------|--------|-------------|----------------------------------|
| 1 | HU-02 | Detectar robo de combustible | Alertas ante caídas bruscas de combustible | 8 |
| 2 | HU-01 | Ver nivel de combustible | Monitoreo en tiempo real del combustible | 5 |
| 3 | HU-06 | Visualizar ubicación GPS | Supervisión de unidades en tiempo real | 5 |
| 4 | HU-18 | Notificaciones en tiempo real | Alertas inmediatas ante eventos críticos | 5 |
| 5 | HU-38 | Recepción IoT | Recepción de datos de sensores | 8 |
| 6 | HU-14 | Dashboard general | Visualización de KPIs principales | 8 |
| 7 | HU-11 | Alertas de mantenimiento | Prevención de fallas en maquinaria | 5 |
| 8 | HU-10 | Registrar horas de motor | Registro automático de uso | 3 |
| 9 | HU-03 | Historial de consumo | Análisis de consumo de combustible | 5 |
| 10 | HU-19 | Configurar umbrales | Personalización de alertas | 3 |
| 11 | HU-39 | API de datos | Exposición de datos para integraciones | 5 |
| 12 | HU-15 | Filtrar información | Análisis avanzado de datos | 3 |
| 13 | HU-07 | Historial de rutas | Consulta de recorridos históricos | 5 |
| 14 | HU-08 | Geocercas de seguridad | Definición de zonas permitidas | 5 |
| 15 | HU-09 | Última ubicación conocida | Ubicación final registrada | 3 |
| 16 | HU-04 | Reportes de consumo | Generación de reportes | 5 |
| 17 | HU-05 | Exportar historial | Exportación a Excel/PDF | 3 |
| 18 | HU-12 | Historial de mantenimiento | Registro de servicios realizados | 3 |
| 19 | HU-13 | Detectar ralentí excesivo | Control de inactividad con motor encendido | 3 |
| 20 | HU-20 | Historial de alertas | Auditoría de eventos | 3 |
| 21 | HU-21 | Notificación por correo | Alertas vía email | 3 |
| 22 | HU-22 | Configurar horario | Control de uso fuera de jornada | 3 |
| 23 | HU-41 | Prioridad de alertas | Clasificación por severidad | 2 |
| 24 | HU-16 | Comparativa de flota | Comparación de rendimiento | 5 |
| 25 | HU-17 | Dashboard sostenibilidad | Visualización de emisiones CO2 | 5 |
| 26 | HU-23 | Registrar maquinaria | Registro de unidades | 3 |
| 27 | HU-24 | Editar unidad | Actualización de datos | 3 |
| 28 | HU-25 | Eliminar unidad | Eliminación de registros | 2 |
| 29 | HU-26 | Estado del nodo | Monitoreo de conexión IoT | 3 |
| 30 | HU-27 | Vincular nodo | Asociación hardware-unidad | 3 |
| 31 | HU-28 | Actualización masiva | Edición múltiple de registros | 3 |
| 32 | HU-29 | Perfil de operador | Asignación de responsables | 3 |
| 33 | HU-30 | Registro de usuario | Creación de cuentas | 3 |
| 34 | HU-31 | Login | Acceso al sistema | 3 |
| 35 | HU-32 | Roles de usuario | Control de permisos | 5 |
| 36 | HU-33 | Auditoría | Registro de acciones | 3 |
| 37 | HU-34 | Recuperar contraseña | Restablecimiento de acceso | 2 |
| 38 | HU-35 | Propuesta de valor | Información del sistema | 2 |
| 39 | HU-36 | Formulario de contacto | Captación de clientes | 2 |
| 40 | HU-37 | Acceso a la app | Redirección a plataforma | 2 |
| 41 | HU-40 | Validación de datos | Control de datos incorrectos | 3 |
| 42 | HU-42 | Tipo de combustible | Registro de carburante | 2 |
| 43 | HU-43 | Galería de fotos | Registro visual de activos | 2 |
| 44 | HU-44 | Cierre automático | Seguridad por inactividad | 2 |
| 45 | HU-45 | Verificación de correo | Validación de usuarios | 2 |
| 46 | HU-46 | Calibración de sensores | Ajuste de mediciones | 3 |
| 47 | HU-47 | Modo offline | Acceso sin conexión | 5 |
| 48 | HU-48 | Dashboard de hardware | Monitoreo de nodos IoT | 5 |
| 49 | HU-49 | Modo oscuro/claro | Personalización visual | 2 |
| 50 | HU-50 | Selección de idioma | Internacionalización | 2 |
