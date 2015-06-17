## Compile-to-the-web

---

### Get the software

Note:
Dump/Rip it if it has a physical support.
Download it otherwise.
Software run on processors or virtual machine

---

Columns for Game Gear<br>
(Japanese version)

![Columns for Game Gear (Japanese version)](img/columns-j-gamegear.png)

---

![Columns for Game Gear in a hex editor](img/columns-gg-hex.png)

Note:
The complete game is a single binary file of 32kB.

---

### Run it in JavaScript

---

<pre><code class="hljs javascript">var rom = new Uint8Array([
 0xC3, 0x7E, 0x00, 0xFF, 0xFF, 0xFF, 
 0xFF, 0xFF, 0xF3, 0x7B, 0xD3, 0xBF,
 0x3E, 0x40, 0xB2, 0xD3, 0xBF, 0xFB,
 0xC9, 0xFF, 0xFF, 0xFF, 0xFF, 0xFF,
 0xF3, 0x7B, 0xD3, 0xBF, 0x7A, 0xD3,
 0xBF, 0xFB, 0xC9, 0xFF, 0xFF, 0xFF,
 0xFF, 0xFF, 0xFF, 0xFF, 0x3E, ...
]);
</code></pre>

Note:
Store it in a typed array (Uint8). Values are hexadecimal.
The ROM is 32kB so the array has 32768 elements.

---

<table>
<tr class="fragment" data-fragment-index="2">
  <th>pc</th>
  <td><span class="fragment highlight-current-red" data-fragment-index="3" style="color: mediumvioletred;">↓</span></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="4" style="color: mediumvioletred;">↓</span></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="4" style="color: mediumvioletred;">↓</span></td>
  <td></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="5" style="color: mediumvioletred;">↓</span></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="7" style="color: mediumvioletred;">↓</span></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="8" style="color: mediumvioletred;">↓</span></td>
  <td><span class="fragment highlight-current-red" data-fragment-index="8" style="color: mediumvioletred;">↓</span></td>
  <td></td>
</tr>
<tr>
  <th>Index</th>
  <td>0x0000</td>
  <td>0x0001</td>
  <td>0x0002</td>
  <td>...</td>
  <td>0x007E</td>
  <td>0x007F</td>
  <td>0x0080</td>
  <td>0x0081</td>
  <td>...</td>
</tr>
<tr>
  <th>Value</th>
  <td>0xC3</td>
  <td>0x7E</td>
  <td>0x00</td>
  <td>...</td>
  <td>0xF3</td>
  <td>0x31</td>
  <td>0xF0</td>
  <td>0xDF</td>
  <td>...</td>
</tr>
</table>

<div class="fragment" data-fragment-index="0" style="white-space: pre; text-align: left;"><code class="hljs javascript"><span class="fragment highlight-current-blue" data-fragment-index="2"><span class="hljs-keyword">var</span> pc = <span class="hljs-number">0x0000</span>, sp;</span>
<span class="hljs-keyword">while</span> (<span class="hljs-literal">true</span>) {</span>  
  <span class="fragment highlight-current-blue" data-fragment-index="3"><span class="fragment highlight-current-blue" data-fragment-index="5"><span class="fragment highlight-current-blue" data-fragment-index="7"><span class="hljs-keyword">var</span> opcode = rom.getUint8(pc);</span></span></span>
  pc++;
  <span class="hljs-keyword">switch</span> (opcode) {
    <span class="fragment highlight-current-blue" data-fragment-index="4"><span class="hljs-keyword">case</span> <span class="hljs-number">0xC3</span>:
      pc = rom.getUint16(pc); <span class="hljs-keyword">break</span>;</span>
    <span class="fragment highlight-current-blue" data-fragment-index="6"><span class="hljs-keyword">case</span> <span class="hljs-number">0xF3</span>:
      di(); <span class="hljs-keyword">break</span>;</span>
    <span class="fragment highlight-current-blue" data-fragment-index="8"><span class="hljs-keyword">case</span> <span class="hljs-number">0x31</span>:
      sp = rom.getUint16(pc); pc+= <span class="hljs-number">2</span>; <span class="hljs-keyword">break</span>;</span>
  }
}</span></code></div>

Note:
The Game Gear is based on a Z80 chipset.

---

### Interpreter

Note:
Execute a format on the fly.
