## [ torch 参数更多 ]torch.clamp
### [torch.clamp](https://pytorch.org/docs/stable/generated/torch.clamp.html#torch-clamp)

```python
torch.clamp(input,
            min=None,
            max=None,
            *,
            out=None)
```

### [paddle.clip](https://www.paddlepaddle.org.cn/documentation/docs/zh/develop/api/paddle/clip_cn.html#clip)

```python
paddle.clip(x,
            min=None,
            max=None,
            name=None)
```

PyTorch 相比 Paddle 支持更多其他参数，具体如下：
### 参数映射

| PyTorch       | PaddlePaddle | 备注                                                   |
| ------------- | ------------ | ------------------------------------------------------ |
| input       |  x             | 表示输入的 Tensor ，仅参数名不一致。  |
| min         | min            | 表示裁剪的最小值。                                      |
| max         | max            | 表示裁剪的最大值。                                      |
|  out        | -              | 表示输出的 Tensor ， Paddle 无此参数，需要转写。    |


### 转写示例
#### out：指定输出
```python
# PyTorch 写法
torch.clamp(torch.tensor([-1.7120,  0.1734]), min=-0.5, max=0.5, out=y)

# Paddle 写法
paddle.assign(paddle.clip(paddle.to_tensor([-1.7120,  0.1734]), min=-0.5, max=0.5), y)
```
