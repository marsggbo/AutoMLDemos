# 《动手学 AutoML：从 NAS 到大语言模型优化实战》代码实例

本仓库包含《动手学 AutoML：从 NAS 到大语言模型优化实战》一书的配套代码实例，涵盖了神经网络架构搜索（NAS）、数据增强、模型压缩等 AutoML 核心技术的实践代码。

## 📚 目录结构

```
AutoMLDemos/
├── ch4/              # 第4章：NAS 搜索策略
│   ├── BO-NAS.ipynb          # 贝叶斯优化 NAS
│   ├── EA-NAS.ipynb          # 进化算法 NAS
│   └── RL-NAS.ipynb          # 强化学习 NAS
├── ch5/              # 第5章：NAS 模型评估
│   ├── nasbench101.ipynb     # NAS-Bench-101 基准
│   ├── nasbench201.ipynb     # NAS-Bench-201 基准
│   └── nasbenchasr.ipynb     # NAS-Bench-ASR 基准
├── ch7/              # 第7章：数据策略自动优化
│   ├── autoaug.ipynb              # AutoAugment 自动数据增强
│   ├── searchable_data_aug.ipynb  # 可搜索数据增强算法
│   └── assets/                    # 示例图片资源
│       └── cat.jpg
└── ch10_11/          # 第10-11章：实际应用案例
    ├── DARTS_CIFAR10.ipynb   # DARTS 在 CIFAR-10 上的应用
    ├── Pruner-Zero.ipynb     # Pruner-Zero 模型剪枝
    ├── RandomNAS_MNIST.ipynb # RandomNAS 在 MNIST 上的应用
    └── ResNet_CIFAR10.ipynb  # ResNet 在 CIFAR-10 上的基准
```

## 🚀 快速开始

### 环境要求

- Python >= 3.7
- PyTorch >= 1.8.1
- Jupyter Notebook 或 JupyterLab

### 安装依赖

主要依赖包包括：

```bash
pip install torch torchvision
pip install kornia  # ch7 章节需要
pip install git+https://github.com/marsggbo/hyperbox.git
```

部分章节可能还需要额外的依赖，具体请参考各章节的 notebook。

### 运行代码

1. 克隆本仓库：
```bash
git clone https://github.com/marsggbo/AutoMLDemos.git
cd AutoMLDemos
```

2. 启动 Jupyter Notebook：
```bash
jupyter notebook
```

3. 打开对应的章节文件夹，运行相应的 notebook 文件。

## 📖 各章节内容说明

### 第4章：NAS 搜索策略

本章介绍了三种主流的 NAS 搜索算法：

- **BO-NAS.ipynb**: 使用贝叶斯优化（Bayesian Optimization）进行神经网络架构搜索
- **EA-NAS.ipynb**: 使用进化算法（Evolutionary Algorithm）进行架构搜索
- **RL-NAS.ipynb**: 使用强化学习（Reinforcement Learning）进行架构搜索

### 第5章：NAS 模型评估

本章展示了如何使用 NAS-Bench 系列基准测试来评估 NAS 算法：

- **nasbench101.ipynb**: NAS-Bench-101 基准测试的使用方法
- **nasbench201.ipynb**: NAS-Bench-201 基准测试的使用方法
- **nasbenchasr.ipynb**: NAS-Bench-ASR（语音识别）基准测试的使用方法

### 第7章：数据策略自动优化

本章演示了自动数据增强技术：

- **autoaug.ipynb**: AutoAugment 自动数据增强策略的实现和应用
- **searchable_data_aug.ipynb**: 可搜索数据增强算法，包括基础的 3D 数据增强算子、可搜索的数据增强策略（使用 OperationSpace），以及与模型结构融合的可搜索模型模块

### 第10-11章：AutoML 项目实战

本章提供了多个实际应用案例：

- 基础
    - **RandomNAS_MNIST.ipynb**: RandomNAS 在 MNIST 数据集上的应用示例
    - **ResNet_CIFAR10.ipynb**: ResNet 在 CIFAR-10 上的基准测试，用于对比 NAS 方法的效果

- 进阶
    - **DARTS_CIFAR10.ipynb**: DARTS（Differentiable Architecture Search）在 CIFAR-10 数据集上的完整应用流程
    - **Pruner-Zero.ipynb**: Pruner-Zero 模型剪枝技术的实现

## 💡 使用建议

1. **按章节顺序学习**：建议按照章节顺序阅读和运行代码，有助于理解 AutoML 技术的递进关系。

2. **理解核心概念**：每个 notebook 都包含了详细的注释和说明，建议仔细阅读代码注释。

3. **动手实践**：尝试修改超参数、搜索空间等配置，观察对结果的影响。

4. **扩展实验**：可以尝试将代码应用到其他数据集或任务上。

## 🔗 相关资源

- **Hyperbox 框架**: https://github.com/marsggbo/hyperbox
- **Colab 在线运行**: 部分 notebook 支持在 Google Colab 上直接运行（点击 notebook 中的 Colab 徽章）

## 📝 注意事项

- 部分实验需要较长的运行时间，建议使用 GPU 加速
- 某些基准测试数据集需要单独下载，请按照 notebook 中的提示操作
- 如果遇到依赖问题，请检查 Python 和 PyTorch 版本是否匹配

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进代码和文档。

## 📄 许可证

本项目遵循原书的许可证要求。

---

**注意**：本代码仓库是《动手学 AutoML：从 NAS 到大语言模型优化实战》一书的配套资源，建议结合书籍内容一起学习使用。