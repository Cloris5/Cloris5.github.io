# CLORIS

Cloris 的个人创作与研习档案库，部署于 GitHub Pages：<https://cloris5.github.io/>

## 结构

- `index.html` — 站点首页：项目档案、Prompt 卡片、技术笔记、归档规范
- `projects/midnight-colossus.html` — P01《子夜钟楼》实时 3D Demo（单文件，Three.js 走 jsDelivr CDN）
- `projects/wave-wall.html` — P02《浪墙》实时 3D Demo（fable middie · 64 分钟游戏；参数化卷浪 / HRTF 音频）
- `projects/white-blade-forge.html` — P03《炽刃熔炉》实时 3D Demo（fable middie · 64 分钟游戏；GTAO / 黑体温度着色）
- `projects/galaxy-highway.html` — P04《银河公路》实时 3D Demo（单文件，Three.js + GPGPU）
- `projects/organ-gorge.html` — P05《管风琴峡》实时 3D Demo（单文件，Three.js + WebAudio）
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

## 推送到 GitHub

本机代理会让普通 `git push` 认证失败，用 `gh-push` 代替即可（已配置，绕开代理并用钥匙串令牌认证）：

```bash
cd ~/Documents/GitHub/Cloris5.github.io
git add -A
git commit -m "说明这次改了什么"
gh-push              # 等同于推送当前分支到 origin
# 或指定：gh-push origin main
```

推送后 GitHub Pages 会自动重新构建，约半分钟后生效。新开的终端若提示找不到 `gh-push`，先执行 `source ~/.zshrc`。

## 操作提示

《子夜钟楼》：WASD 移动 · 鼠标视角 · Shift 冲刺 · Space 跳 · 左键刺剑 · 右键校准（完美格挡）/ 重击 · Ctrl/E 闪步 · Q 拨针加速 · F 互动 · J 导演模式 · K 录制 · P 拍照

《浪墙》：A/D 压板切浪 · W 俯冲取速 / S 回切上浪 · Shift 喷射 · Space 浪顶腾空 / 小跳 · Q/E 空中转体 · 左键救援索 · 右键回看白沫前锋 · F 腾空时向飞艇挥手 · T 第一/第三人称 · J 导演模式 · K 录制 · P 拍照 · 手柄：左摇杆 / A 跳 / X 救援 / RT 喷射

《炽刃熔炉》：WASD 移动 · 鼠标左键挥刃（按住蓄力）· 右键格挡 · Shift 冲刺 · Space 跳 · E 互动 · F 淬火 · X 锁定 · V 切视角 · 长按 R 重开 · Tab 参数面板 · O 导演台 · K 录制 · J 10 秒钩子 · T 照片模式 · M 静音 · H 界面 · L 低端模式 · Esc 暂停

《银河公路》：WASD 移动 · E 交互 · Space 跳 · C 切换视角 · 鼠标左键甩灯 · 1 滑板 / 2 表情 / 3 坐下 · B 全场开花 · P 导演演示 · R 一键录制 · G 图鉴 · M/N/J 三路音频 · X 切换 Look · V 版本信息

《管风琴峡》：WASD 移动 · 鼠标拖拽环顾 · V 第一/第三人称 · E 互动与拉音栓 · Space 跳 · 长按 F 蓄风、松开鼓管 · L 指针锁定 · G 图鉴 · M 静音 · H 键位 · N 小地图 · Tab 参数面板 · Esc 暂停 · P 拍照
