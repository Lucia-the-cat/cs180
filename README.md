# CS180 · Projects Guide

这是一个最小可用（MVP）的 CS180 项目导航站模板，适合用 **GitHub Pages** 托管。

## 快速开始

1. 在 GitHub 新建一个仓库（建议名字：`cs180` 或 `cs180-website`）。
2. 把本仓库里的文件上传（`index.html`、`.nojekyll`、本 README）。
3. 打开仓库 **Settings → Pages**：
   - Build and deployment：选择 **Deploy from a branch**
   - Branch：选择 `main`，文件夹选 `/ (root)`
   - 点击 **Save**
4. 稍等片刻，访问你的站点：`https://<你的 GitHub 用户名>.github.io/cs180/`

> 如果你希望它作为个人主页的子站点，请确保你的个人主页仓库叫 `username.github.io`（可选）。

## 如何添加项目卡片

在 `index.html` 中，复制一份现有的 `<article class="card">...</article>`，然后修改：

- 标题：`<h3>Project N · 名称</h3>`
- 描述：`<p>一句话描述。</p>`
- 状态/时间：`<div class="meta">...</div>`
- 链接按钮的 `href`：替换为该项目 **真实网址**（可以是同仓库下的子路径，或外部链接）

```html
<article class="card">
  <h3>Project 1 · Edge Detection</h3>
  <p>实现 Canny 算法并展示实验结果。</p>
  <div class="meta">状态：已发布 · 最近更新：2025-10-01</div>
  <a class="go" href="https://<username>.github.io/cs180/project1/" target="_blank" rel="noopener">进入 Project 1 →</a>
</article>
```

## 建议结构（可选）

如果你想把每个 Project 的静态页面也放在 **同一个仓库**：

```
cs180/
├─ index.html          # 导航页（本文件）
├─ project0/           # Project 0 的网站文件
│  └─ index.html
├─ project1/
│  └─ index.html
└─ .nojekyll
```

这样每个项目的访问地址会是：

- `https://<username>.github.io/cs180/project0/`
- `https://<username>.github.io/cs180/project1/`

同时在导航页的按钮写成上述 URL 即可。

## 常见问题

- **为什么我要加 `.nojekyll`？**  
  为防止 GitHub Pages 的 Jekyll 处理器忽略带下划线的目录等特殊行为。留一个空的 `.nojekyll` 是个稳妥的做法。

- **我已经有个人主页 `username.github.io` 了怎么办？**  
  不冲突。这个仓库作为二级路径站点：`https://username.github.io/cs180/`。

- **我想自定义域名**  
  在仓库 `Settings → Pages → Custom domain` 里设置即可（需要先在域名 DNS 中添加 CNAME 记录指向 `<username>.github.io`）。

- **我有多个学期**  
  可以在仓库根创建 `fall-2025/`、`spring-2026/` 等文件夹；或在导航页按学期分组。

---

Happy hacking & good luck in CS180! 🎓
