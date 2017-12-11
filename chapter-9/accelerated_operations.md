# 加速操作
`pandas` 支持使用 `numexpr` 库和 `bottleneck` 库来加速某些类型的数值运算和逻辑运算。

这些库在处理大数据集的时候特别有用，并且提供了大量的加速。`numexpr` 使用只能分块、缓存和多核。`bottleneck` 是一组专门的 `cython` 例程，在处理具有 `nans` 的数组时速度特别快。

下面是一个例子（100x100,000 的 `DataFrame`）:

| Operation | 0.11.0 (ms) | Prior Version (ms) | Ratio to Prior |
|:---:|:---:|:---:|:---:|
| df1 > df2 | 13.32 | 125.35 | 0.1063 |
| df1 * df2 | 21.71 | 36.63 | 0.5928 |
| df1 + df2 | 22.04 | 36.50 | 0.6039 |

强烈建议安装这个两个库。可以查看 [推荐的依赖](chapter-2/dependencies/recommended_dependencies.md) 这一节获取更多信息。

这两个库都是默认启用的，你可以通过如下设置来控制 (`pandas 0.20.0` 的新功能):

```python
pd.set_option('compute.use_bottleneck', False)
pd.set_option('compute.use_numexpr', False)
```
