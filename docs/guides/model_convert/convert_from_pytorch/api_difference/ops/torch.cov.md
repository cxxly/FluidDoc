## [ 仅 paddle 参数更多 ]torch.cov
### [torch.cov](https://pytorch.org/docs/stable/generated/torch.cov.html?highlight=cov#torch.cov)

```python
torch.cov(input,
          correction=1,
          fweights=None,
          aweights=None)
```

### [paddle.linalg.cov](https://www.paddlepaddle.org.cn/documentation/docs/zh/develop/api/paddle/linalg/cov_cn.html#cov)

```python
paddle.linalg.cov(x,
                  rowvar=True,
                  ddof=True,
                  fweights=None,
                  aweights=None,
                  name=None)
```

仅 paddle 参数更多，具体如下：
### 参数映射

| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| <font color='red'> input </font>         | <font color='red'> x </font>            | 输入的 Tensor 。                   |
| <font color='red'> correction </font>    | <font color='red'> ddof </font>          | 样本量和样本自由度之间的差异， 若为 True ，返回无偏估计结果；若为 False ，返回普通平均值计算结果。|
| fweights         | fweights  | 表示每一个观测向量的重复次数。 |
| aweights         | aweights  | 表示每一个观测向量的重要性。 |
| -             | <font color='red'> rowvar </font> | 以行或列作为一个观测变量， PyTorch 无此参数， Paddle 保持默认即可。 |
