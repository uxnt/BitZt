# 数字
与大多数其他脚本语言一样，Qi 用双精度浮点数表示所有数值。数字文字看起来与其他语言非常相似：
```c
123
0
-123
1.5
.4562
-930248.64323
10000000000
```

## 本机功能

#### **最小**（数字，数字）
返回两个参数中最小的数字。
```c
打印行（最小（1, 2））； // 1
```
#### **最大**（数字，数字）
返回两个参数中的最大数。
```c
打印行（最大（1, 2））； // 2
```
#### **四舍五入**（数字）
将给定的数字四舍五入到最接近的整数。
```c
打印行（四舍五入（1.5））； // 2
```
#### **四舍五入**（数字，数字）
将第一个参数四舍五入到第二个参数给出的小数位数。
```c
打印行（四舍五入（1.57, 1））； // 1.6
```
#### **平方根**（数字）
取输入数字的平方根。
```c
打印行（平方根（4））； // 2
```
#### **次方**（数字，数字）
计算引发到第二个参数的第一个参数。
```c
打印行（次方（4, 2））； // 16
```