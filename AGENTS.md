# Group Website

## 项目定位

本仓库现在是纯静态课题组网站。生产内容位于 `site/`，部署时直接发布该目录。

旧 al-folio/Jekyll 方案已移除；后续不要重新引入 Ruby、Jekyll、Docker、RenderCV、Google Scholar 自动引用更新或相关模板工作流，除非用户明确要求。

## 目录地图

- `site/index.html`：首页，包含首屏、导师介绍、研究方向、News、Selected publications。
- `site/research.html`：研究方向页面。
- `site/publications.html`：论文与成果页面。
- `site/cv.html`：CV 页面。
- `site/people.html`：成员页面。
- `site/photos.html`：照片页面。
- `site/styles.css`：全站样式。
- `site/photos/`：照片和占位图资源。
- `.github/workflows/deploy.yml`：发布 `site/` 到 GitHub Pages。
- `.github/workflows/prettier.yml`：检查 `site/` 格式。

## 开发约束

1. 保持纯静态实现，优先使用 HTML/CSS，只有明确需要交互时再加入少量原生 JavaScript。
2. 新增页面时同步更新所有页面的顶部导航。
3. 图片资源优先放在 `site/photos/` 或 `site/assets/` 内，避免依赖外部图片链接。
4. 提交前至少运行：

```powershell
npx --yes prettier site --check
```

5. 重要页面结构改动后，检查静态链接是否仍指向存在的本地文件。
