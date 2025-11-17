# CarlZhangQuizVault

一个轻量级、适配移动端的测验应用，专为流畅的题目练习而设计，具备动态题目加载、题型筛选（单选/多选/判断）、题目直接跳转以及实时进度跟踪等功能。采用 HTML、Tailwind CSS 和原生 JavaScript 构建，支持离线使用和响应式设计——针对移动设备和桌面端体验均做了优化。是通过直观的界面与用户体验来组织和练习各类测验内容的理想之选。


## 功能特性
### 1. 核心功能
- **动态题目加载**：逐题加载，无需整页刷新，交互流畅。
- **灵活的题目导航**：
  - 一键切换"上一题"和"下一题"。
  - 通过跳转模态框直接跳转到指定题目（支持输入验证）。
- **题型筛选**：按题型筛选题目（单选题/多选题/判断题），专注特定练习需求。
- **进度跟踪**：实时进度条显示当前练习进度，清晰的题目计数显示（如"题目 5 / 453"）。
- **答案显示**：点击"显示答案"查看正确答案，视觉高亮显示（正确答案绿色，错误选择红色）。


### 2. 响应式设计
- **移动端优化**：小屏幕（≤640px）自动切换为纯图标按钮以节省空间；触控友好的点击区域（≥45px）便于操作。
- **桌面端适配**：完整文字+图标按钮确保清晰易用；扩展的进度条和布局提升可读性。
- **跨设备兼容**：在智能手机、平板、笔记本和桌面电脑上无缝运行（支持 Chrome、Safari、Firefox、Edge）。


### 3. 离线支持
- 无后端依赖——所有题目数据本地存储在 JavaScript 中。
- 初始页面加载后无需网络连接即可使用。


## 技术栈
- **前端**：HTML5（语义化结构）、Tailwind CSS v3（响应式样式）、原生 JavaScript（交互逻辑）。
- **UI/UX**：Font Awesome 图标（直观的视觉提示）、平滑过渡（悬停/点击效果）、清晰的视觉层次结构。


## 快速开始
### 1. 克隆仓库
```bash
git clone https://github.com/carlzhang123/CarlZhangQuizVault.git
cd CarlZhangQuizVault
```

### 2. 运行应用
- 无需构建步骤——直接在浏览器中打开 `index.html`。
- 最佳体验：使用 Chrome（移动端/桌面端）或 Safari（iOS 设备）。


### 3. 自定义题目数据
1. 打开 `index.html` 并找到 `questions` 数组（在标记为"Question Data"的 `<script>` 标签中）。
2. 按照现有格式添加/修改题目：
   ```javascript
   {
     "id": 1,
     "content": "你的题目内容？",
     "type": "单选题", // 可选: "单选题" / "多选题" / "判断题"
     "optionA": "选项 A",
     "optionB": "选项 B",
     "optionC": "选项 C",
     "optionD": "选项 D",
     "answer": "A" // 多选题答案用大写字母拼接，如 "AB"
   }
   ```
3. 保存文件并刷新浏览器查看更改。


## 使用指南
| 功能 | 操作方法 |
|------|----------|
| 筛选题目类型 | 点击"筛选"按钮 → 选择所需类型（如"多选题"）。 |
| 跳转到题目 | 点击"跳转"按钮 → 输入题目编号 → 点击"确认"。 |
| 显示正确答案 | 点击"显示答案"按钮（正确答案用绿色高亮显示）。 |
| 重置当前题目 | 点击"重置"按钮（清除用户选择并隐藏答案）。 |
| 导航题目 | 使用"上一题"/"下一题"按钮，或滑动手势（移动端）/方向键（桌面端）。 |


## 许可证
MIT 许可证 - 允许自由使用、修改和分发本项目用于个人或商业用途。详见 [LICENSE](LICENSE) 文件。


## 贡献指南
1. Fork 本仓库。
2. 创建功能分支（`git checkout -b feature/your-feature`）。
3. 提交更改（`git commit -m 'Add new feature'`）。
4. 推送到分支（`git push origin feature/your-feature`）。
5. 打开 Pull Request。


## 截图展示
### 移动端视图
![mobile_view](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/mobile_view.png)

### 桌面端视图
![desktop_view](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/desktop_view.png)

### 题目筛选
![question_filter](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/question_filter.png)

### 答案显示
![answer_display](https://raw.githubusercontent.com/carlzhang123/CarlZhangQuizVault/refs/heads/main/img/answer_display.png)


## 已知问题
- **题目数据大小**：对于非常大的题库（>1000题），初始页面加载时间可能会增加。对于极大的数据集，考虑实现分页功能。
