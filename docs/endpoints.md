# Documentación de la API - Plataforma de Cosmetología

## 1. Autenticación y Cuentas de Usuario

* **`POST /api/auth/registro`**
  * **Descripción:** Crea una nueva cuenta de usuario.
  * **Cuerpo de la petición:** Nombre, correo, contraseña, teléfono.

* **`POST /api/auth/login`**
  * **Descripción:** Inicia sesión y devuelve el token de autenticación.
  * **Cuerpo de la petición:** Correo y contraseña.

* **`GET /api/usuarios/perfil`**
  * **Descripción:** Obtiene los datos del usuario autenticado.
  * **Requiere:** Token de sesión.

* **`PUT /api/usuarios/perfil`**
  * **Descripción:** Actualiza la información personal del usuario.
  * **Requiere:** Token de sesión.

---

## 2. Catálogo de Productos (Público)

* **`GET /api/productos`**
  * **Descripción:** Obtiene la lista completa de productos. Permite filtros (ej. `?categoria=facial`).

* **`GET /api/productos/{id}`**
  * **Descripción:** Obtiene la información detallada de un producto específico mediante su ID.

---

## 3. Catálogo de Servicios (Público)

* **`GET /api/servicios`**
  * **Descripción:** Obtiene la lista completa de servicios y tratamientos disponibles.

* **`GET /api/servicios/{id}`**
  * **Descripción:** Obtiene la información detallada de un servicio específico mediante su ID.

---

## 4. Configuración y Redes Sociales

* **`GET /api/configuracion/redes-sociales`**
  * **Descripción:** Obtiene los enlaces a las redes sociales oficiales de la cosmetóloga.

---

## 5. Administración (Solo para la Cosmetóloga)
*Nota: Todos estos endpoints requieren permisos de administrador.*

### Gestión de Productos
* **`POST /api/admin/productos`**
  * **Descripción:** Crea un nuevo producto en el catálogo.
* **`PUT /api/admin/productos/{id}`**
  * **Descripción:** Actualiza los datos de un producto existente.
* **`DELETE /api/admin/productos/{id}`**
  * **Descripción:** Elimina u oculta un producto del catálogo.

### Gestión de Servicios
* **`POST /api/admin/servicios`**
  * **Descripción:** Crea un nuevo servicio o tratamiento.
* **`PUT /api/admin/servicios/{id}`**
  * **Descripción:** Actualiza los datos de un servicio existente.
* **`DELETE /api/admin/servicios/{id}`**
  * **Descripción:** Elimina un servicio del catálogo.

  [⬅️ Anterior: Inicio](../README.md) | [Siguiente: Arquitectura del Sistema ➡️](arquitectura.md)