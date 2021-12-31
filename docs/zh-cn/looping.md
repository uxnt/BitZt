# 循环
如果不重复执行一些代码块，很难编写一个有用的程序。为此，您可以使用循环语句。 Qi中有两个，如果您使用过其他命令式语言，应该很熟悉它们。
## 「而」循环
```而``` 循环执行一组语句，直到条件变为假。当在第一次迭代开始之前不知道迭代次数时，最好使用这些类型的循环。
```c
变量 i = 0；
变量 j = 0；
而（i 小 100）「
    j += i；
    如果（i % 2 等 0）「
        i += 3；
    」 否则「
        i += 1；
    」
」
打印行（j）；  // 2475
```
## 「对于」 循环
```而``` 循环在您想要无限循环或根据某些复杂条件循环时很有用。但在大多数情况下，您是在遍历一个列表、一系列数字或其他一些“序列”对象。 ```对于``` 循环可以使这个过程变得更加容易。

有 3 个可选的子句可以传入 ```对于``` 循环：
- 初始值设定项可以是变量声明或表达式。它在语句的开头运行一次。
- 条件子句是一个表达式。就像在```而``` 循环中一样，当它评估为```假``` 时，我们退出循环。
- 增量表达式在每次循环迭代结束时运行一次。
```c
变量 列表 = 【"一"，"二"，"三"，"四"，"五"】；
对于（变量 i = 0；i 小 列表。长度（）；i++）「
    打印（列表【i】+ " "）；
」
打印行（""）；
// 输出： 一 二 三 四 五
```

## 「打断」陈述
要立即退出正在执行的循环，可以使用```打断``` 语句。这有效地将你从最里面封闭的 ```对于``` 或 ```而``` 循环中解脱出来。
```c
变量 日志 = 【"好"，"好"，"好"，"错误"，"好"，"好"】；
对于（变量 i = 0；i 小 日志。长度（）；i++）「
    如果（日志【i】等 "错误"）「
        打印行（"错误在：" + 数到串（i）+ "行"）；
        打断；
    」
」
// 输出： 错误在：3行
```
## 「继续」陈述
要立即跳过当前迭代的其余部分，可以使用 ```继续``` 语句。这有效地将执行跳转到```对于``` 或 ```而``` 循环的下一次迭代的开始。
```c
变量 列表 = 【482，9654，861，6720，5738，2045，18397】；
对于（变量 i = 0；i 小 列表。长度（）；i++）「
    如果（列表【i】% 2 等 0）继续；
    打印（数到串（列表【i】）+ " "）；
」
打印行（""）；
// 输出： 861 2045 18397
```