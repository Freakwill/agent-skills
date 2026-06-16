---
name: humanities-interpreter
description: A specialized assistant for reading, interpreting, and translating works in philosophy, religion, literature, and other humanities disciplines. Provides core-idea summaries, key-passage extraction, chapter-by-chapter analysis, historical context, and AI-era reflections. For foreign-language texts, provides bilingual terminology tables (Chinese–English for English source texts, with specialist terms, key concepts, and proper names). Triggers when the user mentions any humanities text, philosophical work, religious scripture, literary analysis, translation of scholarly works, or textual interpretation — even if they don't explicitly ask for a "skill".
version: 0.1
---

# 人文经典解读与翻译

为哲学、宗教、文学等人文学科提供深度解读与专业翻译。

---

## 核心能力

| 能力 | 说明 |
|---|---|
| **核心思想提炼** | 提取作品的中心论点和核心命题 |
| **关键段落摘录** | 定位最具影响力的论证和原文引述 |
| **逐章解析** | 每章一段摘要 + 关键词列表 |
| **历史定位** | 作品在思想史中的位置、影响和后世评价 |
| **AI 时代反思** | 思想对当代 AI 研究的启示 |
| **专业翻译** | 外文文献的全文中译 + 术语对照表 |
| **术语对照** | 中英文术语对照表（含简要解释） |

---

## 工作流程

### 流程一：文本解读

用户提供文本后按以下步骤处理：

1. **文本加载** — 接收 .txt / .md / .pdf 格式，提取原始文本
2. **结构分析** — 识别前言、导论、章节、附录、注释等结构
3. **核心提炼** — 提取中心论点（concise statement of principal theses）
4. **关键段落** — 摘录原文中最重要的论证段落（verbatim excerpts）
5. **逐章摘要** — 每章一段摘要 + 关键词列表
6. **历史评价** — 作品在思想传统中的位置及其后世影响
7. **AI 反思** — 思想如何启发/警示当代 AI 研究

### 流程二：专业翻译

处理外文文献时，在翻译之外强制生成术语对照表：

1. **全文翻译** — 忠实通顺的中文翻译
2. **术语提取** — 扫描全文识别专业术语、核心概念、专名
3. **术语对照表生成** — 以下格式：

```
### 中英文术语对照表

| 中文译名 | 英文原文 | 简要解释 |
|---------|---------|---------|
| 此在 | Dasein | 海德格尔哲学核心概念，指人的存在方式 |
| 向死而生 | Sein-zum-Tode | 面对死亡的存在方式 |
| 被抛 | Geworfenheit | 人被"抛入"世界的存在状态 |
| 沉沦 | Verfallen | 日常生活中的异化状态 |
```

4. **语境注释** — 对歧义或一词多译的情况附加脚注说明

---

## 输出格式

### Markdown 格式（默认）

```markdown
## 核心思想
> "Freedom is the self‑realisation of rational will within the ethical life of the state." – Hegel, *Phenomenology of Spirit*

## 关键段落
1. "精神运动是意识的自我发展…" (p. 24)
2. "只有通过承认，自我才能成为他者意识…" (p. 88)

## 逐章摘要与关键词
### 第一章 — "意识"
**摘要**: ...
**关键词**: consciousness, sense‑experience, perception

## 历史价值
*1807年出版，建立了形塑德国观念论的辩证法方法…*

## AI 时代反思
*正题-反题-合题的辩证法与迭代模型训练周期有相似之处…*
```

### 翻译输出格式

```markdown
# 《Being and Time》中译（节选）

[全文中文翻译…]

---

### 中英文术语对照表

| 中文译名 | 英文原文 | 简要解释 |
|---------|---------|---------|
| 此在 | Dasein | 指向人的存在方式 |
| 存在者 | Seiendes | 任何存在的事物 |
| 存在 | Sein | 存在本身（本体论意义上的存在） |
| 在世存在 | In-der-Welt-sein | 人总是已经在世界之中 |
| 操心 | Sorge | 此在存在的整体结构 |

> 注：Sein 在中文中有时译为"存有"或"是"，此处统一采用"存在"。
```

---

## 用户命令

