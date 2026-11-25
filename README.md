# Interactive-Learning-skills

面向技术学习的完整 Agent Skill：先创建课程大纲，逐章从头讲解，确认理解后进行动态苏格拉底式追问，最后生成语雀友好的 Markdown 笔记与复习记录。

## 适合场景

Linux、网络、KVM、OpenStack、华为云 Stack、Kubernetes、Docker、存储、数据库、云运维面试等。并不限定领域。

## skills概述
<img width="1199" height="1312" alt="Interactive Learning Flow Infographic" src="https://github.com/user-attachments/assets/4e606dff-5b33-49c6-903d-b6f271afeec9" />

## 安装

解压后保留整个 `Interactive-Learning-skills/` 文件夹及其 `references/`、`templates/`。在支持 Agent Skills 的客户端选择导入整个技能目录，或放入其指定的 skills 目录。

Claude Code 用户级安装示例：

```bash
mkdir -p ~/.claude/skills
cp -R Interactive-Learning-skills ~/.claude/skills/
```

也可将完整目录放入项目的 `.claude/skills/`。安装后可说：“请使用 Interactive-Learning-skills，按我提供的资料建立课程大纲。”

## 文件结构

```text
Interactive-Learning-skills/
├── SKILL.md                 # 核心调度规则
├── README.md                # 使用指南
├── references/
│   ├── syllabus.md          # 大纲与进度
│   ├── teaching.md          # 完整教学规则
│   ├── interactive-engine.md      # 动态互动问答
│   └── notes.md             # 语雀 Markdown 笔记标准
└── templates/
    ├── course-outline.md    # 大纲模板
    ├── chapter-notes.md     # 最终笔记模板
    └── progress.yaml        # 可选进度记录
```

## 推荐操作

1. 发参考 PDF/课件/章节目录：“根据资料建立完整学习大纲，不开始考试。”
2. “开始学习 Nova 第一章。”→ 完整系统讲解。
3. 自由追问，直到你说“我理解了，开始互动问答”。
4. AI 每次只出一道题，评价答案、必要时补讲、动态追问。
5. “结束考核，生成笔记。”→ 生成独立可读 Markdown 文档。
6. 将 `progress.yaml` 保存在自己的项目里，跨会话时重新提供，继续上次学习。

## 教学设计

本技能以课程大纲组织教学，确认理解后按难度逐题追问，逐项纠错并练习实战排障，最后整理独立笔记和学习进度。

## 使用限制

不包含模型本身的联网、读取本地文件、绘图、长期记忆或定时能力。客户端是否能自动激活技能、导出文件、保存进度，取决于运行环境和权限。不存在后台自主推进或自动持久化保证。
