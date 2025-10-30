Explicación del entregable y diagramas que deben presentar tus alumnos

Perfecto — aquí tienes una guía clara y detallada (en español) sobre qué deben entregar y qué diagramas incluir, basada en el enunciado del trabajo final (caso práctico “Tech Solutions”). He tomado como referencia el documento del enunciado que subiste. 

PDSD-437_TRABAJOFINAL

1) ¿De qué trata el entregable?

El entregable es una propuesta completa de solución al caso práctico de la empresa Tech Solutions donde los estudiantes deben diseñar e implementar una aplicación empresarial en Microsoft Visual Studio .NET. El objetivo es demostrar competencia técnica en:

diseño con patrones (especialmente N-Capas y Singleton),

implementación de autenticación/autorization,

uso de transacciones y rollback en SQL Server y .NET,

consultas con LINQ,

generación de reportes (con parámetros y procedimientos almacenados),

interfaz con WPF,

manejo de hilos y Timers,

creación de bibliotecas reutilizables,

empaquetado en proyecto de instalación,

y la presentación de un informe detallado y los diagramas/esquemas que respalden el diseño. 

PDSD-437_TRABAJOFINAL

2) Lista de diagramas obligatorios (y por qué cada uno es necesario)

A continuación, los diagramas que deben presentar — con qué mostrar en cada uno y el nivel de detalle esperado.

1. Diagrama de Arquitectura N-Capas (obligatorio)

Qué mostrar

Capas: Presentación (WPF), Lógica de Negocio, Acceso a Datos, (opcional) Servicios/BLL, Base de Datos.

Comunicaciones entre capas (flechas), protocolos/tecnologías (ej. WPF → BLL: llamadas a métodos; BLL → DAL: repositorios / ADO.NET / Entity Framework).

Donde se aplica Singleton (ej. gestor de conexión, gestor de configuración).
Nivel de detalle

Indicar responsabilidades de cada capa y librerías/proyectos que componen la solución (.dlls, proyectos VS).
Por qué

Demuestra la separación de responsabilidades y cómo se logra la escalabilidad y mantenibilidad. 

PDSD-437_TRABAJOFINAL

2. Diagrama de Componentes / Packages (obligatorio)

Qué mostrar

Componentes principales: UI (WPF), Servicios, Repositorios, Modelos, Reportes, Instalador.

Dependencias entre componentes (qué depende de qué).
Nivel de detalle

Nombres de proyectos (ej. Presentacion.WPF, Negocio, Datos, Reportes), interfaces públicas.
Por qué

Clarifica la modularidad y la reutilización (bibliotecas de clases).

3. Diagrama de Clases (al menos 1-2 principales) — UML

Qué mostrar

Clases clave: Cliente, Producto, Venta, Usuario, RepositorioVenta, ServicioAutenticacion.

Atributos importantes y métodos públicos (sólo los relevantes para la lógica de negocio).

Relaciones (agregación, composición, herencia).
Nivel de detalle

Suficiente para entender modelos de datos y comportamiento; no es necesario diagramar cada clase trivial.
Por qué

Muestra diseño orientado a objetos y cómo se mapeará a la BD / DTOs. 

PDSD-437_TRABAJOFINAL

4. Diagrama Entidad-Relación / Esquema de Base de Datos (obligatorio)

Qué mostrar

Tablas principales (Clientes, Productos, Ventas, DetalleVenta, Usuarios, Roles, etc.), claves primarias/foráneas.

Índices importantes y tipos de datos sugeridos.
Nivel de detalle

Incluir campos clave y relaciones cardinales (1-N, N-M).
Por qué

Fundamenta el uso de transacciones, consultas LINQ y reportes basados en procedimientos almacenados. 

PDSD-437_TRABAJOFINAL

5. Diagrama de Secuencia (2 recomendados: proceso de venta y flujo de login)

Qué mostrar

Mensajes entre objetos/capas para escenarios clave:

Venta: UI → BLL → DAL → BD (incluir transacción, commit/rollback).

Login: UI → ServicioAutenticacion → BD (verificación credenciales, carga de roles).

Señalar puntos donde ocurren transacciones y manejo de errores.
Nivel de detalle

Secuencia paso a paso, con notas sobre validaciones y seguridad.
Por qué

Clarifica el flujo runtime y la implementación de transacciones/rollback y autorización. 

PDSD-437_TRABAJOFINAL

6. Diagrama de Actividad o Flujo de Trabajo (ej. proceso de generación de reporte)

Qué mostrar

Pasos: selección parámetros → ejecución SP → obtención datos → generación reporte → impresión/guardar PDF.

Decisiones (ej. si el usuario tiene permiso, seleccionar impresora por defecto).
Por qué

Es útil para mostrar el comportamiento con condiciones y manejo de errores.

7. Diagrama de Despliegue (Deployment)

Qué mostrar

Servidores (Servidor BD — SQL Server), estaciones cliente (app WPF), ubicación del instalador, impresoras de red.

Si usan autenticación basada en hardware, indicar dispositivos/llaves y dónde se validan.
Por qué

Es obligatorio si se pide un proyecto de instalación y se menciona autenticación basada en hardware. 

PDSD-437_TRABAJOFINAL

