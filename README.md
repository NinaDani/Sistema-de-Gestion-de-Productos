<div align="center">

# 🏪✨ Antoneth ✨🏪
### Sistema de Gestión para Librería Antoneth

```
╔══════════════════════════════════════════════════════════════╗
║  📚 Control de Inventario  •  💰 Ventas  •  📊 Reportes     ║
╚══════════════════════════════════════════════════════════════╝
```

**[🚀 Características](#-características-principales)** • 
**[📥 Instalación](#-instalación)** • 
**[💡 Uso](#-guía-de-uso)** • 
**[🏗️ Arquitectura](#️-arquitectura-del-sistema)** • 
**[🛠️ Tecnologías](#️-tecnologías)**

---

</div>

## 📖 Sobre el Proyecto

> **Antoneth** transforma la gestión tradicional de la Librería Antoneth (Satélite Norte) en un sistema digital moderno, eficiente y confiable.

**¿Qué hace especial a Antoneth?**

🎯 Elimina los procesos manuales y reduce errores  
⚡ Acelera el registro de ventas y control de inventario  
📄 Genera facturas profesionales en PDF automáticamente  
📊 Proporciona análisis detallados para mejores decisiones  
🔒 Protege la información con autenticación segura  

---

## ✨ Características Principales

<div align="center">

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  🔐 AUTENTICACIÓN        📦 INVENTARIO        💰 VENTAS            │
│                                                                     │
│  • Acceso seguro         • Alta de productos  • Registro rápido    │
│  • Control de sesión     • Actualización      • Cálculo automático │
│  • Protección datos      • Búsqueda avanzada  • Factura PDF        │
│                          • Control stock      • Historial          │
│                                                                     │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  📊 REPORTES             👤 USUARIOS          🎨 INTERFAZ          │
│                                                                     │
│  • Ventas detalladas     • Gestión perfiles   • Diseño intuitivo   │
│  • Estado inventario     • Control permisos   • Navegación fluida  │
│  • Exportación datos     • Administración     • Responsive         │
│  • Análisis visual       • Seguridad          • Moderna            │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

</div>

---

## 🏗️ Arquitectura del Sistema

<div align="center">

### 🎯 Patrón MVC - Modelo Vista Controlador

</div>

```
                    👤 USUARIO
                       │
                       ▼
        ╔══════════════════════════════╗
        ║                              ║
        ║    🖥️  CAPA DE VISTA        ║
        ║    (Swing/AWT)               ║
        ║    • Interfaz gráfica        ║
        ║    • Formularios             ║
        ║    • Componentes UI          ║
        ║                              ║
        ╚══════════════╤═══════════════╝
                       │
                       ▼
        ╔══════════════════════════════╗
        ║                              ║
        ║    ⚙️  CAPA CONTROLADOR     ║
        ║    (Lógica de Negocio)       ║
        ║    • Validaciones            ║
        ║    • Procesamiento           ║
        ║    • Coordinación            ║
        ║                              ║
        ╚══════════════╤═══════════════╝
                       │
                       ▼
        ╔══════════════════════════════╗
        ║                              ║
        ║    📦 CAPA MODELO           ║
        ║    (Entidades + JDBC)        ║
        ║    • Clases de datos         ║
        ║    • Conexión BD             ║
        ║    • Operaciones CRUD        ║
        ║                              ║
        ╚══════════════╤═══════════════╝
                       │
                       ▼
        ╔══════════════════════════════╗
        ║                              ║
        ║    🗄️  BASE DE DATOS        ║
        ║    (MySQL)                   ║
        ║    • Productos               ║
        ║    • Ventas                  ║
        ║    • Usuarios                ║
        ║                              ║
        ╚══════════════════════════════╝
```

### 📋 Capas y Responsabilidades

| Capa | 🎯 Función | 🔧 Tecnología |
|:-----|:-----------|:--------------|
| **Vista** | Interfaz gráfica y experiencia de usuario | Java Swing/AWT |
| **Controlador** | Lógica de negocio y flujo de datos | Java Core |
| **Modelo** | Gestión y estructura de datos | JDBC + POJOs |
| **Persistencia** | Almacenamiento y consultas | MySQL 8.0+ |

---

## 🔄 Flujo de Trabajo

<div align="center">

```
                    🔑 INICIO DE SESIÓN
                           │
                           ▼
                ┌──────────────────────┐
                │   🏠 PANEL PRINCIPAL │
                └──────────┬───────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
        ▼                  ▼                  ▼
   ┌─────────┐       ┌─────────┐       ┌─────────┐
   │ 📦 PROD │       │ 💰 VENT │       │ 📊 REPO │
   │ UCTOS   │       │ AS      │       │ RTES    │
   └────┬────┘       └────┬────┘       └────┬────┘
        │                 │                  │
        │                 ▼                  │
        │          ┌──────────────┐          │
        │          │ 📄 FACTURA   │          │
        │          │    PDF       │          │
        │          └──────────────┘          │
        │                                    │
        └────────────────┬───────────────────┘
                         ▼
                  ┌─────────────┐
                  │ 💾 BASE DE  │
                  │    DATOS    │
                  └─────────────┘
```

</div>

### 📝 Proceso Paso a Paso

| Paso | Acción | Descripción |
|:----:|:-------|:------------|
| **1️⃣** | **Login** | Autenticación del administrador con credenciales |
| **2️⃣** | **Dashboard** | Acceso al panel principal del sistema |
| **3️⃣** | **Gestión** | Operaciones CRUD en productos y ventas |
| **4️⃣** | **Facturación** | Generación automática de documentos PDF |
| **5️⃣** | **Reportes** | Análisis y visualización de datos |
| **6️⃣** | **Logout** | Cierre seguro de sesión |

---

## 🛠️ Tecnologías

<div align="center">

### Stack Tecnológico

```
╔════════════════════════════════════════════════════════════╗
║                                                            ║
║  ☕ JAVA 17+          Lenguaje principal                  ║
║  🎨 SWING/AWT        Interfaz gráfica                     ║
║  🗄️ MYSQL 8.0+       Base de datos relacional            ║
║  🔌 JDBC             Conectividad BD                      ║
║  📄 iTEXT 5.x        Generación PDFs                      ║
║  🔧 NETBEANS 12+     IDE de desarrollo                    ║
║  📚 GIT              Control de versiones                 ║
║                                                            ║
╚════════════════════════════════════════════════════════════╝
```

</div>

| Tecnología | Versión | Uso en el Proyecto |
|:-----------|:--------|:-------------------|
| ☕ **Java** | 17+ | Desarrollo completo de la aplicación |
| 🎨 **Swing/AWT** | Built-in | Diseño de la interfaz gráfica |
| 🗄️ **MySQL** | 8.0+ | Almacenamiento de datos |
| 🔌 **JDBC** | Latest | Conexión Java-MySQL |
| 📄 **iText** | 5.x.x | Creación de facturas PDF |
| 🔧 **NetBeans** | 12+ | Entorno de desarrollo |
| 📚 **Git** | Latest | Versionado del código |

---

## 📦 Requisitos del Sistema

<div align="center">

```
┌─────────────────────────────────────────────────────────┐
│  💻 SOFTWARE REQUERIDO                                  │
├─────────────────────────────────────────────────────────┤
│  ☕ Java JDK 17 o superior                              │
│  🔧 NetBeans IDE 12+                                    │
│  🗄️ MySQL Server 8.0+                                   │
│  📚 Librería iText 5.x.x                                │
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│  ⚙️ HARDWARE MÍNIMO                                     │
├─────────────────────────────────────────────────────────┤
│  💻 Sistema: Windows 10/11, Linux, macOS               │
│  🧠 RAM: 2 GB (Recomendado 4 GB)                       │
│  💾 Disco: 200 MB libres                                │
│  🖥️ Pantalla: 1366x768 o superior                      │
└─────────────────────────────────────────────────────────┘
```

</div>

---

## 🚀 Instalación

### 📥 Paso 1: Clonar el Repositorio

```bash
git clone https://github.com/tu-usuario/Antoneth.git
cd Antoneth
```

### 🗄️ Paso 2: Configurar Base de Datos

```sql
-- Crear la base de datos
CREATE DATABASE antoneth_db;

-- Importar la estructura (desde terminal)
mysql -u root -p antoneth_db < database/antoneth_db.sql
```

### 🔧 Paso 3: Configurar Conexión

Edita `src/config/Conexion.java`:

```java
private final String URL = "jdbc:mysql://localhost:3306/antoneth_db";
private final String USER = "root";
private final String PASSWORD = "tu_contraseña";
```

### 📚 Paso 4: Agregar Librerías

```
NetBeans → Libraries → Add JAR/Folder → iText-5.x.x.jar
```

### ▶️ Paso 5: Ejecutar

```
Presiona F6  o  Click en ▶️ Run Project
```

---

## 💡 Guía de Uso

<div align="center">

### 🔑 Credenciales de Acceso

```
┌──────────────────────────────┐
│  Usuario: admin              │
│  Contraseña: admin123        │
└──────────────────────────────┘
```

> ⚠️ **Importante:** Cambia estas credenciales después del primer inicio

</div>

### 📖 Manual Rápido

```
1️⃣  Inicia sesión con tus credenciales de administrador

2️⃣  Selecciona el módulo desde el panel principal:
    • 📦 Productos → Gestiona tu inventario
    • 💰 Ventas → Registra transacciones
    • 📊 Reportes → Consulta estadísticas
    • 👤 Usuarios → Administra el sistema

3️⃣  Realiza las operaciones necesarias:
    ✓ Agregar    ✓ Editar    ✓ Consultar    ✓ Eliminar

4️⃣  Los cambios se guardan automáticamente en MySQL

5️⃣  Genera facturas PDF desde el módulo de ventas

6️⃣  Visualiza reportes actualizados en tiempo real

7️⃣  Cierra sesión al terminar para proteger el acceso
```

---

## 📊 Módulos del Sistema

<div align="center">

```
╔═══════════════════════════════════════════════════════════════╗
║                     MÓDULOS ANTONETH                          ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║  🔐 LOGIN          │  📦 PRODUCTOS      │  💰 VENTAS         ║
║  ─────────────────────────────────────────────────────────   ║
║  • Autenticación   │  • Agregar items   │  • Nueva venta     ║
║  • Validación      │  • Editar datos    │  • Calcular total  ║
║  • Sesión segura   │  • Eliminar        │  • Generar PDF     ║
║                    │  • Buscar          │  • Historial       ║
║                    │  • Stock control   │                    ║
║                                                               ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║  📊 REPORTES       │  👤 USUARIOS       │  ⚙️ SISTEMA        ║
║  ─────────────────────────────────────────────────────────   ║
║  • Ventas diarias  │  • Perfiles        │  • Configuración   ║
║  • Inventario      │  • Permisos        │  • Respaldos       ║
║  • Estadísticas    │  • Seguridad       │  • Logs            ║
║  • Exportar        │  • Admin panel     │  • Ayuda           ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

</div>

---

## 🗺️ Roadmap

<div align="center">

### Evolución del Proyecto

</div>

| Estado | Versión | Características |
|:------:|:--------|:----------------|
| ✅ | **v1.0** | Sistema base con CRUD, ventas y reportes |
| ✅ | **v1.1** | Generación de facturas PDF con iText |
| ✅ | **v1.2** | Sistema de autenticación y sesiones |
| 🚧 | **v2.0** | Dashboard con gráficas estadísticas |
| 🚧 | **v2.1** | Respaldo automático de base de datos |
| 📋 | **v2.2** | Multi-usuario con roles diferenciados |
| 📋 | **v3.0** | Notificaciones y alertas de stock |
| 📋 | **v3.1** | Exportación a Excel y Word |
| 🔮 | **v4.0** | Versión web responsive |
| 🔮 | **v4.1** | API REST para integraciones |

```
Leyenda:  ✅ Completado  |  🚧 En desarrollo  |  📋 Planificado  |  🔮 Futuro
```

---

## 🤝 Contribuciones

<div align="center">

### ¡Tu aporte es bienvenido!

```
╔══════════════════════════════════════════════════════╗
║  💡 ¿Tienes una idea? ¡Compártela!                  ║
║  🐛 ¿Encontraste un bug? ¡Repórtalo!                ║
║  🔧 ¿Quieres mejorar el código? ¡Contribuye!        ║
╚══════════════════════════════════════════════════════╝
```

</div>

### 📝 Proceso de Contribución

```bash
# 1️⃣ Fork el repositorio
# 2️⃣ Crea tu rama
git checkout -b feature/MiNuevaCaracteristica

# 3️⃣ Realiza tus cambios
git add .
git commit -m "✨ Agrega nueva característica increíble"

# 4️⃣ Push a tu rama
git push origin feature/MiNuevaCaracteristica

# 5️⃣ Abre un Pull Request
```

### ✅ Directrices

- 📌 Sigue las convenciones de código Java
- 📝 Documenta tus cambios claramente
- 🧪 Prueba todo antes de enviar
- 💬 Describe el problema que resuelves

---

## 📄 Licencia

<div align="center">

```
┌────────────────────────────────────────────┐
│                                            │
│            📜 LICENCIA MIT                 │
│                                            │
│  ✓ Uso comercial permitido                │
│  ✓ Modificación permitida                 │
│  ✓ Distribución permitida                 │
│  ✓ Uso privado permitido                  │
│                                            │
│  ⚠️ Sin garantía                           │
│  ⚠️ El autor no es responsable            │
│                                            │
└────────────────────────────────────────────┘
```

Ver archivo **LICENSE** para más detalles

</div>

---

## 👩‍💻 Autora

<div align="center">

```
╔════════════════════════════════════════════════╗
║                                                ║
║            👩‍💻 DANIELA NINA                    ║
║                                                ║
║  📧 daninimin08@gmail.com                     ║
║  📍 Satélite Norte, Bolivia                   ║
║  💼 Desarrolladora Java                       ║
║  🎓 Proyecto Académico y Profesional          ║
║                                                ║
╚════════════════════════════════════════════════╝
```

</div>

---

## 🙏 Agradecimientos

Este proyecto fue posible gracias a:

```
🏪  Librería Antoneth
    Por la confianza depositada en este proyecto

👨‍🏫  Mentores y Docentes
    Por la guía durante todo el proceso de desarrollo

👥  Comunidad Java
    Por los recursos y documentación invaluable

💻  Desarrolladores Open Source
    Por las herramientas que hacen esto posible
```

---

<div align="center">

## ⭐ Apoyo al Proyecto

```
╔════════════════════════════════════════════════════════╗
║                                                        ║
║  Si este proyecto te fue útil, considera:             ║
║                                                        ║
║  ⭐ Darle una estrella en GitHub                      ║
║  🐛 Reportar issues si encuentras problemas           ║
║  💡 Sugerir mejoras y nuevas características          ║
║  🤝 Contribuir con código                             ║
║  📢 Compartirlo con otros desarrolladores             ║
║                                                        ║
╚════════════════════════════════════════════════════════╝
```

### 💖 Hecho con dedicación y ☕ por Daniela Nina

```
┌─────────────────────────────────────┐
│  ¿Preguntas? ¿Sugerencias?         │
│  ¡Abre un issue o contáctame!      │
└─────────────────────────────────────┘
```

**[⬆ Volver al inicio](#-antoneth-)**

---

</div>
