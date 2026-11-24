# Sistema web de registro y seguimiento de pedidos — Pollos La Diabla

Proyecto Incremental del curso **ISW-912 Administración de Proyectos Informáticos**
Universidad Técnica Nacional (UTN), Sede Regional de San Carlos · III Cuatrimestre 2026
Profesor: Rudy Barboza Rodríguez

## Equipo Scrum

| Rol Scrum | Integrante | Función |
|---|---|---|
| Product Owner + Developer | Nayely Vega Murillo | Comprender las necesidades, comunicar el Product Goal y ordenar el Product Backlog. |
| Scrum Master + Developer | Fiorella Lazo Reyes | Apoyar la aplicación de Scrum, mejorar la colaboración y atender impedimentos. |

Ambas diseñan, desarrollan, prueban y revisan el código de la otra. El equipo trabaja sin jerarquías internas, con transparencia, inspección y adaptación.

## Descripción del proyecto

**Organización beneficiaria:** Pollos La Diabla, una soda dedicada a preparar y vender comidas.

**Problema.** El registro de pedidos mediante papel y comunicaciones verbales dificulta mantener información clara y actualizada entre atención y cocina, y puede generar confusiones sobre productos, observaciones y estados.

**Objetivo.** Implementar un sistema web de registro y seguimiento de pedidos que mejore la coordinación entre atención y cocina.

**Product Goal.** El personal de la soda dispone de una herramienta compartida para registrar los pedidos y consultar su estado, que facilita la coordinación entre atención y cocina y permite dar seguimiento a cada pedido hasta su entrega.

## Alcance

**Incluido**

- Registro de productos, cantidades y observaciones de cada pedido.
- Asignación de un identificador único por pedido.
- Consulta de pedidos activos y de sus detalles.
- Actualización de estados: **pendiente → en preparación → listo → entregado**.
- Consulta del historial de pedidos entregados.

**Fuera del alcance:** pagos en línea, facturación electrónica, control de inventario y gestión de entregas a domicilio.

## Product Backlog

| ID | Historia | Prioridad | Puntos | Dependencia |
|---|---|---|---|---|
| PB01 | Registrar productos, cantidades y observaciones de un pedido | 1 | 5 | — |
| PB02 | Consultar pedidos activos y sus detalles | 2 | 3 | PB01 |
| PB03 | Actualizar el estado a "en preparación" y "listo" | 3 | 3 | PB01 y PB02 |
| PB04 | Marcar como entregado un pedido listo | 4 | 2 | PB03 |
| PB05 | Consultar el historial de pedidos entregados | 5 | 3 | PB04 |

**Total: 16 puntos.** Las estimaciones son tamaño relativo (esfuerzo, complejidad e incertidumbre), no horas.

## Metodología y cronograma

Se aplica **Scrum** con Sprints cortos de duración variable, ajustados al plazo del proyecto (12 de octubre al 25 de noviembre de 2026).

| Periodo | Fechas | Actividad / entrega | Puntos |
|---|---|---|---|
| Preparación | 12–18 oct | Coordinación, requisitos y preparación del entorno | — |
| Sprint 1 | 19 oct – 1 nov | PB01 y PB02: registro y consulta de pedidos | 8 |
| Sprint 2 | 2–8 nov | PB03: cambio de estados | 3 |
| Sprint 3 | 9–15 nov | PB04 y PB05: entrega e historial | 5 |
| Sprint 4 | 16–19 nov | Integración y pruebas del flujo completo | — |
| Sprint 5 | 20–22 nov | Correcciones y mejoras de usabilidad | — |
| Sprint 6 | 23–24 nov | Validación, documentación y preparación de la entrega | — |
| Entrega final | 25 nov | Revisión final y entrega | — |

**Estado actual:** Sprints 1 a 6 finalizados; las cinco historias (PB01–PB05) cumplen la Definition of Done, la verificación y la aceptación, con los 16 puntos acreditados.

## Presupuesto estimado

| Rubro | Costo (₡) |
|---|---|
| Trabajo de desarrollo y pruebas (180 h × ₡6 000) | 1 080 000 |
| Alojamiento y dominio | 65 000 |
| Conectividad y servicios | 50 000 |
| Equipo y periféricos | 80 000 |
| Capacitación y documentación | 60 000 |
| Subtotal | 1 335 000 |
| Reserva de contingencia (15 %) | 200 250 |
| **Total** | **1 535 250** |

## Definition of Done (resumen)

Una historia se considera terminada solo si:

- está implementada e integrada con el sistema, sin cambios pendientes que impidan su uso;
- cumple sus criterios de aceptación y se ejecutaron las pruebas correspondientes;
- se revisó el código entre las dos desarrolladoras;
- el código actualizado está en el repositorio y la documentación se ajustó cuando corresponde;
- puede demostrarse con un flujo de pedidos y no presenta errores críticos conocidos.

## Estructura del repositorio

```
proyecto-incremental-soda/
├── expediente/   # Documentación del proyecto
│   ├── Proyecto.docx                                      # Expediente del proyecto (secciones 00 a 10 y conclusiones)
│   ├── Pollos_La_Diabla_Backlog_y_Seguimiento_Scrum.xlsx  # Backlog, Sprints, entregas y seguimiento de puntos
│   └── Avance1.docx · Avance2.docx · Avance3.docx         # Avances entregados durante el curso
├── prototipo/    # Imágenes del prototipo del sistema
└── README.md
```

## Documentación

- **Expediente del proyecto** (`expediente/Proyecto.docx`): identificación y Scrum Team, Project Charter y Product Goal, contexto organizacional, interesados, ciclo de vida y primer Sprint, backlog y seguimiento, alcance y criterios de aceptación, plan temporal y costos, riesgos y adquisiciones, calidad y Definition of Done, responsabilidades, comunicación, Working Agreements y registro de cambios.
- **Seguimiento en Excel** (`expediente/Pollos_La_Diabla_Backlog_y_Seguimiento_Scrum.xlsx`), con cuatro hojas:
  - **Backlog:** historias, puntos, prioridad, épica y criterios de aceptación.
  - **Sprints:** tareas por Sprint con responsable y estado (Por hacer, En curso, En revisión, Finalizado).
  - **Entregas:** cronograma de entregas y presupuesto.
  - **Seguimiento:** historias aceptadas, puntos terminados, puntos pendientes y velocidad.
- **Prototipo** (`prototipo/`): imágenes del diseño del sistema, con la selección de productos, las observaciones y el registro del pedido, la consulta de pedidos activos y la preparación y entrega.

## Forma de trabajo

Acuerdos principales del equipo (Working Agreements):

- Comunicación clara y respetuosa, con coordinación diaria durante el trabajo.
- Los cambios de código y documentos se registran en GitHub con mensajes descriptivos.
- El código se revisa entre ambas desarrolladoras antes de integrar cambios relevantes.
- Los cambios de alcance se canalizan por medio del Product Owner y se evalúa su impacto en tiempo, costo y riesgo.
- Una historia solo se marca como terminada si cumple los criterios de aceptación y la Definition of Done.
