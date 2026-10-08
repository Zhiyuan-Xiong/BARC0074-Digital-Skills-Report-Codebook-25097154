# 地震：数据转译

CLIP、文本向量与多源数据融合驱动空间生成。

**[完整设计案例](https://xiongzhiyuan-portfolio.pages.dev/zh/work/earthquake/) · [求职作品总入口](https://github.com/Zhiyuan-Xiong/xiongzhiyuan-portfolio)**

<p align="center"><img src="portfolio/images/earthquake-cover-1280.webp" alt="地震：数据转译" width="100%"></p>

## 项目目标

以地震为主题，将图像中的视觉特征、文本中的叙事信号与地球物理记录转化为可计算的设计变量。在 Jupyter 中完成采集、清洗、分析与融合，再用 Python 将这些变量映射为 Blender 的建筑碎片、地表裂隙与动态场景，最终在 Processing 中转化为粒子、波纹与实时反馈。

## 我的贡献

Python 数据处理、参数映射与空间可视化

完成阶段：多源分析、程序建模与实时可视化

现有产出：Jupyter 分析、特征与聚类图、数据映射 CSV、Blender 生成模型与 Processing 动态反馈

## 我的 AI 策略与迭代工作流

让 AI 提取图像与文本中的可计算表示，再由我定义变量的设计意义与空间映射。重点是数据来源、跨模态对齐、映射解释与视觉结果之间的关系。

```mermaid
flowchart LR
  N0["多源输入<br/>图像 / 文本 / USGS"]:::human
  N1["AI 特征表示<br/>CLIP / 文本向量"]:::ai
  N2["我定义映射<br/>变量意义 / 空间规则"]:::human
  N3["我评审结果<br/>数据 + 空间视觉"]:::human
  N4["可追溯研究成果<br/>Notebook / CSV / 影像"]:::output
  N0 --> N1 --> N2 --> N3 --> N4
  N3 -. "反馈与调整" .-> N0
  classDef human fill:#dcefe5,stroke:#7caa96,color:#183d30;
  classDef ai fill:#eee8fa,stroke:#ada0d0,color:#392c57;
  classDef output fill:#fbefd3,stroke:#cbb574,color:#58461c;
```

### 各阶段的操作、输入与输出

| 阶段 | 输入 | AI 协作与我的控制 | 输出与验收 |
| --- | --- | --- | --- |
| **1. 灵感发散** | 地震图像、新闻、USGS 数据与主题 | 对话辅助理解研究问题和代码思路；我定义数据如何服务灾后空间表达 | 研究问题；明确模态与设计目标 |
| **2. 多渠道检索** | 不同模态的原始数据和资料 | 辅助整理模型、字段和处理路径；我核对来源、样本关联与变量含义 | 输入清单；不把来源差异直接混合 |
| **3. 个人思维组织** | 原始字段、图像与文本 | Notebook 组织清洗和分析；我确定对齐方式、标准化与处理顺序 | 可检查输入；追溯来源与处理 |
| **4. AI 辅助方案** | 对齐数据与分析问题 | CLIP／SentenceTransformer 提取表示；我选择分析路线并解释特征的作用 | 向量与分析方案；区分推理和训练 |
| **5. 原型实现** | 向量、地球物理变量与融合数据 | Python 组织聚类、降维和映射输入；我定义变量到尺度、碎片等空间规则 | 融合 CSV 与映射表；核对字段对应 |
| **6. 迭代与测试** | CSV、聚类结果、空间图像 | 辅助检查代码和组织结果说明；我同时评审数据关系与空间可读性 | 比较结果；检查变量是否按规则变化 |
| **7. 反馈与再检索** | 异常字段、映射偏差或表达问题 | Chat 辅助解释，代码任务交给 Codex；数据问题回处理，空间问题回人工映射 | 修订说明或规则；再次对照结果 |
| **8. 精修与交付** | Notebook、CSV、视觉与案例 | 整理研究和数字呈现入口；我核对原研究文件与可追溯证据 | 原始代码、融合数据、映射与空间资料 |

### 精选决策：把模型表示转成可解释的设计规则

CLIP 和文本向量提供不同模态的表示；空间设计仍由我组织变量意义与映射。每轮判断同时对照数据和视觉，保证可以说明为何形成这样的空间。

| 输入证据 | 我的判断与控制 | 输出证据 |
| --- | --- | --- |
| 图像、文本和 USGS 字段 | 先对齐与标准化，再组织融合关系 | `final_fusion_data.csv` |
| 融合变量和设计意图 | 定义 `data_variable → mapping_rule → design_effect` | `design_mapping_table.csv` |
| 映射表与空间图像 | 检查尺度、碎片、旋转等结果是否对应规则 | 数据与空间视觉对照 |

这里使用预训练模型进行推理和分析；Notebook 与 CSV 保留原研究内容。

### 审美、专业制作与质量控制

| 质量维度 | 我如何控制 | 可查看产出 |
| --- | --- | --- |
| **数据可信** | 核对字段、来源和处理路径，对不同模态做对齐与标准化。 | 可追溯的 Notebook 和 CSV |
| **专业解释** | 由我定义变量的含义与空间映射规则。 | 可检查的设计映射表 |
| **视觉表达** | 将空间结果与原始变量对照，检查层次和主题表达。 | 三维空间与动态视觉资料 |

### 反馈如何改变下一步

```mermaid
flowchart TD
  I["地震图像<br/>CLIP 表示"] --> F["对齐、标准化与融合"]
  T["新闻文本<br/>文本向量"] --> F
  U["USGS 地球物理记录"] --> F
  F --> H["我定义设计映射"]
  H --> B["Blender 空间结构"]
  H --> P["Processing 动态反馈"]
  B --> R["我对照数据评审视觉"]
  P --> R
  R -- "修正规则" --> H
```

### 工具分工

Jupyter 与 Python 承担采集、清洗、标准化与融合；CLIP 和 SentenceTransformer 提供预训练向量；Blender 与 Processing 承担空间和动态视觉。当前数字展示由 Codex 辅助组织。

**过程证据：** [多模态融合 Notebook](earthquake_disaster_fusion_workflow.ipynb) · [设计映射表](design_mapping_table.csv) · [融合数据](final_fusion_data.csv) · [聚类与数据分析](portfolio/media/earthquake/fusion-clusters.webp) · [空间视觉结果](portfolio/media/earthquake/spatial-detail.webp)

[阅读详细工作流与提示词组织方法](工作流.md) · [我的完整 AI 设计方法](https://github.com/Zhiyuan-Xiong/xiongzhiyuan-portfolio/blob/main/docs/AI设计工作流.md)

## 从数据到空间的证据

<table><tr><td width="50%"><img src="portfolio/media/earthquake/fusion-clusters.webp" alt="多源数据融合与聚类" width="100%"><br>多源数据融合与聚类</td><td width="50%"><img src="portfolio/media/earthquake/spatial-detail.webp" alt="数据转译后的三维空间" width="100%"><br>数据转译后的空间成果</td></tr></table>

## 仓库内容

| 内容 | 入口 |
| --- | --- |
| 图像采集与视觉特征 | [earthquake photos scraping.ipynb](earthquake%20photos%20scraping.ipynb) |
| 新闻文本与语义处理 | [earthquake news scraping.ipynb](earthquake%20news%20scraping.ipynb) |
| 多模态融合工作流 | [earthquake_disaster_fusion_workflow.ipynb](earthquake_disaster_fusion_workflow.ipynb) |
| 融合数据 | [final_fusion_data.csv](final_fusion_data.csv) |
| 设计映射 | [design_mapping_table.csv](design_mapping_table.csv) |
| 案例与空间视觉资料 | [portfolio/](portfolio/) |

## 阅读顺序

1. 阅读图像与新闻采集 Notebook，理解各类特征和处理方式。
2. 阅读融合 Notebook，查看对齐、标准化、向量表示和空间指标的计算。
3. 对照 CSV 输出与设计映射表。
4. 在在线案例中查看 Blender 空间生成与 Processing 动态反馈。

## 数据来源与范围

地球物理数据来源为 [USGS 地震数据集](https://www.kaggle.com/datasets/usgs/earthquake-database)。图像、新闻与融合数据的来源和过程保留在原 Notebook 与代码中。模型使用预训练表示，具体配置以代码为准。

当前研究仓库主要记录数据采集、分析与融合阶段；后续原生工程仍沿用原项目的 [完整材料入口](https://liveuclac-my.sharepoint.com/:f:/g/personal/ucbvz94_ucl_ac_uk/IgBhQGdm-1IfSqVe3db81iSOASuGqH7bbghzayAqKxJ76Cw?e=2NrSCx)。

## 署名与使用

作品素材用于个人设计展示。协作项目以案例中的职责说明为准；字体、引擎和第三方资料遵循各自授权。未经许可，不将作品素材用于转载或商业用途。
