# Git 多电脑协作 Skill

## 使用场景

当项目需要在多台电脑之间同步、初始化 Git 仓库、绑定 GitHub 私有仓库、检查提交安全性或规范日常提交流程时，使用本 Skill。

## 成功标准

- 项目由 Git 管理。
- `.gitignore` 已排除本地依赖、构建产物、缓存、日志和环境变量。
- `.env.example` 只包含变量名或无敏感说明。
- 真实 `.env`、密钥、Token、Cookie 和私人配置不会进入 Git。
- 多电脑切换前已 commit 并 push。
- 另一台电脑开发前已 pull 或 pull rebase。

## 初始化流程

1. 检查当前目录状态：

```bash
git status
```

如果还不是 Git 仓库，执行：

```bash
git init
```

2. 创建或检查基础文件：

```text
.gitignore
.env.example
README.md
AGENTS.md
```

3. 首次提交前检查：

```bash
git status
```

4. 只添加明确文件：

```bash
git add .gitignore .env.example README.md AGENTS.md .skills/git-multidevice/SKILL.md
git commit -m "init project"
```

5. 绑定远程仓库：

```bash
git remote add origin <仓库地址>
git branch -M main
git push -u origin main
```

## 第二台电脑同步

```bash
git clone <仓库地址>
cd <项目目录>
```

按项目实际包管理器安装依赖：

```bash
npm ci
```

或：

```bash
pnpm install --frozen-lockfile
```

再创建本地环境变量文件：

```bash
cp .env.example .env
```

## 日常流程

开发前：

```bash
git status
git pull --rebase
```

提交前：

```bash
git status
git add <明确文件>
git commit -m "feat: xxx"
git push
```

## 注意事项

- 避免默认使用 `git add .`，除非已经确认工作区没有敏感文件或无关文件。
- 如果密钥已经提交过，不能只删除文件；必须轮换密钥，并根据需要清理 Git 历史。
- 遇到冲突时先阅读冲突内容，再按当前需求解决，不要机械覆盖。
