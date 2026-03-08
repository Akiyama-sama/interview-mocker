# Interview Mocker - 面试模拟器

一个用于模拟技术面试的 Claude Skill，帮助求职者准备面试。

## 功能特性

- 🎯 模拟技术面试（八股文 + 项目拷打 + 算法题）
- 📋 基于简历定制问题
- 📊 根据目标公司级别调整难度权重（小厂/中厂/大厂）
- 💡 STAR 法则深度追问
- 📈 面试后提供反馈与改进建议

## Skill 结构

```
interview-mocker/
├── SKILL.md          # Skill 定义文件（必需）
├── scripts/          # 可选：可执行脚本
├── references/      # 可选：参考资料
└── assets/          # 可选：静态资源
```

## 安装方式

### 方式一：Claude Code 本地安装（推荐）

#### 全局安装（个人使用）

```bash
# 创建全局 skills 目录
mkdir -p ~/.claude/skills

# 克隆或复制 skill 到全局目录
git clone https://github.com/your-username/interview-mocker.git ~/.claude/skills/interview-mocker
```

#### 项目级安装

```bash
# 在项目根目录创建 .claude/skills 目录
mkdir -p .claude/skills

# 克隆或复制 skill
git clone https://github.com/your-username/interview-mocker.git .claude/skills/interview-mocker
```

#### 验证安装

在 Claude Code 中输入：
```
/skills list
```

应该能看到 `interview-mocker` skill。

---

### 方式二：OpenSkills CLI 安装

[OpenSkills CLI](https://github.com/jimmysong/openskills) 是一个跨平台的 skill 管理工具，支持 Claude Code、Cursor、OpenAI Codex 等。

#### 安装 OpenSkills CLI

```bash
# 使用 npm
npm install -g openskills

# 或使用 bun
bun add -g openskills

# 直接使用 npx
npx openskills --help
```

#### 安装 skill

```bash
# 从 GitHub 仓库安装
npx openskills install your-username/interview-mocker

# 指定目标代理（claude、cursor 等）
npx openskills install your-username/interview-mocker -t claude

# 全局安装
npx openskills install your-username/interview-mocker -g

# 安装后同步
npx openskills sync
```

---

### 方式三：skills.sh / npx add-skill

[skills.sh](https://skills.sh) 是另一个流行的 skill 管理工具。

#### 使用 npx 安装

```bash
# 从 GitHub 安装
npx skills add your-username/interview-mocker

# 或指定仓库
npx skills add https://github.com/your-username/interview-mocker
```

#### 常用命令

```bash
# 列出已安装的 skills
npx skills list

# 更新 skill
npx skills update interview-mocker

# 卸载 skill
npx skills remove interview-mocker
```

---

### 方式四：Claude 官方 Marketplace

> 注意：Claude 官方 Marketplace 目前仍在建设中，部分功能可能需要 Pro/Max/Team 订阅。

#### 通过命令行添加市场

```bash
# 在 Claude Code 中添加市场
/plugin marketplace add anthropics/skills

# 搜索 skill
/plugin search interview-mocker

# 安装 skill
/plugin install interview-mocker@anthropics-skills
```

#### 通过界面上传

1. 将 skill 目录打包成 ZIP 文件
2. 打开 [Claude.ai](https://claude.ai) → Settings → Capabilities → Skills
3. 点击 Upload 上传 ZIP 文件

---

### 方式五：Vercel Skills

[Vercel Skills](https://vercel.com) 是 Vercel 推出的 AI agent skill 管理工具。

#### 安装 Vercel Skills CLI

```bash
# 全局安装
npm i -g @vercel/agent-skills

# 或使用 npx
npx @vercel/agent-skills --help
```

#### 安装 skill

```bash
# 添加 skill 到当前项目
npx add-skill vercel-labs/agent-skills

# 或从本地安装
npx add-skill ./interview-mocker

# 选择安装范围：
# - 全局（所有项目可用）
# - 当前项目（仅当前目录可用）
```

---

### 方式六：手动复制

如果你不想使用任何 CLI 工具，可以手动复制文件：

```bash
# 克隆仓库
git clone https://github.com/your-username/interview-mocker.git

# 复制到 Claude Code skills 目录
cp -r interview-mocker ~/.claude/skills/

# 或复制到项目目录
cp -r interview-mocker .claude/skills/
```

---

## 使用方法

安装完成后，在 Claude Code 中：

1. **触发 skill**：直接告诉 Claude
   - "帮我模拟面试"
   - "面试我"
   - "准备技术面试"
   
2. **首次使用**：提供以下信息
   - 简历内容
   - 开发方向（前端/后端/全栈）
   - 目标公司级别（小厂/中厂/大厂）

3. **开始面试**：按照面试官引导进行

---

## 更新日志

### v1.0.0

- 初始版本
- 支持前端/后端面试模拟
- 提供八股文、项目拷打、算法题
- STAR 法则追问方法论

---

## 相关链接

- [Agent Skills 官方标准](https://agentskills.io)
- [OpenSkills CLI](https://github.com/jimmysong/openskills)
- [skills.sh](https://skills.sh)
- [Claude Code 文档](https://docs.anthropic.com/en/docs/claude-code)
- [SkillsMP 市场](https://skillsmp.com)

---

## License

MIT
