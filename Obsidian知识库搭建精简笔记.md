# 学习笔记：Obsidian + WorkBuddy 搭建私人知识库

> 来源：第二周课堂笔记 + 飞书文档《第二周课程随堂笔记》《实战课：用AI Agent+Obsidian 打造你的第二大脑》
> 目标：用本地 Obsidian 建一个 AI 能读懂、会帮你持续整理与思考的"第二大脑"

## 1. 核心认知

- **公共知识 vs 私人知识**：AI 已读遍公共知识，唯一不懂的是你的私人知识（经验、思考、经历）——这才是知识库的核心价值
- **知识库本质** = 存储 + 加工 + 思考，缺一不可
- **一句话**：打造属于你的私人维基百科（Wiki）

## 2. 为什么选 Obsidian

- 本地文件 + Markdown：AI 读取损耗最低的格式，数据自己掌控
- 双向链接：笔记连成网
- 对比：Notion 数据在云端、飞书围绕组织、腾讯 ima 数据锁死

## 3. LLM Wiki 方法论（核心）

- 普通 RAG 的局限：只翻找碎片、看不到全局、无法综合
- **三层架构**：
  - Raw/ 原始素材层（只读不改）
  - Wiki/ 知识层（AI 生成维护）
  - Schema 规则层（AGENTS.md，约束 AI 行为）
- **三种操作**：Ingest 摄入 / Query 查询 / Lint 检查修复
- **两个关键文件**：index.md（索引）、log.md（变更日志）
- 知识被"编译"进体系而非存储，每次摄入让体系更强

## 4. Vault 目录结构

```
MyVault/
├── AGENTS.md      # 给 AI 的地图（入口文件）
├── Raw/           # 原始素材：articles / recordings / books / images
├── Wiki/          # 知识层：index.md + log.md + entities / concepts / sources
└── Outputs/       # 输出：drafts / projects / daily
```

对应三层：Raw 存储、Wiki 处理、Outputs 思考。

## 5. 实操五步（WorkBuddy）

1. Obsidian 新建 Vault（本地文件夹）
2. WorkBuddy：选工作空间 → 指向 Vault 文件夹 → 选 **plan 模式**
3. 让 AI 采访你（一问一答 15-20 个问题，答完 AI 就懂你了）
4. 给 AI 源文件地址 → 让它设计目录框架 → 你确认
5. AI 自动创建目录、持续维护，知识库自生长

## 6. 关键技巧

- **省 Token**：plan 模式 + 请求批准权限 + 渐进式披露（只给 AI 需要的文件，目录一层层展开）
- **会员 ≠ API**：OpenAI 会员不能给第三方 Agent 接 API；API 选 DeepSeek，价格是 OpenAI 的几百分之一
- **跨设备**：把知识库文件夹复制给另一台 AI 读取即可，记忆随文件走
- **推荐 WorkBuddy 而非 Hermes**：右侧可见可修改文件，交互直观

## 7. 自动化进阶（可选）

- 输入管道：Web Clipper 剪藏网页、录音豆、飞书云文档、微信读书
- cron 定时：每日自动摄入新素材（必做）、每周深度研究、每周日归档检查

## 8. 避坑要点

- 别只收藏不加工（= 信息坟场）
- 别先建完美系统，先跑起来再迭代
- 插件 3-5 个起步就够
- 少堆公共知识书，多沉淀自己的思考
