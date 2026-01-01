---
layout: single
title: "LaTeX Template Preview"
permalink: /tex-preview/
---

### LaTeX Template Preview

[View source code on GitHub](https://github.com/MyosotisAlpestris/MyosotisAlpestris.github.io/blob/master/files/note_2.tex)

---

### Code Display

<!-- 样式部分：只做透明度处理，不写死颜色，这样就会自动跟随你的深色主题 -->
<style>
  .my-code-box {
    background: rgba(128, 128, 128, 0.1); /* 半透明背景，深浅色通用 */
    color: inherit;                       /* 强制继承主题的文字颜色 */
    padding: 15px;
    border: 1px solid rgba(128, 128, 128, 0.3);
    border-radius: 6px;
    overflow: auto;
    max-height: 600px;
    font-family: monospace;
    white-space: pre;                     /* 保持代码缩进 */
    display: block;
  }
</style>

<pre class="my-code-box"><code id="latex-code">正在加载内容...</code></pre>

<script>
  // 恢复到你之前成功的路径写法
  fetch('/files/note_2.tex')
    .then(response => {
      if (!response.ok) throw new Error('Status: ' + response.status);
      return response.text();
    })
    .then(data => {
      // 成功后填入内容
      document.getElementById('latex-code').textContent = data;
    })
    .catch(err => {
      document.getElementById('latex-code').textContent = "加载失败: " + err;
    });
</script>
