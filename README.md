# 秋水仙素的小站

这是 `https://ntczyz.github.io/` 的 Hexo 源码配置建议版，主题使用 Fluid。

## 分支策略

源码放在 `source` 分支，生成后的静态网页发布到 `master` 分支。不要把 `public/` 当作源码维护，也不要长期手改 `master` 里的 HTML。

更详细的说明见 `DEPLOYMENT.md`。

## 个性化定位

- 身份：材料科学与工程研究生
- 主题：科研笔记、材料学习、实验与计算记录、明日方舟兴趣内容
- 风格：清爽、克制，保留 Fluid 的阅读体验，用 `/img/flowerfield.jpg` 作为首页视觉锚点

## 内容地图

建议把博客当成自己的研究生知识库，而不只是时间线：

- `科研笔记`：论文阅读、组会总结、实验复盘
- `材料基础`：相图、缺陷、扩散、热力学、力学性能
- `计算与数据`：Python、MATLAB、Origin、模拟与绘图
- `生活记录`：读书、日常、阶段总结
- `罗德岛档案`：明日方舟相关兴趣内容

## 常用命令

```bash
npm install
npm run server   # 直接启动本地预览
npm run preview  # 清理、生成、再启动预览
npm run check    # 部署前构建检查
npm run deploy   # 从 source 分支生成并发布到 master
```

## 目录说明

```text
source/
  _posts/       # 博客文章
  about/        # 关于页
  categories/   # 分类页
  tags/         # 标签页
  css/          # 自定义视觉样式
  img/          # 站点图片资源
scaffolds/      # 新文章模板
```

## 图片资源

当前配置依赖这些文件，已经放在 `source/img/`：

- `favicon.ico`：浏览器图标
- `fluid.jpg`：移动端图标和备用 logo
- `avatar.png`：个人头像
- `flowerfield.jpg`：首页视觉图
- `default.jpg`：文章、分类、标签默认背景图
- `wild.jpg`：关于页背景图
- `loading.gif`：图片懒加载占位图

## 写作建议

每篇科研笔记尽量保留四件事：背景、方法、观察、结论。材料研究里的很多判断都依赖条件，把参数和不确定性写下来，比只写漂亮结论更有长期价值。
