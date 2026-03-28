Esto es lo que tedemos de poner en la consola:

```javascript
allow pasting
```

Y luego todo esto:

```javascript
// 1. Forzar el video de YouTube al principio y bajar su calidad al mínimo
if (typeof player !== 'undefined') {
    player.seekTo(0, true);
    if (player.setPlaybackQuality) player.setPlaybackQuality('small'); // Fuerza calidad baja (240p)
}

// 2. Matar el audio para que deje de descargar
var a = document.getElementById('audio-player');
if (a) {
    a.pause();
    a.removeAttribute('src');
    a.load();
    a.play = function() { return Promise.resolve(); };
}

// 3. Detener el rastreador fantasma de Vimeo
if (typeof syncInterval !== 'undefined') {
    clearInterval(syncInterval);
}

console.log("¡Limpieza completada! Red y CPU liberadas.");
```
