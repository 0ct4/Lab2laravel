# 🧪 Laboratorio [Laboratorio 2 Laravel]

## 🎯 Objetivo del Laboratorio

Este laboratorio tiene como **objetivo principal** identificar la estructura básica de un proyecto en Laravel, comprender la organización del framework bajo el patrón Modelo–Vista–Controlador (MVC) y reconocer la
importancia de esta arquitectura en el desarrollo de aplicaciones web modernas.

---

## 💻 Arquitectura y Estructura (Patrón MVC)

Laravel se basa en el patrón de arquitectura **Modelo-Vista-Controlador (MVC)**, que organiza el código en torno a tres componentes principales para mejorar la modularidad y el mantenimiento:

| Carpeta | Componente MVC | Función Principal |
| :--- | :--- | :--- |
| `app/Models` | **Modelo** | Interactúa directamente con la base de datos (tablas). Define la lógica de negocio y las relaciones. |
| `app/Http/Controllers` | **Controlador** | Actúa como intermediario. Recibe las peticiones del usuario (Rutas), llama a la lógica del Modelo y selecciona la Vista a mostrar. |
| `resources/views` | **Vista** | Contiene el código de la interfaz de usuario (HTML/Blade). Es lo que el usuario final ve en el navegador. |
| `routes/web.php` | **Rutas** | Define los puntos de acceso de la aplicación (URLs). Dirige las peticiones a los Controladores correspondientes. |

---

## 🛠️ Requisitos del Ecosistema

Para ejecutar este laboratorio localmente, es necesario tener configurado el siguiente entorno de desarrollo.

| Prerrequisito | Versión Requerida | Estado |
| :--- | :--- | :--- |
| **PHP** | 8.0 o superior | ✔️ |
| **Composer** | Última versión estable | ✔️ |
| **Instalador de Laravel** | (Instalado globalmente o proyecto creado con `composer create-project`) | ✔️ |
| **Entorno de Servidor Web Local** | XAMPP, WampServer, Laragon, o similar | [Utilizé WampServer] |
| **Servidor Web** | Apache o Nginx | [Utilizé Apache] |
| **Base de Datos** | MySQL/MariaDB funcionando | ✔️ |
| **Editor de Código** | Visual Studio Code o Sublime Text| [utilice Visual Studio Code] |
| **Sistema Operativo** | [Windows 11] | |

---

## 🚀 Proceso de Instalación y Configuración

A continuación se documenta la secuencia de comandos utilizados para inicializar el proyecto, instalar dependencias y configurar la autenticación.

### 1. Inicialización y Dependencias

| Comando | Descripción |
| :--- | :--- |
| `composer install` | Instala todas las dependencias del proyecto definidas en `composer.json`. |
| `cp .env.example .env` | Crea el archivo de configuración `.env` a partir de la plantilla. |
| `php artisan key:generate` | Genera la clave de aplicación, esencial para la seguridad de Laravel. |

### 2. Instalación del Paquete de Autenticación

Para la funcionalidad de autenticación se utilizó el paquete **[Laravel/ui]**.

**Comandos utilizados para la Autenticación (Laravel/ui):**

```bash
composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev 
# Este último paso compila los assets (CSS/JS) necesarios para que la autenticación se vea correctamente.

## 📂 Migraciones y Base de Datos

### Configuración del entorno `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_base_de_datos
DB_USERNAME=usuario
DB_PASSWORD=contraseña
```

### Comandos utilizados para migraciones

```bash
php artisan migrate
```

### Respaldo de la base de datos

Para generar un backup:

```bash
mysqldump -u usuario -p nombre_base_de_datos > database/backups/backup_lab2.sql
```

---

## 🖼️ Resultado Visible

![Capturas de pantalla del laboratorio](C:/wamp64/www/lab2laravel/imágenes/laravel (1))

![Capturas de pantalla del laboratorio](C:/wamp64/www/lab2laravel/imágenes/laravel (2))

---

## ⚠️ Dificultades y Soluciones

- **Error de migración:** Path no encontrado. Solución: borrar y volver a realizar la migración.
- **Configuración del `.env`:** Error de conexión. Solución: Borrar la caché.
- **Dependencias:** Problemas con Composer. Solución: Ejecutar `composer install` y actualizar.

---

## 📚 Referencias

- [Documentación oficial de Laravel](https://laravel.com/docs/10.x)
- [Tutorial instalación de Laravel](https://www.youtube.com/watch?v=GZMGyYNq3hE)
- [Guía de Blade Templates](https://laravel.com/docs/10.x/blade)

---

## 📝 Footer

> Este laboratorio ha sido desarrollado por el estudiante de la Universidad Tecnológica de Panamá:  
> **Nombre:** Octavio Frauca  
> **Correo:** octavio.frauca@utp.ac.pa  
> **Curso:** Ingeniería Web  
> **Instructor del Laboratorio:** Irina Fong.

---

## 📅 Fecha de Ejecución

**Fecha:** 28 de septiembre de 2025
