---
title: 一篇ai写的学习规划
categories:
  - 学习
tags:
  - CS
  - AI
date: 2026-10-15 16:19:13
cover: /img/a.jpg
description: 这是我用deepseek写的一篇cs和ai学习指南，基于本人的实际处境和学校的培养计划，是一份周期两年的基础性学习规划
---

# CS + AI 自学规划（上海交通大学 · 信息安全专业版 · 千行详细版）

> **适用对象**：上海交通大学信息安全专业本科生（从大二上学期开始，覆盖约 24 个月）  
> **整合来源**：  
> - [《ai自学规划.md》](../AI/自学ai/ai自学规划.md)  
> - [《AI工具自学规划.md》](../AI/自学ai/AI工具自学规划.md)  
> - [《AI工具大全.md》](../AI/自学ai/AI工具大全.md)  
> - [《cs自学规划.md》](../CS/自学cs/cs自学规划.md)  
> - [《信息安全指南.md》](../CS/自学cs/信息安全指南.md)  
> - 《2025 信息安全专业培养方案》  
>
> **总体目标**：在完成信息安全专业课的同时，补齐 CS 核心能力（系统、算法、工程）与 AI 核心能力（数学、机器学习、深度学习、大模型应用），并把「安全 × AI」打造为差异化竞争力。  
>
> **验证原则**：以项目验证能力，以输出倒逼输入。宁可少学一门课，不可少做一个可运行、可演示、可复盘的作品。

---

