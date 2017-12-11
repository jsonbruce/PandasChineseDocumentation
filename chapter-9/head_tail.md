# Head 和 Tail
使用 `head()` 和 `tail()` 方法来查看一个 `Series` 或 `DataFrame` 对象的一个小样本。默认显示 5 条记录，但也可以自定义显示几条。

```python
In [5]: long_series = pd.Series(np.random.randn(1000))

In [6]: long_series.head()
Out[6]:
0    0.229453
1    0.304418
2    0.736135
3   -0.859631
4   -0.424100
dtype: float64

In [7]: long_series.tail(3)
Out[7]:
997   -0.351587
998    1.136249
999   -0.448789
dtype: float64
```
