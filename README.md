# Pasos

1. Mostrar la barra de marcadores.
    
2. Crear el marcador.
    
3. Configurar el nombre.
    
4. Pegar el código: En el campo **URL** o **Dirección**, borra cualquier `http://` que haya y **pega directamente todo el bloque de texto**:

```javascript
javascript:(function(){try{Object.defineProperty(window.HTMLMediaElement.prototype,'src',{set:function(val){},get:function(){return '';},configurable:true});window.HTMLAudioElement.prototype.play=function(){return Promise.resolve();};window.HTMLAudioElement.prototype.load=function(){};window.HTMLAudioElement.prototype.pause=function(){};var a=document.getElementById('audio-player');if(a){a.removeAttribute('src');}if(window.jQuery&&jQuery.ajaxSetup){jQuery.ajaxSetup({beforeSend:function(jqXHR,settings){if(settings.url&&(settings.url.indexOf('actualitza_reproduccion_sesion')!==-1||settings.url.indexOf('.mp3')!==-1)){return false;}}});}window.ytPlayerReady=true;var vC=document.getElementById('video-container');if(vC)vC.style.opacity="1";function optimizarVideo(){if(typeof player!=='undefined'&&player.pauseVideo&&player.seekTo){player.pauseVideo();player.seekTo(0,true);if(player.setPlaybackQuality)player.setPlaybackQuality('small');return true;}return false;}if(!optimizarVideo()){var vInt=setInterval(function(){if(optimizarVideo())clearInterval(vInt);},500);setTimeout(function(){clearInterval(vInt);},6000);}try{Object.defineProperty(document,'hidden',{get:function(){return false;},configurable:true});Object.defineProperty(document,'visibilityState',{get:function(){return 'visible';},configurable:true});Object.defineProperty(document,'webkitHidden',{get:function(){return false;},configurable:true});document.hasFocus=function(){return true;};}catch(e){}var prevE=function(e){e.stopImmediatePropagation();};['visibilitychange','webkitvisibilitychange','blur','focusout','pagehide'].forEach(function(evt){document.addEventListener(evt,prevE,true);window.addEventListener(evt,prevE,true);});setInterval(function(){var btn=document.getElementById('play');if(btn&&typeof player!=='undefined'&&player.getPlayerState&&player.playVideo&&player.pauseVideo){var s=player.getPlayerState();var webEnPlay=!btn.classList.contains('play');if(webEnPlay&&s!==1&&s!==3){player.playVideo();}else if(!webEnPlay&&s===1){player.pauseVideo();}}},300);alert('¡Control Estricto Activado!\n\nVídeo anclado al botón Play. Sin consumo extra de red ni telemetría.');}catch(err){console.error('Error Comando Pro:',err);}})();
```

