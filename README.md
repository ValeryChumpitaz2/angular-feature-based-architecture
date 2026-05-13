# 🚀 Angular Feature-Based Architecture

<p align="center">
  <img src="https://angular.io/assets/images/logos/angular/angular.svg" width="120">
</p>

<h1 align="center">
📦 Arquitectura Modular Profesional para Angular
</h1>

<p align="center">
Plantilla base orientada a proyectos modernos, escalables y mantenibles utilizando Angular.
</p>

---

# 📖 Descripción

Este repositorio implementa una arquitectura basada en funcionalidades (**Feature-Based Architecture**) siguiendo buenas prácticas modernas en desarrollo frontend con :contentReference[oaicite:0]{index=0}.

La finalidad de esta estructura es mantener proyectos:

- ✅ Escalables
- ✅ Ordenados
- ✅ Reutilizables
- ✅ Fáciles de mantener
- ✅ Profesionales
- ✅ Preparados para trabajo colaborativo

---

# 🏗️ Arquitectura General

```bash
src/
└── app/
    ├── core/
    ├── shared/
    ├── features/
    ├── app.routes.ts
    ├── app.config.ts
    └── app.component.ts
````

---

# 🧠 Estructura del Proyecto

# 📂 core/

Contiene lógica global reutilizable en toda la aplicación.

## 📌 Aquí va:

* 🔐 Autenticación
* 🛡️ Guards
* 🌐 Interceptors
* ⚙️ Servicios globales
* 🧩 Layouts
* 📦 Configuración general

```bash
core/
├── guards/
├── interceptors/
├── services/
├── layouts/
└── models/
```

---

# ♻️ shared/

Contiene elementos reutilizables por múltiples módulos.

## 📌 Aquí va:

* 🔘 Botones
* 📋 Tablas
* 🪄 Pipes
* 📌 Directivas
* 📦 Componentes reutilizables
* 🧰 Helpers y utilidades

```bash
shared/
├── components/
├── directives/
├── pipes/
├── interfaces/
└── utils/
```

---

# 🧩 features/

Cada carpeta representa un módulo funcional independiente.

## 📌 Ejemplos:

* 👤 auth
* 📦 products
* 💰 sales
* 🏭 production
* 🩺 diseases

```bash
features/
├── auth/
├── products/
├── sales/
└── production/
```

---

# 📁 Estructura Interna de una Feature

```bash
products/
├── pages/
├── components/
├── services/
├── interfaces/
└── products.routes.ts
```

---

# 📚 Explicación de Carpetas

| Carpeta       | Descripción                         |
| ------------- | ----------------------------------- |
| 📄 pages      | Vistas principales del módulo       |
| 🧩 components | Componentes internos reutilizables  |
| 🌐 services   | Lógica de negocio y consumo de APIs |
| 🧾 interfaces | Interfaces y tipado TypeScript      |
| 🛣️ routes    | Configuración de rutas del módulo   |

---

# ⚡ Diferencia Entre `core/services` y `feature/services`

| Tipo                  | Uso                              |
| --------------------- | -------------------------------- |
| 🌍 `core/services`    | Servicios globales reutilizables |
| 🧩 `feature/services` | Servicios exclusivos del módulo  |

---

## ✅ Ejemplo `core/services`

```bash
core/services/
├── auth.service.ts
├── notification.service.ts
└── storage.service.ts
```

### 📌 Se usan globalmente:

* login
* guards
* interceptors
* dashboard
* sesión

---

## ✅ Ejemplo `feature/services`

```bash
features/products/services/
├── product.service.ts
└── inventory.service.ts
```

### 📌 Solo pertenecen al módulo:

* productos
* inventario

---

# 🚀 Crear Proyecto Angular

## 1️⃣ Crear Proyecto

```bash
ng new angular-feature-based-architecture --standalone --routing --style=css
```

---

# 📂 Crear Estructura de Carpetas

## 🖥️ Windows PowerShell

```powershell
# CORE
New-Item -ItemType Directory -Force -Path src/app/core/guards
New-Item -ItemType Directory -Force -Path src/app/core/interceptors
New-Item -ItemType Directory -Force -Path src/app/core/services
New-Item -ItemType Directory -Force -Path src/app/core/layouts
New-Item -ItemType Directory -Force -Path src/app/core/models

# SHARED
New-Item -ItemType Directory -Force -Path src/app/shared/components
New-Item -ItemType Directory -Force -Path src/app/shared/directives
New-Item -ItemType Directory -Force -Path src/app/shared/pipes
New-Item -ItemType Directory -Force -Path src/app/shared/interfaces
New-Item -ItemType Directory -Force -Path src/app/shared/utils

# FEATURES
New-Item -ItemType Directory -Force -Path src/app/features/auth/pages
New-Item -ItemType Directory -Force -Path src/app/features/auth/components
New-Item -ItemType Directory -Force -Path src/app/features/auth/services
New-Item -ItemType Directory -Force -Path src/app/features/auth/interfaces
```

---

# 📄 Crear Archivos README Automáticos

Estos archivos sirven para:

* mantener carpetas visibles en GitHub,
* documentar cada carpeta,
* orientar al equipo de desarrollo.

---

## 🖥️ Windows PowerShell

```powershell
Set-Content src/app/core/services/README.md "# Core Services`n`nAquí van los servicios globales del sistema."

Set-Content src/app/shared/components/README.md "# Shared Components`n`nAquí van los componentes reutilizables."

Set-Content src/app/features/auth/services/README.md "# Auth Services`n`nAquí van los servicios del módulo auth."
```

---

# ⚡ Tecnologías Utilizadas

| Tecnología         | Uso                   |
| ------------------ | --------------------- |
| 🅰️ Angular        | Framework frontend    |
| 📘 TypeScript      | Tipado estático       |
| 🌐 RxJS            | Programación reactiva |
| 🛣️ Angular Router | Navegación            |
| 🎨 Tailwind o CSS    | Estilos modernos      |

---

# 🚀 Instalación del Proyecto

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/USUARIO/angular-feature-based-architecture.git
```

---

## 2️⃣ Instalar dependencias

```bash
npm install
```

---

## 3️⃣ Ejecutar aplicación

```bash
ng serve
```

---

# 🌍 Acceso Local

```bash
http://localhost:4200
```

---

# 📌 Buenas Prácticas

✅ Organizar por funcionalidades
✅ Mantener módulos independientes
✅ Reutilizar componentes compartidos
✅ Mantener servicios encapsulados
✅ Utilizar interfaces TypeScript
✅ Mantener `core` solo para lógica global
✅ Evitar carpetas globales gigantes

---

# 📈 Beneficios de esta Arquitectura

| Beneficio            | Resultado               |
| -------------------- | ----------------------- |
| 📈 Escalabilidad     | Fácil crecimiento       |
| 🛠️ Mantenimiento    | Código organizado       |
| 👥 Trabajo en equipo | Menos conflictos        |
| ♻️ Reutilización     | Componentes compartidos |
| 🧹 Limpieza          | Mejor lectura           |

---

# 👨‍💻 Recomendado Para

✅ Sistemas empresariales
✅ Proyectos académicos
✅ Equipos de desarrollo
✅ Aplicaciones escalables
✅ Arquitecturas modernas frontend

---

# 📚 Referencias

* Angular Official Documentation
* Angular Style Guide
* Feature-Based Architecture
* Clean Architecture Principles

---

# ⭐ Autor

Desarrollado por **Valery Chumpitaz** como plantilla base para proyectos Angular con arquitectura modular y escalable.

---

# 📄 Licencia

Este proyecto puede utilizarse con fines educativos y profesionales.


