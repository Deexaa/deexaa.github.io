# Academic Homepage Template

这是一个类似参考站点的静态学术个人主页模板。你通常只需要改 `data.js`，不用改 `index.html` 和 `styles.css`。

## 文件说明

- `index.html`: 页面结构和自动渲染逻辑。
- `styles.css`: 页面样式。
- `data.js`: 你的个人信息、新闻、论文、教育经历、工作经历、服务和获奖。
- `assets/`: 放头像、论文缩略图、PDF 简历等文件。

## 只改内容的流程

1. 打开 `data.js`。
2. 修改 `profile` 里的姓名、头像、单位、邮箱和链接。
3. 修改 `about` 数组里的自我介绍段落。
4. 修改 `news`、`publications`、`education`、`experience`、`services`、`awards`。
5. 把你的头像放到 `assets/`，例如 `assets/me.jpg`，然后把 `profile.avatar` 改成 `"assets/me.jpg"`。
6. 如果有简历 PDF，放到 `assets/cv.pdf`，并保留 `profile.links` 里的 CV 链接。
7. 双击打开 `index.html` 预览。

## 发布到 GitHub Pages

1. 新建一个仓库，仓库名建议用 `你的用户名.github.io`。
2. 把本目录里的文件上传到仓库根目录。
3. 进入 GitHub 仓库的 `Settings` -> `Pages`。
4. Source 选择 `Deploy from a branch`，Branch 选择 `main` 和 `/root`。
5. 等待部署完成，访问 `https://你的用户名.github.io`。

## 添加一篇论文

在 `data.js` 的 `publications` 数组中复制一个对象，然后改成你的论文信息：

```js
{
  venue: "Conference 2026",
  title: "Your Paper Title",
  url: "https://arxiv.org/abs/xxxx.xxxxx",
  authors: "Your Name, Coauthor A, Coauthor B.",
  image: "assets/your-paper-image.jpg",
  summary: "One-sentence contribution summary.",
  links: [
    { label: "Paper", url: "https://arxiv.org/abs/xxxx.xxxxx" },
    { label: "Code", url: "https://github.com/yourname/project" }
  ],
  bullets: [
    "Main contribution.",
    "Important result."
  ]
}
```

如果不想显示论文图片，可以先继续使用 `assets/publication-placeholder.svg`。
