# Pasos

1. Mostrar la barra de marcadores.
    
2. Crear el marcador.
    
3. Configurar el nombre.
    
4. Pegar el código: En el campo **URL** o **Dirección**, borra cualquier `http://` que haya y **pega directamente todo el bloque de texto**:

```javascript
javascript:(function(){ if(typeof player!=='undefined'){player.seekTo(0,true); if(player.setPlaybackQuality)player.setPlaybackQuality('small');} var a=document.getElementById('audio-player'); if(a){a.pause();a.removeAttribute('src');a.load();a.play=function(){return Promise.resolve();};} if(typeof syncInterval!=='undefined')clearInterval(syncInterval); Object.defineProperty(document,'hidden',{get:function(){return false;}}); Object.defineProperty(document,'visibilityState',{get:function(){return 'visible';}}); document.addEventListener('visibilitychange',function(e){e.stopImmediatePropagation();},true); window.addEventListener('blur',function(){setTimeout(function(){if(typeof player!=='undefined'&&typeof player.playVideo==='function')player.playVideo();},100);}); alert('Video al inicio y red liberada.'); })();
```

