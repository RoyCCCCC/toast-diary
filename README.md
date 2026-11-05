# Toast 的奇妙日常

公开日记网站：[https://toastcl.com/](https://toastcl.com/)。使用 GitHub Pages 自带的 Jekyll 发布 Markdown 日记，首页自动显示新文章。

## 当前发布设置

- 仓库：`RoyCCCCC/toast-diary`（公开）
- Pages 来源：`main` 分支的 `/ (root)`
- 自定义域名：`toastcl.com`，已开启 HTTPS
- 腾讯云 DNSPod：`@` 的两条 A 记录分别指向 `185.199.108.153` 和 `185.199.109.153`；`www` 的 CNAME 指向 `RoyCCCCC.github.io`

腾讯云免费版阻止继续给 `@` 添加第三条 A 记录。GitHub 文档要求根域名至少有一条有效 A、ALIAS 或 ANAME 记录；当前两条 A 记录已经让网站和 HTTPS 正常访问。保留现有的 `ledger`、`site` 和验证记录，勿误删。

## 以后怎么写日记

1. 打开仓库的 [`_posts` 文件夹](https://github.com/RoyCCCCC/toast-diary/tree/main/_posts)，点击 **Add file → Create new file**。
2. 文件名写成 `年-月-日-英文短名.md`，例如 `2026-11-08-weekend.md`。一天可以写多篇，只要短名不同。
3. 粘贴下面的模板，改标题、标签并写正文。第一组 `---` 之间是文章信息，不能省略。

   ```md
   ---
   title: "今天的标题"
   tags: [日常]
   ---

   从这里开始写日记。段落之间留一个空行。

   ## 一个小标题

   后面继续写。**加粗**、列表、引用和图片都支持 Markdown。
   ```

4. 点击编辑器上方的 **Preview** 检查内容，再点 **Commit changes...**，选择直接提交到 `main`。GitHub Pages 会自动发布，首页也会自动出现新日记。

`title` 是文章标题；`tags` 是板块标签，默认的 `日常` 可改成 `游戏`、`随笔` 等。多个标签写成 `tags: [游戏, 随笔]`，板块页会自动收录。文件名中的日期就是发布日期；版式已经在网站设置中指定，不用再写 `date` 或 `layout`。

首页摘要默认从正文提取文字，即使文章以图片开头也会显示文字。若想自己写摘要，可在 `tags` 下一行加 `description: "一句摘要"`。若想在标题下加一句引言，可再加 `lead: "一句开头"`。这些都是可选项。

**添加图片：** 在 GitHub 的 Markdown 编辑框中拖入图片、粘贴截图，或点击编辑框下方的上传提示选择图片。等上传完成，GitHub 会自动插入图片代码，例如 `![傍晚的天空](图片地址)`。把方括号里的文字改成能描述图片的内容。网站会把图片缩到正文宽度，点击图片可以放大查看；这只调整显示尺寸，不压缩原文件。段落之间要留一个空行，连续换行在 Markdown 中通常仍是同一段。

发布前检查：文件在 `_posts` 文件夹、文件名是 `年-月-日-短名.md`、开头的 `---` 成对、`title` 和 `tags` 的冒号是英文冒号、图片上传完成后再提交。GitHub 的 Preview 展示内容排版；网站上的字体和配色以发布后的页面为准。

## 文件说明

- `index.html`：首页，自动列出 `_posts` 里的日记
- `_posts/*.md`：Markdown 日记，文件名决定发布日期
- `_layouts/post.html`：日记页面的固定版式
- `topics.html`：按标签自动汇总的板块页
- `_config.yml`：网站地址和文章规则
- `posts/2026-11-05-first-day.html`：旧链接，保留兼容
- `styles.css`：全站样式，含手机布局
- `toast.png`：已选定的吐司插画
- `CNAME`：自定义域名

参考：[GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)、[GitHub Pages 自定义域名](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)。
