# Yi Zuo · Academic Homepage

无需构建的单页学术主页。直接双击 `index.html` 即可打开；无需 Jekyll、npm 或 JavaScript。页面内容为英文，适配桌面与手机。

## 文件结构

```text
.
├── index.html             # 全部页面内容
├── assets/
│   ├── styles.css         # 排版、响应式与打印样式
│   ├── books/             # 专著封面
│   ├── paper/             # 每篇论文的配图（按论文名称分目录）
│   └── images/            # 个人照片、项目图片与图标
├── .nojekyll              # GitHub Pages 跳过 Jekyll
├── .gitignore
├── LICENSE
└── README.md
```

## 修改内容

- 论文：编辑 `index.html` 的 `#publications`，每个 `article.publication` 对应一篇。
- 简介、教育、项目、专著和奖项：编辑对应的 section。
- 照片：替换 `assets/images/portrait.jpeg`；当前以原始横向比例展示，不裁剪人物。若图片比例改变，请同步更新 HTML 中的宽高与 CSS 的 `aspect-ratio`。
- 样式：编辑 `assets/styles.css`。

所有资源使用相对路径，支持本地文件访问与静态托管。论文、GitHub 等外部链接需要联网。

## 预览与部署

可直接打开 `index.html`，或在此目录运行：

```sh
python3 -m http.server 8000
```

然后访问 `http://localhost:8000`。

GitHub Pages 可选择从发布分支的根目录发布。原有 Jekyll 模板、生成结果、Markdown 页面、历史备份与旧页面跳转目录已移除，所有内容集中在首页。原模板作者的自定义域名配置已移除；如使用自己的域名，请另行配置。
