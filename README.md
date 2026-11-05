# Toast 的奇妙日常

公开日记网站，使用静态 HTML 和 CSS。无需服务器、数据库或构建工具。

## 发布到 GitHub Pages

1. 在 GitHub 账户 `RoyCCCCC` 下新建**公开**仓库，建议名称 `toast-diary`。不要勾选自动生成 README，因为本文件夹已有完整内容。
2. 将本文件夹中的文件和 `posts` 文件夹上传到仓库根目录。仓库根目录应能直接看到 `index.html`、`styles.css`、`toast.png`、`favicon.svg`、`CNAME` 和 `posts/`。
3. 打开仓库的 **Settings → Pages**，在 **Build and deployment** 中选择 **Deploy from a branch**，分支选 `main`，目录选 `/ (root)`，保存。
4. 在同一页面的 **Custom domain** 输入 `toastcl.com` 并保存。即使仓库已有 `CNAME` 文件，也要在这里设置一次。
5. 再去腾讯云 DNSPod 的 `toastcl.com` 解析页面添加记录：

   | 主机记录 | 类型 | 记录值 |
   | --- | --- | --- |
   | `@` | `A` | `185.199.108.153` |
   | `@` | `A` | `185.199.109.153` |
   | `@` | `A` | `185.199.110.153` |
   | `@` | `A` | `185.199.111.153` |
   | `www` | `CNAME` | `RoyCCCCC.github.io` |

   先在 GitHub 设置自定义域名，再改 DNS。若 `@` 或 `www` 已有冲突的旧记录，核对用途后再处理。
6. 等待 GitHub Pages 与 DNS 生效，在 Pages 页面开启 **Enforce HTTPS**。首次可用时间可能取决于证书签发与 DNS 传播。

## 以后怎么写日记

1. 复制 `posts/2026-11-05-first-day.html`，改成新日期和英文短文件名，例如 `posts/2026-11-08-weekend.html`。
2. 修改新文件的 `<title>`、简介、规范网址、日期、标题和正文。
3. 在 `index.html` 的 `<div class="entries">` 里复制一段 `<article class="entry">`，填上新日期、标题、摘要、文章链接，并放在最上面。
4. 上传或提交改动；GitHub Pages 会重新发布。也可以每次把日记内容发给 Codex，由 Codex 更新页面。

## 文件说明

- `index.html`：首页和日记列表
- `posts/*.html`：独立日记文章
- `styles.css`：全站样式，含手机布局
- `toast.png`：已选定的吐司插画
- `CNAME`：自定义域名

参考：[GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)、[GitHub Pages 自定义域名](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)。
