### JavaScript only is not the web 

Note:
So, we only took care of the JS.
Compile to the web truly.

---

Chack'n Pop for NES (Famicom)<br>
(Japanese version)

![Chack'n Pop for NES (Japanese version)](img/chack-n-pop-j-nes.png)

---

#### Video game sprites

![Ghosts from Pacman](img/pac-man-sprites.png)

![Ghosts from Pacman](img/ghost-sprite.png)

Note:
Video game console store sprites and palettes separately.
It allows game developers to reuse sprite and just change the palette.
Think ghost sprites in Pacman: same sprite, different palettes.

---

#### Extract the sprites

![Sprites from Chack'n Pop for NES (Japanese version)](img/chack-n-pop-sprites-0.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/chack-n-pop-sprites-1.png)

---

#### Extract the palettes

<style>
  div.pal {width: 2rem; height: 2rem; float: left;}
  div.container {margin: 2%; width: 46%; float: left;}
</style>
<div class="container">
  <div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(247, 180, 0);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(34, 14, 220);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(176, 255, 255);"></div><div class="pal" style="background: rgb(43, 244, 3);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(117, 227, 0);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(34, 14, 220);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 224, 0);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(0, 136, 44);"></div>
</div>
<div class="container">
  <div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(184, 184, 248);"></div><div class="pal" style="background: rgb(255, 73, 223);"></div><div class="pal" style="background: rgb(91, 106, 0);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(184, 184, 248);"></div><div class="pal" style="background: rgb(255, 73, 223);"></div><div class="pal" style="background: rgb(255, 73, 223);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(117, 227, 0);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(231, 213, 196);"></div><div class="pal" style="background: rgb(231, 213, 196);"></div><div class="pal" style="background: rgb(231, 213, 196);"></div>
</div>

<div class="container">
  <div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 224, 0);"></div><div class="pal" style="background: rgb(24, 226, 229);"></div><div class="pal" style="background: rgb(242, 72, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(129, 121, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 73, 223);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(43, 244, 3);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(255, 224, 0);"></div>
</div>
<div class="container">
  <div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 224, 0);"></div><div class="pal" style="background: rgb(24, 226, 229);"></div><div class="pal" style="background: rgb(242, 72, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(129, 121, 255);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(255, 73, 223);"></div><div class="pal" style="background: rgb(255, 255, 255);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(0, 0, 0);"></div><div class="pal" style="background: rgb(43, 244, 3);"></div><div class="pal" style="background: rgb(188, 25, 0);"></div><div class="pal" style="background: rgb(255, 224, 0);"></div>
</div>

---

#### Generate all possible combinations

![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-0.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-1.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-2.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-3.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-4.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-5.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-6.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-7.png)

![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-8.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-9.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-10.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-11.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-12.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-13.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-14.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-0-15.png)

![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-0.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-1.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-2.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-3.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-4.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-5.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-6.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-7.png)

![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-8.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-9.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-10.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-11.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-12.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-13.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-14.png)
![Sprites from Chack'n Pop for NES (Japanese version)](img/palette/chack-n-pop-1-15.png)

Note:
Because we can't determine statically which sprites are going to use which
palette, we have to generate all possible combinations and pick the appropriate
one at runtime.

---

Build an emulator for the web by combining:

* These PNG files
* A JavaScript file generated

---

[github.com/gmarty/**nesCompiler**](https://github.com/gmarty/nesCompiler)

---

Sita Sings the Blues (DVD)

![Sita Sings the Blues (DVD)](img/dvd-sita-sings-the-blues.png)

---

#### DVD chapters

Note:
Chapters on a DVD a stored in binary files containing structured objects.

---

#### Parse the IFO files

![IFO file content](img/ifo-file-hex.png)

Note:
Look for the chapters

---

#### Generate WebVTT files

![WebVTT file for chapters](img/webvtt.png)

---

Build a player that maps DVD features to web features

Note:
Video, chapters, interactive menu, subtitles... 

---

[github.com/gmarty/**dvd.js**](https://github.com/gmarty/dvd.js)
