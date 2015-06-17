What about the following code?

---

<div style="white-space: pre; text-align: left;"><code class="hljs javascript"><span class="hljs-keyword">var</span> pc = <span class="hljs-number">0x0000</span>, sp;
<span class="hljs-keyword">var</span> instructions = {
  <span class="hljs-number">0x0000</span>: <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">()</span> </span>{
    pc = <span class="hljs-number">0x007E</span>;
  },
  <span class="hljs-number">0x007E</span>: <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">()</span> </span>{
    di();
    sp = <span class="hljs-number">0xDFF0</span>;
    <span class="hljs-comment">//...</span>
  }
};
<span class="hljs-keyword">while</span> (<span class="hljs-literal">true</span>) instructions\[pc]();</code></div>

Note:
We get a nice JavaScript file and we don't need the ROM file.
This compilation process must be done on a ROM basis.
There's a huge potential for optimisation on the generated JavaScript code.

---

### Compiler

Note:
Or recompiler to speak properly.

---

[github.com/gmarty/**jsSMS**](https://github.com/gmarty/jsSMS)
