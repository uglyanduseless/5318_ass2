# COMP5318 Assignment 2 - Image Classification

## 项目简介

本项目实现了基于CIFAR-10数据集的图像分类任务，使用了卷积神经网络(CNN)进行训练和评估。

## 文件结构

- `COMP5318-assignment2-template-notebook.ipynb` - 主要的Jupyter Notebook，包含完整的实现
- `COMP5318-assignment2-2025-specification-final-2.pdf` - 作业规范文档
- `Assignment2Data/` - CIFAR-10数据集（未包含在git中，需单独下载）

## 环境配置

### 必需的库

```bash
pip install numpy pandas matplotlib seaborn tensorflow scikit-learn jupyter
```

### Python版本

- Python 3.11+

## 使用方法

1. 克隆仓库：
```bash
git clone https://github.com/uglyanduseless/5318_ass2.git
cd 5318_ass2
```

2. 安装依赖：
```bash
pip install -r requirements.txt
```

3. 下载数据集（如果未包含）：
   - 将CIFAR-10数据文件（.npy格式）放入 `Assignment2Data/` 目录

4. 启动Jupyter Notebook：
```bash
jupyter notebook
```

5. 打开 `COMP5318-assignment2-template-notebook.ipynb` 并运行

## 项目内容

本项目实现了完整的机器学习流程：

### 1. 数据探索与预处理
- 数据集基本信息分析
- 类别分布可视化
- 像素值分布分析
- 数据归一化（0-1缩放）
- 训练/验证集分割

### 2. CNN模型设计
- 3个卷积块架构
- 每块包含2个卷积层 + MaxPooling + Dropout
- 滤波器数量递增：32 → 64 → 128
- 全连接层：128个神经元
- 输出层：10类softmax分类

### 3. 超参数调优
- 网格搜索策略
- 调优参数：
  - 学习率：[0.001, 0.0001]
  - Dropout率：[0.3, 0.5]
  - 批次大小：[32, 64]
- 详细结果记录和可视化

### 4. 模型评估
- 测试集性能评估
- 混淆矩阵
- 分类报告（precision, recall, F1-score）
- 错误分类样本分析

## 模型性能

详细的性能指标请参考notebook中的输出结果。

## 注意事项

- 数据文件（.npy）较大，未上传到GitHub
- 超参数搜索需要较长时间（15-30分钟）
- 建议使用GPU加速训练（可选）

## 作者

COMP5318 Machine Learning and Data Mining - 2025 S2

## 许可

本项目仅用于学习目的。

