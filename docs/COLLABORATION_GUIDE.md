# 团队知识库协作指引（请用 Qoder 完成）

> 本文档面向新加入的同事，介绍如何参与团队知识库的维护。

## 一、前置准备

1. **注册 GitHub 账号**（如果还没有）：https://github.com/signup
2. **安装 Qoder**（日常所有操作由 Qoder 代劳）

## 二、克隆仓库

打开终端，执行：

```bash
git clone git@github.com:zhengshuhang-damo/team-knowledge.git
cd team-knowledge
```

> 如果报错 `Permission denied (publickey)`，说明还没配置 SSH，继续看下一步。

## 三、配置 SSH（只需一次）

打开 Qoder，让它帮你完成：

> **发给 Qoder 的指令：**
> "帮我生成 SSH 密钥并配置 Git，我的 GitHub 用户名是 XXX"

Qoder 会自动：

- 生成 SSH 密钥（`~/.ssh/id_ed25519`）
- 配置 Git 身份（用户名、邮箱）

**然后你只需手动做一步**（需要登录 GitHub 网页）：

1. 打开 https://github.com/settings/ssh/new
2. Title 随便填，Key 粘贴 Qoder 显示的公钥内容
3. 点击 **Add SSH key**

配置完成后测试：

```bash
ssh -T git@github.com
```

看到 `Hi XXX! You've successfully authenticated` 就说明成功了。

## 四、日常使用

以后每次更新内容，**直接让 Qoder 帮你完成**，例如：

> **更新知识：**
> "帮我把这份文档整理成 Markdown，提交到 team-knowledge 的 knowledge/verification 目录，并推送到远程"

> **共享 Skill：**
> "帮我把这个 Skill 文件夹发布到 team-knowledge 的 skills/custom 目录，并推送"

> **更新现有文件：**
> "帮我修改 team-knowledge 里的 xxx.md，然后提交推送"

> **拉取最新内容：**
> "帮我拉取 team-knowledge 的最新更新"

## 五、目录说明

```
team-knowledge/
├── knowledge/            # 知识文档
│   ├── ai-coding/        # AI 辅助开发经验
│   └── verification/     # 验证方法论
├── skills/custom/        # 团队共享的 Qoder Skill
├── slides/               # 演示材料
├── templates/            # 通用模板
└── docs/                 # 使用指南
```

## 六、注意事项

- 每次推送前先 `git pull` 拉取最新，避免冲突
- 提交信息请用规范格式：`update: 更新xxx` / `feat: 新增xxx`
- 如果和同事改了同一文件导致冲突，Qoder 可以帮你解决，把冲突信息发给它即可
