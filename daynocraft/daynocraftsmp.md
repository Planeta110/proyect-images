# Guía Oficial de Mecánicas - Daynocraft SMP

Bienvenido a la wiki del servidor. Aquí encontrarás toda la información detallada sobre el funcionamiento del sistema de vida, la economía de fragmentos y las fronteras de nuestro mundo.

---

## ❤️ Sistema de Corazones

La supervivencia en este servidor requiere que protejas tu vida por encima de todo. Nuestro sistema penaliza la muerte y recompensa el combate.

* **Pérdida por Muerte:** Cada vez que mueres por cualquier motivo (entornos, monstruos o caídas), pierdes **1 corazón**.
* **Robo de Corazones:** Si eliminas a otro jugador en combate PvP, le robarás automáticamente **1 corazón**, el cual se sumará a tu barra de vida.
* **Límite Máximo:** Puedes acumular un máximo de **30 corazones** (300 puntos de vida).
* **Eliminación y Baneo Temporal:** Si pierdes todos tus corazones y tu contador llega a cero, serás sancionado con un **baneo temporal de 3 días**.
* **Sistema de Reanimación (Revividores):** Puedes eludir el baneo temporal o resucitar a un amigo que se haya quedado sin vidas utilizando un **Revividor**. Este objeto especial se puede adquirir directamente a través de nuestra tienda oficial: [store.daynocraft.com](https://store.daynocraft.com).

---

## 💎 Sistema de Fragmentos

Los **Fragmentos** son una moneda especial y exclusiva dentro del servidor que te permite acceder a objetos avanzados. Puedes gestionar y gastar tus fragmentos ejecutando el siguiente comando en el chat del juego:

> `/fragmentos`

Para hacer la **conversión** de **Fragmentos** tendrás que poner el siguiente comando en el chat del juego:
> `/cf`

### ¿Cómo conseguir Fragmentos?

Dispones de dos vías diferentes para acumular esta divisa especial:

1. **Tienda Oficial:** Compra paquetes de fragmentos de forma directa en nuestra plataforma web: [store.daynocraft.com](https://store.daynocraft.com).
2. **Conversión Económica:** Intercambia el dinero virtual estándar que consigues jugando por esta moneda premium. La tasa de conversión fija es:
   * 🪙 **100 monedas normales** = 💎 **1 Fragmento**


---

# 🖼️ Cómo usar ImageFrame

Bienvenidos. Esta es la guía definitiva para usar el plugin **ImageFrame** en el servidor. Este sistema permite colocar imágenes, fotos y GIFs desde internet directamente en los marcos de ítems (Item Frames) del juego. 

Lean detenidamente. No se dará soporte en el chat a dudas sobre comandos que ya están explicados aquí.

## 📌 Requisitos Previos

Antes de intentar colocar una imagen, asegúrate de cumplir con esto:
* **Mapas vacíos:** Necesitas tener **mapas vacíos (Empty Maps)** en tu inventario. Para crear las imágenes, el plugin consumirá estos mapas físicos.
* **Enlaces directos (URLs):** La imagen que quieras usar debe estar alojada en internet (Imgur, Discord, etc.) y debes usar un **enlace directo** que termine en la extensión del archivo (`.png`, `.jpg`, `.jpeg`, o `.gif`). Los enlaces a galerías o páginas web enteras no funcionarán.

---

## 🛠️ Herramienta de Selección Inteligente (El Método Recomendado)

La forma más eficiente y menos propensa a errores para colocar una imagen que ocupa varios bloques es usando la herramienta de selección.

1. Coloca los Marcos de Ítems (Item Frames) en la pared formando el tamaño exacto que quieras para tu imagen (por ejemplo, 2x2, 3x2).
2. Mira hacia esos marcos y escribe el comando:
   `/imageframe select`
3. Haz clic (izquierdo o derecho) en los marcos para seleccionarlos. El sistema calculará el espacio por ti.

---

## 🖼️ Creación de Imágenes

Una vez tengas tu URL y tus mapas listos, utiliza los siguientes comandos. *(Nota: Los parámetros entre `< >` son obligatorios, los que están entre `[ ]` son opcionales).*

* **Creación en Selección (El más fácil):**
  `/imageframe create <nombre_imagen> <url> selection`
  *Crea la imagen y la coloca **directamente** en los marcos que seleccionaste previamente con el comando de selección. Usa este método para evitar problemas.*

* **Creación Básica:**
  `/imageframe create <nombre_imagen> <url> <ancho> <alto>`
  *Crea una imagen especificando cuántos marcos de ancho y alto ocupará. Te entregará los mapas cortados en el inventario para que los coloquenses manualmente en la pared.*

* **Creación de Ítem Combinado:**
  `/imageframe create <nombre_imagen> <url> <ancho> <alto> combined`
  *Te entrega la imagen gigante condensada en un único ítem en el inventario. Al colocar este ítem en la pared, la imagen completa se despliega automáticamente (si hay suficiente espacio físico).*

---

## ⚙️ Gestión de tus Imágenes

Todas las imágenes que creas quedan guardadas a tu nombre. Si pierdes los mapas o quieres hacer modificaciones, usa estas herramientas:

* **Obtener una copia:** `/imageframe get <nombre_imagen>` (Te devuelve los mapas de una imagen que ya habías creado).
* **Lista de tus creaciones:** `/imageframe list` (Muestra todas las imágenes registradas a tu nombre).
* **Renombrar:** `/imageframe rename <nombre_antiguo> <nombre_nuevo>`
* **Refrescar/Actualizar:** `/imageframe refresh [nombre]` (Si actualizaste la imagen en el enlace original pero mantuviste la misma URL, esto fuerza al servidor a descargar la versión nueva).
* **Eliminar del sistema:** `/imageframe delete <nombre_imagen>` (Borra permanentemente la imagen de tus registros).

---

## 🎬 GIFs y Animaciones

El servidor soporta GIFs animados, pero consumen rendimiento. Úsalos con moderación.

* **Pausar/Reanudar animación:** `/imageframe playback <nombre_imagen> pause`
* **Saltar a un segundo específico:** `/imageframe playback <nombre_imagen> jumpto <segundos>`

---

## 📍 Marcadores en Imágenes (Map Markers)

Puedes añadir iconos (como los marcadores de los mapas del tesoro de Minecraft Vanilla) sobre tus cuadros para señalar puntos de interés en mapas personalizados.

* **Añadir marcador:** `/imageframe marker add [texto_opcional]` (Añade un marcador en el mapa que tienes en la mano).
* **Eliminar el último marcador:** `/imageframe marker remove`
* **Limpiar todos los marcadores:** `/imageframe marker clear`

---

### ⚠️ Reglas y Rendimiento

1. **No satures el cliente:** Las imágenes gigantes (ej. 10x10 marcos) o los GIFs muy pesados generan caída de FPS para ti y los jugadores cercanos. Usa el sentido común con los tamaños.
2. **Protección de Terreno:** El plugin respeta las zonas protegidas. No intentes colocar o superponer imágenes en terrenos de otros jugadores si no tienes permisos.
3. **Contenido Inapropiado:** Las imágenes NSFW, ilegales o que rompan las normas del servidor resultarán en la eliminación total de tus marcos y un ban innegociable.