## 目录
- [一、总体路线图（24 个月）](#一总体路线图24个月)
- [二、核心原则与风险控制](#二核心原则与风险控制)
- [三、环境搭建与基础设施](#三环境搭建与基础设施)
- [四、CS 主线：计算机科学基础](#四cs-主线计算机科学基础)
- [五、AI 主线：从数学到应用](#五ai-主线从数学到应用)
- [六、安全主线：信息安全专业强化](#六安全主线信息安全专业强化)
- [七、旗舰项目路线图](#七旗舰项目路线图)
- [八、时间表：结合上海交大信息安全培养方案的学期映射](#八时间表结合上海交大信息安全培养方案的学期映射)
- [九、每周学习节奏与时间管理](#九每周学习节奏与时间管理)
- [十、工具 / 资源总览](#十工具--资源总览)
- [十一、参考培养方案摘录与自学取舍（内部参考）](#十一参考培养方案摘录与自学取舍内部参考)
- [十二、风险与自检清单（季度回顾）](#十二风险与自检清单季度回顾)
- [十三、最终目标与成果清单（24 个月后）](#十三最终目标与成果清单24个月后)
- [十四、CS 主线补充细则：如何把课程内化为能力](#十四cs-主线补充细则如何把课程内化为能力)
- [十五、AI 主线补充细则：大模型时代的学习路径](#十五ai-主线补充细则大模型时代的学习路径)
- [十六、安全主线补充细则：从 CTF 到真实漏洞](#十六安全主线补充细则从-ctf-到真实漏洞)
- [十七、课程替代方案：不同兴趣方向的自学路线](#十七课程替代方案不同兴趣方向的自学路线)
- [十八、简历与求职准备](#十八简历与求职准备)
- [十九、附录：每周学习目标模板（可复制使用）](#十九附录每周学习目标模板可复制使用)
- [二十、结语](#二十结语)
- [二十一、名词速查表](#二十一名词速查表)
- [二十二、最终检查清单（每月 1 次）](#二十二最终检查清单每月-1-次)

---

## 一、总体路线图（24 个月）

### 1.1 为什么这样设计

大学二、三两年是自学最关键的窗口：

- 大二还有缓冲期，GPA 压力相对可控，适合打地基；
- 大三有实习、科研、保研等目标，需要有作品集和项目支撑；
- 信息安全专业本身与 CS、AI 高度重合，学 CS 和 AI 的同时就是在学安全。

本路线图把 **CS 主线、AI 主线、安全主线** 并行推进，并用“旗舰项目”串起来，避免出现“学了很多却没有产出”的状态。

### 1.2 两年四个阶段

```text
【第一阶段】第 0–6 个月  大二上 ~ 寒假
目标：CS 地基 + AI 入门
CS：CS61A（Python 编程与抽象）、CSAPP 前 5 章（数据、汇编、机器码、栈）
AI：线性代数、概率统计、Python 数据栈（numpy/pandas/matplotlib）
安全：密码学基础 + CryptoHack 入门 + 建立笔记体系
产出：CLI 工具 + 数学笔记 + CryptoHack 50+ 题

【第二阶段】第 6–12 个月 大二下 ~ 暑假
目标：系统能力 + 机器学习
CS：CS61B / 6.006（数据结构与算法）、CSAPP 后 6~9 章（链接、异常、并发）
AI：机器学习基础（线性回归、逻辑回归、决策树、SVM、聚类、评估）
安全：Web 安全基础（HTTP、Burp、OWASP Top10、SQLi / XSS）
产出：完整算法笔记 + 1 个 ML 小项目 + 5 篇 Web 安全 writeup

【第三阶段】第 12–18 个月 大三上 ~ 寒假
目标：深度学习 + 大模型应用 + 项目
CS：CS144（计算机网络）、CMU 15-445 选做（数据库）
AI：深度学习（CNN/RNN/Transformer）、PyTorch、大模型 RAG/Agent
安全：二进制安全入门（PWN、逆向）、AI 安全初步
产出：旗舰项目 v1 + 复现 1 篇论文 + 竞赛经历

【第四阶段】第 18–24 个月 大三下 ~ 暑假
目标：旗舰项目 2.0 + 作品集 + 实习/保研准备
CS：系统设计、分布式基础（6.5840 选做）
AI：MLOps、部署、评估、优化
安全：红队 / 蓝队 / 合规专项，AI 安全作品
产出：旗舰项目 2.0 + 个人网站 + 简历 + 20 篇高质量文章
```

### 1.3 主线时间分配

| 阶段 | CS | AI | 安全 | 项目 | 其他 |
|---|---|---|---|---|---|
| 第 0–6 个月 | 40% | 30% | 20% | 5% | 5% |
| 第 6–12 个月 | 35% | 30% | 20% | 10% | 5% |
| 第 12–18 个月 | 20% | 40% | 20% | 15% | 5% |
| 第 18–24 个月 | 20% | 30% | 30% | 25% | 5% |

---

## 二、核心原则与风险控制

### 2.1 学习原则

1. **完成大于完美**：一个能跑的 Demo 好过十个没完成的课程。
2. **课程不是终点**：公开课的 Lab 和 Project 才是核心资产。
3. **项目驱动**：每个阶段至少有一个可展示物。
4. **输出倒逼输入**：每周至少写 1 篇 300 字以上的学习记录。
5. **安全前提**：一切实验在授权环境、本地虚拟机、CTF 平台上进行。

### 2.2 常见风险与应变

| 风险 | 表现 | 对策 |
|---|---|---|
| GPA 下降 | 自学术科失衡 | 每周只留固定自习时间，删减非核心任务 |
| 课程囤积 | 收藏一堆课却没学 | 同一时间只保留 1–2 门主课 |
| 只学不练 | 视频看了无数，代码没写 | 任何课程必须配有 Lab/Project |
| 方向漂移 | 今天学安全，明天学 CV | 每半年做一次复盘，只保留一个主线 |
| 项目烂尾 | 项目做到一半放弃 | 项目范围越小越好，保持可交付 |

---

## 三、环境搭建与基础设施

### 3.1 操作系统与终端

- 推荐使用 [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) 或直接安装 [Ubuntu](https://ubuntu.com/desktop/)。
- 常用命令：`cd`、`ls`、`pwd`、`touch`、`mkdir`、`rm`、`mv`、`cp`、`cat`、`less`、`head`、`tail`。
- 文本处理：`grep`、`rg`、`sed`、`awk`、`sort`、`uniq`、`wc`。
- 网络工具：`curl`、`wget`、`ping`、`ssh`、`scp`、`nc`、`nslookup`。
- 系统工具：`ps`、`top`、`htop`、`df`、`du`、`free`、`lsof`、`strace`。

### 3.2 编辑器

- 主编辑器：VS Code。
- 终端编辑器：vim / nano，至少掌握 `i`、`Esc`、`:wq`、`:q!`、`dd`、`yy`、`p`。
- 对应任选编辑器插件：Python、Pylance、flake8、black、GitLens。

### 3.3 Git 与 GitHub

学习 [Pro Git](https://git-scm.com/book/zh/v2)：

- Git 基础：`init`、`add`、`commit`、`status`、`log --oneline`。
- 分支：`branch`、`checkout -b`、`merge`、`rebase`。
- 远程：`remote add`、`push`、`pull`、`fetch`。
- 协作：Pull Request、code review、issue。

### 3.4 Docker

学习 [Docker Docs](https://docs.docker.com/)：

- `docker run`、`ps`、`stop`、`rm`、`logs`。
- `docker build`、`docker-compose.yml`。
- 常用安全靶场：DVWA、OWASP Juice Shop、Metasploitable。

### 3.5 知识管理

- 使用 Obsidian / Notion 建立自己的知识库。
- 记录模板：目标、资源、进度、产出、卡点。
- 写作平台：GitHub Pages / Hexo / Typora 均可。

---

---

## 四、CS 主线：计算机科学基础

### 阶段 0：工具与学习系统（第 1–2 周）

#### 4.0.1 学习目标

- 建立 Linux / WSL 开发环境。
- 掌握 Git 和终端工作流。
- 创建自己的知识管理系统。

#### 4.0.2 具体任务

1. 安装 [WSL](https://learn.microsoft.com/en-us/wsl/install) 或 Ubuntu，配置终端、Windows Terminal、SSH Key。
2. 学会：

```bash
cd ~
mkdir projects
touch README.md
cat /etc/os-release
```

3. 学习 git 基础操作，并将本地仓库推送到 GitHub。
4. 建立学习仓库目录结构：

```text
cs-learning/
├── README.md
├── learning-log.md
├── notes/
│   ├── cs61a/
│   ├── cs61b/
│   ├── os/
│   ├── ai/
│   └── security/
├── projects/
│   ├── cli/
│   ├── ml/
│   └── security/
└── writeups/
    ├── crypto/
    ├── web/
    └── pwn/
```

#### 4.0.3 交付物与 DoD

- [ ] 能在终端完成日常文件操作
- [ ] 能用 Git 创建 repo、提交、push、解决冲突
- [ ] 学习日志已有第一篇周记
- [ ] 能解释 PATH、HOME、进程、环境变量

---

### 阶段 1：程序设计与抽象（第 1–3 个月）

#### 4.1.1 目标

掌握 Python 编程、函数式抽象、面向对象、基础测试，能够独立读完一本编程书并完成 500 行以上的代码。

#### 4.1.2 推荐课程

- [CS61A: Structure and Interpretation of Computer Programs](https://cs61a.org/)
- [Composing Programs](https://www.composingprograms.com/)
- [Python Official Tutorial](https://docs.python.org/3/tutorial/)
- [Automate the Boring Stuff](https://automatetheboringstuff.com/)
- [CS50P](https://cs50.harvard.edu/python/) 或任意一门 Python 入门课

#### 4.1.3 12 周详细安排

| 周次 | 主题 | 练习 | 输出 |
|---|---|---|---|
| 1 | 表达式、变量、函数 | 写 `sum_to_n`、`is_prime` | 在 REPL 中操作 |
| 2 | 循环、条件、字符串格式化 | 写一个命令行计算器 | 小工具 |
| 3 | 函数设计、测试 | 给计算器写 pytest 用例 | 测试脚本 |
| 4 | 递归、树递归 | 汉诺塔、组合数 | 算法笔记 |
| 5 | 高阶函数 | `map`/`filter`/`reduce` 练习 | 代码仓库 |
| 6 | 数据抽象、tuple、list | 手写向量运算 | 简单数学工具 |
| 7 | 可变性、dict、set | 统计词频 | 代码 |
| 8 | 面向对象 | 设计 `Task` / `Note` 类 | 类设计 |
| 9 | 迭代器/生成器 | yield 实现股票数据流 | 可复用模块 |
| 10 | 异常处理、调试 | 给程序加日志、错误处理 | README |
| 11 | 综合项目 | 命令行备忘录 | 发布 repo |
| 12 | 复习 + LeetCode easy | 30 题 | 刷题记录 |

#### 4.1.4 项目：个人知识库 CLI

功能建议：

- 支持添加 / 搜索 / 删除条目；
- 用 JSON 或 SQLite 持久化；
- 标签、关键词、时间排序；
- 命令行参数解析（argparse/click）；
- 单元测试和 README。

#### 4.1.5 DoD

- [ ] 完成 CS61A 至少 2 个官方 Project
- [ ] 面向对象 + 测试 + 命令行项目已完成
- [ ] 能解释闭包、装饰器、生成器和异常处理

---

### 阶段 2：数据结构与算法（第 4–6 个月）

#### 4.2.1 目标

理解复杂度、常见数据结构、经典算法，能独立应对笔试和面试中的中等难度题目。

#### 4.2.2 课程与资源

- [CS61B: Data Structures](https://cs61b.org/)
- [MIT 6.006 Introduction to Algorithms](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/)
- [LeetCode](https://leetcode.cn/) / [NeetCode](https://neetcode.io/)
- [CP-Algorithms](https://cp-algorithms.com/) 作为参考手册

#### 4.2.3 知识点清单

1. **复杂度**：最好/最坏/平均情况，大 O，空间复杂度。
2. **数据结构**：
   - 数组、链表、栈、队列、双端队列；
   - 哈希表、冲突解决；
   - 二叉搜索树、平衡树（概念）；
   - 堆、优先队列；
   - 并查集；
   - Trie；
   - 图（邻接矩阵、邻接表）。
3. **算法**：
   - 排序：插入、选择、归并、快排、堆排序；
   - 搜索：二分、DFS、BFS；
   - 图算法：最短路（Dijkstra）、最小生成树（概念）；
   - 动态规划：背包、最长公共子序列、编辑距离；
   - 回溯：全排列、N 皇后。

#### 4.2.4 刷题节奏建议

- 每天 1–2 题，记录到表格：难度、思路、复杂度、错误点。
- 优先做 Top 100 热题前 50。
- 每周末做一次复盘，重写错题。

#### 4.2.5 DoD

- [ ] 完成 50+ 道算法题，至少覆盖 5 种数据结构
- [ ] 能实现并解释快速排序和 Dijkstra 算法
- [ ] 常用数据结构手写实现并有测试

---

### 阶段 3：系统编程和计算机组成（第 7–9 个月）

#### 4.3.1 目标

理解 C 语言、汇编、内存布局、链接过程和系统调用，为安全课程的逆向、Pwn 打基础。

#### 4.3.2 资源

- [CSAPP](https://csapp.cs.cmu.edu/)：重点第 1–9 章
- [Beej's Guide to C](https://beej.us/guide/bgc/)
- [Compiler Explorer](https://godbolt.org/)
- [GDB Documentation](https://sourceware.org/gdb/documentation/)
- [Valgrind Documentation](https://valgrind.org/docs/manual/quick-start.html)

#### 4.3.3 学习内容

1. **C 基础**：数组、指针、结构体、字符串处理。
2. **内存管理**：malloc/free、堆栈、内存泄漏、越界。
3. **汇编基础**：x86-64 指令、寄存器、栈帧、调用约定。
4. **编译链接**：预处理、编译、汇编、链接、ELF。
5. **调试**：gdb、breakpoints、bt、watch、ASan、Valgrind。

#### 4.3.4 实践

- 用 C 重写之前写过的 Python 小工具。
- 完成 CSAPP Data Lab 或 Bomb Lab 的部分题目。
- 阅读简单开源项目源码，画出模块图。

#### 4.3.5 DoD

- [ ] 理解指针、内存布局、malloc/free
- [ ] 能用 gdb 定位段错误
- [ ] 完成至少 3 个经典 Lab

---

### 阶段 4：操作系统（第 8–11 个月）

#### 4.4.1 资源

- [MIT 6.S081](https://pdos.csail.mit.edu/6.S081/2021/)
- [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/)
- [xv6 源码](https://github.com/mit-pdos/xv6-riscv)

#### 4.4.2 内容清单

1. 系统调用：fork、exec、wait、pipe、dup。
2. 进程：进程状态、上下文切换、调度。
3. 线程：用户级与内核级、同步、互斥、死锁。
4. 虚拟内存：分页、页表、页错误、内存映射。
5. 文件系统：inode、目录、磁盘布局、持久化。

#### 4.4.3 实践

- 在 xv6 中完成 Lab（syscall、pgtbl、threads、util）。
- 写一个 mini-shell，支持内置命令、外部命令、管道。
- 阅读《程序员的自我修养》相关章节。

#### 4.4.4 DoD

- [ ] 完成 xv6 至少 3 个 Lab
- [ ] 能解释 fork 之后的内存复制行为
- [ ] 能解释死锁四个条件及如何避免

---

### 阶段 5：计算机网络（第 11–14 个月）

#### 4.5.1 资源

- [CS144](https://cs144.github.io/)
- [UDP/TCP 指南](https://beej.us/guide/bgnet/)
- [MDN HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- 必要时阅读 [Computer Networking: A Top-Down Approach](https://gaia.cs.umass.edu/kurose_ross/index.php)

#### 4.5.2 内容清单

1. HTTP/1.1、HTTPS、REST 基础。
2. TCP 三次握手、四次挥手、拥塞控制。
3. UDP 与可靠传输区别。
4. DNS 解析、常见记录类型。
5. TLS 握手、证书链。
6. 常用工具：`curl`、`tcpdump`、`wireshark`、`dig`、`nc`。

#### 4.5.3 实践

- 用 Python/Go 写一个 HTTP server，支持静态文件与路由。
- 抓包分析一次完整 HTTP 请求。
- 写一篇笔记：输入 URL 后发生了什么？（DNS → TCP → TLS → HTTP → 渲染）

#### 4.5.4 DoD

- [ ] 能解释 DNS 解析步骤
- [ ] 能描述一次 HTTPS 请求的完整链路
- [ ] 能写一个支持 GET 的简单 HTTP server

---

### 阶段 6：数据库与后端工程（第 14–17 个月）

#### 4.6.1 资源

- [CMU 15-445](https://15445.courses.cs.cmu.edu/fall2023/)
- PostgreSQL / MySQL 官方文档
- [SQLBolt](https://sqlbolt.com/)

#### 4.6.2 内容清单

1. 关系模型、SQL 查询、聚合、连接。
2. 索引、B+ Tree、哈希索引。
3. 事务：ACID、隔离级别、锁。
4. 数据库设计：范式、ER 图、反范式。
5. 后端：FastAPI/Flask、认证、日志、权限。

#### 4.6.3 实践

- 给旗舰项目加一个 PostgreSQL 数据层。
- 写 API：CRUD、分页、搜索。
- 部署 Docker 容器 + `docker-compose.yml`。

#### 4.6.4 DoD

- [ ] 能设计一个带索引和事务的表结构
- [ ] API 已完成并可通过 curl 测试
- [ ] 项目可在 Docker 中运行

---

## 五、AI 主线：从数学到应用

> AI 是本次自学规划的另一条平行主线，重点不是“看教程”，而是建立数学、算法、模型、工程四层能力。信息安全专业学习 AI 时，建议同步思考安全视角：对抗样本、模型隐私、滥用检测，这些会在第九部分集中展开。

### 5.0 AI 主线总体结构

| 阶段 | 主题 | 时长 | 产物 | 对应资源 |
|------|------|------|------|----------|
| A0 | 数学基础 | 第 1–5 个月 | 数学笔记 + 公式推导库 | [3Blue1Brown](https://www.3blue1brown.com/) / [Khan Academy](https://www.khanacademy.org/) |
| A1 | 机器学习基础 | 第 6–10 个月 | sklearn 项目 3–5 个 | [吴恩达机器学习](https://www.coursera.org/learn/machine-learning) |
| A2 | 深度学习基础 | 第 10–15 个月 | PyTorch 模型 + 训练脚本 | [D2L](https://zh-v2.d2l.ai/) / [PyTorch](https://pytorch.org/tutorials/) |
| A3 | NLP / 大模型 | 第 15–20 个月 | LLM 微调 / RAG 项目 | [Hugging Face](https://huggingface.co/learn) / [LLM 实战](https://github.com/datawhalechina/llm-course) |
| A4 | AI 工程与安全 | 第 20–24 个月 | 部署 + 对抗攻防实验 | [OLLAMA](https://ollama.com/) / [HiddenLayer](https://hiddenlayer.com/) / [对抗鲁棒性](https://adversarial-robustness-toolbox.readthedocs.io/) |

### 5.1 A0：数学基础（第 1–5 个月）

#### 5.1.1 为什么先学数学

AI 的算法本质上是线性代数、概率统计和最优化方法叠加在数据上。不把数学基础打牢，后面看论文会非常吃力，尤其是安全领域需要读大量涉及对抗样本、梯度、期望收益的论文。

#### 5.1.2 学习内容

1. **线性代数**
   - 向量、矩阵、线性变换。
   - 矩阵乘法、秩、行列式、特征值/特征向量。
   - 奇异值分解（SVD）、PCA 背后的数学。
   - 推荐：[3Blue1Brown 线性代数](https://www.3blue1brown.com/topics/linear-algebra)、[MIT 18.06](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)。
   - 额外资源：[Khan Academy 线性代数](https://www.khanacademy.org/math/linear-algebra)。

2. **微积分与优化**
   - 导数、偏导、链式法则。
   - 梯度、方向导数、极值。
   - 梯度下降、Batch / Mini-batch / SGD。
   - 推荐：[Calculus Made Easy](https://calculusmadeeasy.org/)、[梯度下降可视化](https://www.joshwcomeau.com/library/vectors-in-css/)。
   - 需要做推导的部分：反向传播中的链式法则。

3. **概率论与统计**
   - 随机变量、分布、期望、方差。
   - 条件概率、贝叶斯公式。
   - 极大似然估计、正态分布、大数定律。
   - 推荐：[Harvard Stat110](https://projects.iq.harvard.edu/stat110)、[Khan Academy 概率](https://www.khanacademy.org/math/statistics-probability)。

4. **信息论（安全视角尤其重要）**
   - 熵、联合熵、互信息。
   - 交叉熵与 KL 散度。
   - 与机器学习损失函数的关系：交叉熵损失。
   - 从安全角度理解：信息量、不确定性、信道容量与隐写分析。
   - 推荐：[MIT 6.004 信息论讲稿](https://ocw.mit.edu/courses/6-004-computation-structures-spring-2017/)、[DeepLearning Book](https://www.deeplearningbook.org/)。

#### 5.1.3 每周安排（建议 4–6 小时/周）

| 周 | 主题 | 输出 |
|----|------|------|
| 1–2 | 线性代数：向量 / 矩阵运算 | 手写推导 30 题 |
| 3–4 | 线性代数：特征值 / 对角化 | 用 NumPy 验证特征分解 |
| 5–6 | 微积分：导数 / 梯度 | 手推线性回归梯度 |
| 7–8 | 优化：梯度下降 / SGD | 写一个 mini SGD 演示 |
| 9–10 | 概率：分布 / 条件概率 | 贝叶斯分类小实验 |
| 11–12 | 信息论：熵 / KL | 写写熵计算脚本 |
| 13–15 | 矩阵应用：SVD / PCA | 用 sklearn 对图片做 PCA |
| 16–20 | 复习 + 建立公式库 | 用 LaTeX 整理公式库 |

#### 5.1.4 DoD

- [ ] 能不用参考书写出反向传播链式法则推导
- [ ] 能解释 PCA 与 SVD 的关系
- [ ] 能自己推导线性回归的闭式解
- [ ] 有一个包含 50+ 公式的 LaTeX / MathJax 笔记库

### 5.2 A1：机器学习基础（第 6–10 个月）

#### 5.2.1 目标

理解机器学习基本流程：数据清洗 → 特征工程 → 建模 → 评估 → 部署。掌握常用模型，不追求深度，但保证能独立完成一个端到端项目。

#### 5.2.2 推荐课程

- [吴恩达机器学习](https://www.coursera.org/learn/machine-learning)：经典入门，内容全面。
- [Kaggle 微课](https://www.kaggle.com/learn)：机器学习、Python、Pandas、SQL。
- [Datawhale 机器学习](https://github.com/datawhalechina/leeml-notes)：中文笔记，适合快速扫读。
- 书：[Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/)。

#### 5.2.3 知识点清单

1. 回归：线性回归、岭回归、Lasso。
2. 分类：逻辑回归、kNN、决策树、随机森林。
3. 聚类：K-Means、层次聚类、DBSCAN。
4. 降维：PCA、t-SNE。
5. 评估：accuracy / precision / recall / F1 / ROC-AUC。
6. 偏差与方差、过拟合、交叉验证。
7. 特征工程：标准化、编码、缺失值处理。
8. 模型保存与部署：pickle、onnx、FastAPI 接口。

#### 5.2.4 实战项目建议

1. **泰坦尼克号**（Kaggle）：完整走一遍分类流程。
2. **房价预测**（Kaggle）：回归问题 + 特征工程。
3. **垃圾邮件分类**（本地数据）：朴素贝叶斯 + TF-IDF。
4. **恶意软件检测初探**（安全 × AI）：用公开恶意软件数据集做分类（参考 [EMBER](https://github.com/elastic/ember)）。

#### 5.2.5 DoD

- [ ] 能独立完成 Kaggle 上的一个入门比赛并提交结果
- [ ] 能解释评估指标在不同场景下的取舍
- [ ] 能说出过拟合的常见原因和解决方法
- [ ] 至少有一个模型部署到本地 / Docker

### 5.3 A2：深度学习基础（第 10–15 个月）

#### 5.3.1 推荐课程

- [斯坦福 CS231N](https://cs231n.stanford.edu/)：CNN + 视觉任务，工程性强。
- [Stanford CS224N](https://web.stanford.edu/class/cs224n/)：NLP 与词向量。
- [动手学深度学习 D2L](https://zh-v2.d2l.ai/)：配合代码学习，最实用。
- [PyTorch 官方教程](https://pytorch.org/tutorials/)：不必全看，按需检索。
- 书：[Deep Learning（花书）](https://www.deeplearningbook.org/)：作为参考手册。

#### 5.3.2 核心概念

1. 神经网络、反向传播、激活函数。
2. 损失函数：CrossEntropy、MSE、Triplet Loss。
3. 优化器：SGD、Adam、RMSProp。
4. 正则化：Dropout、Weight Decay、BatchNorm。
5. CNN：卷积、池化、ResNet、经典架构。
6. RNN / LSTM：序列建模。
7. Transformer：Self-Attention、多头注意力，为后续 LLM 打基础。
8. 训练技巧：学习率调度、早停、梯度裁剪、混合精度。

#### 5.3.3 实验安排

- 第 1–2 周：用 PyTorch 从零实现一个两层 MLP 做 MNIST。
- 第 3–4 周：用 torchvision 训练 ResNet 做 CIFAR-10。
- 第 5–6 周：实现注意力机制，读 [Attention Is All You Need](https://arxiv.org/abs/1706.03762) 并复述论文思想。
- 第 7–8 周：训练一个小型 Transformer 做文本分类。
- 第 9–12 周：阅读 1–2 篇论文并复现代码（如 BERT / CNN 攻击）。

#### 5.3.4 DoD

- [ ] 能解释反向传播的数学流程
- [ ] 能独立用 PyTorch 搭建和训练一个 CNN
- [ ] 能讲清 Transformer 中自注意力机制的计算步骤
- [ ] 积累了至少 3 个可复现的训练实验记录

### 5.4 A3：NLP / 大语言模型（第 15–20 个月）

#### 5.4.1 目标

从传统的词向量过渡到 Transformer / LLM，能够使用开源模型完成微调、RAG、Agent 等应用；同时具备阅读 LLM 安全论文的基础能力。

#### 5.4.2 学习路径

1. 文本表示：One-hot → Word2Vec → BERT 嵌入。
2. 语言模型：GPT / LLaMA / Qwen 等系列演进。
3. Transformers 库（HuggingFace）：tokenizer、dataset、pipeline。
4. 微调：PEFT 方法（LoRA / QLoRA）、指令微调。
5. RAG：向量数据库（Chroma / FAISS / Milvus）、Embedding、Retrieval。
6. Agent：Function Calling、ReAct、Tool use。
7. 评估：BLEU / ROUGE / 人工评估 / 对齐评测。
8. 效率：量化（GGUF / AWQ）、vLLM 推理、Ollama 本地部署。

#### 5.4.3 实战项目

- 用 [LlamaIndex](https://www.llamaindex.ai/) 或 [LangChain](https://www.langchain.com/) 做一个知识库问答机器人，主题可定为“安全文档问答”。
- 用 [Ollama](https://ollama.com/) 在本地跑一个 7B 模型，做提示词注入检测实验。
- 用 [Hugging Face datasets](https://huggingface.co/datasets) 找一个中文数据集，做 LoRA 微调，尝试 [firework LoRA 示例](https://github.com/microsoft/LoRA)。

#### 5.4.4 大模型安全文档推荐

- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [DSPy 安全提示工程](https://github.com/stanfordnlp/dspy)
- [arXiv: Universal and Transferable Attacks](https://arxiv.org/abs/2307.15043)

#### 5.4.5 DoD

- [ ] 能解释 RAG 的基本流程和关键组件
- [ ] 成功在本地部署一个开源 LLM 并完成 API 调用
- [ ] 能写出 2–3 种常见的提示词注入攻击样例
- [ ] 完成一个基于向量数据库的知识库问答项目

### 5.5 A4：AI 工程与安全交叉（第 20–24 个月）

#### 5.5.1 方向选择

| 方向 | 说明 | 代表工具/论文 |
|------|------|----------------|
| 对抗样本 | 让模型在微小扰动下犯错 | [Adversarial Robustness Toolbox](https://github.com/Trusted-AI/adversarial-robustness-toolbox) / [FGSM](https://arxiv.org/abs/1412.6572) |
| 模型后门 | 训练阶段注入隐藏行为 | [BadNets](https://arxiv.org/abs/1708.06733) / [Trojan](https://arxiv.org/abs/1707.08945) |
| 数据投毒 | 影响模型训练结果 | [Nightshade](https://github.com/genie-Platform/nightshade) |
| 提示注入 | 针对 LLM 的应用层攻击 | [Gandalf 游戏](https://gandalf.lakera.ai/) / [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/) |
| 模型窃取 | 通过查询 API 复制模型 | [Knockoff Nets](https://arxiv.org/abs/1812.02766) |
| 可解释性 | 理解模型内部行为 | [SHAP](https://shap.readthedocs.io/) / [Captum](https://captum.ai/) |

#### 5.5.2 第一周计划

- 了解什么是对抗样本：给猫图加一点噪声，模型识别成吉他。
- 阅读 FGSM 的数学推导。
- 跑一个简单的 FGSM 攻击 demo。

#### 5.5.3 终极目标：写一篇短报告或做一个 Demo

- 选题建议：对 BERT 做文本对抗攻击 / 对 CNN 做 PGD 攻击 / 对本地 LLM 做提示注入防御检测。
- 输出：GitHub 仓库 + README + 实验报告，可作为申请方向或求职作品。

#### 5.5.4 DoD

- [ ] 能解释对抗攻击的主要类型和原理
- [ ] 能复现至少一种对抗攻击
- [ ] 能说出 3 种模型防御手段
- [ ] 完成一篇安全 × AI 的实验报告

---

## 六、安全主线：信息安全专业强化

> 安全主线与校内课程互补：校内课程偏理论和体系，自学主线偏实践和攻防。建议按照“Web 安全 → 二进制/逆向 → 密码学 → 系统安全 → 安全自动化”的顺序展开。AI 部分学得越深，越能读到安全领域的前沿论文，两条线会逐渐交叉。

### 6.1 安全能力层次模型

| 层级 | 能力 | 对应内容 | 进阶级 |
|------|------|----------|--------|
| L1 | 基础能力 | 网络、Linux、编程、协议 | PicoCTF 入门 |
| L2 | Web 安全 | OWASP 10 项漏洞 | PortSwigger Web Security Academy |
| L3 | 二进制与逆向 | 汇编、缓冲区溢出、逆向工程 | Pwn.college / 攻防世界 |
| L4 | 密码学 | 古典、现代、公钥、协议 | Cryptohack |
| L5 | 系统安全 | 操作系统、权限、内核 | 0ops、CTF 系统题目 |
| L6 | 安全×AI | 对抗样本、模型攻击、LLM 安全 | 论文 + 工程项目 |

### 6.2 阶段 1：网络与 Linux 基础（第 1–4 个月，与 CS 主线并行）

#### 6.2.1 目标

- 熟练掌握 Linux 基础命令、文件权限、进程管理、网络工具。
- 能读懂 TCP/IP 包，会使用 Wireshark。
- 会写简单的 Bash/Python 脚本。

#### 6.2.2 内容

1. Linux:
   - 常用命令：ind、grep、wk、sed、ssh、scp。
   - 权限模型：chmod、sudo、setuid。
   - 软链接/硬链接、/proc、/sys。
2. 网络:
   - 子网划分、DNS、HTTP、SMTP。
   - 用 ping、
slookup、dig、	raceroute 排查。
   - Wireshark 抓包分析。
3. 脚本:
   - Bash 脚本能否完成自动化任务？
   - Python 能用标准库读写文件、发 HTTP 请求、解析 JSON。

#### 6.2.3 项目

- 写一个端口扫描器（注意仅用于自己授权的目标）。
- 用 Wireshark 分析手机连接 https 网站时的 TLS 握手。

#### 6.2.4 DoD

- [ ] 能在 Linux 上只凭命令行完成日常开发
- [ ] 能用 Python 写代理脚本做 HTTP 请求抓取
- [ ] 能用 Wireshark 识别三次握手、TLS 版本

### 6.3 阶段 2：Web 安全（第 5–9 个月）

#### 6.3.1 推荐资源

- [PortSwigger Web Security Academy](https://portswigger.net/web-security)：最系统的 Web 安全训练平台。
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)：可本地部署的漏洞靶场。
- 书：[Web Hacking 101](https://www.hackerone.com/resources/web-hacking-101)。

#### 6.3.2 必须掌握的漏洞类型

1. **SQL 注入**：绕过登录、联合查询、报错注入。
2. **XSS**：存储型、反射型、DOM 型。
3. **CSRF**：跨站请求伪造的防御。
4. **SSRF / 文件上传**：权限绕过和服务端请求伪造。
5. **认证缺陷**：Session 固定、弱口令、JWT 漏洞。
6. **命令注入**：利用系统命令执行。
7. **访问控制**：水平越权、垂直越权。

#### 6.3.3 实战训练

- 完成 PortSwigger 的 All labs（至少 30 个）。
- 在 Juice Shop 上完成 10 道难度递增的题。
- 搭建 DVWA 靶场做 SQL 注入实验。
- 用 Burp Suite 抓包分析一个真实网站的登录流程（注意仅授权环境）。

#### 6.3.4 DoD

- [ ] 能独立完成 PortSwigger SQLi 模块全部实验室
- [ ] 能在 Juice Shop 攻下 5 个不同漏洞
- [ ] 能写出 3 种常见漏洞的修复建议

### 6.4 阶段 3：二进制安全与逆向（第 8–13 个月）

#### 6.4.1 推荐资源

- [Pwn.college](https://pwn.college/)：覆盖从入门到进阶的二进制漏洞利用。
- [Attack Lab](https://csapp.cs.cmu.edu/)：缓冲区溢出实验。
- [Reverse Engineering for Beginners](https://beginners.re/)：逆向入门。
- [Crackmes.one](https://crackmes.one/)：逆向练习题。
- [Ghidra](https://ghidra-sre.org/) / [IDA](https://hex-rays.com/ida-pro/) / [Radare2](https://www.radare.org/)。

#### 6.4.2 学习内容

1. **汇编基础**
   - x86 / x64 基础：寄存器、栈帧、调用约定。
   - 常见指令：mov、lea、push、pop、call、
et。
2. **缓冲区溢出**
   - 栈溢出原理、覆盖返回地址。
   - 保护机制：NX、ASLR、canary、PIE。
   - ROP 基础。
3. **逆向工程**
   - 用 Ghidra 反编译简单 C 程序。
   - 分析导入表、字符串、交叉引用。
   - 通过 crackme 练习。

#### 6.4.3 练习安排

- 完成 Pwn.college 模块 1–5（程序交互、代码注入、ROP）。
- 完成 CSAPP Attack Lab。
- 解开 10 个 crackme。

#### 6.4.4 DoD

- [ ] 能看懂简单的 x86 汇编
- [ ] 能在关闭 protections 的条件下完成栈溢出利用
- [ ] 能用 Ghidra 分析一个未知二进制的基本逻辑

### 6.5 阶段 4：密码学基础（第 10–14 个月）

#### 6.5.1 推荐资源

- [Cryptohack](https://cryptohack.org/)：互动式密码学题解平台。
- 书：[Introduction to Modern Cryptography](https://www.cs.umd.edu/~jkatz/imc.html)（Katz & Lindell）。
- 课程：[Coursera Cryptography I](https://www.coursera.org/learn/crypto)。

#### 6.5.2 知识点

1. 对称加密：AES、分组模式（ECB/CBC/GCM）。
2. 非对称加密：RSA、DH、ECC。
3. 哈希函数：SHA-2/SHA-3、碰撞攻击。
4. 数字签名与证书。
5. 密码学协议：TLS、SSH、Kerberos。
6. 后量子密码概念（了解即可）。

#### 6.5.3 项目

- 用 Python 实现 AES-CBC 加解密。
- 在 Cryptohack 完成 50+ 道题。
- 用 Wireshark 分析 TLS 握手密码套件。

#### 6.5.4 DoD

- [ ] 能解释 AES-CBC 与 AES-GCM 的区别
- [ ] 能说明 RSA 加解密的基本原理
- [ ] 能独自完成 Cryptohack 入门到中级模块

### 6.6 阶段 5：系统安全与实战（第 14–18 个月）

#### 6.6.1 推荐资源

- [TryHackMe](https://tryhackme.com/)：适合系统化平台。
- [HackTheBox](https://www.hackthebox.com/)：实战靶机。
- [MITRE ATT&CK](https://attack.mitre.org/)：理解攻击链。
- [红队技术手册](https://github.com/redteamsecurity/Red-Team-TTPs)

#### 6.6.2 内容

- Linux 提权：SUID、sudo 配置、内核漏洞。
- 横向移动：SSH 密钥、凭证复用。
- 日志分析：auth.log、web server 日志。
- 应急响应：定位入侵行为。
- 防火墙与 IDS/IPS 基础。

#### 6.6.3 DoD

- [ ] 能在 TryHackMe 完成 10 台中高级靶机
- [ ] 能写一份报告：攻击链 + 防御建议
- [ ] 了解 MITRE ATT&CK 的主要战术阶段

### 6.7 阶段 6：安全自动化与工具开发（第 18–24 个月）

#### 6.7.1 方向可选

- 安全工具开发：用 Python/Go 写扫描器、插件。
- 自动化检测：从日志中自动化提取威胁指标。
- Franework：给 [Nuclei](https://github.com/projectdiscovery/nuclei) 写模板。
- 威胁情报：从公开源抓取并关联 IOC。

#### 6.7.2 推荐项目

- 编写一个插件化的端口扫描/配置检查工具。
- 用自然语言处理做一个安全日志摘要工具（结合 AI）。
- 搭建一套家庭“安全实验室”：攻击机 + 靶场 + 日志分析。

#### 6.7.3 DoD

- [ ] 有一个公开的 GitHub 安全工具项目（哪怕 500 行代码）
- [ ] 能自动化筛查一份日志中的异常行为
- [ ] 说出至少 5 个常用的安全自动化平台/工具

---

## 七、旗舰项目路线图

> 自学与课程最大的不同是：必须有作品。两年的时间里，建议围绕一个“旗舰项目”持续迭代，用它把 CS、AI、安全三条主线串起来。项目选择不必过早决定，但最好在第 6 个月时确定，并持续迭代到第 24 个月。

### 7.1 项目选择建议

| 方向 | 项目主题 | 技术栈 | 安全/学术亮点 |
|------|----------|--------|--------------|
| AI 安全 | 对大语言模型做提示注入检测/防御 | Python、LangChain、LLM | 属于热点方向，容易写成论文 |
| 二进制安全 | 自动化漏洞挖掘工具 | C、Python、Ghidra、fuzzing | 可与开源项目结合 |
| 应用安全 | 开源 Web 应用自动化渗透测试平台 | Go、FastAPI、Docker | 易做成 Demo 演示 |
| 密码学 | 后量子签名方案性能对比实现 | Python、C | 学术性强，可投赛事 |
| 分析引擎 | 安全日志智能分析平台 | Python、Pandas、sklearn | 把 ML 和 SOC 场景结合 |

### 7.2 旗舰项目里程碑

#### 第 1–3 个月：确立方向

- 浏览 CS、AI、安全三个方向的典型项目，写下 3 个候选。
- 每个候选写 100 字“为什么是我”，并列出可行性。
- 确定一个方向，暂时不必写代码。

#### 第 4–6 个月：完成最小可行版本（MVP）

- 用最小技术栈跑通一个端到端用例。
- 例如：输入一个 URL → 爬取内容 → 提取特征 → 分类是否钓鱼。
- 发布到 GitHub，写 README。

#### 第 7–12 个月：第一个完整版本（v0.2）

- 加入 CI/CD：GitHub Actions 自动测试、构建。
- 加入 Docker 部署。
- 写单元测试、集成测试。
- 输出一篇不超过 3000 字的技术博客。

#### 第 13–18 个月：综合能力打磨

- 引入安全/AI 交叉功能：
  - 如果做 AI 安全，加入对抗训练或评估指标。
  - 如果做安全工具，加入 LLM 生成报告。
- 加入性能优化：缓存、并发、内存。
- 尝试在 GitHub 开源活动中贡献代码，提升项目可见度。

#### 第 19–24 个月：产出成果

- 总结项目：README、架构图、Demo 视频。
- 写入简历：项目背景、你的角色、量化结果。
- 投稿或比赛：CTF、Kaggle、CCF 或学校科创项目。

### 7.3 项目每周节奏模板

| 周 | 周一至周三 | 周四、周五 | 周末 |
|----|-----------|-----------|------|
| 第 1 周 | 阅读相关资料，写设计文档 | 开始关键技术调研 | 写第一个 Demo |
| 第 2 周 | 实现核心模块 | 修 bug + 补测试 | 写 README、提交 GitHub |
| 第 3 周 | 功能迭代 | 性能/安全自查 | 输出周报或博客 |
| 第 4 周 | 集成新能力 | 评估结果 | 计划下月目标 |

### 7.4 项目学习清单

- [ ] 能熟练使用 Git 分支、PR、Issue
- [ ] 了解 CI/CD 的基本概念，能用 GitHub Actions
- [ ] 写过至少 10 个单元测试
- [ ] 能画出系统架构图
- [ ] 能演示项目并解释每个环节
- [ ] 代码有 README、LICENSE、CONTRIBUTING（可选）
- [ ] 项目跑在 Docker 或云端可访问

---

## 八、时间表：结合上海交大信息安全教育培养方案的学期映射

> 该映射参考《2025 信息安全培养方案》的学分结构：通识教育 74 学分、公共课程类 64 学分、专业基础 17 学分、专业核心 41 学分、专业选修 14 学分、个性化 10 学分。自学的节奏要与课业节奏错峰，避免“自学比课业更赶”的陷阱。

### 8.1 学期总览

| 学期 | 校内重点 | 自学重点 | 自学时间预算 |
|------|----------|----------|--------------|
| 大二上（第 1 学期） | 数学基础、程序设计、专业导论 | CS61A、Linux、Git | 每周 12–16 小时 |
| 大二下（第 2 学期） | 数据结构、离散数学、密码学入门 | 算法、CS61B、Web 安全入门 | 每周 14–18 小时 |
| 大二暑假 | 无课业压力 | 集中突破：OS/CSAPP、ML 入门 | 每天 4–6 小时 |
| 大三上（第 3 学期） | 操作系统、计算机网络、密码学 | 深度学习、CTF 系统训练 | 每周 16–20 小时 |
| 大三下（第 4 学期） | 专业核心课增多 | LLM、安全 × AI、项目收尾 | 每周 14–18 小时 |
| 大三暑假 | 暂无课业压力 | 实习/竞赛/论文冲刺 | 每天 4–6 小时 |

### 8.2 大二上学期（第 1–5 个月）详细计划

#### 目标

- 编程功底：完成 CS61A（Python 入门 + 抽象）。
- 工具链：搞定 Git、GitHub、Linux 命令行、Docker 基础。
- 安全意识：搭建自己的安全实验环境。

#### 学习安排

| 周次 | CS 主线 | AI 主线 | 安全主线 |
|------|---------|---------|----------|
| 1–2 | 完成 CS61A Week1–2 | 数学：线性代数基础 | 配置 Kali / Ubuntu 练习环境 |
| 3–4 | 完成 CS61A Week3–4 | 数学：向量、矩阵 | PicoCTF 入门题 10 道 |
| 5–6 | CS61A 上机实践 + 项目 | 概率：随机变量 | Linux 权限/用户管理实验 |
| 7–8 | 完成 CS61A Week5–6 | 开始吴恩达 ML 前 2 周 | 网络基础：Wireshark |
| 9–10 | CS61A 项目收尾 | sklearn 第一个分类项目 | Web 安全概述 |
| 11–12 | 复习 + 整理笔记 | 机器学习线性模型 | 阅读 OWASP Top 10 |
| 13–15 | 进入 CS61B 前 3 周 | 数学复习 + 公式库 | PortSwigger 入门 lab |
| 16–20 | CS61B 数据结构和面向对象 | 完成吴恩达 ML 课程前半 | 完成 Web Security Basics 模块 |

#### 大二上学期 DoD

- [ ] CS61A 完成 60% 以上视频 + 作业
- [ ] 有一个 PyTorch 或 sklearn 的 Mini 项目
- [ ] Git 可以完成日常版本管理
- [ ] 能处理常见的 Linux 权限异常
- [ ] 至少完成 15 道 PicoCTF / PortSwigger 题

### 8.3 大二下学期（第 6–10 个月）详细计划

#### 目标

- 建立算法基础：CS61B 数据结构 + 刷题上线 200 题。
- 机器学习进入实操：吴恩达 ML + sklearn。
- 安全进入 Web 深水区：PortSwigger + CTF Web 专项。

#### 学习安排

| 周次 | CS 主线 | AI 主线 | 安全主线 |
|------|---------|---------|----------|
| 1–2 | CS61B 基础排序 + 链表 | 逻辑回归 + 评估 | SQL 注入专项 |
| 3–4 | CS61B 树、图 | 特征工程 | XSS 专项 |
| 5–6 | CS61B 哈希表 | 决策树/随机森林 | CSRF / SSRF |
| 7–8 | 练习算法题 30 道 | 开始 D2L 深度学习 | 文件上传 / 命令注入 |
| 9–10 | CS61B 项目实战 | D2L 多层感知机 | CTF Web 模拟赛 |
| 11–12 | 算法专题：DP | D2L CNN | 搭靶场练习 |
| 13–15 | 算法专题：图论 | D2L 优化器 | PortSwigger 中级题 |
| 16–20 | 刷题巩固：LeetCode 200+ | 开始第一个 Kaggle | CTF 周赛旧题复盘 |

#### 大二下学期 DoD

- [ ] CS61B 完成度达到 80%
- [ ] LeetCode 刷题 200+，含中难度题 50 个
- [ ] 完成 Kaggle 入门赛并提交
- [ ] PortSwigger 完成 25 个实验室
- [ ] 参加至少 1 场 CTF 并提交 writeup

### 8.4 大二暑假（第 11–14 个月）详细计划

#### 目标

- 系统编程和操作系统：CSAPP + 6.S081。
- AI 深度学习：完成 D2L 的 CNN/RNN。
- 安全实战：NahamCon / CTF 暑期赛 + 二进制入门。

#### 学习安排

| 周 | 重点 | 具体内容 |
|----|------|----------|
| 1–2 | 系统编程 | CSAPP 机器级代码部分 |
| 3–4 | 操作系统 | 6.S081 操作系统实验 |
| 5–6 | AI | D2L CNN 章节 |
| 7–8 | AI | D2L RNN/时序模型 |
| 9–10 | 安全 | Pwn.college 入门模块 |
| 11–12 | 安全 | Attack Lab 完成 |
| 13–14 | 项目 | Flagship 项目推进 |

#### 暑假 DoD

- [ ] 完成 CSAPP 第 1–9 章核心概念
- [ ] 完成 6.S081 至少 3 个实验（或用替代项目）
- [ ] 能训练自己的第一个深度学习模型
- [ ] 完成 Attack Lab 全部关卡
- [ ] 参加至少 1 场线上 CTF

### 8.5 大三上学期（第 15–19 个月）详细计划

#### 目标

- 计算机系统再深入 + 计算机网络。
- 大模型 / NLP。
- 安全方向定岗：AI 安全、二进制 or Web。

| 周 | CS 主线 | AI 主线 | 安全主线 |
|----|---------|---------|----------|
| 1–4 | CS144 网络实践 | 词向量 / Transformer | CTF 高级 Web |
| 5–8 | 系统设计基础 | 微调 / PEFT | 二进制 ROP 进阶 |
| 9–12 | 设计分布式小系统 | RAG 项目 | AI 安全论文阅读 |
| 13–19 | 复习 + 项目整合 | 部署 / 推理优化 | 完成安全 × AI 实验报告 |

#### 大三上学期 DoD

- [ ] 完成 CS144 全部实验
- [ ] 能使用 HuggingFace 加载和微调模型
- [ ] 完成一个 RAG 问答系统
- [ ] 写出一份安全 × AI 实验报告
- [ ] 秋季校园招聘简历草稿含至少 2 个项目

### 8.6 大三下学期及以后（第 20–24 个月）

- 求职/保研/科研方向逐渐确定。
- 对旗舰项目做一次重构，提升代码质量和文档。
- 参加 Hackathon、Kaggle、CISCN、WCTF 等比赛。
- 保持输出：技术博客全年更新 12 篇以上。
- 准备面试常见题清单，覆盖 CS、AI、安全三块。

---

## 九、每周学习节奏与时间管理

> 建议参考“在校上课 + 自学项目”双轨模式。整块时间优先给自学主线，零碎时间用于背单词、刷题和读论文。既要避免拖延，也要避免“感动自己式”的刷进度。

### 9.1 每周时间分配（参考）

| 时间段 | 内容 | 备注 |
|--------|------|------|
| 周一至周五：上午课间 | 背英语 / 刷算法题 1~2 题 | 零碎时间 |
| 周一至周五：晚上 1–2 小时 | 当前主线的系统课程 / 项目 | 固定整块时间 |
| 周六：上午 | 本周复盘 + 整理笔记 | 用 [Obsidian](https://obsidian.md/) 或 [Notion](https://www.notion.so/) |
| 周六：下午 | 旗舰项目迭代 3–4 小时 | 深度工作 |
| 周日：上午 | 安全/AI 实验和靶场 | 动手为主 |
| 周日：下午 | 自由探索 / 竞赛 / 阅读论文 | 保持兴趣 |

### 9.2 每日学习模板（示例）

- 09:00 – 09:10：写今日优先级（3 件事）。
- 19:30 – 21:00：主线课程或项目。
- 21:00 – 21:30：复习今天学到的 3 个知识点。
- 21:30 – 22:00：归档笔记、提交代码。

### 9.3 对抗拖延的四个机制

1. **公开承诺**：每周在 GitHub 提交本周学习汇报。
2. **两分钟法则**：不想学时，先学两分钟。
3. **任务切分**：把“学完操作系统”改成“今天读完第 2 章讲义”。
4. **复盘奖励**：周末完成目标后给自己一个休息奖励。

### 9.4 避免自嗨清单

- [ ] 不要只看视频不写代码。
- [ ] 不要重复做你已经会做的题。
- [ ] 不要囤积教程，重要的是完成度。
- [ ] 不要以“我在学习”为借口回避输出。
- [ ] 不要忽视休息和运动。

## 十、工具 / 资源总览

> 所有资源均使用超链接，便于直接点击跳转。建议每周抽出时间浏览相关社区，但保持克制，避免信息过载。

### 10.1 通用基础

- [csdiy.wiki](https://csdiy.wiki/)：计算机自学路线图，可对标电子科大/清华等体系，适合补充课程。
- [GitHub](https://github.com/)：你的代码仓库、学习记录和项目展示平台。
- [Git - Book](https://git-scm.com/book/zh/v2)：Git 官方中文书籍。
- [MDN Web Docs](https://developer.mozilla.org/zh-CN/)：Web 技术权威文档。

### 10.2 CS 主线

- [CS50](https://cs50.harvard.edu/)、[CS61A](https://cs61a.org/)、[CS61B](https://cs61b.org/)、[CSAPP](https://csapp.cs.cmu.edu/)、[6.S081](https://pdos.csail.mit.edu/6.S081/2021/)、[CS144](https://cs144.github.io/)、[CMU 15-445](https://15445.courses.cs.cmu.edu/fall2023/)。
- [LeetCode](https://leetcode.cn/)、[Codeforces](https://codeforces.com/)、[PTA](https://pintia.cn/)。

### 10.3 AI 主线

- [动手学深度学习（D2L）](https://zh-v2.d2l.ai/)。
- [吴恩达机器学习](https://www.coursera.org/learn/machine-learning)。
- [Hugging Face Learn](https://huggingface.co/learn)。
- [Kaggle](https://www.kaggle.com/)。
- [Paper with Code](https://paperswithcode.com/)。
- [arXiv](https://arxiv.org/)。
- [OpenAI](https://openai.com/) / [Anthropic](https://www.anthropic.com/) 官方文档。

### 10.4 安全主线

- [PortSwigger Web Security Academy](https://portswigger.net/web-security)。
- [picoCTF](https://picoctf.org/)、[CTFtime](https://ctftime.org/)、[HackTheBox](https://www.hackthebox.com/)、[TryHackMe](https://tryhackme.com/)。
- [Cryptohack](https://cryptohack.org/)。
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)。
- [Nuclei](https://github.com/projectdiscovery/nuclei) / [Burp Suite](https://portswigger.net/burp) 等工具。
- [Reverse Engineering for Beginners](https://beginners.re/) / [Pwn.college](https://pwn.college/)。
- [MITRE ATT&CK](https://attack.mitre.org/)。
- 中文社区：[先知](https://forum.butian.net/)、[安全客](https://www.anquanke.com/)、[FreeBuf](https://www.freebuf.com/)。

### 10.5 学习工具

- [Obsidian](https://obsidian.md/)：本地知识库，适合记录笔记和知识图谱。
- [Notion](https://www.notion.so/)：任务管理、项目规划。
- [Anki](https://apps.ankiweb.net/)：间隔重复记忆算法题和密码学名词。
- [VS Code](https://code.visualstudio.com/)、[JetBrains](https://www.jetbrains.com/)：开发环境。
- [Docker](https://www.docker.com/)、[GitHub Actions](https://github.com/features/actions)：部署与自动化。

## 十一、参考培养方案摘录与自学取舍（内部参考）

> 以下摘录自《2025 信息安全培养方案》，仅用于规划提醒，不作为本文件正文依据展示全部学分细节。重点是在校课程与自学规划的对应和取舍原则。

### 11.1 学分结构速览

| 板块 | 建议重视程度 | 与自学的关系 |
|------|-------------|--------------|
| 通识教育（约 74 学分） | 及格通过即可，不追求高分 | 课程压力大时优先保证校内不挂科，自学主线少排 |
| 公共课程类（约 64 学分） | 保持基本均分 | 英语能力对读论文重要，数学课程要用心学 |
| 专业基础（约 17 学分） | 高投入 | 数学、程序设计、离散数学是自学主线的基础 |
| 专业核心（约 41 学分） | 高投入 | 信息安全数学基础、密码学、系统课程与自学框架重叠最大，可替换进阶资源 |
| 专业选修（约 14 学分） | 结合兴趣选 | 尽量选择与 AI、SecAI 相关的课程 |
| 个性化（约 10 学分） | 灵活 | 可以把旗舰项目和竞赛作品纳入展示材料 |

### 11.2 课程与自学对应关系

| 校内课程类 | 自学替代 / 延伸资源 |
|-----------|---------------------|
| 程序设计基础 | CS61A、CS50 |
| 数据结构 | CS61B、LeetCode |
| 计算机组成 | CSAPP、Nand2Tetris |
| 操作系统 | 6.S081、MIT 6.S081 实验 |
| 计算机网络 | CS144、Wireshark 实验 |
| 密码学基础 | Cryptohack、Katz & Lindell 教材 |
| AI 导论 / 机器学习 | Wu Enda ML、D2L |
| 信息安全教育 | PortSwigger、CTF writeup 阅读 |

### 11.3 取舍原则

1. 校内绩点是你最基本的安全网，不要为了自学放弃核心课程。
2. 自学主线按“最小必要知识”推进：不需要每个知识都完美，但主线不能中断。
3. 大三之后的两条线会明显收敛：安全性 AI、AI 辅助攻防、大模型安全都是交叉点。
4. 优先产出可展示的作品，而不是无限“打好基础”。

## 十二、风险与自检清单（季度回顾）

> 建议每季度按此清单做 15 分钟自检，判断是否需要调整节奏。

| 风险 | 信号 | 应对策略 |
|------|------|----------|
| 只学不写 | 课堂视频完成度 80% 但代码库无新增 | 每看 1 小时课程，要求至少有 30 分钟动手 |
| 项目太多 | 同时维护 3 个 projects，每个都未完成 | 将项目合并，先完成一个完整 demo |
| 课程内卷 | 校内作业耗时过多，占用自学时间 | 寻求同学协作，控制单科完美主义 |
| 论文焦虑 | 开始读高难度论文但读不懂 | 先读综述／博客，再用 AI 工具辅助理解 |
| 工具依赖 | 用 AI 写代码但无法解释 | 每周挑 1 个 AI 生成代码，亲手重写一遍 |

## 十三、最终目标与成果清单（24 个月后）

- [ ] 完成 CS61A + CS61B + CSAPP（或等价进阶课程）。
- [ ] 完成至少 300 道算法题，熟悉常见模板。
- [ ] 完成“机器学习 → 深度学习 → LLM 应用”全链路入门。
- [ ] 完成 1 个旗舰项目（含 README、Demo、测试）。
- [ ] 完成 1 篇安全 × AI 的实验报告或技术博客。
- [ ] 参加至少 3 场 CTF 或 Kaggle，并留下复盘记录。
- [ ] 建立自己的知识库（笔记 / 博客 / GitHub）。

---

> 祝你在大二到大三这两年，把“课程学习、自主学习、动手项目、职业方向”四件事建立成一套正循环系统。所有规划都仅供参考，最终节奏请结合你的真实精力和兴趣动态调整。

---

## 十四、CS 主线补充细则：如何把课程内化为能力

> 很多同学都看过 CSAPP 第一章，但真正让他谈一谈“虚拟内存为什么让指针变得更危险”时却讲不清楚。学习 CS 不是“看完”，而是达到“能用、能讲、能改”三层标准。

### 14.1 每门课的三层检验

| 课程 | 能复述 | 能实现 | 能改进 |
|------|--------|--------|--------|
| CS61A | 解释递归、lambda、高阶函数 | 完成全部 Project | 给 Scheme 解释器加一个语法 |
| CS61B | 说出 Map/Set 接口差异 | 手写 HashMap、AVL | 对比 JDK 实现差异 |
| CSAPP | 解释 cache / 内存 | 完成 bomb lab，了解缓存优化 | 对自己项目做性能 profiling |
| 6.S081 | 解释系统调用和进程 | 完成 xv6 实验 | 写一个 mini 内核特性 |
| 15-445 | 解释 B+ 树和事务 | 完成 buffer pool | 调参并做压测 |

### 14.2 关于“刷题”的正确姿势

- **不是刷数量**，而是每道题回答三个问题：为什么用这个数据结构？复杂度是多少？如果数据变大 100 倍会怎样？
- 建议按 Tag 刷题：数组、链表、树、图、DP、二分、并查集、Trie。
- 每周至少 3 题，保持手感；大二暑假前达到 300+ 题。
- 复习节奏：错题要回刷，10 天后重做一次。

### 14.3 代码阅读与工程能力

- 阅读 3 个中大型开源项目：例如 [flask](https://github.com/pallets/flask)（Python）、[minio](https://github.com/minio/minio)（Go）、[netdata](https://github.com/netdata/netdata)（C）。
- 学会用 debugger：gdb / lldb / pdb / VS Code Debug。
- 学会 profiling：Python cProfile、py-spy；Go pprof。
- 熟悉测试框架：pytest、Go testing、JUnit。

---

## 十五、AI 主线补充细则：大模型时代的学习路径

### 15.1 从哪里开始

1. **先重数学**：第 5.1 节提到的线性代数、概率论是地基。
2. **再入门 ML**：吴恩达课程或者 [机器学习基石](https://www.coursera.org/learn/ntumltwo-mathematicalfoundations) 任意一套都行，重要的是跟着做完作业。
3. **再进深度学习**：不要把时间花在过时的教程上，直接使用 [PyTorch](https://pytorch.org/) + [D2L](https://zh-v2.d2l.ai/)。
4. **再进 LLM/NLP**：推荐 [Hugging Face Course](https://huggingface.co/learn)、[斯坦福 CS224N](https://web.stanford.edu/class/cs224n/)。
5. **最后结合安全**：考虑对抗样本、模型窃取、提示注入、LLM 对齐。

### 15.2 大模型时代的能力矩阵

| 能力 | 具体动作 | 对应资源 |
|------|----------|----------|
| 会用 API | 完成至少 3 个 LLM 应用 | [OpenAI API 文档](https://platform.openai.com/docs) / [智谱 AI](https://open.bigmodel.cn/) |
| 会做 RAG | 搭建知识库问答 | [LlamaIndex](https://www.llamaindex.ai/) / [LangChain](https://www.langchain.com/) |
| 会做微调 | 用 LoRA 微调小模型 | [Hugging Face PEFT](https://huggingface.co/docs/peft) |
| 会做推理部署 | 量化 + vLLM | [vLLM](https://github.com/vllm-project/vllm) / [Ollama](https://ollama.com/) |
| 会做安全评估 | 提示注入 / 越狱测试 | [Garak](https://github.com/leondz/garak) |

### 15.3 AI 项目清单

- **第 1 个项目**：用 sklearn 完成一个二分类任务，例如钓鱼网站检测。
- **第 2 个项目**：用 PyTorch 训练一个 MNIST / CIFAR-10 模型，并尝试攻击（FGSM）。
- **第 3 个项目**：做一个 LLM 对话机器人，支持多轮对话和自定义 Prompt。
- **第 4 个项目**：做一个 RAG 问答系统，例如“安全公告问答”。
- **第 5 个项目**：做一个提示注入检测工具，或者对抗样本 Demo。

---

## 十六、安全主线补充细则：从 CTF 到真实漏洞

### 16.1 CTF 是训练的“最小闭环”

CTF 的价值不是拿牌，而是逼你把知识变成能力。推荐路径：

1. **Web**：从 PortSwigger 开始，配合 [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) 练习。
2. **Pwn**：从 PicoCTF + [pwn.college](https://pwn.college/) 开始，练习栈溢出、ROP。
3. **Crypto**：从 [CryptoHack](https://cryptohack.org/) 从零开始。
4. **Reverse**：先学 Python 逆向（pyc），再接触 C 和 Windows PE。
5. **Misc / Forensics**：练习流量分析、内存取证。

### 16.2 安全 × AI 的四个方向

| 方向 | 说明 | 示例项目 |
|------|------|----------|
| 对抗鲁棒性 | 如何让模型经受攻击 | 实现 FGSM / PGD 攻击并评估防御 |
| LLM 安全 | 提示注入、越狱、幻觉 | 检测恶意 Prompt 的 API |
| AI 检测 | 利用 ML 做恶意软件检测 | 基于 API 序列的恶意样本分类 |
| AISecOps | 自动化安全运营 | 用 LLM 生成安全事件报告 |

### 16.3 安全技能树（五年长期）

- **第一年**：Linux、网络、Web 漏洞、CTF 入门。
- **第二年**：二进制、逆向、密码学协议、渗透测试方法论。
- **第三年**：AI 安全、云安全、供应链安全、漏洞研究。
- **第四年**：论文阅读、竞赛奖项、实习项目、应届求职。

---

## 十七、课程替代方案：不同兴趣方向的自学路线

### 17.1 偏系统/二进制

- CSAPP + 6.S081 + 逆向基础。
- 学习 gdb、objdump、ghidra。
- 目标：能读懂内核或恶意软件样本。

### 17.2 偏 Web / 应用

- CS61B + 数据库 + 后端项目。
- 学习 Burp Suite、Nginx、Docker。
- 目标：能独立搭建并审计一个 Web 应用。

### 17.3 偏 AI / 数据

- 数学基础 + ML + 深度学习 + NLP。
- 学习 pandas、sklearn、PyTorch。
- 目标：做 1 个 AI 安全项目并写报告。

### 17.4 偏研究 / 学术

- 读 CS + AI 顶会论文，每周精读 1 篇。
- 学习 LaTeX、markdown、引用管理、论文复现。
- 尝试在自己的项目里增加一个小创新点。

---

## 十八、简历与求职准备

### 18.1 两年后的简历“三件套”

1. 一个可持续迭代的旗舰项目。
2. 一个可展示的 GitHub 仓库（README、Demo、测试）。
3. 一份技术博客（至少 10 篇高质量文章）。

### 18.2 投递方向

- **安全工程师/红队/SOC**
- **AI 算法/应用/安全 AI**
- **后端/基础架构/运维**
- **研究实习生/科研助理**

### 18.3 常见面试题分类

| 类别 | 问题举例 | 备考来源 |
|------|----------|----------|
| 算法 | LRU、反转链表、Top K | LeetCode 热题 100 |
| 操作系统 | 线程与进程、死锁 | CSAPP + 六章知识点 |
| 网络 | TCP 三次握手、HTTPS | CS144 + 面试题库 |
| 安全 | XSS 原理、密码交换 | PortSwigger + CTF writeup |
| AI | 过拟合、激活函数、Attention | 吴恩达课程 + D2L |

---

## 十九、附录：每周学习目标模板（可复制使用）

> 复制下面模板，每周粘贴到你的学习日志里使用。

### 每周目标（第 __ 周）

**主题：** __

| 日期 | 学习内容 | 学习时长 | 产出/完成情况 |
|------|----------|----------|----------------|
| 周一 | | | |
| 周二 | | | |
| 周三 | | | |
| 周四 | | | |
| 周五 | | | |
| 周六 | | | |
| 周日 | | | |

**本周完成：**
1.
2.
3.

**本周未完成：**
1.
2.

**下周计划：**
1.
2.

**收获 / 心得：**

---

## 二十、结语

> 这是一个“自学、课程、项目、求职”四线并进的规划。不要追求一天学很多，而要保持每天有稳定的进步。只要坚持每两周都有一个可见产出，两年之后你会比大多数人想象中走得更远。

> 规划文档只是一个入口，真正的成长来自你持续输入、动手和输出。祝你顺利。

> **最后，提醒你：任何学习计划都应该允许被修改。每 3 个月回头看看，根据学校课程、兴趣和机会调整。计划是工具，不是枷锁。**

---

## 二十一、名词速查表

> 遇到不认识的术语，先回这里扫一眼有没有收录。该表不是死记硬背，而是让你在阅读资料时能快速定位到关键词。

| 术语 | 含义 | 关联方向 |
|------|------|----------|
| Cache | 高速缓存，缓解 CPU 与内存速度差距 | CSAPP |
| Virtual Memory | 虚拟内存，隔离进程地址空间 | CSAPP/OS |
| ROP | Return-Oriented Programming，面向返回的编程攻击 | Pwn |
| CNN | 卷积神经网络 | AI |
| RNN | 循环神经网络 | AI |
| Transformer | 基于自注意力机制的模型架构 | AI / LLM |
| RAG | 检索增强生成 | LLM |
| LoRA | 低秩适配，用于参数高效微调 | LLM |
| SSRF | Server-Side Request Forgery，服务端请求伪造 | Web 安全 |
| CSRF | Cross-Site Request Forgery，跨站请求伪造 | Web 安全 |
| XSS | Cross-Site Scripting，跨站脚本攻击 | Web 安全 |
| SQLi | SQL Injection，SQL 注入 | Web 安全 |
| CVE | Common Vulnerabilities and Exposures，公共漏洞披露 | 通用 |
| CWE | Common Weakness Enumeration，软件弱点分类 | 通用 |
| SIGINT | 信号中断，GDB 中 Ctrl+C 触发的信号 | 逆向 / 调试 |
| Golden Ticket | Kerberos 域控票据伪造攻击 | 内网/域渗透 |
| 2FA | Two-Factor Authentication，双因素认证 | 认证安全 |
| Zero Trust | 零信任安全模型 | 安全架构 |
| MLOps | 机器学习运维 | AI 工程 |
| Federated Learning | 联邦学习，数据不出本地 | AI 安全 |
| Differential Privacy | 差分隐私 | AI 安全 |

---

## 二十二、最终检查清单（每月 1 次）

- [ ] 本月我有没有完成至少 1 个可展示产出？
- [ ] 我有没有在读一个“不舒适区”的资源？
- [ ] 我的代码库是否比上个月更整洁？
- [ ] 我有没有本周期的学习心得或博客输出？
- [ ] 我在 CTF / Kaggle / Open Source 有没有保持参与？
- [ ] 我有没有和同学或社区交流专业话题？

---

> 强烈建议你把这份文档加入你的 Obsidian 或笔记库，并把每个阶段拆成单独的笔记，方便随时添加截图、链接和复盘。祝你每天都能进步一点点。
