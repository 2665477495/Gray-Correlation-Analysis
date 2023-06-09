# 项目名称：Gray Correlation Analysis

## 描述

这个项目提供了一个用于灰色关联度分析的实现。灰色关联度分析是一种在不确定性条件下进行因素影响度量的方法。它被广泛用于系统性能评价、风险评估、决策支持等领域。

项目包含两个主要部分：

1. 数据预处理：这部分包含了数据同向化和无量纲化的处理。这是灰色关联度分析的前置步骤，用于确保数据的可比性。

2. 灰色关联度计算：这部分包含了灰色关联度的计算函数。可以将预处理后的数据输入到这个函数中，得到各个评价对象的关联度。

## 使用方法

在使用灰色关联度分析之前，首先需要对数据进行预处理，包括同向化和无量纲化。项目中的`DataPretreatment`类提供了这些功能。

```python
from common.data_pretreatment import DataPretreatment

# 实例化预处理类
pre = DataPretreatment(data, do_forward=True, do_normalize=True)

# 执行预处理
pre.pretreatment()
```

然后，可以使用`gray_corr`函数进行灰色关联度计算。

```python
from gray_correlation import gray_corr

# 计算灰色关联度
result = gray_corr(data)
```

## 测试

项目包含一个测试文件，用于测试灰色关联度分析的正确性。测试使用`unittest`框架编写。

## 贡献

欢迎各种形式的贡献，包括但不限于提交问题、改进代码、完善文档等。

## 许可

请查看项目中的LICENSE文件。
