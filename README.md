# B06 招新任务提交仓库

索思科技协会 · 技术部 B06 创新实验室 招新任务的完成记录。本仓库用于在面试时展示任务完成情况。

## 运行环境

| 项 | 值 |
|---|---|
| 操作系统 | Ubuntu 24.04.2 LTS |
| 运行方式 | WSL2（内核 6.6.75.1-microsoft-standard-WSL2） |
| 登录用户 | herta |
| IDE | VS Code 1.138.0（Remote Development 扩展，Connect to WSL） |

## 任务完成情况

| 任务 | 要求 | 状态 |
|---|---|---|
| 任务一 本地 Linux 环境 | 能跑一种以 Linux 为内核的系统 | 完成：WSL2 + Ubuntu 24.04.2 LTS |
| 任务二 配置 IDE 远程连接 | IDE 打开的文件属于 Linux 而非 Windows | 完成：VS Code + Remote-WSL，打开的是 `/home/herta/...` 下的文件 |
| 任务三 获取 GitHub 账户 | 有一个可展示的 GitHub 账号 | 完成：[@herta0127](https://github.com/herta0127)；SSH 走 443 通道 |
| 任务四 IDE 内的 agent | 在 IDE 里用上 AI agent | 已打通：VS Code 内置 GitHub Copilot Chat（0.66.0）在 WSL 窗口中可用 |
| 任务五 git 提交与推送 | 本地提交并推送到 GitHub | 完成：本仓库（`git log` 可查提交历史） |

## 自检命令（可复现）

```bash
whoami                 # -> herta
uname -a               # -> 含 microsoft-standard-WSL2 的 Linux 内核
head -3 /etc/os-release # -> Ubuntu 24.04.2 LTS
code --version         # -> 1.138.0
git log --oneline      # -> 本仓库的提交记录
git remote -v          # -> git@github.com:herta0127/b06-hello.git
```

## 目录说明

```
.
├── README.md     本文件：环境与任务完成情况
└── .gitignore    忽略编译产物与编辑器/系统文件（C/C++ 学习工程用）
```

## 备注

- 环境截图（`uname -a` / `os-release` / `whoami`）在面试现场按需展示，未纳入本仓库。
- 后续课程练习代码会继续提交到本仓库，作为持续使用 git 与 IDE 的记录。