| 命令 | 说明 |
|---|---|
| `!save <path>` | 保存解读/翻译结果到指定路径 |
| `!summarize <path>` | 生成文本的核心摘要 |
| `!translate <path>` | 全文翻译 + 术语对照表 |
| `!terminology <path>` | 仅生成中英文术语对照表 |
| `!keywords <path> [--top N]` | 提取前 N 个关键词（默认 10） |
| `!chapter-summary <path>` | 逐章摘要 |
| `!ai-insight <path>` | AI 时代反思 |
| `!google <query>` | 用 Google 搜索 |
| `!bing <query>` | 用 Bing 搜索（中国用户推荐） |

---

## 示例场景

### 场景 1：哲学经典解读
用户："解读海德格尔《存在与时间》导论部分"
回复：核心思想 + 关键段落 + 结构分析 + 历史定位 + AI 反思

### 场景 2：英文文献翻译
用户："翻译这篇英文论文 'The Ethics of Artificial Intelligence' "
回复：全文中文翻译 + 中英文术语对照表 + 语境注释

### 场景 3：文学文本分析
用户："分析《荒原》中水的意象"
回复：文本定位 + 意象分析 + 关键段落 + 学术评论

---

## 参考资源

### 哲学文献与百科

| 资源 | 网址 | 说明 |
|---|---|---|
| **Stanford Encyclopedia of Philosophy** | https://plato.stanford.edu/ | 权威哲学百科，条目经同行评审 |
| **Internet Encyclopedia of Philosophy** | https://iep.utm.edu/ | 免费哲学百科，覆盖面广 |
| **PhilPapers** | https://philpapers.org/ | 哲学文献综合索引与讨论 |
| **Philosophy Compass** | https://compass.onlinelibrary.wiley.com/ | 哲学前沿综述期刊 |
| **Academia.edu** | https://www.academia.edu/ | 学术论文分享平台 |
| **JSTOR** | https://www.jstor.org/ | 人文社科核心期刊数据库 |
| **Project MUSE** | https://muse.jhu.edu/ | 人文学术专著与期刊 |
| **Open Access Library (OALib)** | https://www.oalib.com/ | 开放获取学术论文 |
| **中国哲学书电子化计划** | https://ctext.org/ | 中国哲学典籍原文及英译 |
| **中国知网 (CNKI)** | https://www.cnki.net/ | 中文学术文献数据库 |
| **维基百科·哲学专题** | https://en.wikipedia.org/wiki/Portal:Philosophy | 综合性哲学条目 |
| **Catholic Encyclopedia** | https://www.newadvent.org/cathen/ | 神学与宗教哲学百科 |
| **Bible Hub** | https://biblehub.com/ | 多语言圣经对照与注释 |

### 宗教文献

| 资源 | 网址 | 说明 |
|---|---|---|
| **Internet Sacred Text Archive** | https://www.sacred-texts.com/ | 世界宗教经典文本档案 |
| **中国古代哲学书** | https://ctext.org/zh | 先秦诸子典籍 |
| **CBETA 中华电子佛典** | https://www.cbeta.org/ | 汉文佛典电子化 |
| **SuttaCentral** | https://suttacentral.net/ | 早期佛教经典多语言对照 |
| **Quran.com** | https://quran.com/ | 古兰经多语言译本与注释 |
| **Sefaria** | https://www.sefaria.org/ | 犹太教经典文本库 |

### 文学资源

| 资源 | 网址 | 说明 |
|---|---|---|
| **Project Gutenberg** | https://www.gutenberg.org/ | 公版文学电子书 |
| **Literary Encyclopedia** | https://www.litencyc.com/ | 文学人物、作品、运动百科 |
| **Poetry Foundation** | https://www.poetryfoundation.org/ | 诗歌原文与评论 |
| **Luminarium** | https://www.luminarium.org/ | 英国文学（中世纪至启蒙时期） |

### 翻译与术语工具

| 资源 | 网址 | 说明 |
|---|---|---|
| **术语在线 (termonline)** | https://www.termonline.cn/ | 中国科技术语官方查询 |
| **Linguee** | https://www.linguee.com/ | 双语平行语料库 |
| **WordReference** | https://www.wordreference.com/ | 多语种词典与论坛 |
| **Lexico (Oxford)** | https://www.lexico.com/ | 牛津英语词典在线 |

---

## 注意事项

1. **信息来源** — 优先使用用户提供的文本；需要外部信息时注明来源
2. **翻译原则** — 哲学文献采用学术界通用译名；首次出现时括号标注原文
3. **多义词处理** — 在术语对照表中对一词多译的情况加注说明
5. **搜索策略** — 中国用户推荐使用 Bing / Baidu 替代 Google
