# 英国电商交易数据分析

这是一个在 AI 指导下完成的个人入门练习项目。
使用 Python、Pandas 和 Matplotlib，在 Jupyter Notebook 中分析交易数据。

## 数据来源

UCI Online Retail：
https://archive.ics.uci.edu/dataset/352/online%2Bretail

原始数据为 Online Retail.xlsx，共 541,909 行、8 列。

## 分析问题

2011 年 1—11 月的销售金额主要来自哪些月份、商品和市场？

## 计算规则

- 排除 InvoiceNo 以 C 开头的取消记录。
- 排除 Quantity ≤ 0、UnitPrice ≤ 0 的记录。
- 仅保留 2011 年 1—11 月；2011 年 12 月不完整。
- 排除 M、DOT、POST 三个特殊编号。
- Revenue = Quantity × UnitPrice。
- 月度、商品和市场分析均使用上述规则，最终保留 461,584 行。

## 主要发现

1. 11 月销售金额最高，为 1,458,925.53；2 月最低，为 509,167.87。
2. 商品编号 22423（三层蛋糕架）销售金额最高，为 140,607.91。
3. 英国销售金额为 7,481,365.13，占全部市场金额的 84.09%。

## 检查与限制

- 明细、月度及国家汇总金额核对一致，均为 8,896,339.78。
- Notebook 已重启内核并从头运行，未出现报错。
- 销售金额不是利润，也未扣除退款。
- 排除三个特殊编号，不保证已识别全部非商品项目。
- 商品编号 22502 存在两种描述，按编号合并统计。
- 不做客户画像，不凭趋势直接判断增长原因。
- 这是公开数据练习，未产生实际业务收益。

## 文件

- Retail_Sales_Analysis.ipynb：分析代码、结果和说明。
- data/raw/Online Retail.xlsx：原始数据。
- outputs/monthly_sales_2011.png：月度折线图。
- outputs/top10_products_2011.png：商品前十横向柱状图。
- outputs/market_share_2011.png：英国与其他市场占比图。

## 运行方法

1. 环境需要 Jupyter、pandas、openpyxl 和 matplotlib。
2. 将原始数据放到 data/raw/Online Retail.xlsx。
3. 在项目文件夹打开 Retail_Sales_Analysis.ipynb。
4. 重启内核并按顺序运行所有单元格。
5. 检查汇总金额和图表；图片保存在 outputs 文件夹。
