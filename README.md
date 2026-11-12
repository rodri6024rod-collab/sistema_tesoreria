# Sistema de Tesorería – IESTP Utcubamba (HTML/CSS/JavaScript)

## Publicar en GitHub Pages
1. Crea un repositorio en GitHub.
2. Sube `index.html`, `app.html` y la carpeta `assets`.
3. En Settings → Pages, selecciona Deploy from a branch, rama `main` y carpeta `/ (root)`.
4. Abre la URL publicada.

## Accesos de demostración
- Administrador: `admin` / `123`
- Tesorero: `tesorero` / `321`

## Funciones incluidas
- Inicio de sesión demostrativo y perfiles administrador/tesorero.
- Panel de ingresos confirmados, egresos confirmados, saldo y cantidad de movimientos.
- Registro de ingresos y egresos como pendientes.
- Confirmación de movimientos y anulación con motivo (administrador).
- Registro y búsqueda de comprobantes con adjuntos de hasta 8 MB.
- Gestión básica de usuarios (administrador).
- Auditoría local y exportación CSV de movimientos.
- Diseño adaptable a móviles.

## MUY IMPORTANTE: límites de esta versión
Esta conversión es una **demostración frontend estática**. GitHub Pages solo publica archivos; no ejecuta PHP ni proporciona MySQL.
Los datos se guardan en `localStorage` del navegador y los archivos adjuntos como datos locales. Por tanto:
- Los datos solo existen en ese navegador/dispositivo; no se sincronizan entre administrador y tesorero.
- Borrar los datos del navegador puede eliminar los registros.
- El inicio de sesión y las contraseñas de demostración están en JavaScript y **NO son seguros**.
- No usar para dinero real, datos personales ni documentos institucionales confidenciales.

## Para convertirla en sistema real
Conecta el frontend a un backend, por ejemplo Supabase (Auth + PostgreSQL + Storage) o un servidor propio. Deben configurarse políticas RLS, roles/permisos, almacenamiento privado y validación en servidor. No publiques claves secretas ni credenciales de base de datos en GitHub. Puedo preparar esa integración cuando tengas el proyecto de Supabase creado.

## Nota
La base original también describe cierres de caja y auditoría; el SQL de origen aclara que bancos/conciliación, presupuesto, proveedores, cierres operativos y reportes descargables avanzados todavía requieren desarrollo. Esta versión no los presenta como funciones terminadas.
