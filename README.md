# 排序实验项目

用于整理排序任务的数据准备、模型训练、融合与校准实验。

## 项目结构

```text
rank-lab/
├── data/                 # 原始数据；数据文件不提交 Git
├── notebooks/            # 数据探索与曲线分析
├── src/
│   ├── prepare.py        # 数据划分与预处理
│   ├── train_lr.py       # 逻辑回归基线
│   ├── train_lgbm.py     # LightGBM 模型
│   ├── train_deepfm.py   # DeepFM 模型
│   ├── blend.py          # 预测融合
│   └── calibrate.py      # 预测校准
├── outputs/              # 模型、预测结果与图表；生成文件不提交 Git
├── experiments.csv       # 实验记录
└── README.md
```

## 开始使用

1. 将数据放入本地 `data/` 目录。数据文件会被 `.gitignore` 忽略，请勿提交原始数据。
2. 在 `notebooks/` 中进行数据探索和曲线分析。
3. 按实际数据格式补充 `src/` 中的预处理、训练、融合和校准逻辑。
4. 将模型、预测文件和图表写入 `outputs/`；这些生成文件默认不会提交。
5. 每次实验在 `experiments.csv` 中记录配置、验证指标及结论。

## 实验记录

`experiments.csv` 提供空白记录模板。请记录可复现的配置、数据划分、评估指标和结论。当前脚本是项目骨架，具体实现需根据数据集和评估方案补充。
