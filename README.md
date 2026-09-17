# Scientific Agents 2026 · 科研 Agent 文献索引

面向科研 agent 的精选文献综述，覆盖文献检索、假设生成、实验执行、复现和研究可信度。

**收录 20 篇 · 检索快照 2026-09-17 · 中文导读**

| 来源 | 条目数 |
|---|---:|
| Nature 主刊 | 5 |
| Nature Machine Intelligence | 1 |
| Science 观点文章 | 1 |
| ICLR 2026 | 6 |
| ICML 2026 | 5 |
| ACL 2026 | 1 |
| IJCAI 2026 | 1 |
| **合计** | **20** |

- 本页：完整中文综述、论文链接、能力边界与阅读顺序。
- [结构化论文索引](data/papers.json)：20 条论文元数据，支持按 venue、publication_type 和 tags 筛选。
- [维护说明](CONTRIBUTING.md)：收录标准、元数据含义及更新方式。
- [更新记录](CHANGELOG.md)：快照版本与验证范围。

> 本仓库由已有文献综述整理而来。初版沿用原综述的发表信息与论文报告，未重新逐篇联网核验或独立复现实验；它是一份选择性阅读清单，不代表穷尽统计。部分链接指向预印本或作者仓库，其会议归属另见官方目录。

## 范围与总体判断

本综述基于 **截至 2026 年 9 月 17 日的发表／录用信息检索快照**，重点关注能参与“文献检索—提出假设—执行实验—分析结果—写作与验证”的科研 agent。

整体判断是：**2026 年的重点，已经从“能否自动写出论文”，推进到“能否通过真实执行不断改进，并留下可靠、可复现的证据”。**下面是重点清单；属于选择性综述，不是全部论文的穷尽统计。

需要先明确两个范围：

- **Nature 主刊、Nature 子刊和 Science 观点文章分开列。**
- **本快照未将 NeurIPS 2026 投稿纳入已录用成果。**后续补充时需按具体 track 的官方录用信息核对。

## Nature 主刊

下面五篇覆盖科研流程的不同环节。年份按期刊正式发表计算，其中部分工作此前已有预印本。

