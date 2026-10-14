# Control de Usuarios — Naturisa

Pantalla para solicitar y controlar usuarios de AP1 (alta, edición de roles/sucursales y baja).

- **Creación de usuario**: busca por cédula; muestra si la persona está en RRHH, si ya tiene usuario en AP1, sus aplicaciones, roles y sucursales. Desde ahí se solicita el usuario, se edita o se da de baja.
- **Solicitudes**: los administradores aprueban/rechazan y marcan como ejecutadas después de hacer el cambio en AP1 → Seguridad. Cada solicitante solo ve las de sus campamentos.
- **Administradores**: lista de usuarios AP1 con rol de administrador en esta pantalla.

Publicada en: https://jparraga-naturisa.github.io/control-usuarios/

El backend son las rutas `/d1/usuarios/*` del worker `naturisa-proxy` (repo `reportes-naturisa`, carpeta `cloudflare-worker`); los datos de las solicitudes se guardan en Cloudflare D1 (`naturisa-db`, tablas `usuarios_solicitudes` y `usuarios_admins`).
