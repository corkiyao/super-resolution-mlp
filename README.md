# super-resolution-mlp
MAXIM: Multi-Axis MLP for Image Processing  ##底层MLP
1.原文里的代码发现调试的时候，发现有些bug。一是原文输入是256*256，但是有些时候不需要256*256输入，所以修改成输入128*128，
但这个时候发现代码出现问题，作者公布的代码没有修复bug，是代码里面存在H=W=C的情况，所以导致当H、W发生变化时，会报错。
我在代码里，调整了这部分的代码。
2.原作者给出的代码是针对两阶段、单损失的，没有给出多损失的。查看相关的代码后，自己添加了损失监督为3。并且使用64*64能跑下去（窗口大小为8*8、4*4,）
3.第三方库timm库就不上传了，我是直接复制Swim-Transformer代码里面的，你可以自己调出来出来，添加上去。
