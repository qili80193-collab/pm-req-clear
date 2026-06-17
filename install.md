# 安装指南

## Claude Code

将本仓库克隆或下载到本地，然后在 Claude Code 中注册 skill 路径。

### 方法一：克隆到全局 skills 目录（推荐）

```bash
# 克隆仓库
git clone https://github.com/<你的用户名>/prd-framework-skill.git ~/.claude/skills/prd-framework

# 或在已有 ~/.claude/skills/ 目录下添加子模块
cd ~/.claude/skills && git submodule add https://github.com/<你的用户名>/prd-framework-skill.git prd-framework
```

### 方法二：添加到项目级 skills 目录

```bash
# 在项目根目录下
mkdir -p .claude/skills
git submodule add https://github.com/<你的用户名>/prd-framework-skill.git .claude/skills/prd-framework
```

### 使用方法

在 Claude Code 中，输入与产品需求相关的内容时，skill 会自动触发。你也可以手动引用：

```
/claude 我想做一个数据报表功能，帮我梳理一下需求
```

## Copilot CLI

将 `SKILL.md` 放置到 Copilot CLI 配置的 skills 目录中。

```bash
# 克隆到 Copilot CLI 的 skills 目录
gh copilot skills add https://github.com/<你的用户名>/prd-framework-skill
```

参考 `references/copilot-tools.md` 了解工具名映射。

## Gemini CLI

将 `SKILL.md` 放置到 Gemini CLI 的 skills 目录中。本 skill 为纯思维框架，不依赖平台特定工具，可直接使用。

## 验证安装

启动你的 AI 助手，输入类似以下内容来验证 skill 是否生效：

> 我想做一个运营数据看板，每天自动更新核心指标。帮我梳理一下这个需求。

如果助手开始按 WHY → WHAT → HOW 的结构引导你，说明安装成功。
