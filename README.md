# CLORIS

Cloris 的个人创作与研习档案库，部署于 GitHub Pages：<https://cloris5.github.io/>

## 结构

- `index.html` — 站点首页：项目档案、Prompt 卡片、技术笔记、归档规范
- `projects/midnight-colossus.html` — 《子夜钟楼》实时 3D Demo（单文件，Three.js 走 jsDelivr CDN）
- `README.md` — 本说明

## 新增内容

在 `index.html` 中按对应区块复制一个 `<article>` / `<div class="note">` 即可：

- 项目：复制 `#projects` 下的 `.project` 区块，替换编号、标题与链接
- Prompt 卡片：复制 `#cards` 下的 `.card`，`data-c` 决定筛选分组（`pipeline` / `material` / `system`）
- 技术笔记：复制 `#notes` 下的 `.note`，更新编号与时长

## 本地预览

```bash
cd Cloris5.github.io
python3 -m http.server 8000
# 打开 http://localhost:8000
```

直接双击 `projects/midnight-colossus.html` 也可以运行；若浏览器限制本地模块加载，请走上面的 HTTP 服务。

## 操作提示（3D Demo）

WASD 移动 · 鼠标视角 · Shift 冲刺 · Space 跳 · 左键刺剑 · 右键校准（完美格挡）/ 重击 · Ctrl/E 闪步 · Q 拨针加速 · F 互动 · J 导演模式 · K 录制 · P 拍照
