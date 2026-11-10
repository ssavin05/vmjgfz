# Smart Hub 2.9.4 — retirada la pantalla “Qué se ve en la app”

Se eliminó completamente del panel administrador la pantalla que permitía decidir
qué módulos, espacios, plano o modelo 3D se mostraban.

Cambios:
- Ya no existe `/admin/apariencia`.
- Ya no aparece “Configuración” / “Qué se ve en la app” en los menús de administración.
- Se quitaron los controles de:
  - descuentos/promociones,
  - adornos/testimonios,
  - reseñas,
  - favoritos,
  - lista de espera,
  - tutorial,
  - chat,
  - asistente,
  - mapa,
  - cobro,
  - plano arquitectónico,
  - modelo GLB/GLTF,
  - espacios visibles en el catálogo.
- Los ajustes guardados por versiones anteriores en `co.ajustes` se eliminan e ignoran.
- El catálogo ya no puede ocultar espacios por un ajuste local del navegador.
- La configuración real queda fijada por el código y, cuando aplique, por `window.__APP_CONFIG__`.
