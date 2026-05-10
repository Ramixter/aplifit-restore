# Pasos

1. Mostrar la barra de marcadores.
    
2. Crear el marcador.
    
3. Configurar el nombre.
    
4. Pegar el código: En el campo **URL** o **Dirección**, borra cualquier `http://` que haya y **pega directamente todo el bloque de texto**:

```javascript
javascript:(function(){try{Object.defineProperty(window.HTMLMediaElement.prototype,'src',{set:function(val){},get:function(){return '';},configurable:true});window.HTMLAudioElement.prototype.play=function(){return Promise.resolve();};window.HTMLAudioElement.prototype.load=function(){};window.HTMLAudioElement.prototype.pause=function(){};var a=document.getElementById('audio-player');if(a){a.removeAttribute('src');}if(window.jQuery&&jQuery.ajaxSetup){jQuery.ajaxSetup({beforeSend:function(jqXHR,settings){if(settings.url&&(settings.url.indexOf('actualitza_reproduccion_sesion')!==-1||settings.url.indexOf('.mp3')!==-1)){return false;}}});}window.ytPlayerReady=true;var vC=document.getElementById('video-container');if(vC)vC.style.opacity="1";function optimizarVideo(){if(typeof player!=='undefined'&&player.pauseVideo&&player.seekTo){player.pauseVideo();player.seekTo(0,true);if(player.setPlaybackQuality)player.setPlaybackQuality('small');return true;}return false;}if(!optimizarVideo()){var vInt=setInterval(function(){if(optimizarVideo())clearInterval(vInt);},500);setTimeout(function(){clearInterval(vInt);},6000);}try{Object.defineProperty(document,'hidden',{get:function(){return false;},configurable:true});Object.defineProperty(document,'visibilityState',{get:function(){return 'visible';},configurable:true});}catch(e){}document.addEventListener('visibilitychange',function(e){e.stopImmediatePropagation();},true);alert('¡Rendimiento Extremo Activado! \n\n✔️ Telemetría bloqueada desde la raíz\n✔️ Descarga de audio anulada al 100%\n✔️ Vídeo preparado a mínima calidad\n\nDale al botón Play de la web para iniciar.');}catch(err){console.error('Error Comando Pro:',err);}})();
```

