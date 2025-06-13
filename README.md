# Proyecto de Arquitectura de Software para Aplicativo Web

[cite_start]Este documento servirá como guía y registro de todo el proceso de arquitectura de software. 

## 1. Descripción de la Idea

[cite_start]La aplicación es una página web diseñada para que agricultores y administradores de cultivos lleven un control detallado de las actividades diarias y los insumos utilizados. 

* [cite_start]**Propósito:** Facilitar el seguimiento de tareas agrícolas (fertilización, labores de terreno, riego, etc.) y gestionar el inventario de insumos. 
* [cite_start]**Público objetivo:** Pequeños y medianos productores agrícolas que requieren una herramienta sencilla para organizar y registrar sus labores y materiales. 
* [cite_start]**Funcionalidades básicas:** 
    * [cite_start]Registro de actividades por fecha (fertilizaciones, desinfecciones, labores de suelo). 
    * [cite_start]Gestión de inventario de insumos (fertilizantes, semillas, químicos). 
    * [cite_start]Visualización de historial de actividades y consumos. 
    * [cite_start]Alertas de stock bajo en inventario. 

## 2. Análisis de Requisitos

### 2.1 Recolección de Requisitos

* **Stakeholders clave:**
    * [cite_start]Agricultores con experiencia en registros de campo. 
    * [cite_start]Agrónomo para perspectiva técnica y agronómica. 
* **Métodos de recopilación:**
    * [cite_start]Entrevistas semiestructuradas con cada agricultor y el agrónomo. 
    * [cite_start]Cuestionarios breves sobre expectativas de uso y funcionalidades deseadas. 
    * [cite_start]Observación de procesos actuales de registro en papel o digital. 

### 2.2 Identificación de Requisitos

#### 2.2.1 Requisitos Funcionales (RF)

| ID | Requisito |
| :--- | :--- |
| RF-1 | [cite_start]Registrar nueva actividad (fecha, tipo, descripción, responsable).  |
| RF-2 | [cite_start]Listar actividades en orden cronológico (ascendente/descendente).  |
| RF-3 | [cite_start]Filtrar/buscar actividades por fecha, tipo o responsable.  |
| RF-4 | [cite_start]Editar datos de una actividad existente.  |
| RF-5 | [cite_start]Eliminar un registro de actividad.  |
| RF-6 | [cite_start]Agregar artículo al inventario (nombre, cantidad, unidad, proveedor, fecha de ingreso).  |
| RF-7 | [cite_start]Listar inventario completo, con orden y filtros.  |
| RF-8 | [cite_start]Actualizar datos o cantidad de un artículo.  |
| RF-9 | [cite_start]Eliminar artículos del inventario.  |

#### 2.2.2 Requisitos No Funcionales (NFR)

| ID | Requisito |
| :--- | :--- |
| NFR-1| [cite_start]Usabilidad: interfaz intuitiva y responsive (escritorio y móvil).  |
| NFR-2| [cite_start]Rendimiento: listados (<2 s) para hasta 1 000 registros.  |
| NFR-3| [cite_start]Seguridad: autenticación de usuarios y control de acceso por roles (agricultor vs. agrónomo).  |
| NFR-4| [cite_start]Escalabilidad: base de datos preparada para crecer hasta 10 000 registros sin degradar experiencia.  |
| NFR-5| [cite_start]Disponibilidad: tiempo de actividad ≥ 99.5%.  |

### 2.3 Priorización y Validación

* **Must have (Debe)**
    * [cite_start]RF-1: Registrar nueva actividad. 
    * [cite_start]RF-2: Listar actividades en orden cronológico. 
    * [cite_start]RF-6: Agregar artículo al inventario. 
    * [cite_start]RF-7: Listar inventario completo. 
    * [cite_start]NFR-1: Interfaz intuitiva y responsive. 
    * [cite_start]NFR-3: Autenticación y control de acceso por roles. 

* **Should have (Debería)**
    * [cite_start]RF-3: Filtrar/buscar actividades. 
    * [cite_start]RF-4: Editar una actividad existente. 
    * [cite_start]RF-8: Actualizar datos o cantidad de un artículo. 
    * [cite_start]NFR-2: Listados carguen en <2 s con hasta 1 000 registros. 
    * [cite_start]NFR-4: Base de datos preparada para crecer hasta 10 000 registros. 

* **Could have (Podría)**
    * [cite_start]RF-5: Eliminar un registro de actividad. 
    * [cite_start]RF-9: Eliminar artículos del inventario. 
    * [cite_start]NFR-5: Disponibilidad ≥ 99,5 %. 

* **Won’t have (No estará en esta versión)**
    * [cite_start]Generación de reportes avanzados ni gráficas históricas. 
    * [cite_start]Notificaciones automáticas (e.g. alertas de bajo inventario). 
    * [cite_start]Integración con sensores IoT o sistemas externos. 

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