8. Diagrama de Estado (opcional, recomendado para objetos con estados complejos)

Qué mostrar

Ciclo de vida de una Venta (creada → pendiente → confirmada → facturada → anulada) y transiciones que provocan rollback.
Por qué

Útil para auditoría y manejo de transacciones.

9. Mockups / Wireframes de la interfaz WPF (obligatorio)

Qué mostrar

Pantalla de login (con control de niveles), pantallas principales: gestión de clientes, productos, ventas, reporte.

Indicar controles clave (DataGrid, filtros, botones, Timer visual si aplica).
Por qué

Demuestra usabilidad y diseño de la interfaz. 

PDSD-437_TRABAJOFINAL

10. Diagrama o esquema del Proceso de Impresión y Reportes

Qué mostrar

Flujo: generación de dataset → parámetros → llamada al generador de reportes → spool/driver → impresión.

Indicar el uso de procedimientos almacenados y parámetros.
Por qué

Es un requisito explícito del enunciado (gestión de impresiones y reportes con parámetros). 

PDSD-437_TRABAJOFINAL

11. (Opcional pero recomendable) Diagrama de Concurrencia / Hilos y Timer

Qué mostrar

Cómo se usan Threads/Timers para tareas programadas (p. ej. actualización de stock, backups).

Gestión de sincronización (locks, monitores) para evitar condiciones de carrera.
Por qué

Especificado en el enunciado: usar hilos y Timer para mejorar rendimiento y eventos programados. 

PDSD-437_TRABAJOFINAL

3) Requisitos formales y notas sobre cada diagrama

Notación: UML o ER estándar. No hace falta notación académica perfecta, pero sí claridad.

Nivel de detalle: cada diagrama debe permitir a otra persona (profesor/examinador) entender: propósito, actores, flujo y componentes necesarios para la implementación.

Archivos: incluir diagramas en el informe (PDF) y subir fuentes editables (Diagramas en Draw.io, Visual Paradigm, PlantUML, Lucidchart, o imágenes PNG).

Relación con código: cada diagrama debe tener una breve explicación (1-2 párrafos) que enlace el diagrama con el módulo/proyecto/archivo de código donde se implementará.

Ejemplos: en el diagrama de clases, mencionar clases concretas del proyecto (nombres que aparecerán en la solución VS). 

PDSD-437_TRABAJOFINAL

4) Checklist de entrega (sugerido)

Informe técnico (documento) que explique la solución y responda las Preguntas Guía del enunciado. 

PDSD-437_TRABAJOFINAL

Diagrama de Arquitectura N-Capas + explicación de por qué mejora la escalabilidad.

Diagrama de Componentes / Packages.

Diagrama de Clases (mín. 1).

Diagrama ER / Esquema BD con claves y relaciones.

Diagrama(s) de Secuencia: venta y login.

Mockups/Wireframes WPF (pantallas clave).

Diagrama de Despliegue (Deployment).

Diagrama de Actividad: flujo de generación de reportes.

Código fuente (solución VS con proyectos separados), incluyendo bibliotecas de clase.

Scripts SQL: DDL para crear tablas, índices, procedimientos almacenados (usados por reportes).

Pruebas de transacción: ejemplo de una operación con commit + ejemplo que desrolle rollback.

Proyecto de instalación / instalador (o documentación de cómo desplegar).

Archivos de reportes (plantillas) y captura de impresión o PDF generado.

README con instrucciones para ejecutar y credenciales de prueba (usuarios/roles).

5) Sugerencias para la entrega y evaluación (cómo justificar cada diagrama)

Acompañar cada diagrama con:

Una línea que explique su propósito.

Elementos clave a revisar por el docente (p.ej. “verificar integridad referencial en ER”).

Mapear clases del diagrama con archivos del proyecto (p. ej. Negocio/ServicioVenta.cs ↔ DiagramaClase: ServicioVenta).

Demostrar trazabilidad: que cada requerimiento (autenticación, transacciones, reportes, timer, hilos, instalador) esté asociado a un diagrama y a un módulo de código.

Pruebas: incluir capturas/registro de prueba para:

Login con diferentes roles.

Compra que hace commit y compra que falla y hace rollback.

Generación e impresión de reporte.

Documentación adicional: manual de usuario breve (cómo instalar y usar).

6) Formato recomendado para los diagramas (herramientas)

Draw.io / diagrams.net — gratis, exporta PNG/PDF/Editable.

PlantUML — bueno si quieren generar diagramas desde texto (útil en repos).

Visual Paradigm / StarUML — si prefieren UML más formal.

Figma / Balsamiq — para mockups de UI.

SQL Server Management Studio — para diagramas de BD y scripts SQL.
Indicar en el informe los archivos fuente (.drawio, .puml, .vsdx, .sql). 

PDSD-437_TRABAJOFINAL

7) Criterios rápidos de evaluación (sugeridos)

Completitud: ¿están todos los diagramas requeridos? (30%)

Coherencia: ¿los diagramas y el código coinciden? (25%)

Calidad técnica: transacciones, rollback, autenticación segura, uso adecuado de patrones (25%)

Presentación y documentación: informes, scripts y guía de instalación (20%)
