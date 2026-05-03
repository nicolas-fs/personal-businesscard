# 🔳 QR Projects Hub – Tu portafolio, en una tarjeta

![Next.js](https://img.shields.io/badge/Next.js-15+-black?logo=nextdotjs)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6?logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4+-06B6D4?logo=tailwindcss)
![License MIT](https://img.shields.io/badge/License-MIT-green)
[![Vercel](https://img.shields.io/badge/Deploy%20con%20Vercel-gratis-black?logo=vercel)](https://vercel.com)

**De un código QR físico a una landing individual con tabla comparativa persuasiva para cada uno de tus proyectos o servicios.**

En lugar de llevar a tus clientes a un simple WhatsApp, llévalos a un dashboard profesional que les muestra por qué deben trabajar contigo.

## 🎯 ¿Qué problema resuelve?

Como desarrollador o profesional con múltiples especializaciones, necesitas mostrar diferentes proyectos a diferentes clientes sin tener que preparar una presentación cada vez.  
**QR Projects Hub** te permite:

- Tener **una sola tarjeta física** con un código QR base.
- Que ese QR lleve al cliente **automáticamente al proyecto adecuado** según el sector (turismo, fintech, e‑commerce, etc.).
- Mostrar una **tabla comparativa al estilo Tapstar**, donde resaltas tus ventajas frente a la competencia.
- Gestionar todo desde un panel de administración sin tocar código.

## ✨ Características principales

- 🧭 **QR dinámico**: un único enlace base redirige al proyecto correcto mediante parámetros (`/p/ecochain-nexus`).
- 📊 **Tabla comparativa interactiva**: cada proyecto se presenta con una tabla de características, precios, competidores y una recomendación final persuasiva.
- 🎨 **Diseño responsive y moderno**: construido con Next.js, TypeScript y Tailwind CSS, listo para móviles.
- 🛠 **Dashboard de administración**: ruta protegida (`/admin`) donde puedes editar textos, precios y competidores sin modificar código.
- 🖨 **Tarjeta física lista para imprimir**: exporta un PDF en formato 85×55 mm con el código QR y los datos del proyecto.
- 🔒 **Seguridad integrada**: helmet, CSP, CORS restrictivo, ruta admin protegida con token.
- 🚀 **Despliegue gratuito en Vercel**: la aplicación funciona completamente sin backend costoso, los datos se cargan desde archivos JSON.

## 📸 Demostración visual

| Landing de proyecto | Panel de administración |
|---------------------|--------------------------|
| ![landing](docs/landing.png) | ![admin](docs/admin.png) |

*Agrega tus propias capturas en la carpeta `docs/`*

## 🧰 Stack tecnológico

**Frontend**
- [Next.js 15](https://nextjs.org/) (App Router)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [QRCode.react](https://www.npmjs.com/package/qrcode.react) (generación de QR)

**Backend (opcional)**
- [Next.js API Routes](https://nextjs.org/docs/app/building-your-application/routing/route-handlers)
- [Prisma](https://www.prisma.io/) + PostgreSQL (si activas persistencia)

**Despliegue**
- [Vercel](https://vercel.com/) (gratis)
- [Supabase](https://supabase.com/) (base de datos gratuita si se necesita)

## 📂 Estructura del proyecto
qr-projects-hub/
├── app/
│ ├── page.tsx # Landing genérica
│ ├── layout.tsx # Layout principal
│ ├── admin/
│ │ └── page.tsx # Dashboard protegido
│ └── p/
│ └── [id]/
│ └── page.tsx # Landing individual del proyecto
├── components/
│ ├── ComparativaTable.tsx # Tabla comparativa reutilizable
│ ├── ProjectQR.tsx # Componente de QR
│ ├── AdminPanel.tsx # Formulario de edición
│ └── TarjetaPDF.tsx # Exportación a PDF
├── data/
│ └── projects.json # Datos de los proyectos (8 ejemplos incluidos)
├── lib/
│ ├── projects.ts # Funciones de acceso a datos
│ └── security.ts # Middleware de seguridad
├── public/
│ └── qrcodes/ # QR pregenerados (opcional)
├── styles/
│ └── globals.css
├── .env.example
├── package.json
└── README.md

text

## ⚙️ Instalación y puesta en marcha

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/tuusuario/qr-projects-hub.git
   cd qr-projects-hub
