电子商务用户行为分析 (E-commerce User Behavior Analysis)
本项目旨在通过对真实电商交易数据的深度挖掘与分析，探索用户购买行为特征、识别高价值商品与核心客户群体。分析结果可为电商平台的库存管理、精准营销及客户关系维护提供数据支撑与决策依据。

项目背景
在竞争激烈的电子商务市场中，了解"什么商品最赚钱"以及"谁在大量消费"是制定商业策略的关键。本项目基于一段特定时间内的真实交易流水，通过数据清洗与探索性分析，量化了商品的销售表现与客户的消费能力，从而帮助业务团队聚焦核心资源，优化运营效率。

数据集介绍
本项目使用的原始数据文件为 ecommerce_data.csv，包含 12,462 行交易记录与 8 个字段。时间跨度为 2010年12月1日 至 2010年12月6日。

字段名称	数据类型	描述
InvoiceNo	字符串	发票号（唯一交易标识）
StockCode	字符串	商品编号
Description	字符串	商品描述
Quantity	浮点数	购买数量
InvoiceDate	字符串	发票日期与时间
UnitPrice	浮点数	商品单价
CustomerID	浮点数	客户唯一标识
Country	字符串	客户所在国家
分析工具与技术栈
编程语言：Python
数据处理：Pandas
数据可视化：Matplotlib
开发环境：Jupyter Notebook (ecommerce_analysis.ipynb)
数据清洗过程
原始数据中存在一定程度的缺失与冗余，为确保分析结果的准确性，执行了以下清洗步骤：

处理缺失值：原始数据中 CustomerID 缺失 3,506 条，Description 缺失 45 条，Quantity、InvoiceDate、UnitPrice、Country 各缺失 1 条。
删除无效记录：删除了所有 CustomerID 为空的行，以及其他列存在缺失值的行。
数据类型转换：将 InvoiceDate 转换为 datetime 格式，将 CustomerID 转换为整数类型。
去除重复值：清理了完全重复的交易记录。
清洗结果：最终保留有效数据 8,720 行，共丢弃 3,742 条不合规记录。

分析内容与主要发现
Top 10 最赚钱商品
基于总销售额（Total_Revenue）降序排列，以下商品为本期利润贡献主力：

排名	商品描述 (Description)	销量 (Quantity)	销售额 (Total_Revenue)
1	REGENCY CAKESTAND 3 TIER	476	5,363.40
2	BLACK RECORD COVER FRAME	1,141	3,868.35
3	WHITE HANGING HEART T-LIGHT HOLDER	1,014	2,665.70
4	CHILLI LIGHTS	572	2,379.24
5	RED WOOLLY HOTTIE WHITE HEART	726	2,275.14
6	SET 7 BABUSHKA NESTING BOXES	255	1,989.00
7	RED HARMONICA IN BOX	1,677	1,830.25
8	BOX OF VINTAGE ALPHABET BLOCKS	180	1,564.80
9	HAND WARMER SCOTTY DOG DESIGN	741	1,508.10
10	ASSORTED COLOUR BIRD ORNAMENT	920	1,478.00
Top 10 消费最高客户
基于客户总消费金额（Monetary）降序排列，以下为最具价值的核心客户：

排名	客户ID (CustomerID)	购买频次	总消费金额 (Monetary)
1	15061	73	9,407.34
2	13777	33	6,585.16
3	17850	297	5,391.21
4	16210	25	4,738.54
5	16029	12	4,271.52
6	17381	11	3,603.72
7	14911	128	3,445.18
8	13081	74	2,366.78
9	16754	2	2,002.40
10	12433	73	1,919.14
项目结构
E-commerce-User-Behavior-Analysis/
├── README.md                 # 项目说明文档
├── ecommerce_data.csv        # 原始数据集
└── ecommerce_analysis.ipynb  # 数据分析代码 (Jupyter Notebook)
如何运行代码
确保已安装 Python 3.x 及 Jupyter Notebook。
安装必要的依赖库：
pip install pandas matplotlib
启动 Jupyter Notebook 并打开 ecommerce_analysis.ipynb：
jupyter notebook ecommerce_analysis.ipynb
按顺序执行所有单元格即可复现完整的分析与可视化结果。
注意事项
数据隐私：本项目使用的数据仅用于学习与分析目的。在实际业务应用中，请务必对客户ID等敏感信息进行脱敏处理，遵守相关数据隐私法规。
数据时效性：当前数据集仅包含 2010年12月初的短期交易记录，分析结论可能受季节性或短期促销活动影响，建议结合更长周期的数据进行综合评估。
作者信息：Li Shuai Hao | 18634128810
