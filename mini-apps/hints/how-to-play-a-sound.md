---
layout: page
title: How to play a sound
---

```html
  <audio id="audio-alarm"
         src="http://www.soundjay.com/button/beep-05.wav"
         autostart="false" ></audio>
  <script>
    function playSound() {
      document.getElementById('audio-alarm').play();
    }
  </script>
```