# Toast 的奇妙日常

公开日记网站：[https://toastcl.com/](https://toastcl.com/)。使用静态 HTML 和 CSS，托管在 GitHub Pages；无需服务器、数据库或构建工具。

## 当前发布设置

- 仓库：`RoyCCCCC/toast-diary`（公开）
- Pages 来源：`main` 分支的 `/ (root)`
- 自定义域名：`toastcl.com`，已开启 HTTPS
- 腾讯云 DNSPod：`@` 的两条 A 记录分别指向 `185.199.108.153` 和 `185.199.109.153`；`www` 的 CNAME 指向 `RoyCCCCC.github.io`

腾讯云免费版阻止继续给 `@` 添加第三条 A 记录。GitHub 文档要求根域名至少有一条有效 A、ALIAS 或 ANAME 记录；当前两条 A 记录已经让网站和 HTTPS 正常访问。保留现有的 `ledger`、`site` 和验证记录，勿误删。

## 以后怎么写日记

1. 复制 `posts/2026-11-05-first-day.html`，改成新日期和英文短文件名，例如 `posts/2026-11-08-weekend.html`。
2. 修改新文件的 `<title>`、简介、规范网址、日期、标题和正文。
3. 在 `index.html` 的 `<div class="entries">` 里复制一段 `<article class="entry">`，填上新日期、标题、摘要、文章链接，并放在最上面。
4. 将这两个文件提交到 `main`；GitHub Pages 会自动重新发布。也可以每次把日记内容发给 Codex，由 Codex 更新页面。

## 文件说明

- `index.html`：首页和日记列表
- `posts/*.html`：独立日记文章
- `styles.css`：全站样式，含手机布局
- `toast.png`：已选定的吐司插画
- `CNAME`：自定义域名

参考：[GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)、[GitHub Pages 自定义域名](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)。
