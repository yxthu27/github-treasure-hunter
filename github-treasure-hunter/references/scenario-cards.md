# 场景卡片库

> **说明**：本文件是场景卡片的**参考模板库**，包含27个预设场景卡片，覆盖常见技术方向。
>
> **使用策略**：
> - **优先复用**：当用户需求与已有卡片匹配时，直接复用
> - **参考生成**：当用户需求无匹配卡片时，参考本文件的格式动态生成新卡片
> - 保持灵活性，不要局限于这27个卡片

## 目录

- [场景卡片模板](#场景卡片模板)
- [搜广推方向](#搜广推方向)
- [LLM方向](#llm方向)
- [前端方向](#前端方向)
- [后端方向](#后端方向)
- [数据工程方向](#数据工程方向)
- [DevOps方向](#devops方向)
- [计算机视觉方向](#计算机视觉方向)
- [NLP方向](#nlp方向)

---

## 场景卡片模板

```
【场景卡片{序号}】{场景名称}
- 核心任务：{该场景的核心任务列表，用→表示流程}
- 典型项目：{该场景的典型项目类型，用、分隔}
- 技术栈：{该场景常用的技术栈，用/分隔}
- 搜索关键词：{确定选择后使用的搜索关键词，英文}
```

---

## 搜广推方向

### 【场景卡片A】电商推荐系统
- 核心任务：召回→排序→重排
- 典型项目：用户行为建模、多目标优化、在线推理
- 技术栈：Faiss/Milvus、XGBoost/LightGBM、TensorFlow Serving
- 搜索关键词：recommendation system、collaborative filtering、deep learning recommendation、recommender system

### 【场景卡片B】搜索引擎
- 核心任务：Query理解→检索→排序
- 典型项目：倒排索引、语义检索、排序学习
- 技术栈：Elasticsearch、BERT/RoBERTa、Learning to Rank
- 搜索关键词：search engine、information retrieval、semantic search、learning to rank

### 【场景卡片C】广告投放系统
- 核心任务：CTR预估→出价→创意生成
- 典型项目：点击率预估、实时竞价、多模态创意
- 技术栈：DeepFM/DIN、Flink、线上serving
- 搜索关键词：ctr prediction、ad system、deepfm、din、click through rate

---

## LLM方向

### 【场景卡片A】RAG知识库问答
- 核心任务：文档处理→向量化→检索→生成
- 典型项目：企业知识库、文档问答、智能客服
- 技术栈：LangChain/LlamaIndex、Milvus/Chroma、OpenAI/DeepSeek
- 搜索关键词：rag、retrieval augmented generation、vector database、langchain、llamaindex

### 【场景卡片B】AI Agent开发
- 核心任务：规划→工具调用→执行→反思
- 典型项目：任务自动化、数据分析Agent、多Agent协作
- 技术栈：LangChain、AutoGen、CrewAI、MCP
- 搜索关键词：ai agent、langchain、autogen、crewai、function calling、mcp

### 【场景卡片C】LLM微调
- 核心任务：数据准备→微调训练→评估→部署
- 典型项目：垂直领域微调、指令微调、RLHF
- 技术栈：LoRA、QLoRA、Llama Factory、Unsloth
- 搜索关键词：llm fine-tuning、lora、qlora、rlhf、instruction tuning、peft

---

## 前端方向

### 【场景卡片A】React全栈应用
- 核心任务：组件开发→状态管理→API对接→部署
- 典型项目：中后台系统、电商平台、内容管理
- 技术栈：React/Next.js、Redux/Zustand、Tailwind CSS
- 搜索关键词：react、next.js、full stack、dashboard、admin panel

### 【场景卡片B】跨平台移动应用
- 核心任务：UI开发→平台适配→原生功能→上架
- 典型项目：社交应用、电商App、工具类App
- 技术栈：Flutter/React Native、Dart/TypeScript
- 搜索关键词：flutter、react native、mobile app、cross platform

### 【场景卡片C】前端可视化
- 核心任务：数据处理→图表渲染→交互设计→性能优化
- 典型项目：数据大屏、BI工具、3D展示
- 技术栈：D3.js、ECharts、Three.js、WebGL
- 搜索关键词：d3.js、echarts、three.js、data visualization、charts

---

## 后端方向

### 【场景卡片A】Python Web服务
- 核心任务：API设计→数据库→业务逻辑→部署
- 典型项目：RESTful API、微服务、后台管理系统
- 技术栈：FastAPI/Django/Flask、PostgreSQL、Redis
- 搜索关键词：fastapi、django、flask、python web、rest api

### 【场景卡片B】微服务架构
- 核心任务：服务拆分→通信→治理→监控
- 典型项目：电商系统、金融系统、分布式应用
- 技术栈：Spring Cloud、Go Micro、Kubernetes、gRPC
- 搜索关键词：microservices、spring cloud、kubernetes、distributed system

### 【场景卡片C】实时消息系统
- 核心任务：消息路由→持久化→推送→高可用
- 典型项目：即时通讯、通知系统、实时数据流
- 技术栈：Kafka、RabbitMQ、RocketMQ、WebSocket
- 搜索关键词：kafka、rabbitmq、rocketmq、message queue、realtime

---

## 数据工程方向

### 【场景卡片A】实时数据处理
- 核心任务：数据采集→流处理→存储→分析
- 典型项目：实时数仓、实时推荐、监控告警
- 技术栈：Apache Flink、Kafka、ClickHouse
- 搜索关键词：apache flink、stream processing、realtime analytics

### 【场景卡片B】ETL数据管道
- 核心任务：数据抽取→转换→加载→调度
- 典型项目：数据仓库、数据湖、数据集成
- 技术栈：Apache Spark、Airflow、dbt
- 搜索关键词：etl、apache spark、airflow、data pipeline、dbt

### 【场景卡片C】数据可视化平台
- 核心任务：数据源→建模→图表→仪表盘
- 典型项目：BI系统、报表平台、数据大屏
- 技术栈：Superset、Metabase、Plotly、Tableau
- 搜索关键词：superset、metabase、bi dashboard、data visualization

---

## DevOps方向

### 【场景卡片A】容器化与编排
- 核心任务：容器化→编排→服务发现→扩缩容
- 典型项目：云原生应用、微服务部署、CI/CD
- 技术栈：Docker、Kubernetes、Helm、Istio
- 搜索关键词：kubernetes、docker、helm、istio、cloud native

### 【场景卡片B】CI/CD自动化
- 核心任务：代码提交→构建→测试→部署
- 典型项目：DevOps流水线、自动化测试、灰度发布
- 技术栈：GitHub Actions、GitLab CI、Jenkins、ArgoCD
- 搜索关键词：github actions、gitlab ci、jenkins、argocd、cicd

### 【场景卡片C】监控与可观测性
- 核心任务：指标采集→日志收集→链路追踪→告警
- 典型项目：监控平台、日志分析、性能优化
- 技术栈：Prometheus、Grafana、ELK、Jaeger
- 搜索关键词：prometheus、grafana、elk、observability、monitoring

---

## 计算机视觉方向

### 【场景卡片A】目标检测
- 核心任务：数据标注→模型训练→推理→部署
- 典型项目：安防监控、自动驾驶、工业质检
- 技术栈：YOLO、Faster R-CNN、OpenCV、TensorRT
- 搜索关键词：object detection、yolo、faster rcnn、opencv、computer vision

### 【场景卡片B】图像生成
- 核心任务：数据准备→模型训练→生成→优化
- 典型项目：AI绘画、图像修复、风格迁移
- 技术栈：Stable Diffusion、GAN、Diffusion Models
- 搜索关键词：stable diffusion、gan、diffusion model、image generation

### 【场景卡片C】OCR文字识别
- 核心任务：图像预处理→文字检测→识别→后处理
- 典型项目：证件识别、发票识别、文档数字化
- 技术栈：PaddleOCR、Tesseract、CRNN、Transformer
- 搜索关键词：ocr、paddleocr、tesseract、text recognition

---

## NLP方向

### 【场景卡片A】文本分类与情感分析
- 核心任务：数据清洗→特征提取→模型训练→预测
- 典型项目：舆情监控、评论分析、内容审核
- 技术栈：BERT、TextCNN、Transformers、scikit-learn
- 搜索关键词：text classification、sentiment analysis、bert、nlp

### 【场景卡片B】命名实体识别（NER）
- 核心任务：数据标注→模型训练→实体抽取→应用
- 典型项目：知识图谱构建、信息抽取、智能客服
- 技术栈：BERT-CRF、spaCy、Hugging Face Transformers
- 搜索关键词：named entity recognition、ner、spacy、information extraction

### 【场景卡片C】机器翻译
- 核心任务：语料对齐→模型训练→翻译→后处理
- 典型项目：文档翻译、实时翻译、多语言平台
- 技术栈：Transformer、Marian NMT、Fairseq、OpenNMT
- 搜索关键词：machine translation、transformer、nmt、neural machine translation
