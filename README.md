# 电商销售数据ETL与分析项目 (Sales Data ETL & Analysis Project)

这是一个使用Python进行端到端数据处理的入门项目。项目旨在处理和分析一整年的电子产品销售数据，从中提取关键业务洞察，并将最终分析结果存入MySQL数据库。


## 🚀 技术栈 (Tech Stack)
*   **数据处理与分析**: Python, Pandas, Jupyter Notebook
*   **数据库**: MySQL
*   **数据库连接**: SQLAlchemy, PyMySQL


## 📂 项目流程 (Project Workflow)
1.  **数据提取 (Extract)**: 从12个独立的CSV文件中加载原始销售数据。
2.  **数据转换 (Transform)**:
    *   将12个文件合并为一个完整的数据集。
    *   清洗数据，包括处理缺失值、删除重复的表头、转换数据类型。
    *   进行特征工程，从现有数据中创建新的分析维度（如月份、城市、销售额）。
3.  **数据分析 (Analysis)**: 针对清洗后的数据，回答了以下关键业务问题：
    *   哪个是销售额最高的月份？
    *   哪个城市的总销售额最高？
    *   应该在什么时间点投放广告以最大化效果？
    *   哪些产品最常被一起购买？
4.  **数据加载 (Load)**: 将最终的月度销售额分析报告，通过SQLAlchemy自动化写入MySQL数据库中的`monthly_sales_report`表。

---

## 📊 分析成果 (Key Insights)
*   **销售高峰**: 12月份是销售额最高的月份，达到了约460万美元。
*   **核心市场**: 旧金山(CA)是销售额最高的城市，贡献了超过820万美元。
*   **最佳广告时段**: 订单量在上午11点-12点和晚上7点左右达到峰值。
*   **热门组合**: (`iPhone`, `Lightning Charging Cable`) 和 (`Google Phone`, `USB-C Charging Cable`) 是最常见的捆绑销售组合。

---

## 🔧 如何运行 (How to Run)
1.  克隆本仓库。
2.  确保已安装Python及相关依赖库 (`pip install pandas sqlalchemy pymysql jupyterlab`)。
3.  在本地MySQL中创建一个数据库。
4.  修改Jupyter Notebook中数据库连接字符串为你自己的配置。
5.  按顺序运行Notebook中的单元格。
