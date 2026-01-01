---
layout: single
title: "LaTeX Template Preview"
permalink: /tex-preview/
---

### LaTeX Template Preview

[View source code on GitHub](https://github.com/MyosotisAlpestris/MyosotisAlpestris.github.io/blob/master/files/note_2.tex)

---

### Code Display

<pre style="padding: 15px; border: 1px solid #888; border-radius: 5px; overflow: auto; max-height: 600px; background: transparent; color: inherit; font-family: monospace; white-space: pre-wrap;">
<code id="latex-code">准备抓取文件...</code>
</pre>

<script>
  // 使用 window.location.origin 确保绝对路径从网站根目录开始
  const targetPath = window.location.origin + "/files/note_2.tex";
  const displayElement = document.getElementById('latex-code');

  displayElement.textContent = "正在连接服务器: " + targetPath;

  fetch(targetPath)
    .then(response => {
      if (!response.ok) {
        throw new Error("服务器返回错误 " + response.status + " (请检查文件是否存在)");
      }
      return response.text();
    })
    .then(data => {
      if (data.trim().length === 0) {
        displayElement.textContent = "文件内容为空。";
      } else {
        displayElement.textContent = data;
      }
    })
    .catch(error => {
      // 如果出错，把错误直接打在屏幕上，不再卡在“加载中”
      displayElement.textContent = "❌ 加载失败！原因: " + error.message;
      console.error(error);
    });
</script>
