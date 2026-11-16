# Puesta en producción con MySQL

1. Cree una base de datos con codificación UTF-8:

   ```sql
   CREATE DATABASE joyeria CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```

2. Copie `.env.example` como `.env` y coloque el host, usuario, contraseña y nombre de base de datos reales. No suba `.env` al repositorio.
3. Instale dependencias con `pip install -r requirements.txt`.
4. Inicie la aplicación. Con `DB_ENGINE=mysql`, el sistema crea automáticamente tablas, relaciones, índices y los datos iniciales del catálogo.

Para producción use HTTPS y mantenga `COOKIE_SECURE=true`. Cree un usuario MySQL exclusivo para la aplicación con permisos solo sobre la base `joyeria`; no use el usuario `root`.
