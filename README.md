# 📋 智能测试用例生成器

基于 Groq AI + Llama 3.1 的智能测试用例生成工具，永久免费使用！

## ✨ 功能特性

- ✅ **多格式支持** - Word、PDF、TXT、Markdown
- ✅ **AI 智能生成** - 使用 Llama 3.1 70B 模型
- ✅ **三种测试模式** - 功能测试、全面测试、专业测试
- ✅ **历史记录** - 自动保存最近 10 条记录
- ✅ **多格式导出** - Excel 表格、Markdown 文档
- ✅ **永久免费** - Groq API 免费层 + Streamlit Cloud 免费部署
- ✅ **极速响应** - Groq 推理加速，比传统 API 快 5-10 倍

## 🚀 快速开始

### 方式一：本地运行

1. **克隆或下载代码**

```bash
cd pinpin_Workspace
```

2. **安装依赖**

```bash
pip install -r requirements.txt
```

3. **获取 Groq API Key**

- 访问 [https://console.groq.com](https://console.groq.com)
- 注册账号（免费）
- 创建 API Key
- 复制保存

4. **运行应用**

```bash
streamlit run app.py
```

5. **打开浏览器**

访问 `http://localhost:8501`

### 方式二：云端部署（推荐）

#### 部署到 Streamlit Community Cloud

1. **创建 GitHub 仓库**

```bash
# 在项目目录执行
git init
git add .
git commit -m "Initial commit"
# 在 GitHub 创建新仓库，然后执行
git remote add origin https://github.com/你的用户名/仓库名.git
git push -u origin main
```

2. **部署到 Streamlit Cloud**

- 访问 [https://streamlit.io/cloud](https://streamlit.io/cloud)
- 点击 "New app"
- 连接你的 GitHub 仓库
- 选择 `app.py` 作为主文件
- 点击 "Deploy"

3. **配置 API Key**

- 在部署后的应用设置中
- 找到 "Secrets" 或 "Environment variables"
- 添加：`GROQ_API_KEY = 你的API密钥`

4. **完成！**

获得免费域名，如：`https://你的应用名.streamlit.app`

## 📖 使用说明

### 1. 配置 API Key

在侧边栏输入 Groq API Key（只需输入一次）

### 2. 上传需求文档

支持格式：
- 📄 Word 文档 (.docx)
- 📕 PDF 文档 (.pdf)
- 📝 文本文件 (.txt)
- 📃 Markdown 文件 (.md)

### 3. 选择测试类型

- **功能测试** - 覆盖正常流程和基本异常场景
- **全面测试（含边界/异常）** - 包含边界值、等价类划分等
- **行业级专业测试** - 符合 IEEE 829 标准的专业测试用例

### 4. 生成测试用例

点击 "🚀 开始生成" 按钮，AI 将自动分析需求并生成测试用例

### 5. 导出测试用例

- **Excel 表格** - 可导入测试管理系统（TestRail、Jira 等）
- **Markdown 文档** - 便于版本控制和阅读

### 6. 查看历史记录

自动保存最近 10 条生成记录，可随时重新下载

## 💰 成本说明

### 完全免费

| 项目 | 费用 |
|------|------|
| Groq API | **免费**（免费层足够个人使用）|
| Streamlit Cloud | **免费**（永久免费部署）|
| GitHub | **免费**（私有仓库）|

### Groq 免费层额度

- 每月大量免费请求
- 速度极快（推理加速）
- Llama 3.1 70B 高质量模型

## 🛠️ 技术栈

- **前端框架**: Streamlit
- **AI 模型**: Groq + Llama 3.1 70B
- **文档解析**: python-docx, pypdf
- **数据处理**: pandas, openpyxl
- **部署平台**: Streamlit Community Cloud

## 📁 项目结构

```
pinpin_Workspace/
├── app.py                    # 主应用
├── requirements.txt          # Python 依赖
├── README.md                 # 使用说明
├── .streamlit/
│   └── config.toml          # Streamlit 配置
└── history.json             # 历史记录（自动生成）
```

## ❓ 常见问题

### Q: Groq API 真的永久免费吗？

A: Groq 目前提供慷慨的免费层，足够个人使用。官方政策可能调整，但即使将来收费，也有大量免费额度。

### Q: 生成的测试用例质量如何？

A: 使用 Llama 3.1 70B 模型，质量接近 Claude 3.5 Sonnet，足以应对大部分测试场景。

### Q: 支持中文吗？

A: 完全支持！界面和生成的测试用例都是中文。

### Q: 可以部署到私有服务器吗？

A: 可以！使用 Docker 或直接在服务器上运行 `streamlit run app.py`。

### Q: 历史记录保存在哪里？

A: 保存在 `history.json` 文件中，本地运行时在项目目录，云端运行在应用目录。

## 🔐 安全说明

- API Key 仅存储在本地或云端环境变量中
- 文档内容不会永久保存（仅保存生成的测试用例）
- 建议定期备份 `history.json` 文件

## 📞 支持

- Groq 文档: [https://console.groq.com/docs](https://console.groq.com/docs)
- Streamlit 文档: [https://docs.streamlit.io](https://docs.streamlit.io)
- 问题反馈: 在 GitHub 提 Issue

## 📄 许可证

MIT License

---

**享受免费的 AI 测试用例生成！** 🎉
