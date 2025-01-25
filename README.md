# Git 基础知识与项目初始化指南

## Git 基本概念
- 仓库（Repository）：代表一个完整的项目，包含项目的所有文件和版本历史

## 常用 Git 命令
### 基本操作
- `git init` - 初始化新的 Git 仓库
- `git status` - 查看仓库当前状态
- `git add <文件名>` - 添加文件到暂存区
- `git commit -m "提交信息"` - 提交更改
- `git log` - 查看提交历史
- `git diff` - 查看文件修改的具体内容

### 分支操作
- `git branch` - 查看所有分支
- `git checkout <分支名>` - 切换分支
- `git checkout -b <新分支名>` - 创建并切换到新分支
- `git merge <分支名>` - 合并指定分支到当前分支

### 远程仓库操作
- `git remote add origin <仓库地址>` - 添加远程仓库
- `git pull` - 从远程仓库拉取更新
- `git push` - 推送到远程仓库
- `git push -u origin main` - 首次推送时使用，设置上游分支，之后可以直接使用 git push
- `git push origin main` - 最常用的形式，将本地的 main 分支推送到名为 origin 的远程仓库
- `git clone` - 克隆远程仓库
- `git stash` - 暂存当前修改

## 新项目初始化步骤

### 1. 初始化 Git 仓库
```bash
git init
```

### 2. 创建必要文件
- 创建 README.md
- 创建 .gitignore

### 3. .gitignore 文件模板
```gitignore
# Python 虚拟环境
.venv/
venv/
ENV/

# 环境变量文件
.env

# Python 缓存文件
__pycache__/
*.py[cod]
*$py.class

# IDE 配置文件
.vscode/
.idea/

# 系统文件
.DS_Store
Thumbs.db

# 构建输出
dist/
build/
*.exe
```

### 4. 配置 SSH 连接
1. 测试 SSH 连接：
```bash
ssh -T git@github.com
```

### 5. 关联远程仓库
1. 在 GitHub 创建新的空仓库
2. 关联远程仓库：
```bash
git remote add origin git@github.com:用户名/仓库名.git
```
3. 推送到远程仓库：
```bash
git push -u origin main
```

### 6. 提交初始文件
```bash
git add README.md .gitignore
git commit -m "Initial commit: Add README and .gitignore"
git push origin main
```
```

