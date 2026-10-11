# El Renacer del Fénix · Inventario y caja (APK)

App Android para un puesto de comida rápida: inventario, ventas con método de pago
(Pago Móvil, Efectivo, Divisas, Débito, Otro), compras, cierre del día y reportes.
Funciona sin internet; los datos viven dentro del teléfono.

## Obtener el APK
1. Sube TODO este contenido a un repositorio **privado** de GitHub (incluida la carpeta oculta `.github`
   y tu archivo `debug.keystore` en la raíz).
2. Pestaña **Actions** → la compilación inicia sola (5 a 8 min). También puedes usar *Run workflow*.
3. Con el check verde abre la ejecución y descarga **renacer-fenix-apk** (Artifacts): dentro está `app-debug.apk`.
4. Instálalo en el teléfono (permite "origen desconocido").

## Actualizar sobre la versión anterior sin perder datos
Funciona solo si el APK se firma con **la misma** `debug.keystore` de siempre (archivo en la raíz del repo).
Si no la subes, el workflow crea una llave nueva (te la entrega como artifact para que la guardes) y Android
exigirá desinstalar la app anterior: **antes** haz Inicio → Ajustes → Respaldo → Exportar → Copiar.

## Respaldo
Inicio → Ajustes → Respaldo. "Copiar" y guarda el texto (WhatsApp a ti mismo, Notas). "Importar" lo restaura.

## Estructura
- `www/index.html`: toda la app (HTML, CSS y JS).
- `android-res/`: ícono y pantalla de inicio; se copian en cada compilación.
- `capacitor.config.json`, `package.json`: configuración de Capacitor.
- `.github/workflows/build-apk.yml`: compilación automática.
