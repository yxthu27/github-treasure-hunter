# 搜索策略

## 目录

- [搜索概述](#搜索概述)
- [热门项目搜索](#热门项目搜索)
- [新项目搜索](#新项目搜索)
- [关键词构造](#关键词构造)
- [时间计算规则](#时间计算规则)

---

## 搜索概述

本 Skill 需要搜索两类项目：

| 类型 | 目的 | 筛选条件 |
|-----|------|---------|
| 热门项目 | 社区验证过的优质项目 | star > 1000、最近更新 < 6个月、有README |
| 新项目 | 早期发现的有潜力项目 | star < 500、创建时间在用户指定范围内、有README |

搜索使用 GitHub 的搜索语法，通过 Web 搜索工具执行。

---

## 热门项目搜索

### 搜索参数

| 参数 | 值 | 说明 |
|-----|-----|------|
| stars | >1000 | 社区认可度 |
| pushed | <6个月前 | 活跃维护 |
| 排序 | stars | 按star数降序 |

### 搜索语法示例

```
site:github.com "推荐系统" stars:>1000 pushed:>2025-01-01
```

### 搜索关键词组合

对于每个场景，使用以下关键词组合：

1. **主关键词**（场景核心词）
2. **细分关键词**（技术栈/子方向）
3. **筛选条件**（stars、pushed）

**示例：电商推荐系统**

| 搜索轮次 | 关键词 | 完整搜索语句 |
|---------|-------|-------------|
| 第1轮 | recommendation system | site:github.com "recommendation system" stars:>1000 |
| 第2轮 | collaborative filtering | site:github.com "collaborative filtering" stars:>1000 |
| 第3轮 | deep learning recommendation | site:github.com "deep learning recommendation" stars:>1000 |

---

## 新项目搜索

### 搜索参数

| 参数 | 值 | 说明 |
|-----|-----|------|
| stars | <500 | 早期项目 |
| created | >用户指定日期 | 新项目 |
| 排序 | stars 或 recently created | 增长趋势 |

### 时间范围计算

**动态获取当前日期**，计算 created 筛选条件：

| 用户输入 | 时间范围 | 示例（当前日期 2026-04-05） |
|---------|---------|---------------------------|
| 1个月 | created:>当前日期-30天 | created:>2026-03-06 |
| 3个月 | created:>当前日期-90天 | created:>2026-01-05 |
| 6个月 | created:>当前日期-180天 | created:>2025-10-07 |

### 搜索语法示例

```
site:github.com "recommendation system" stars:<500 created:>2026-01-05
```

---

## 关键词构造

### 通用关键词模板

```
{基础关键词} + {细分关键词} + {筛选条件}
```

### 各方向关键词对照

| 方向 | 基础关键词 | 细分关键词 |
|-----|-----------|-----------|
| 推荐系统 | recommendation system、recommender system | collaborative filtering、matrix factorization、deep learning recommendation |
| 搜索引擎 | search engine、information retrieval | semantic search、learning to rank、elasticsearch |
| RAG | rag、retrieval augmented generation | vector database、langchain、llamaindex |
| AI Agent | ai agent、autonomous agent | langchain、autogen、crewai、function calling |
| React | react、reactjs | next.js、react hooks、react native |
| Python Web | python web、python backend | fastapi、django、flask |
| 微服务 | microservices | kubernetes、docker、grpc |
| 实时处理 | realtime processing、stream processing | apache flink、kafka |
| 目标检测 | object detection | yolo、faster rcnn、ssd |
| 图像生成 | image generation | stable diffusion、gan、diffusion |

### 关键词组合策略

1. **先宽后窄**：先用宽泛关键词获取候选集，再用细分关键词补充
2. **同义词替换**：使用不同表达方式扩大搜索范围
3. **技术栈限定**：加入具体技术栈关键词提高相关性

---

## 时间计算规则

### 获取当前日期

Skill 运行时动态获取当前日期（YYYY-MM-DD格式）。

### 日期计算

| 时间粒度 | 计算方法 | 示例结果（2026-04-05） |
|---------|---------|---------------------|
| 1个月前 | 当前日期 - 30天 | 2026-03-06 |
| 3个月前 | 当前日期 - 90天 | 2026-01-05 |
| 6个月前 | 当前日期 - 180天 | 2025-10-07 |

### 应用到搜索

```
# 热门项目（最近6个月有更新）
pushed:>2025-10-07

# 新项目（3个月内创建）
created:>2026-01-05
```

---

## 搜索执行流程

1. 确定场景对应的搜索关键词（从场景卡片获取）
2. 计算时间范围（基于当前日期和用户输入）
3. 构造搜索语句（关键词 + 筛选条件）
4. 执行 Web 搜索
5. 提取项目信息（名称、链接、star数、更新时间、创建时间）
6. 验证项目真实性（检查README、确认数据）
7. 返回候选项目列表
