# 邻家帮 UI 案例集线上发布包

本目录按照“职业技能培训学习小程序”长期公开站点规则整理：以独立发布包作为站点根目录，根地址直接打开 UI 案例集。

- `index.html`：公开站点入口，包含 5 页案例展示与按需加载逻辑。
- `lucide.min.js`：项目内置图标库，避免外部 CDN 阻塞页面。
- `user-app.html`、`worker-app.html`、`admin.html`：三端独立交互页面，仅进入对应案例页时加载。
- `user-home.jpg`、`user-orders.jpg`、`user-profile.jpg`：部署专用展示图，使用浏览器懒加载与异步解码。
- 发布文件采用仓库根目录扁平结构，便于通过 GitHub 网页端一次性更新。
- 站点不依赖外部图标 CDN；首个 HTML 保持轻量，避免一次初始化全部三端页面。

重新生成：

```bash
ruby scripts/build_standalone_site.rb
```
