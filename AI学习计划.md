# AI 学习计划：零基础 → 熟练使用 AI 与 GitHub → 能开发 AI 应用

> 制定日期：2026-10-22 ｜ 适用画像：编程零基础，每周投入 5~15 小时
> 总周期：**24 周（约 6 个月）**，之后进入自选深化路线
> 原则：**所有资源均为免费或开源**；每个阶段有明确的"验收标准"；所有产出公开到 GitHub——用学习计划本身来练 GitHub。
> **📌 配套文件：[AI学习-每日任务表.md](./AI学习-每日任务表.md)（每天 20:00 定时提醒，按日期逐天打卡）**

---

## 目录

- [0. 总览与路线图](#0-总览与路线图)
- [1. 阶段 0（第 1~2 天）：环境与账号准备](#1-阶段-0第-12-天环境与账号准备)
- [2. 阶段 1（第 1~4 周）：Python 零基础 + 把 AI 当导师](#2-阶段-1第-14-周python-零基础--把-ai-当导师)
- [3. 阶段 2（第 5~8 周）：Git 与 GitHub 熟练使用](#3-阶段-2第-58-周git-与-github-熟练使用)
- [4. 阶段 3（第 9~14 周）：AI 工具层——会用、用深](#4-阶段-3第-914-周ai-工具层会用用深)
- [5. 阶段 4（第 15~22 周）：AI 开发层——能做出真应用](#5-阶段-4第-1522-周ai-开发层能做出真应用)
- [6. 阶段 5（第 23 周起）：融入开源 + 深化选修](#6-阶段-5第-23-周起融入开源--深化选修)
- [7. 每周时间排布模板（5h / 10h / 15h 三档）](#7-每周时间排布模板5h--10h--15h-三档)
- [8. 免费/开源资源总表](#8-免费开源资源总表)
- [9. 打卡与跟踪机制（把这份计划变成 GitHub 项目）](#9-打卡与跟踪机制把这份计划变成-github-项目)
- [10. 新手常见坑](#10-新手常见坑)

---

## 0. 总览与路线图

| 阶段 | 时间 | 主题 | 阶段产出（验收物） |
|---|---|---|---|
| 阶段 0 | 第 1~2 天 | 装机、注册账号 | 可用的开发环境 + 你的第一个 GitHub 仓库 |
| 阶段 1 | 第 1~4 周 | Python 零基础 | 3 个小工具 + 学会用 AI 辅导自己学习 |
| 阶段 2 | 第 5~8 周 | Git & GitHub | 绿格子、合并的第 1 个外部 PR、Pages 个人主页 |
| 阶段 3 | 第 9~14 周 | AI 深度使用 | 个人提示词库 + 1 条自动化工作流 + 本地大模型 |
| 阶段 4 | 第 15~22 周 | AI 应用开发 | 3 个可展示的 GitHub 作品集项目（API 调用 / RAG / Agent） |
| 阶段 5 | 第 23 周起 | 开源融入与选修 | 参与开源贡献 + 自选理论/大模型深化路线 |

```
Python基础 ──► GitHub协作 ──► AI工具精通 ──► AI应用开发 ──► 开源社区
   (阶段1)        (阶段2)        (阶段3)         (阶段4)       (阶段5)
```

> 两条主线并行推进：**"会用 AI"**（提示词、AI 编程助手、自动化、本地模型）和 **"会开发 AI 应用"**（API、RAG、Agent），零基础起步，阶段 3 起合流。

---

## 1. 阶段 0（第 1~2 天）：环境与账号准备

### 1.1 安装软件（全部免费/开源）

- [ ] **VS Code**（免费开源）：https://code.visualstudio.com —— 唯一需要的主编辑器
- [ ] **Python 3.12+**（官网安装包即可）：https://www.python.org/downloads/ （安装时勾选 *Add to PATH*）
- [ ] **Git**（开源）：https://git-scm.com/download/win —— 安装后命令行输入 `git --version` 验证
- [ ] **Ollama**（开源本地大模型工具，电脑 ≥16GB 内存建议装）：https://ollama.com —— 低配电脑可跳过，先用在线免费对话工具

### 1.2 注册账号（全部免费）

- [ ] **GitHub**：https://github.com/signup （如果是在校学生，注册后用学信网/学生证申请 **GitHub Student Pack**，能白嫖大量付费工具）
- [ ] **Hugging Face**：https://huggingface.co/join （全球最大的开源模型社区，有大量免费课程）
- [ ] **DeepSeek**（对话免费）：https://chat.deepseek.com
- [ ] **智谱清言 / 智谱开放平台**（对话免费；其 **GLM-4-Flash API 长期免费**，是后面练手 API 的首选）：https://open.bigmodel.cn
- [ ] **Google Gemini**（免费额度 API）：https://aistudio.google.com
- [ ] **Kaggle**（免费 AI 课程 + 免费 GPU 算力）：https://www.kaggle.com
- [ ] （可选）**SiliconFlow 硅基流动**：新用户送免费 API 额度，可跑开源模型 API：https://siliconflow.cn

### 1.3 配置 Git 身份 + 建第一个仓库

```bash
git config --global user.name  "你的昵称"
git config --global user.email "你的邮箱"
```

- [ ] 在 GitHub 新建仓库 `ai-learning-journal`，**把本计划文件复制进去并推送**——这就是你的第一次 commit + push（不会也没关系，阶段 2 会系统教，现在先照抄命令成功一次）：

```bash
git init
git add .
git commit -m "docs: 添加 AI 学习计划"
git branch -M main
git remote add origin https://github.com/<你的用户名>/ai-learning-journal.git
git push -u origin main
```

---

## 2. 阶段 1（第 1~4 周）：Python 零基础 + 把 AI 当导师

**核心方法**：不报付费班，用"开源教材 + 免费视频 + AI 私人导师"三件套。遇到任何不懂的概念，立刻问 AI（这是本计划最重要的习惯训练）：

> 📌 万能导师提示词（存在你的笔记里反复用）：
> "我是编程零基础学习者。请用生活中的类比解释【概念】，给一个 10 行以内的最短可运行示例，然后出 2 道由易到难的小练习让我做，不要直接给答案。"
> 遇到报错时："解释这个报错的原因（用零基础能懂的说法），并告诉我检查哪三步：`<粘贴报错>`"

### 每周任务表

| 周 | 学什么 | 主要资源（免费/开源） | 本周交付物（必做） |
|---|---|---|---|
| **W1** | 变量、数据类型、输入输出、运算符 | 《简明Python教程》（开源书）https://github.com/swaroopch/byte-of-python （有中文）；B站"黑马程序员 Python 入门"前 20 集挑着看 | ✅ 命令行"单位换算器"脚本 |
| **W2** | if/while/for、列表、字典、元组 | 同上教程对应章节 + FreeCodeCamp 中文《科学计算 with Python》前 5 关 https://www.freecodecamp.org/chinese/ | ✅ "猜数字"游戏（含难度选择） |
| **W3** | 函数、模块、异常处理、文件读写 | 教程对应章节；Python 官方中文教程 https://docs.python.org/zh-cn/3/tutorial/ 第 4~7 章 | ✅ "通讯录"程序（文件持久化存 JSON） |
| **W4** | pip 第三方库、API 初体验、综合复习 | 让 AI 教你用 `requests` 调一个免费天气/汇率 API | ✅ 综合小工具（如"每日天气+名言推送到控制台"）；并把 4 个脚本整理进 `ai-learning-journal/python-basics/` |

### 阶段 1 验收标准

- [ ] 不看教程，独立写出"学生成绩管理"小程序（录入、排序、求平均、存文件）
- [ ] 已经形成肌肉记忆：**卡住 15 分钟 → 问 AI → 理解后自己重写**（绝不复制粘贴 AI 代码了事）
- [ ] 每周至少 3 天有提交/学习记录

> 说明：不要在此阶段碰数学和机器学习理论，那是阶段 5 选修内容。目标是"能写脚本 + 会用 AI 学习"。

---

## 3. 阶段 2（第 5~8 周）：Git 与 GitHub 熟练使用

**目标定位**："熟练使用 GitHub"= 会用 Git 管版本 + 会用 GitHub 协作（Issue/PR/Fork/Actions/Pages）+ 能参与开源。

| 周 | 学什么 | 主要资源（免费/开源） | 本周交付物 |
|---|---|---|---|
| **W5** | Git 核心：`config / add / commit / log / diff / branch / merge / 解决冲突` | 《Pro Git 中文版》第 1~3 章（开源书）https://git-scm.com/book/zh/v2 ；游戏化练习（开源）https://learngitbranching.js.org/?locale=zh_CN 基础关卡全通 | ✅ `learngitbranching` 基础关卡通关截图存入仓库 |
| **W6** | GitHub 协作流：remote / push / pull / fork / **PR / Issue** / 官方中文入门课 | GitHub Skills 官方互动课程（免费）https://skills.github.com 依次做：*Your first project on GitHub*、*Let's contribute to an open-source project*、*Understanding the GitHub flow* | ✅ 向 `first-contributions` 仓库（https://github.com/firstcontributions/first-contributions/blob/main/README.zh-template.md）提交你**人生第一个 PR** 并等待合并 |
| **W7** | 进阶：rebase / stash / tag / `.gitignore` / **GitHub Pages** | Pro Git 第 3.6、7.x 章；官方课 *GitHub Pages* | ✅ 用 GitHub Pages 免费上线一个个人主页/学习博客（模板可用开源的 Jekyll "Just the Docs"） |
| **W8** | 工程规范：README / LICENSE / Releases / **GitHub Projects 看板** / GitHub Actions 入门 | 官方课 *Hello World GitHub Actions*；参考 awesome-readme（开源）https://github.com/matiassingers/awesome-readme | ✅ 给 `ai-learning-journal` 配好 README、把本计划导入 GitHub Projects 看板；加一个 Actions（如每周自动更新 README 的学习进度徽章） |

### 阶段 2 验收标准

- [ ] 第一个外部 PR 被合并 🎉
- [ ] GitHub 贡献绿格子连续 4 周不断
- [ ] 个人主页/Pages 博客可访问
- [ ] 能向别人口头讲清：Fork 和 Clone 的区别、PR 是怎么工作的

---

## 4. 阶段 3（第 9~14 周）：AI 工具层——会用、用深

| 周 | 学什么 | 主要资源（免费/开源） | 本周交付物 |
|---|---|---|---|
| **W9** | 提示词工程：角色/示例/思维链/结构化输出 | DAIR.AI《提示工程指南》中文（开源）https://github.com/dair-ai/Prompt-Engineering-Guide ；Anthropic 官方提示库 https://docs.anthropic.com/en/prompt-library/library ；OpenAI 免费学院 https://academy.openai.com | ✅ 建公开仓库 `my-prompt-library`：≥20 条你亲测有效的提示词，分场景（学习/写作/代码/翻译） |
| **W10~11** | **AI 编程助手**实战：用 AI 写代码的正确姿势 | 二选一：VS Code + **GitHub Copilot Free**（免费档：每月 2000 次补全 + 50 次对话，https://github.com/features/copilot/plans）或开源插件 **Cline** https://github.com/cline/cline / **Continue** https://github.com/continue-dev 接智谱免费 API | ✅ 用 AI 助手重构阶段 1 的 4 个脚本，写出"AI 结对编程心得"发成 Issue/博客 |
| **W12** | AI 自动化工作流（无代码/低代码） | **n8n**（开源）https://github.com/n8n-io/n8n 本地 docker 部署，或 **Dify**（开源）https://github.com/langgenius/dify ；教程看 B 站官方中文频道 | ✅ 搭 1 条工作流：如"每天抓取关注领域新闻 → AI 摘要 → 生成 Markdown 存入你的 GitHub 仓库" |
| **W13** | 本地大模型：私有化使用 | Ollama（https://ollama.com）+ 开源模型（qwen3 小参数量版）+ **Open WebUI**（开源）https://github.com/open-webui/open-webui ；让 AI 给你讲清 token/上下文/量化是什么 | ✅ 本地断网也能用的私人 AI 助手；记录你的模型配置 |
| **W14** | 生成式 AI 原理通识：LLM 怎么工作、Embedding、向量 | 微软开源课程 **Generative AI for Beginners**（含中文翻译）https://github.com/microsoft/generative-ai-for-beginners 选学 1~8 章 | ✅ 写一篇《给外行讲明白大模型》发布到你的 Pages 博客（费曼学习法：讲得清才算懂） |

### 阶段 3 验收标准

- [ ] 提示词库、AI 编程、自动化、本地模型四项都有可运行成果
- [ ] 能向非技术人员解释：大模型为什么会产生幻觉、Embedding 有什么用

---

## 5. 阶段 4（第 15~22 周）：AI 应用开发——能做出真应用

**技术栈主线**：Python + LLM API + RAG + Agent。API 全程用免费/极低价（智谱 GLM-4-Flash 免费、Gemini 免费额度、DeepSeek 便宜）。

| 周 | 学什么 | 主要资源（免费/开源） | 本周交付物 |
|---|---|---|---|
| **W15~16** | LLM API 应用开发：对话、system prompt、temperature、结构化输出、Function Calling | OpenAI API 文档（协议已成事实标准，智谱/DeepSeek 都兼容其 SDK）https://platform.openai.com/docs ；微软课程对应章节；Datawhale《LLM Cookbook 中文重建版》（开源）https://github.com/datawhalechina/llm-cookbook 选读 | ✅ 项目 1：CLI "智能翻译/简历解析助手"，要求输出校验 JSON，代码传 GitHub |
| **W17~18** | **RAG 检索增强**：Embedding、向量库、切块、召回 | Hugging Face 免费课程 LLM Course https://huggingface.co/learn/llm-course ；开源向量库 **Chroma** https://github.com/chroma-core/chroma ；LangChain 中文文档 https://langchain.com.cn / LlamaIndex https://docs.llamaindex.ai | ✅ 项目 2：**"个人笔记问答助手"**——把你阶段 1~3 的笔记全部变成可以问答的知识库 |
| **W19~20** | **AI Agent 智能体**：工具调用、ReAct、多步任务规划 | Hugging Face Agents 课程（免费）https://huggingface.co/learn/agents-course ；微软 **AI Agents for Beginners**（开源）https://github.com/microsoft/ai-agents-for-beginners ；开源框架 smolagents https://github.com/huggingface/smolagents | ✅ 项目 3：能"搜索+查天气+计算"多步完成一个任务的 Agent |
| **W21~22** | 综合作品集：选一个做成"可给别人用"的产品 | 复用前面全部技术；部署免费方案：前端 GitHub Pages，后端 Python 可本地/免费容器平台 | ✅ 作品集主打项目（三选一）：① 挂在你 Pages 博客上的"博客 AI 问答"；② Telegram/微信 AI 机器人；③ Dify 搭建并导出的完整工作流应用。配 README + GIF 演示 |

### 阶段 4 验收标准

- [ ] GitHub 上有 **3 个完整作品集项目**（README、演示、提交历史、issue 跟踪一应俱全）
- [ ] 能独立走通：想法 → 原型 → API 联调 → 部署 → 文档
- [ ] 每个项目都用 AI 助手开发过，并清楚记录"哪些代码是 AI 写的、你如何验证"

---

## 6. 阶段 5（第 23 周起）：融入开源 + 深化选修

### 6.1 开源融入（持续进行）

- [ ] 参与中国最大的开源 AI 学习社区 **Datawhale**：https://github.com/datawhalechina —— 从文档纠错/翻译起步，逐步认领 `good first issue`
- [ ] 找开源项目练习贡献：https://goodfirstissue.dev 、GitHub Explore 按 topic 找
- [ ] 给你的每个项目互相写文档、加徽章；开始 review 别人的 PR（这是"熟练使用 GitHub"的最高阶形态）

### 6.2 选修路线 A：理论补强（想真正"懂" AI）

| 内容 | 资源（全部免费） |
|---|---|
| 数学直觉 | 3B1B《线性代数的本质》《神经网络》系列（B站官方号，免费） |
| 机器学习入门 | 吴恩达《机器学习》课程（Coursera 可免费旁听 / B站中文字幕版） |
| 深度学习 | 《动手学深度学习》d2l.ai 中文版（开源书+视频，李沐主讲）https://zh.d2l.ai ；fast.ai 实战课 https://course.fast.ai |
| 数据科学练手 | Kaggle Learn 免费微课 + 入门赛 https://www.kaggle.com/learn |

### 6.3 选修路线 B：大模型实战（部署、微调）

| 内容 | 资源（全部免费/开源） |
|---|---|
| 开源大模型本地部署 | Datawhale **self-llm《开源大模型食用指南》** https://github.com/datawhalechina/self-llm |
| 从零理解大模型 | Datawhale **Happy-LLM** https://github.com/datawhalechina/happy-llm ；Hugging Face LLM Course |
| 微调（LoRA/QLoRA） | Hugging Face PEFT 文档 https://huggingface.co/docs/peft ；用 **Kaggle/Colab 免费 GPU** 微调一个 7B 小模型 |
| 综合项目课（开源） | Datawhale **llm-universe《动手搭建个人AI助手》** https://github.com/datawhalechina/llm-universe （RAG+微调全流程实战课） |

---

## 7. 每周时间排布模板（5h / 10h / 15h 三档）

| 档位 | 建议分配 | 适用 |
|---|---|---|
| **每周 5h** | 工作日 5×40min（学习+动手）+ 周日 60min（复盘、写 Issue 日志）；总周期按本计划 ×1.5 拉长 | 时间碎、加班多 |
| **每周 10h（推荐）** | 工作日 5×1h（其中 30min 必须写代码/动手）+ 周末 5h 集中做本周交付物 | 标准节奏 |
| **每周 15h** | 每天 1.5h + 周末 4.5h；允许提前进入下一周内容，但**交付物必须验收后再进** | 冲刺节奏 |

**每日最小闭环（约 1 小时）**：20min 学新内容 → 30min 动手练习（AI 当导师）→ 10min `git commit` + 一句话学习日志推上 GitHub。

---

## 8. 免费/开源资源总表

| 类别 | 资源 | 链接 | 说明 |
|---|---|---|---|
| Python 入门 | 简明 Python 教程 | https://github.com/swaroopch/byte-of-python | 开源书，有中文 |
| Python 入门 | Python 官方中文教程 | https://docs.python.org/zh-cn/3/tutorial/ | 权威免费 |
| Python 入门 | FreeCodeCamp 中文 | https://www.freecodecamp.org/chinese/ | 免费互动 + 证书 |
| Python 入门 | 哈佛 CS50P | https://cs50.harvard.edu/python/ | 免费，B站有中字幕版 |
| Git | Pro Git 中文版 | https://git-scm.com/book/zh/v2 | 开源权威书 |
| Git 练习 | Learn Git Branching | https://learngitbranching.js.org/?locale=zh_CN | 开源游戏化 |
| GitHub 官方课 | GitHub Skills | https://skills.github.com | 免费互动教程 |
| 开源首贡献 | first-contributions | https://github.com/firstcontributions/first-contributions | 第一个 PR 圣地 |
| 提示工程 | Prompt Engineering Guide | https://github.com/dair-ai/Prompt-Engineering-Guide | 开源，含中文 |
| AI 通识课 | Microsoft Generative AI for Beginners | https://github.com/microsoft/generative-ai-for-beginners | 微软官方开源 |
| Agent 课 | Microsoft AI Agents for Beginners | https://github.com/microsoft/ai-agents-for-beginners | 官方开源 |
| 免费课程平台 | Hugging Face Learn | https://huggingface.co/learn | LLM/Agent 全免费 |
| 免费课程平台 | Kaggle Learn | https://www.kaggle.com/learn | 短课 + 免费 GPU |
| 免费课程平台 | DeepLearning.AI 短课 | https://www.deeplearning.ai/short-courses/ | 大量限时免费 |
| 理论教材 | 动手学深度学习 d2l | https://zh.d2l.ai | 开源书 + 视频 |
| 理论教材 | fast.ai | https://course.fast.ai | 免费实战派课程 |
| 中文开源社区 | Datawhale | https://github.com/datawhalechina | llm-cookbook / self-llm / happy-llm |
| 本地模型 | Ollama + Open WebUI | https://ollama.com / https://github.com/open-webui/open-webui | 开源，永久免费 |
| AI 编程助手 | GitHub Copilot Free / Cline / Continue | 见正文 | 免费档或开源自带 |
| 自动化 | n8n / Dify | https://github.com/n8n-io/n8n / https://github.com/langgenius/dify | 开源自部署 |
| 免费 API | 智谱 GLM-4-Flash、Gemini 免费档、DeepSeek | 见阶段 0 | 开发练手成本≈0 |
| 深度学习视频 | 3Blue1Brown（B站） | https://space.bilibili.com/88461697 | 数学直觉，免费 |

---

## 9. 打卡与跟踪机制（把这份计划变成 GitHub 项目）

这份计划**本身就该跑在 GitHub 上**，一举两得：

- [ ] 本文件已存入 `ai-learning-journal/PLAN.md`（阶段 0 已做）
- [ ] 在 GitHub Projects（免费看板）建立列：`待办 / 本周 / 进行中 / 已验收`，每周交付物 = 一张卡片
- [ ] 每周日开一个 "W__ 周复盘" Issue：学了什么、卡在哪、下周计划；让 AI 根据你的日志提问，逼自己讲清楚
- [ ] 每阶段结束写一篇验收总结博客（Pages），公开承诺倒逼执行

**周复盘 Issue 模板**：

```markdown
## W__ 周复盘（起止日期）
- 本周计划：
- 实际完成：
- 交付物链接：
- 卡点与解决过程：
- AI 帮我了什么 / 我在哪些地方不许 AI 代劳：
- 下周唯一重点：
```

---

## 10. 新手常见坑

1. **收藏≠学会**：所有资源限定"当周用完"，看不完就删出计划，不要囤课囤书。
2. **环境党**：装完 VS Code/Python/Git 就开工，别折腾主题、别迷信"最强配置"，编辑器不会让你变强。
3. **复制 AI 代码不自测**：AI 给的每段代码，你必须（a）让 AI 逐行讲解，（b）亲手改一个变量再跑一遍，（c）合上屏幕手敲核心部分。阶段 4 前，手敲是底线。
4. **数学焦虑**：前 22 周完全不需要微积分线代。想懂原理时看 3B1B 建立直觉即可，别一头扎进教材劝退。
5. **只学不用**：每周交付物是硬约束——"学完"的定义是"做出来并推送了"。
6. **绿格子造假式勤奋**：每天 0.1 行的 commit 有意义，但意义在于持续记录，不在于凑数；优先保证每周 3 个以上"真学习"提交。

---

## 结语：完成这份计划后你将拥有

- ✅ 用 Python 独立写工具、调 API 的能力
- ✅ GitHub 的完整工作流：分支、PR、Issue、Actions、Pages、开源协作
- ✅ 提示词工程 + AI 编程助手 + 自动化工作流的日常提效能力
- ✅ 3 个可展示、可写进简历的 AI 应用项目（API / RAG / Agent）
- ✅ 一个持续记录学习过程的公开仓库和社区连接

**下一步行动（今天就能做）**：完成阶段 0 的装机和账号注册清单，把这份文件推送成你的第一个 commit。
