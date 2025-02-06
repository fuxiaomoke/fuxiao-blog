---
title: "开始学习在github上搭建blog"
date: 2025-02-06
---
总之要开始学习怎么在github上搭建blog了，千里之行，始于足下！

下面是具体步骤的记录↓

## 步骤1：启用 GitHub Pages

欢迎来到 GitHub Pages 、Jekyll 🎉!

第一步，您需要在新仓库上启用GitHub Pages。启用后，GitHub 会自动获取 `main` 分支的内容并用于发布网站。

⌨️ 动手

1. 点击您仓库的 **Settings** 菜单

2. 进入设置后，点击 **Code and automation** 下的 Pages

3. 请确保 **Source** 下拉框选择 "Deploy from a branch"，**Branch** 选择 `main`

4. 点击 **Save** 保存

5. 等待大约20秒，然后刷新页面。[GitHub Actions](https://docs.github.com/en/actions) 将自动更新到下一步。

   > 启用 GitHub Pages 会创建仓库的部署。 在等待部署期间，GitHub Actions 可能需要长达一分钟的时间才能响应。 这一步比较慢，请您耐心等待，后续步骤大约是20秒。 注意：在Pages设置页面顶部，会出现您网站的链接地址，复制链接或点击 "Visit site" 按钮可查看您的 GitHub Pages 站点。

## 步骤2：配置您的网站

恭喜，您已开启了GitHub Pages！🎉

我们将在我为您创建的一个分支`my-pages`中工作，以使该网站看起来很棒。 ❇️

Jekyll 使用名为 `_config.yml` 的文件来保存站点配置、如主题、网站名称、等设置。

我们需要使用博客主题，这里我们选择 "minima"。

### 动手练习：开始配置您的站点

1. 切换到`my-pages`分支，点击`_config.yml`文件

2. 右上角有个编辑按钮，打开文件编辑器

3. 为了使用`minima`主题，我们在`_config.yml`文件里添加下面的内容

   ```
   theme: minima
   ```

4. （可选）您还可以添加其他配置变量，例如站名`title:`, 作者`author:`、站点描述`description:`

5. 提交修改

6. （可选）创建一个拉取请求以便查看您在本课程中将进行的所有更改。 单击**Pull Requests** tab，单击**New pull request**，设置`base: main`和`compare:my-pages`

7. 等待大约20秒，然后刷新页面。[GitHub Actions](https://docs.github.com/en/actions) 将自动更新到下一步。

## 步骤3：自定义你的网站首页

干的漂亮，您已设置好了网站主题✨

想要自定义首页，您可以修改 `index.md` 或者 `README.md` 文件，向其添加内容。GitHub Pages 会首先查找是否有 index.md 文件。 我们的仓库里已经有一个 index.md 文件，因此我们可以修改它。

### ⌨️ 动手练习：创建您的首页

1. 切换到`my-pages`分支，点击`index.md`文件
2. 右上角有个编辑按钮，打开文件编辑器
3. 在编辑框内输入你想要在首页上展示的内容，注意使用Markdown格式
4. （可选）您还可以修改 `title:` 或暂时不管，我们将在下一步中讨论
5. 提交`my-pages`分支中的修改
6. 等待大约20秒，然后刷新页面。[GitHub Actions](https://docs.github.com/en/actions) 将自动更新到下一步。

## 步骤4：发布一篇文章

您的首页看起来很棒！🤠

GitHub Pages 使用 Jekyll 工具来生成网站。在 Jekyll 中，博客需要遵守特定的文件命名格式和frontmatter。文件必须以 `_posts/YYYY-MM-DD-title.md` 方式命名， frontmatter中必须包括`title`和`date`。

**什么是frontmatter？** Jekyll 文件使用的语法称为 YAML frontmatter，它位于文件开头，示例如下：

```
---
title: "Welcome to my blog"
date: 2019-01-20
---
```

更多关于front matter配置说明请参考 [Jekyll frontmatter 文档](https://jekyllrb.com/docs/front-matter/)

### ⌨️ 动手练习：创建一篇博客文章

1. 切换到 `my-pages` 分支

2. 点击 **Add file** 点击 **Create new file** 创建文件

3. 文件取名为 `_posts/YYYY-MM-DD-title.md`

4. 将 `YYYY-MM-DD` 替换为今天的日期，同时可以修改`title`

   > 如果您确实要编辑标题，请确保单词之间有连字符。 如果您的博客文章日期不遵循正确的日期约定，您将收到错误消息，并且您的网站将无法构建。 有关详细信息，请参阅“[排查 GitHub Pages 站点的 Jekyll 构建错误](https://docs.github.com/zh/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites)”。

5. 将下面的内容放于文件顶部

   ```
   ---
   title: "YOUR-TITLE"
   date: YYYY-MM-DD
   ---
   ```

6. 将 `YOUR-TITLE` 替换为你真实的文章标题

7. 将 `YYYY-MM-DD` 替换为今天的日期，例如 `2023-09-04`

8. 快速编写一段文章草稿，后面可以随时对其修改

9. 提交修改

10. 等待大约20秒，然后刷新页面。[GitHub Actions](https://docs.github.com/en/actions) 将自动更新到下一步。

## 步骤5：合并您的拉取请求

干的漂亮，朋友 ❤️！大家很快就能阅读您的博客！

您现在可以合并您的拉取请求！

### 动手

1. 将`my-pages`分支的修改合并到`main`。如果您已经在步骤2中创建了Pull Request，那么现在只需打开那个PR，然后点击**Merge pull request**完成合并。 如果您之前没有创建，现在可以按照步骤2 中的说明进行操作。
2. (可选) 删除`my-pages`分支
3. 等待大约20秒，然后刷新页面。[GitHub Actions](https://docs.github.com/en/actions) 将自动更新到下一步。

## 完成 
