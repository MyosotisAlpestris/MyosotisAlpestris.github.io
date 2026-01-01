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
  // 放弃复杂的 baseurl，直接使用相对于根目录的绝对路径
  const filePath = "/files/note_2.tex"; 
  
  console.log("正在尝试抓取文件:", filePath); // 在控制台打印路径，方便调试

  fetch(filePath)
    .then(response => {
      if (!response.ok) {
        throw new Error('服务器返回了 ' + response.status);
      }
      return response.text();
    })
    .then(data => {
      console.log("抓取成功！内容长度:", data.length);
      document.getElementById('latex-code').textContent = data;
    })
    .catch(err => {
      console.error("抓取失败:", err);
      document.getElementById('latex-code').textContent = "加载失败: " + err.message;
    });
</script>
