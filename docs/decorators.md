# 接收函数装饰器

这个模块提供了一些常用操作的装饰器, 像判断文字中是否存在关键字、只处理特定的消息类型、忽略机器人自身的消息等等

## 各个装饰器签名

```python
{!../docs_src/decorators_outline.py!}
```

## 示例

```python
{!../docs_src/decorators_example.py!}
```

## 注意

- 这个模块都是一些简单的封装，可以根据需要使用

- 每个装饰器的作用是重合关系

```python
    @deco.in_content('a')
    @deco.in_content('b')
```

表示要求消息中同时存在 a 和 b，而不是 a 或 b

- 因为消息类型很多，比如图片视频语音，所以有些判断会很麻烦或者不好处理,
  对函数有疑问的请看注释或查看源码