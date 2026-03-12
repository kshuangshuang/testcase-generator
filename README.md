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

### 敏感信息保护

**重要：为了保护你的 API Key 和敏感信息，本项目的安全策略：**

- ✅ **API Key 仅通过用户界面输入** - 不会硬编码在代码中
- ✅ **GitHub 仓库设为私有** - 只有你能访问代码
- ✅ **敏感文件已添加到 .gitignore** - 不会被提交到 Git
- ✅ **使用环境变量管理密钥** - 在云端部署时使用 Secrets

### 本地开发安全

```bash
# ❌ 错误做法：不要这样做
# 在代码中硬编码 API Key
api_key = "gsk_1234567890"

# ✅ 正确做法：通过用户界面输入
# 用户在应用界面输入 API Key，存储在 session 中
```

### 云端部署安全

**Streamlit Cloud Secrets 配置：**

1. 访问你的 Streamlit Cloud 应用
2. 进入 "Settings" > "Secrets"
3. 添加以下 Secret：
   ```
   GROQ_API_KEY = "your_api_key_here"
   ```

**GitHub Actions Secrets（如果使用 CI/CD）：**

1. 访问 GitHub 仓库
2. 进入 "Settings" > "Secrets and variables" > "Actions"
3. 点击 "New repository secret"
4. 添加必要的密钥

### 推送前检查清单

在 `git push` 之前，务必确认：

- [ ] 代码中没有硬编码的 API Key 或密码
- [ ] `.env` 文件已添加到 `.gitignore`
- [ ] `.streamlit/secrets.toml` 已添加到 `.gitignore`
- [ ] 使用 `git diff` 查看将要提交的更改
- [ ] 确认仓库设置为 Private（私有）

### 数据隐私

- **需求数据**：仅在生成测试用例时临时处理，不会永久存储
- **历史记录**：保存在 `history.json`，仅包含生成的测试用例
- **API Key**：仅在浏览器 session 中临时存储，刷新后需要重新输入

### 如果意外泄露了 API Key

1. **立即撤销**：访问 [Groq Console](https://console.groq.com) 撤销泄露的 Key
2. **生成新 Key**：创建新的 API Key
3. **更新配置**：在本地和云端更新为新 Key
4. **清理 Git 历史**（如果已提交）：
   ```bash
   git filter-branch --force --index-filter \
     "git rm --cached --ignore-unmatch 文件路径" \
     --prune-empty --tag-name-filter cat -- --all
   git push origin --force --all
   ```

### 推荐安全实践

- ✅ 定期更换 API Key
- ✅ 使用强密码保护 GitHub 账号
- ✅ 启用 GitHub 双因素认证（2FA）
- ✅ 定期审查 GitHub 仓库的访问权限
- ✅ 不要在不信任的网络环境中使用

## 📞 支持

- Groq 文档: [https://console.groq.com/docs](https://console.groq.com/docs)
- Streamlit 文档: [https://docs.streamlit.io](https://docs.streamlit.io)
- 问题反馈: 在 GitHub 提 Issue

## 📄 许可证

MIT License

---

**享受免费的 AI 测试用例生成！** 🎉
