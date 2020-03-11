Please have a look at the [wiki](https://github.com/obfuscator-llvm/obfuscator/wiki)!

Current version: [LLVM-4.0](https://github.com/obfuscator-llvm/obfuscator/tree/llvm-4.0)

You can cite Obfuscator-LLVM using the following Bibtex entry:

```
@INPROCEEDINGS{ieeespro2015-JunodRWM,
  author={Pascal Junod and Julien Rinaldini and Johan Wehrli and Julie Michielin},
  booktitle={Proceedings of the {IEEE/ACM} 1st International Workshop on Software Protection, {SPRO'15}, Firenze, Italy, May 19th, 2015},
  editor = {Brecht Wyseur},
  publisher = {IEEE},
  title={Obfuscator-{LLVM} -- Software Protection for the Masses},
  year={2015},
  pages={3--9},
  doi={10.1109/SPRO.2015.10},
}
```


# 01 Ollvm介绍

OLLVM（Obfuscator-LLVM）是瑞士西北应用科技大学安全实验室于2010年6月份发起的一个项目，该项目旨在提供一套开源的针对LLVM的代码混淆工具，以增加逆向工程的难度（该工具在github上地址点击此处跳转）。只不过Ollvm仅更新到llvm的4.0，2017年开始就没再更新。

# 02 Ollvm混淆介绍

Ollvm混淆主要分成三种模式，这三种模式主要是流程平坦化，指令替换，以及控制流伪造。
流程平坦化 ：这个模式主要通过将if-else语句替换成do-while语句，然后通过switch语句来对流程的控制，这样就能模糊基本块之间的前后关系。
指令替换 ：这个模式主要通过使用更复杂的指令序列来替换一些标准的二元运算符，从而增加逆向的难度。
控制流伪造 ：这个模式主要是会在一个简单的运算中外包好几层if-else的判断，从而增加逆向的难度。
如果想要对Ollvm有更深入的理解，可参阅论文《Obfuscating C++ programs via control flow flattening》


著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