| 论文与发表日期 | 做了什么 | 贡献与能力边界 |
|---|---|---|
| **The AI Scientist**：*[Towards end-to-end automation of AI research](https://www.nature.com/articles/s41586-026-10265-5)*，3 月 25 日 | 串联想法生成、编程、实验、作图、论文写作和自动评审；包含模板驱动与无模板的实验搜索。 | 是理解完整科研流水线的基础论文。但生成论文通过的是**录用率约 70% 的 workshop 第一轮评审**，不能解读为达到顶会主会水平。 |
| **Co-Scientist**：*[Accelerating scientific discovery with Co-Scientist](https://www.nature.com/articles/s41586-026-10644-y)*，5 月 19 日 | 多个 agent 分别生成、批评、排序和演化假设，通过锦标赛机制持续改进。 | 核心是**假设搜索与筛选**。在药物再利用、肝纤维化靶点和抗菌药物耐药机制上进行了验证；研究者仍参与目标设定、方向选择及实验验证。 |
| **Robin**：*[A multi-agent system for automating scientific discovery](https://www.nature.com/articles/s41586-026-10652-y)*，5 月 19 日 | 将文献检索、假设生成、实验建议和数据分析连接起来，再根据实验结果提出新假设。 | 在干性年龄相关性黄斑变性研究中提出候选药物并获得体外实验支持。突出的是**实验反馈驱动下一轮发现**；湿实验和详细实验协议仍依赖人类。 |
| **ERA**：*[An AI system to help scientists write expert-level empirical software](https://www.nature.com/articles/s41586-026-10658-6)*，5 月 19 日 | 用 LLM 与树搜索反复生成、运行和改进科研代码，并引入外部文献中的研究思路。 | 在单细胞分析、疾病预测等任务中找到超过比较基线的方法。适用于**有明确可计算评价指标的科研任务**，不能直接外推到所有开放式科学问题。 |
| **Paper2Agent**：*[Reimagining research papers as interactive and reliable AI agents](https://www.nature.com/articles/s41586-026-11044-y)*，9 月 16 日 | 将论文、代码、数据及工作流封装为可调用的 MCP 服务，并自动生成和执行测试。 | 把论文变成可以询问、运行、应用到新数据上的“交互式研究助手”；展示了结果复现及多篇论文 agent 协作分析。重点是**研究成果复用与组合**。 |

这五篇可以对应科研流程中的五个问题：**完整流程怎么组织、假设怎么改进、实验反馈怎么利用、计算方法怎么搜索、已有成果怎么复用。**

## Science 观点文章

原检索收录的相关文章是 **James Evans 等人的 [Agentic AI and the next intelligence explosion](https://doi.org/10.1126/science.aeg1895)**，发表于 **3 月 19 日**。它是一篇观点性文章，讨论智能如何从多个 agent 与人类之间的分工、争辩和制度化协作中产生，适合作为科研组织形态的背景阅读。**本轮尚未核实到可以与上述五篇并列的、2026 年 Science 主刊科研 agent 系统原始研究**；这不代表确定不存在。

## Nature 子刊

补充阅读 **[An agentic artificially intelligent X-ray scientist](https://www.nature.com/articles/s42256-026-01261-5)**，发表于 **Nature Machine Intelligence，7 月 1 日**。它让 agent 根据仪器观测规划并调整 X 射线样品对准操作，从模拟环境走到真实同步辐射设施。值得注意的是，真实束线演示中的指令由人类转交执行，以满足设施要求；它证明的是具体实验任务中的自主决策能力。

## 计算机会议

重点成果集中在 **ICLR、ICML，以及 ACL、IJCAI**。下列会议归属依据官方目录或论文元数据核对；部分链接指向作者公开稿或项目仓库。[ICLR 官方目录](https://iclr.cc/virtual/2026/papers.html)、[ICML 官方目录](https://icml.cc/Downloads/2026)、[IJCAI 正式论文集](https://www.ijcai.org/proceedings/2026/)

| 论文 | 会议 | 核心贡献与阅读价值 |
|---|---|---|
| **[DeepScientist: Advancing Frontier-Pushing Scientific Findings Progressively](https://iclr.cc/virtual/2026/poster/10008492)** | ICLR 2026 | 以贝叶斯优化和累计研究记忆组织长时间实验搜索。作者报告使用超过 2 万 GPU 小时，在三个 AI 任务上超过比较基线。适合研究**长期运行、经验积累与算力预算**。 |
| **[SR-Scientist: Scientific Equation Discovery With Agentic AI](https://iclr.cc/virtual/2026/poster/10010150)** | ICLR 2026 | agent 自主分析数据、实现方程、调用评价工具并根据反馈优化，还探索强化学习训练。适合研究**可解释公式发现与工具执行闭环**。 |
| **[AstaBench: Rigorous Benchmarking of AI Agents with a Scientific Research Suite](https://iclr.cc/virtual/2026/poster/10009971)** | ICLR 2026，Oral | 覆盖 2,400 多个科研问题，强调检索工具、成本和实验条件可控。评估 57 个 agent，表明科研辅助仍存在明显缺口。适合建立**完整系统的评价框架**。 |
| **[ScienceBoard](https://iclr.cc/virtual/2026/poster/10008621)** | ICLR 2026 | 提供包含专业软件的真实科研工作环境和 169 个任务。论文受测模型总体成功率约 15%，揭示**跨软件、多模态、多步骤执行**的困难。 |
| **[From Reproduction to Replication: Evaluating Research Agents with Progressive Code Masking](https://iclr.cc/virtual/2026/poster/10007273)** | ICLR 2026 | 提出 AutoExperiment，逐步遮蔽论文代码，测试从运行现成代码到重新实现实验的能力。缺失代码越多，表现下降越快；适合研究**复现能力如何分级测量**。 |
| **[The Ideation-Execution Gap](https://iclr.cc/virtual/2026/poster/10010564)** | ICLR 2026 | 招募 43 位专家，每人投入超过 100 小时执行随机分配的人类或 LLM 想法。LLM 想法在执行后的评价下降更明显，说明**想法看起来新颖，未必带来更好的研究结果**。 |
| **[Towards Execution-Grounded Automated AI Research](https://arxiv.org/abs/2601.14525)** | ICML 2026 | 自动实现想法并运行 GPU 实验，以执行结果指导演化搜索或强化学习。在所测环境中，演化搜索有效，强化学习则出现模式坍缩。适合研究**如何用真实结果训练和改进 ideation**。 |
| **[MARS: Modular Agent with Reflective Search for Automated AI Research](https://arxiv.org/abs/2602.02660)** | ICML 2026 | 结合考虑成本的树搜索、模块化代码实现和比较式反思记忆，在 MLE-Bench 上评估。适合研究**实验成本控制及不同搜索分支之间的经验迁移**。 |
| **[SciNet: Evaluating AI Agents in Relation-Aware Scientific Literature Retrieval](https://arxiv.org/abs/2601.03260)** | ICML 2026 | 评估 agent 能否理解论文之间的支持、批评、知识组合和技术发展关系。包含 8,940 个任务，强调**文献检索不能只匹配关键词或语义相似度**。 |
| **[SciAgentGym](https://arxiv.org/abs/2602.12984)** | ICML 2026 | 提供 1,780 个科学工具与分层任务，并通过工具依赖关系合成训练轨迹。重点是**多步骤科学工具调用能力及其训练方法**。 |
| **[CauSciBench](https://github.com/causalNLP/CauSciBench)** | ICML 2026 | 评估从问题理解、变量选择、因果方法选择，到代码执行和统计解释的完整流程。对**社会科学、经济学及实证研究 agent**尤其相关。 |
| **[BadScientist: Can a Research Agent Write Convincing but Unsound Papers that Fool LLM Reviewers?](https://aclanthology.org/2026.acl-long.1134/)** | ACL 2026 主会 | 在受测自动评审设置中，虚构论文可获得很高的接受评分。揭示**自动评审分数不能代替实验真实性和证据核查**；这里的“接受”不是真实会议录用。 |
| **[ResearchEnvBench](https://arxiv.org/abs/2603.06739)** | IJCAI 2026 | 专门测试 agent 能否为研究代码搭建可运行环境，暴露依赖解析和版本耦合问题。补上科研复现中常被忽略的**环境准备能力**。 |

## 研究趋势与阅读顺序

基于这组论文，可以归纳出三个值得关注的变化：

- **评价重心转向执行结果。** Ideation-Execution Gap 与 Execution-Grounded Research 可以连着读：前者说明只评想法的局限，后者尝试把实验反馈纳入改进过程。
- **长期研究需要管理状态和成本。** DeepScientist、MARS、ERA 分别从研究记忆、预算和搜索策略切入，说明“把流程串起来”之后，还要解决如何有效持续探索。
- **可信度正在成为独立研究问题。** AstaBench、AutoExperiment、ResearchEnvBench 和 BadScientist 分别检查系统表现、实验实现、运行环境与评审可靠性。

**面向科研 agent 系统设计，建议优先读：Paper2Agent → AstaBench → Execution-Grounded Research → SciNet → CauSciBench。**它们分别对应成果复用、系统评价、实验反馈、文献证据关系和实证分析；再用 AutoExperiment 与 BadScientist 检查复现和审查设计。这个阅读顺序是编辑建议，以上性能结果均来自论文报告，本轮未独立复现实验。
