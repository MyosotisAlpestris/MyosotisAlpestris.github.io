---
layout: single
title: "LaTeX Template Preview"
permalink: /tex-preview/
---

### LaTeX Template Preview

[View source code on GitHub](https://github.com/MyosotisAlpestris/MyosotisAlpestris.github.io/blob/master/files/note_2.tex)

---

### Code Display

<!-- 使用系统自动适配的配色方案 -->
<style>
  #latex-display-container {
    width: 100%;
    margin: 1em 0;
    padding: 1.5em;
    /* 关键：使用 currentColor 和继承背景，或者设置透明背景 */
    background: rgba(128, 128, 128, 0.05); 
    border: 1px solid rgba(128, 128, 128, 0.3);
    border-radius: 8px;
    
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.9em;
    line-height: 1.5;
    
    overflow: auto;
    max-height: 70vh;
    white-space: pre-wrap;
    word-break: break-all;
    
    /* 自动跟随主题文字颜色 */
    color: inherit; 
  }
</style>

<pre id="latex-display-container"><code id="latex-code">正在加载代码内容...</code></pre>

<script>
  // 自动获取 baseurl 并拼接路径
  const filePath = "{{ site.baseurl }}/files/note_2.tex";
  
  fetch(filePath)
    .then(response => {
      if (!response.ok) throw new Error('无法连接到文件 (404)');
      return response.text();
    })
    .then(data => {
      // textContent 会保留所有的 LaTeX 反斜杠和括号，且不会被误当作 HTML
      document.getElementById('latex-code').textContent = data;
    })
    .catch(err => {
      document.getElementById('latex-code').textContent = "加载失败: " + err.message;
    });
</script>
