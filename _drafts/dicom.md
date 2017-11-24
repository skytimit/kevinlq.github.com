
> 所有压缩的(7FE0,0010)像素缓存的 DICOM 数据对象都是使
用显式 VR 小端字节序类型编码的(见 5.5.1)

## 无损压缩
  如果我们将原始数据中重复最多的元素进行处理,其实就
  是用最短的符号来替换他们
 	霍夫曼(Huffman)压缩算法

```
1000, 1001, 1002, 1002, 1000, 1000, 1001, 1057,....
一种典型的无损压缩算法是找出那些最频繁出现数值的重复性,像 1000 就可以用更短的符
号来代替。比如,如果我们用“a”来代替“1000”,那么上面的像素串就变成了:
a, 1001, 1002, 1002, a, a, 1001, 1057,....
由于 “a”比“1000”要短,因此我们整个数据串会变得更短,只要我们记住“a”代替了“1000”
```

## 有损压缩
```
1000, 1001, 1002, 1002, 1000, 1000, 1001, 1057,....
如果像素密度大约都是 1000,你真的能在视觉上分辨出 1000 和 1001 的区别吗?估计是不
行,因为在像素亮度上只有 0.1%的区别。因此,我们可以稍微修改一下这个序列,选择一
个灰阶作为可接受的容差然后将 1001 用 1000 替换:
1000, 1000, 1002, 1002, 1000, 1000, 1000, 1057,....
如果我们再对上面这个序列进行无损压缩,那么它就会变成:
a, a, 1002, 1002, a, a, a, 1057,....
```

## 流式压缩