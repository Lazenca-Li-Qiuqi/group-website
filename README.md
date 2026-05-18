# Group Website

这是一个纯静态课题组网站，不再依赖 Jekyll、Ruby、Docker 或 al-folio 构建链路。

## 目录

- `site/index.html`：首页
- `site/research.html`：研究方向
- `site/publications.html`：成果与论文
- `site/cv.html`：CV
- `site/people.html`：成员
- `site/photos.html`：照片墙
- `site/styles.css`：全站样式
- `site/photos/`：照片与占位图

## 本地预览

直接用浏览器打开 `site/index.html` 即可。

也可以启动一个本地静态服务器：

```powershell
python -m http.server -d site 8000 --bind 127.0.0.1
```

然后访问 `http://127.0.0.1:8000/`。

## 部署

推送到 `main` 后，GitHub Actions 会把 `site/` 目录发布到 GitHub Pages。

当前部署入口：

- `.github/workflows/deploy.yml`
- `.github/workflows/prettier.yml`

## 维护方式

网站内容直接编辑 `site/*.html`；样式直接编辑 `site/styles.css`。

如果要替换照片，把图片放入 `site/photos/`，再更新页面中的 `img src`。
