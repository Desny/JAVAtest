# JAVAtest
For tests on MOOC
####First Week里的代码是用来进行分数（Fraction）相加运算的，得到的分数已经被约分

####Second Week里的代码是用来模拟时钟(clock)运行的，进行时分秒的进位和格式化输出

####CoinName使用HashMap来代替switch-case

####NoteBook使用泛型类（容器类）ArrayList

####CDandDVD 通过对两个类DVD,CD所拥有的共同属性进行合并，得到父类Item-->主要讨论了继承，向上造型等

Q: Second Week里的字符串如何设定格式？让字符串的变量以hh:mm:ss的格式展示出来呢？
A: 用format()  如：String s = String.format("%02d:%02d:%02d",hour,minute,second);  括号里面的书写格式和printf()应该是一样的
