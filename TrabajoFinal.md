# 💼 PDSD-437_TRABAJOFINAL — Tech Solutions  
### 📘 Proyecto Final: Aplicación Empresarial en Microsoft Visual Studio .NET

---

## 🧩 1. Descripción General del Entregable  

El proyecto consiste en el **diseño e implementación de una aplicación empresarial** para la empresa ficticia **Tech Solutions**, desarrollada en **Microsoft Visual Studio (.NET)**.  

La solución debe cumplir con los siguientes requisitos técnicos y de arquitectura:

- **Diseño con patrones**: especialmente **N-Capas** y **Singleton**.  
- **Autenticación y autorización** de usuarios.  
- **Transacciones y rollback** en SQL Server y .NET.  
- **Consultas con LINQ**.  
- **Generación de reportes** (con parámetros y procedimientos almacenados).  
- **Interfaz WPF** (Windows Presentation Foundation).  
- **Manejo de hilos (Threads) y Timers**.  
- **Creación de bibliotecas reutilizables (.dll)**.  
- **Proyecto de instalación (Setup Project)**.  
- **Informe detallado + diagramas UML y técnicos** que respalden el diseño.

---

##  2. Diagramas necesarios

A continuación se listan los diagramas exigidos y el contenido que debe mostrar cada uno:

### 1️⃣ Diagrama de Arquitectura N-Capas (Obligatorio)
**Capas:**  
- Presentación (WPF)  
- Lógica de Negocio (BLL)  
- Acceso a Datos (DAL)  
- Servicios / API (opcional)  
- Base de Datos (SQL Server)

**Debe mostrar:**  
- Flujo de comunicación entre capas (flechas).  
- Tecnologías utilizadas (WPF, Entity Framework, ADO.NET, etc.).  
- Aplicación del patrón **Singleton** (gestor de conexión o configuración).  
- Proyectos y librerías que forman la solución (.dll / .csproj).  

---

### 2️⃣ Diagrama de Componentes / Packages
**Componentes principales:**  
- UI (WPF)  
- Servicios  
- Repositorios  
- Modelos  
- Reportes  
- Instalador  

**Debe mostrar:**  
- Dependencias entre componentes y relaciones de uso.

---

### 3️⃣ Diagrama de Clases
**Clases clave sugeridas:**  
- `Cliente`, `Producto`, `Venta`, `Usuario`, `RepositorioVenta`, `ServicioAutenticacion`  

**Debe incluir:**  
- Atributos y métodos principales.  
- Relaciones (herencia, agregación, composición).  
- Correspondencia con entidades de la BD y DTOs.  

---

### 4️⃣ Diagrama Entidad–Relación / Esquema de Base de Datos
**Tablas principales:**  
`Clientes`, `Productos`, `Ventas`, `DetalleVenta`, `Usuarios`, `Roles`, etc.  

**Debe indicar:**  
- Claves primarias y foráneas.  
- Relaciones (1–N, N–N).  
- Procedimientos almacenados usados por reportes.

---

### 5️⃣ Diagramas de Secuencia (2 Recomendados)
**Procesos a modelar:**
- **Venta:** `UI → BLL → DAL → BD`  
  - Incluir manejo de transacciones (Commit/Rollback).  
- **Login:** `UI → ServicioAutenticacion → BD`  
  - Verificación de credenciales y carga de roles.  

**Objetivo:** visualizar el flujo runtime y puntos de control de errores/transacciones.

---

### 6️⃣ Diagrama de Actividad / Flujo de Trabajo
**Ejemplo:** Proceso de generación de reportes  
Pasos:  
1. Selección de parámetros.  
2. Ejecución de procedimiento almacenado.  
3. Obtención de datos.  
4. Generación del reporte.  
5. Exportación / impresión.  

Incluir decisiones (condicionales de permisos, selección de impresora, etc.).

---

### 7️⃣ Diagrama de Despliegue (Deployment)
**Debe mostrar:**  
- Servidor de base de datos (SQL Server).  
- Estaciones cliente (App WPF).  
- Ubicación del instalador y dispositivos (impresoras, llaves de hardware, etc.).  
- Conexiones y protocolos de red utilizados.  

Obligatorio si se entrega un proyecto de instalación.

---

### 8️⃣ Mockups / Wireframes WPF
**Pantallas obligatorias:**  
- Pantalla de **Login** (con control de roles).  
- **Gestión de Clientes / Productos / Ventas / Reportes**.  

**Debe incluir:**  
- Controles principales (DataGrid, TextBox, Buttons, Timer, Filtros, etc.).  
- Navegación entre pantallas.  
- Diseño visual coherente y funcional.

---

## 📋 3. Requisitos Formales y Notas sobre Diagramas

- **Notación:** UML o ER estándar.  
- **Nivel de detalle:** suficiente para comprender flujo, actores y componentes.  
- **Archivos:**  
  - Incluir diagramas en el informe (PDF).  
  - Subir fuentes editables (`.drawio`, `.uml`, `.vpp`, `.fig`, `.png`).
  - Base de datos
  - Instalador
- **Relación con el código:** cada diagrama debe tener una breve explicación que vincule con el módulo/proyecto correspondiente.  

**Ejemplo:**  
> En el diagrama de clases, la clase `RepositorioVenta` se implementa en el proyecto `TechSolutions.DAL` y contiene métodos que interactúan con la tabla `Ventas` en SQL Server.

---

## ✅ 4. Checklist de Entrega

| Ítem | Descripción | Estado |
|------|--------------|--------|
| 📄 Informe técnico | Explicación completa de la solución y respuestas a las preguntas guía | ☐ |
| 🧱 Diagrama N-Capas | Justificación del patrón y ventajas de escalabilidad | ☐ |
| ⚙️ Diagrama de Componentes | Estructura modular de la solución | ☐ |
| 🧬 Diagrama de Clases | Clases principales y relaciones | ☐ |
| 🗃️ Diagrama ER | Esquema completo de la base de datos | ☐ |
| 🔁 Diagramas de Secuencia | Flujo de venta y login | ☐ |
| 🧭 Diagrama de Actividad | Generación de reportes | ☐ |
| 🖥️ Mockups WPF | Interfaz principal y pantallas clave | ☐ |
| 🌐 Diagrama de Despliegue | Infraestructura y comunicación | ☐ |
| 💻 Código fuente | Solución VS con proyectos separados | ☐ |
| 🧾 Scripts SQL | DDL + procedimientos almacenados | ☐ |
| 🔄 Pruebas de transacción | Ejemplo con commit y rollback | ☐ |
| 📦 Instalador | Proyecto de instalación o guía de despliegue | ☐ |
| 📊 Reportes | Archivos de reporte y salida PDF | ☐ |
| 🔑 README | Instrucciones de ejecución y credenciales de prueba | ☐ |

---

## 🧰 5. Herramientas Recomendadas

| Tipo | Herramienta | Comentario |
|------|--------------|------------|
| 🧠 Diagramas UML | **Draw.io (diagrams.net)** | Gratuito, exporta PNG/PDF/Editable |
| 🧩 Modelado textual | **PlantUML** | Ideal si trabajas con código fuente |
| 💼 Diseño profesional | **Visual Paradigm / StarUML** | UML formal y completo |
| 🎨 Mockups | **Figma / Balsamiq** | Para pantallas WPF |
| 🗃️ BD | **SQL Server Management Studio (SSMS)** | Diagramas ER y ejecución de scripts |

---


