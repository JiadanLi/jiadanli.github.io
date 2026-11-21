# JADAN · 交互式 GitHub Pages 作品集

## 本版真正可以操作的内容

1. `teacher.html`：在案例页内嵌 `teacher-demo.html`，或全屏打开。该演示基于上传的班主任工作台原始 HTML，保留座位拖动、学生档案、待办管理、成长及问题记录、数据备份等前端交互。每位访客的更改保存在**其自己的浏览器**，不是网站共享数据库。
2. **重要：** `teacher-demo.html` 的“AI 快速创建待办”在 GitHub Pages 上使用明确标注的**本地规则模拟器**。会做简单的文本拆分、日期识别、可编辑任务卡和保存，不是真正调用 AI 大模型。原始上传 HTML 的 `/api/ai-todo` 接口需要独立后端，GitHub Pages 无法运行 Node/Python API。以后如要真实接入模型，需要部署安全后端并设置访问限额与数据脱敏。
3. `math.html`：内嵌已经发布的森林数学探险原站，并设有全屏访问链接。**如果原站设置 CSP frame-ancestors 或 X-Frame-Options 禁止 iframe，则作品集里不能内嵌，但全屏链接仍可打开。** 请部署后验证；无法控制第三方站点的嵌入策略。

## 发布到 GitHub Pages

- 建立仓库 `你的GitHub用户名.github.io`（仓库 Public）。
- 将本压缩包**解压后的文件**全部上传到仓库根目录（包含 `index.html`、`teacher-demo.html`、`style.css`、`assets/` 等）。
- 仓库 Settings → Pages → Source: Deploy from a branch → main → /(root) → Save。
- 访问 `https://你的GitHub用户名.github.io/`，点击两张项目卡片进行互动测试。

## 对外发布安全提醒

- 不要输入真实学生姓名、联系方式或家庭情况。此站是公开演示网站，不提供登录鉴权和加密数据存储。
- 演示样本中的姓名全部是虚构的；不要向代码上传 API Key、环境变量或任何学生真实数据。
- “数据导出”会下载当前浏览器中的用户输入；不要用真实数据测试。
- 如果你需要真实 AI 调用，必须通过受保护的后端实现，不能在浏览器脚本里放大模型 API 密钥。

## 文件结构
- `index.html` 首页
- `teacher.html` 班主任案例 + 内嵌交互演示
- `teacher-demo.html` 班主任完整可交互演示（本地规则模拟 AI）
- `math.html` 数学案例 + 内嵌在线游戏（如允许）
- `resume.html` 在线简历
- `style.css` / `script.js` 样式与导航
- `assets/teacher-dashboard.png` 真实截图
