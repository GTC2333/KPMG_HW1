
# KPMG_HW1 作业说明

本仓库包含五个问题（Q1–Q5）的数据分析Notebook与导出结果，支持全量运行与可视化输出。

## 环境准备
- 推荐 Python 3.10/3.11
- 安装依赖：
```bash
pip install -r requirements.txt
```
- 交互式运行：
```bash
jupyter notebook
```

## 数据位置
- PDF：/workspace/数据分析技术在企业内部审计中的应用以及具体案例.pdf
- Excel：
  - Case 1&2：/workspace/Sample Data.Case 1&2.xlsx
  - Case 3：/workspace/Sample Data.Case 3.xlsx
  - Case 4：/workspace/Sample Data.Case 4.xlsx
  - Case 5：/workspace/Sample Data.Case 5.xlsx

## Notebook
- 路径：/workspace/KPMG_HW1/notebooks
  - Q1_conflict.ipynb：供应商与员工利益冲突检测
  - Q2_procurement_spikes.ipynb：采购金额激增异常
  - Q3_sales_anomalies.ipynb：销售订单金额异常
  - Q4_pos_channel.ipynb：POS/渠道异常
  - Q5_travel_expense.ipynb：差旅与费用报销异常

每个Notebook包含：
- 子集开发以避免超时
- 全量运行的补充代码块（更长timeout）
- 导出清单CSV至 outputs

## 运行步骤
1. 安装依赖：`pip install -r requirements.txt`
2. 打开对应Notebook并按顺序运行全部单元，生成CSV输出至 `/workspace/KPMG_HW1/outputs`。
3. 查看答案报告：`/workspace/KPMG_HW1/answers/Q*/report.md`（包含可视化与部分结果表格）。

## 输出目录
- `/workspace/KPMG_HW1/outputs`：各题的清单和统计结果（CSV）
- `/workspace/KPMG_HW1/answers/Q*`：每题的Markdown报告与图片（PNG）

## 注意事项
- 大型数据解析时已采用容错（errors='coerce'）与日期标准化；如需固定格式，请在Notebook中指定`format`。
- 可根据业务特性调整阈值（如spike≥3或≥5、Z≥3、MAD阈值、IQR倍数）。
- 对季节性与促销政策强相关的数据，建议采用季节性基准与白名单策略降低误报。

## 环境配置（详细）

- 使用虚拟环境（推荐）：
  - Python venv：
    
  - Conda：
    

- 常见问题：中文字体缺失导致图表文字方块或警告
  - Ubuntu/Debian 安装：
    
  - 在 Notebook 中设置字体（可选）：
    

- 批量执行Notebook（可选，需安装 papermill）：
  

- 运行位置提醒：
  - 数据源位于 /workspace 路径下；请保持Notebook中的路径一致或使用 Pathlib 构建绝对路径。

## 下载依赖
- 统一使用：
- 若需增加：在 requirements.txt 中追加包名与版本范围，例如：。

## 运行指引（再次强调）
1. 安装依赖并启动 Jupyter：
   
2. 依次运行 Q1–Q5 Notebook；如数据量较大，可先运行子集单元再运行全量单元。
3. 检查 /workspace/KPMG_HW1/outputs 中导出的CSV，以及 /workspace/KPMG_HW1/answers/Q*/report.md 中的报告与图片。
