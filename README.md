# Bagisto
TiendaBagisto
# Práctica Final Bagisto: Instalación, Configuración y Publicación en GitHub

## 🔧 1. Configuración Inicial del Proyecto

### Jira

* Proyecto creado en Jira con nombre **"Tienda Bagisto"**.
* Tareas definidas:

  * Instalación entorno
  * Configuración de base de datos
  * Migraciones y seeding
  * Creación de productos
  * Comprobación en frontend
  * Documentación

### Repositorio GitHub

* Crear nuevo repositorio: `tienda-bagisto`
* Inicializar Git:

```bash
cd ~/Desktop/TiendaBagisto
git init
git remote add origin https://github.com/usuario/tienda-bagisto.git
```

* Crear `.gitignore` para excluir `vendor/`, `.env`, `node_modules/`, `storage/*.log`
* Primer commit:

```bash
git add .
git commit -m "Inicialización del proyecto Bagisto"
git push -u origin master
```

## 📄 2. Configuración de Entorno

* Clonado de proyecto Bagisto o descarga desde su web oficial
* Instalación de dependencias:

```bash
composer install
npm install
npm run dev
```

* Copiar archivo `.env.example` a `.env` y configurar:

```
APP_URL=http://localhost:8000
DB_DATABASE=Tienda_Bagisto
DB_USERNAME=bagisto_user
DB_PASSWORD=tu_clave_segura
APP_LOCALE=es
```

* Generar clave:

```bash
php artisan key:generate
```

## ♻️ 3. Migraciones y Seeders

```bash
php artisan migrate
php artisan db:seed
```

* **Captura 1**: `ejercicio_1_migraciones_seeders.png`

## 🚀 4. Lanzamiento del servidor

```bash
php artisan serve
```

* Acceder a `http://localhost:8000`
* **Captura 2**: `ejercicio_2_pagina_principal.png`

## 📅 5. Acceso a Panel de Administración

* URL: `http://localhost:8000/admin`
* Credenciales por defecto o configuradas:

  * Email: `admin@example.com`
  * Password: `admin123`
* **Captura 3**: `ejercicio_3_panel_admin.png`

## 🛒 6. Creación de Producto

* Ir a **Catalog > Products > Add Product**
* Tipo: Simple
* SKU: `CAM-HIS-001`
* Product Number: `PROD-001`
* Nombre: Camiseta Histórica
* Precio: 49.99
* Stock: 10
* Visible Individualmente: Sí
* Imagen cargada
* Asignar a categoría "Root"
* Asignar al canal "Default"
* **Captura 4**: `ejercicio_4_crear_producto.png`

## 🛎 7. Configuración de Impuestos

* Settings > Taxes > Tax Rates > Add:

  * Identifier: IVA 21%
  * Rate: 21
  * Country: Spain
  * State: \*
* Settings > Taxes > Tax Categories > Add:

  * Name: IVA 21%
  * Asignar la regla creada
* Editar producto y asignar la categoría de impuesto
* **Captura 5**: `ejercicio_5_producto_impuesto.png`

## 📰 8. Visualización en la Tienda

* Acceder a `http://localhost:8000`
* Buscar el producto creado
* Verificar imagen, precio e impuestos aplicados
* **Captura 6**: `ejercicio_6_producto_en_tienda.png`

## 🗋 9. Documentación y Entrega

* Crear documento PDF con los pasos realizados y capturas
* Publicar código en GitHub:

```bash
git add .
git commit -m "Producto creado y visible en tienda"
git push
```

* Opcional: grabar vídeo demostrativo navegando por el admin y la tienda

## ✅ Práctica Completada

* Revisión final y comprobación de requisitos del profesor
* Enlace al repo: `https://github.com/usuario/tienda-bagisto`
* Subida a Moodle o entrega según instrucciones
