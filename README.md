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

Modo completo:

```javascript
javascript:(function(){ if(typeof player!=='undefined'){player.seekTo(0,true); if(player.setPlaybackQuality)player.setPlaybackQuality('small');} var a=document.getElementById('audio-player'); if(a){a.pause();a.removeAttribute('src');a.load();a.play=function(){return Promise.resolve();};} if(typeof syncInterval!=='undefined')clearInterval(syncInterval); Object.defineProperty(document,'hidden',{get:function(){return false;}}); Object.defineProperty(document,'visibilityState',{get:function(){return 'visible';}}); document.addEventListener('visibilitychange',function(e){e.stopImmediatePropagation();},true); window.addEventListener('blur',function(){setTimeout(function(){if(typeof player!=='undefined'&&typeof player.playVideo==='function')player.playVideo();},100);}); alert('¡Modo Dios activado! Video al inicio, red liberada y anti-pausa activo.'); })();
```
