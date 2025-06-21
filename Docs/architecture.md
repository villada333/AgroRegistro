# Proyecto de Arquitectura de Software para Aplicativo Web

Este documento servirá como guía y registro de todo el proceso de arquitectura de software. 

## 1. Descripción de la Idea

La aplicación es una página web diseñada para que agricultores y administradores de cultivos lleven un control detallado de las actividades diarias y los insumos utilizados. 

* **Propósito:** Facilitar el seguimiento de tareas agrícolas (fertilización, labores de terreno, riego, etc.) y gestionar el inventario de insumos. 
* **Público objetivo:** Pequeños y medianos productores agrícolas que requieren una herramienta sencilla para organizar y registrar sus labores y materiales. 
* **Funcionalidades básicas:** 
    * Registro de actividades por fecha (fertilizaciones, desinfecciones, labores de suelo). 
    * Gestión de inventario de insumos (fertilizantes, semillas, químicos). 
    * Visualización de historial de actividades y consumos. 
    * Alertas de stock bajo en inventario. 

## 2. Análisis de Requisitos

### 2.1 Recolección de Requisitos

* **Stakeholders clave:**
    * Agricultores con experiencia en registros de campo. 
    * Agrónomo para perspectiva técnica y agronómica. 
* **Métodos de recopilación:**
    * Entrevistas semiestructuradas con cada agricultor y el agrónomo. 
    * Cuestionarios breves sobre expectativas de uso y funcionalidades deseadas. 
    * Observación de procesos actuales de registro en papel o digital. 

### 2.2 Identificación de Requisitos

#### 2.2.1 Requisitos Funcionales (RF)

| ID | Requisito |
| :--- | :--- |
| RF-1 | Registrar nueva actividad (fecha, tipo, descripción, responsable).  |
| RF-2 | Listar actividades en orden cronológico (ascendente/descendente).  |
| RF-3 | Filtrar/buscar actividades por fecha, tipo o responsable.  |
| RF-4 | Editar datos de una actividad existente.  |
| RF-5 | Eliminar un registro de actividad.  |
| RF-6 | Agregar artículo al inventario (nombre, cantidad, unidad, proveedor, fecha de ingreso).  |
| RF-7 | Listar inventario completo, con orden y filtros.  |
| RF-8 | Actualizar datos o cantidad de un artículo.  |
| RF-9 | Eliminar artículos del inventario.  |

#### 2.2.2 Requisitos No Funcionales (NFR)

| ID | Requisito |
| :--- | :--- |
| NFR-1| Usabilidad: interfaz intuitiva y responsive (escritorio y móvil).  |
| NFR-2| Rendimiento: listados (<2 s) para hasta 1 000 registros.  |
| NFR-3| Seguridad: autenticación de usuarios y control de acceso por roles (agricultor vs. agrónomo).  |
| NFR-4| Escalabilidad: base de datos preparada para crecer hasta 10 000 registros sin degradar experiencia.  |
| NFR-5| Disponibilidad: tiempo de actividad ≥ 99.5%.  |

### 2.3 Priorización y Validación

* **Must have (Debe)**
    * RF-1: Registrar nueva actividad. 
    * RF-2: Listar actividades en orden cronológico. 
    * RF-6: Agregar artículo al inventario. 
    * RF-7: Listar inventario completo. 
    * NFR-1: Interfaz intuitiva y responsive. 
    * NFR-3: Autenticación y control de acceso por roles. 

* **Should have (Debería)**
    * RF-3: Filtrar/buscar actividades. 
    * RF-4: Editar una actividad existente. 
    * RF-8: Actualizar datos o cantidad de un artículo. 
    * NFR-2: Listados carguen en <2 s con hasta 1 000 registros. 
    * NFR-4: Base de datos preparada para crecer hasta 10 000 registros. 

* **Could have (Podría)**
    * RF-5: Eliminar un registro de actividad. 
    * RF-9: Eliminar artículos del inventario. 
    * NFR-5: Disponibilidad ≥ 99,5 %. 

* **Won’t have (No estará en esta versión)**
    * Generación de reportes avanzados ni gráficas históricas. 
    * Notificaciones automáticas (e.g. alertas de bajo inventario). 
    * Integración con sensores IoT o sistemas externos. 

---
*Las siguientes secciones son una plantilla para continuar con el desarrollo del documento.*

## 3. Selección del Enfoque Arquitectónico

* Estilos arquitectónicos candidatos (monolito, microservicios, capas, cliente-servidor)
* Criterios de selección (complejidad, escalabilidad, mantenibilidad)

## 4. Diseño de la Arquitectura

* Diagramas de componentes
* Diagramas de despliegue
* Definición de módulos y sus interfaces

## 5. Evaluación y Validación de la Arquitectura

* Escenarios de uso y casos de prueba arquitectónicos
* Revisión con expertos (arquitectos senior)

## 6. Documentación Final

* Documento de decisiones arquitectónicas (ADR)
* Manual de referencia de componentes

## 7. Implementación y Revisión Continua

* Guías de codificación y estándares
* Estrategia de pruebas y CI/CD