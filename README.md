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

### 从灵感到交付

| 阶段 | AI 策略与我的判断 |
| --- | --- |
| **1. 从设计问题确定数据任务** | 围绕地震如何转化为空间经验，拆分图像视觉、新闻叙事和地球物理三个输入。先明确想表达的空间变化，再决定需要收集与计算哪些变量。 |
| **2. 多渠道采集与来源核对** | 结合 USGS 地震记录、地震图像与新闻文本，保留 Notebook 中的采集和处理路径。分别检查不同来源的字段与含义，再进入后续分析。 |
| **3. AI 解析多模态信息** | 在现有 Notebook 中使用 CLIP 图像向量与 SentenceTransformer 文本向量，结合 TF-IDF、K-means、PCA 和标准化组织数据表示。这里使用预训练模型推理与分析。 |
| **4. 我组织融合与变量意义** | 对图像、文本和地球物理变量进行对齐与归一化，再建立融合数据。数值之间的对应关系需要由我解释，不能把模型输出直接等同于设计结论。 |
| **5. 建立可解释的空间映射** | 把融合结果转换为设计映射表，利用 Python 连接 Blender 的建筑碎片、裂隙与空间参数，并延伸到 Processing 的粒子与波纹。映射规则由我定义。 |
| **6. 用数据和视觉双重评审** | 同时查看特征、聚类、映射 CSV 和空间结果：数值变化是否对应预期的形态变化，视觉是否能够传达主题。根据问题重新调整分析或映射规则。 |
| **7. 回到对话、检索与代码迭代** | 将变量解释、代码理解与展示问题重新拆成具体任务，通过 AI 对话辅助组织说明，由 Codex 辅助当前案例呈现。研究代码、数据分析与空间成果分别保留，便于追溯。 |
| **8. 形成可检查的研究交付** | 交付原始 Notebook、CSV、融合与映射记录、空间图像和动态视觉。当前仓库主要完整记录数据阶段；后续原生工程仍沿用案例中的完整材料入口。 |

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
