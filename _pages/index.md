---
layout: single
title: "LaTeX Template Preview"
permalink: /tex-preview/
---

### LaTeX Template Preview

[View source code on GitHub](https://github.com/MyosotisAlpestris/MyosotisAlpestris.github.io/blob/master/files/note_2.tex)

---

### Code Display

<pre style="background: transparent; color: inherit; padding: 15px; border: 1px solid #888; overflow: auto; max-height: 600px;"><code id="latex-code">正在加载代码内容...</code></pre>

<!-- 用 JavaScript 抓取文件内容 -->
<script>
  fetch('/files/note_2.tex')
    .then(response => response.text())
    .then(data => {
      document.getElementById('latex-code').textContent = data;
    })
    .catch(err => {
      document.getElementById('latex-code').textContent = "加载失败，请检查文件路径是否正确。";
    });
</script>
