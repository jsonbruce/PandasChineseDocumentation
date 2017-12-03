# 版本变化

## 新特性


## 后向不兼容的 API 更改


## 弃用 (Deprecations)
- `DataFrame.from_csv()` 和 `Series.from_csv()` 方法被弃用，使用 `read_csv()`
- `read_excel()` 被弃用 `sheetname`，使用 `sheet_name` 以和 `.to_excel()` 保持一致
- `read_excel()` 被弃用 `parse_cols`，使用 `usecols` 以和 `read_csv()` 保持一致
- `read_csv()` 弃用 `tupleize_cols` 参数。列元组将始终转换成 `MultiIndex`
- `DataFrame.to_csv()` 弃用 `tupleize_cols` 参数。多层索引列将始终作为行写入 CSV 文件
- `.take()` 方法弃用 `convert` 参数，因为它没有被遵守
- `pd.options.html.border` 被弃用，使用 `pd.options.display.html.border`
- `SeriesGroupBy.nth()` 被弃用 `True` 而使用 `all` 作为关键字参数 `dropna` 的值
- `DataFrame.as_blocks()` 弃用，因为暴露了内部实现
- `pd.TimeGrouper` 被弃用，使用 `pandas.Grouper`
- `cdate_range` 被弃用，使用 `bdate_range()`。后者可以使用 `weekmask` 和 `holidays` 参数来创建自定义频率日期范围
- `Series.astype()` 的关键字参数 `categories` 和 `ordered` 被弃用，使用 `CategoricalDtype`
- `Series`、`DataFrame`、`Panel`、`SparseSeries` 和 `SparseDataFrame` 的 `.get_value` 和 `.set_value` 方法被弃用，使用 `.iat[]` 或 `.at[]` 访问器
- 传递一个不存在的列到 `.to_excel(..., columns=)` 被弃用，而且在以后会引发 `KeyError` 异常
- `Series.where()`、`Series.mask()`、`DataFrame.where()` 和 `DataFrame.mask()` 的 `raise_on_error` 参数被弃用，使用 `errors=`
- 使用 `DataFrame.rename_axis()` 和 `Series.rename_axis()` 来修改索引和列标签被弃用，使用 `.rename` 方法。`rename_axis` 方法仍然可以用来修改索引或列的名称
- `reindex_axis()` 被弃用，使用 `reindex()`

### Series.select 和 DataFrame.select
`Series.select()` 方法和 `DataFrame.select()` 方法已经被弃用，使用 `df.loc[labels.map(crit)]`。

```python
In [72]: df = DataFrame({'A': [1, 2, 3]}, index=['foo', 'bar', 'baz'])
```

```python
In [3]: df.select(lambda x: x in ['bar', 'baz'])
FutureWarning: select is deprecated and will be removed in a future release. You can use .loc[crit] as a replacement
Out[3]:
     A
bar  2
baz  3
```

```python
In [73]: df.loc[df.index.map(lambda x: x in ['bar', 'baz'])]
Out[73]:
     A
bar  2
baz  3
```

### Series.argmax 和 Series.argmin
`Series.argmax()` 方法和 `Series.argmin()` 已经被弃用，使用 `Series.idxmax()` 和 `Series.idxmin()`。

为了兼容 Numpy 数组，`pd.Series` 实现了 `argmax` 和 `argmin` 这两个方法。从 pandas 0.13.0 开始，`argmax` 被设置为 `pandas.Series.idxmax()` 的别名，而 `argmin` 被设置为 `pandas.Series.idxmin()` 的别名。它们返回最大值和最小值的标签而不是位置。

`Series.argmax` 和 `Series.argmin` 的当前行为已被弃用。使用这两个方法回引起 `FutureWarning`。可以使用 `Series.idxmax()` 来获得最大值的标签，使用 `Series.values.argmax()` 来获得最大值的位置，对于最小值也是一样的结果。在未来的版本中 `Series.argmax` 和 `Series.argmin` 将返回最大值和最小值的位置。


## 删除以前版本的弃用/更改


## 性能提升
- 实例化 `SparseDataFrame` 的性能提升
- `Series.dt` 不再执行频率推断，在访问属性时速度大幅加快
- 通过不实现值来提升 `set_categories()` 的性能
- 在访问属性时 `Timestamp.microsecond` 不再重新计算
- 当数据已是类别类型时 `CategoricalIndex` 的性能提升
- 通过使用 `RangeIndex` 属性执行计算来提升 `RangeIndex.min()` 和 `RangeIndex.max()` 的性能


## 文档变化
- 一些 `NaT` 方法的文档描述（如 `NaT.ctime()`）不正确
- 移除版本小于 `v0.17` 的文档


## 错误修复
### 转换

### 索引

### I/O

### 绘图

### 分组/重采样/回滚

### 稀疏

### 重塑

### 数值

### 类别

### PyPy

### 其它
