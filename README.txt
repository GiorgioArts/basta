¡BASTA! — Juego de letras (PWA offline) — v2
=============================================

index.html ES AUTOCONTENIDO: trae los 338 temas embebidos.
Funciona abriéndolo solo. sw.js, manifest.json e iconos solo se
necesitan para instalarlo como app y para el modo offline.

CÓMO SE JUEGA (v2)
  1. Toca JUGAR e ingresa de 2 a 6 jugadores (nombres editables).
  2. Aparece el tema y se anuncia a quién le toca (al azar, sin repetir
     hasta que todos jueguen; luego se vuelve a barajar).
  3. El jugador TOCA una letra del tablero (una sola activa; incluye Ñ).
     Si no caben todas, usa "Más letras" para pasar de página.
  4. Dice una palabra del tema con esa letra y pulsa el botón BASTA
     (redondo, colorido, 3D) antes de que acabe el cronómetro.
  5. La letra queda bloqueada, se reinicia el tiempo y le toca al
     siguiente jugador. Perder = NO pulsar BASTA a tiempo.
  6. Si se usan las 27 letras y nadie perdió -> segunda ronda con el
     mismo tema y la misma secuencia de jugadores.

PROBAR RÁPIDO
  Abre index.html en el navegador. El sonido arranca con el primer toque.

INSTALAR / OFFLINE (necesita servidor, no file://)
  Local:        python3 -m http.server 8080  -> http://localhost:8080
  GitHub Pages: sube todo a la raíz, activa Pages, abre la URL y en el
  celular elige "Agregar a pantalla de inicio". Rutas relativas (./).

EDITAR TEMAS
  Al inicio del <script> de index.html ("TEMAS EMBEBIDOS").
  Formato: ["texto","etiquetas"].  Dificultad: facil|medio|dificil.
  Audiencia: ninos|familiar|fiesta|creativo|adultos.

ACTUALIZAR APP YA INSTALADA
  Sube el número de versión en sw.js (CACHE = 'basta-v3').

CAMBIAR SONIDOS POR MP3 (opcional)
  Reemplaza el cuerpo de Snd.correct(), Snd.fail(), etc. (objeto Snd)
  por new Audio('archivo.mp3').play() y añade los .mp3 a ASSETS en sw.js.
