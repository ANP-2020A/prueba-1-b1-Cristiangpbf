# Prueba 1 - Bimestre 1

Desarrollar una API con Laravel que tenga en cuenta las siguientes entidades y atributos:

```
- users
  - id : bigint(20) unsigned
  - name : varchar(255)
  - email : varchar (255)
  - email_verified_at : timestamp
  - password : varchar(255)
  - remember_token : varchar(100)
  - created_at : timestamp
  - updated_at : timestamp
 
 
- products
  - id : bigint(20) unsigned
  - name : varchar(255)
  - code : varchar(80)
  - price : double
  - status : enum('active','deleted')
  - created_at : timestamp
  - updated_at : timestamp
  
  
- customers
  - id : bigint(20) unsigned
  - name : varchar(255)
  - lastname : varchar(255)
  - document : varchar(80)
  - created_at : timestamp
  - updated_at : timestamp

```

**NOTA:** para la columna `status` de product, los productos se insertan en `active` por defecto. Revisar la documentación: https://laravel.com/docs/6.x/migrations#creating-columns

## Tareas
  1. **(1)** Configuración de tablero de Github, cración y protección de las ramas `master` y `dev`.

  1. Creación de las siguientes tareas en el tablero (se debe trabajar con ramas para cada tarea creada).
      
      a. **(0.5)** Creación y configuración inicial del proyecto. **Usar la versión 6 de Laravel**

      b. **(0.5)** Creación de modelo y migración para products, customers, users

      c. **(2)** Creación de seeders para products, customers y users

      d. **(1)** Creación de rutas y controladores para products, customers y users

      e. **(2)** Autenticación con JWT

      f. **(3)** Protección de rutas. Crear las rutas de la manera correcta y protegerlas según la siguiente lista.
      
        * Rutas públicas
          * Lista de productos (todos)
          * Detalle de producto según el id
        * Rutas privadas (solo con autenticación)
          * Creación de producto
          * Actualización de producto según el id
          * Eliminar producto según el id. Esta no debería eliminar el producto de la base, solamente debe actualizar la columna `status` a `deleted`
          * Creación de customers
          * Lista de customers
          * Detalle de customers
          * Eliminación de customers

