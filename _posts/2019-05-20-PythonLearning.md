---
layout: post
title:  "Python语言学习"
date:   2019-05-20 19:11:32
categories: 编程语言学习
tags: Python
---

* content
{:toc}

记录一下我学习Python的过程。





## 1、环境搭建

1）下载Python

具体地址在[这里](https://www.python.org/downloads/release/python-373/)，这是Python 3.7.3版本，我下载时是最新的，具体安装方法是[这样的](https://jingyan.baidu.com/album/0bc808fc42dfab1bd485b99f.html?picindex=2)。

2）选择开发环境

我选用的开发环境是Pycharm,可以自己搜索下载，然后需要注册码。或者直接按照[这里](https://www.cnblogs.com/dcpeng/p/9031405.html)进行安装也可以，里面还有如何创建一个工程。运行的按钮在右上角，绿色的三角。

## 2、开始学习了

我的学习方式很随意，也就是只关注一些基础的东西，然后之后用到什么就找什么。

### 2.1 2019-5-20

#### 1）Turtle模块

可以用来编写图形程序。一个简单的程序如下所示：

```python
import turtle # 导入turtle模块定义的所有函数

turtle.write("welcome to turtle") # 在turtle模块绘制一个文本

turtle.color("blue")                # 将turtle的画笔改为蓝色
turtle.penup()                       # 将turtle的画笔拿起
turtle.goto(-110,-25)                # 将turtle的画笔移动到某个位置
turtle.pendown()                     # 将turtle的画笔放下
turtle.circle(45)                    # 绘制半径为45的圆

turtle.done()
```
其运行结果为：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/Turtle结果.jpg)

常用方法：
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/Turtle方法1.jpg)
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/Turtle方法2.jpg)
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/Turtle方法3.jpg)
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/Turtle方法4.jpg)

#### 2）输入输出

```python
radius = eval(input("Enter a value for radius:"))
# input:让用户输入，括号内为提示语
# eval:求得括号内的值并转化为数值
area = radius * radius * 3.14159 # 计算
print("The area for radius",radius,"is",area) # 将括号里的内容输出
```
其运行结果为：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/输入输出.jpg)

#### 3）标识符

规则：

标识符由26个英文字符大小写（a~z,A~Z）、数字(0~9)、下划线(_)组成;
不能以数字开头;
不能是关键字;
严格区分大小写;
标识符的可以为任意长度。

#### 4）变量，赋值语句，赋值表达式,定名常量

变量用于引用在程序中可能引起变化的值

变量在被表达式使用之前必须被赋值

```python
y = 1
x = y + 1
x = x + 1
x , y = y , x # 交换变量，或者说同时赋值
```
定名常量是一种表示定值的标识符，代表永远不会改变的固定数据。Python没有命名常量的特殊语法，我们一般用全部大写来表示常量。
例如：
```python
PI = 3.14159
```
#### 5）数据类型、运算符、优先级、增强型赋值运算符

数据类型：整数、浮点数

运算符：
```python
a / b  #除法，得到浮点数结果
a // b #除法，得到整数结果
a ** b #表示a的b次幂
a % b  #取余运算
1.23E2 #科学计数法，1.23乘10的2次方
```
优先级：
1、括号内
2、指数运算
3、乘法、浮点除法(/)、整数除法(//),取余运算
4、加减法

增强型赋值运算符：
```python
a += 4   # a = a + 4
a -= 4   # a = a - 4
a *= 4   # a = a * 4
a /= 4   # a = a / 4
a //= 4  # a = a // 4
a %= 4   # a = a % 4
```

#### 6）类型转换、四舍五入

```python
value = 5.6 
int(vlue)     #返回整数部分，结果为5
round(value)  #四舍五入
```

#### 7）实例————显示当前时间

```python
import time

currentTime = time.time() # 以秒为单位的时间数据
totalSeconds = int(currentTime) # 取整
currentSeconds = totalSeconds % 60 # 取余得到秒

totalMinutes = totalSeconds // 60 # 取整得到以分钟为单位的时间数据
currentMinutes = totalMinutes % 60 # 取余得到分钟

totalHours = totalMinutes // 60 # 取整得到以小时为单位的时间数据
currentHour = totalHours % 24 # 取余得到小时

print("Current time is",currentHour,":",currentMinutes,":",currentSeconds)
```

### 2.2 2019-5-21


#### 1）常见的Python函数

1、内置函数：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/内置函数.jpg)

2、数学函数（使用时必须【import math】，然后【math.函数名（）】）：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/数学函数1.jpg)
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/数学函数2.jpg)

#### 2）字符串和字符

1、以双引号【""】括住多个字符构成的字符串，以单引号【''】括住单个字符的字符串或者空字符串。

2、函数ord()和chr()的用法：
```python
ch = 'a'   #字符串赋值

ord(ch)    #返回字符的ASCII码

chr(98)    #返回码字代表的字符
```

3、转义序列：
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/转义序列.jpg)

4、函数str
```python
s = str(3.4) # 将数字转换为字符串，输出'3.4'
```

5、字符串连接
```python
message = "welcome" + "to" + "python" # 输出'welcome to python'

s = "number" + str(3) # 输出'number3'

message += " and python is fun" # 在加上这一部分字符串
```

6、从控制台读取字符串

```python
s1 = input("Enter a string: ")

print("s1 is " + s1)
```

7、格式化数字和字符串

format()函数：
```python
print(format(57.859845,"10.2f")) # 格式化为：包括小数点在内共十位，小数点后2位

print(format(57.859845,".2f")) # 格式化为：宽度自动，小数点后保留2位

print(format(57.859845,"10.2e")) # 格式化为：所有东西加起来宽度10位，小数点后2位，小数点前1位，科学计数

print(format(7.859845,"10.2%")) # 格式化为：共10位宽度，小数点后2位，表示为百分数

print(format(57.859845,"<10.2f")) # 格式化为：包括小数点在内共10位，小数点后2位，但是靠左对齐

print(format(57,"10d")) # 格式化为：共10位,十进制
print(format(57,"10x")) # 格式化为：共10位,十六进制
print(format(57,"10o")) # 格式化为：共10位,八进制
print(format(57,"10b")) # 格式化为：共10位,二进制

print(format("welcome to","20s")) # 格式化为：共10位,默认左对齐
```

常用说明符：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/说明符.jpg)

#### 3）选择和循环

1、产生随机数字并进行比较运算
```python
import random

···
num1 = random.randint(0,9) # 在0到9之间产生随机整数
num2 = random.randint(0,9)

answer = eval(input("what is" + str(num1) + "+" + str(num2) + "？"))

print(num1,"+",num2,"=",answer,"is",num1 + num2 == answer)

```

2、if语句

在if块中的语句必须进行缩进，并且缩进的空白必须相同

if-else语句，注意else后面有【冒号】
```python
···
if num1 >= 0:
	num2 = num1
elif num1 <-9:
	num2 = -9
else:
	num2 = 0
```

3、逻辑运算符和条件表达式

```python
···
if num1 >= 0 and num2 >= 0:              #与
	num2 = num1
elseif num1 <-9 or num2 <-9:             #或
	num2 = -9
elseif (num1 != 1) == not (num2 == -9):  #非
	num2 = 0

max = num1 if num1 > num2 else num2     #条件表达式
```
4、while和for循环
 
注意【冒号】
```python
count = 0
while count < 100:
	count = count + 1

for v in range(4,8):    #默认步长为1
	print(v)

for v in range(4,8,2):  #步长为2
	print(v)
```

#### 4）函数

1、函数定义与调用
```python
def max(num1,num2):
	if num1 > num2:
		result = num1
	else:
		result = num2
	return result

def main():
	i = 5
	j = 2
	k = max(i,j)
	print(k)

main()
```
2、模块化代码

在GCDFunction.py中
```python
def gcd(n1,n2):
	gcd = 1
	k = 2
	while k <= n1 and k <= n2:
		if n1 % k == 0 and n2 % k == 0:
			gcd = k
		k += 1
	
	return gcd
```
在 test.py中
```python
from GCDFunction import gcd
input("n1:")
input("n2:")

print(gcd(n1,n2))
```

3、默认参数
```python
def area(width = 1,heigh = 2)
	print(width * heigh)

area() #默认1*2
area(width = 3) #默认3*2
```
4、返回多个输出
```python
def f(x,y):
    return x + y,x - y,x * y,x / y

t1,t2,t3,t4 = f(9,5)
print(t1,t2,t3,t4)
```
#### 5）类和对象

1、定义类,构造、访问对象

Circle.py
```python
import math

class Circle:
	def _ _init_ _(self,radius = 1):
		self.radius = radius

	def getPerimeter(self):
		return 2 * self.radius * math.pi

	def getArea(self):
		return self.radius * self.radius * math.pi

	def setRadius(self,radius):
		self.radius = radius
```
main.py
```python
from Circle import Circle 

c = Circle(5)
print(c.radius)
print(c.getPerimeter())
print(c.getArea())

```
2、隐藏数据域

以两个下划线开头表示私有数据
```python
import math

class Circle:
	def _ _init_ _(self,radius = 1):
		self._ _radius = radius

	def getPerimeter(self):
		return 2 * self._ _radius * math.pi

	def getArea(self):
		return self._ _radius * self._ _radius * math.pi

	def getRadius(self,radius):
		return self._ _radius
```

#### 6）str类

1、创建字符串
```python
s1 = "welcome"
s2 = "welcome" #此时s1和s2是同一字符串

len(s1) #长度
max(s1) #ASCII码最大值代表的字母
min(s1) #ASCII码最小值代表的字母
```
2、运算符
```python
s = "welcome"
s2 = "python"

#下标运算符
s[-1] #'e'
s[-2] #'m'

#截取运算符
s[1:4]  #'elc'
s[ :6]  #'welcom'
s[4: ]  #'ome'
s[1:-1] #'elcom'

#连接运算符
s3 = s + " to " + s2 #'welcome to python'

#复制运算符
s4 = 2 * s #'welcomewelcome' 

#in 和 not in 运算符
"come" in s     #True
"come" not in s #False

```
3、字符串
```python
s = "welcome"

#比较字符串
"green" == "glow"   #False
"green" != "glow"   #True
"green" > "glow"    #True
"green" >= "glow"   #True
"green" < "glow"    #False
"green" <= "glow"   #False

#迭代字符串
for i in range(0,len(s),2):
	print(s[i])

#测试字符串
s.isalnum()       #是数字且至少有一个字符，返回True
s.isalpha()       #是字母且至少有一个字符
s.isdigit()       #只含数字
s.isidentifier()  #是Python标识符
s.islower()       #全小写且至少有一个字符
s.isupper()       #全大写且至少有一个字符
s.isspace()       #只包含空格

#搜索字符串
s.endswith("me")     #以字符串"me"结尾，True
s.startswith("me")   #以字符串"me"开始，False
s.find("com")        #寻找最低下标，3,没有返回-1
s.rfind("o")         #返回最高下标，4，没有返回-1
s.count("o")         #出现次数

#转换字符串
s.capitalize()   #返回大写首字母的字符串
s.lower()        #返回所有字母小写的字符串
s.upper()        #返回所有字母大写的字符串
s.title()        #返回大写每个单词首字母的字符串
s.swapcase()     #返回大写变小写，小写变大写的字符串
s.replace(s1,s2) #返回s2代替s1后的字符串

#删除字符串空格
s.lstrip()   #去掉前端空白
s.rstrip()   #去掉末端空白
s.strip()    #去掉两端空白

#格式化字符串
s.center(10)  #宽度为10，字符串居中
s.ljust(10)   #宽度为10，字符串居左
s.rjust(10)   #宽度为10，字符串居右
s.format()  

```
#### 7）运算符重载


![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/运算符重载.jpg)


### 2.3 2019-5-23

#### 1）列表

1、创建列表
```python
list1 = []
list2 = [2,3,4]
list3 = ["red","green"]

```

2、对列表（序列）的操作
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/序列操作.jpg)

3、列表相关函数
```python
list1 = [2,3,4,1,32]

len(list1) #5
max(list1) #32
min(list1) #1
sum(list1) #42

import random

random.shuffle(list1) #随意排列列表元素
```

4、列表下标
```python
list1 = [2,3,4,1,32]

list1[-1] #32
list1[-3] #4
```
5、列表截取
```python
list1 = [2,3,5,7,9,1]

list1[2:4] #[5,7]
list1[ :2] #[2,3]
list1[3: ] #[7,9,1]
```
6、列表运算
```python
list1 = [2,3,5,7,9,1]

2 in list1     #True
2 not in list1 # False
```

7、列表解析
```python
list1 = [x for x in range(5)]    #[0,1,2,3,4]

list2 = [0.5*x for x in list1]   #[0.0,0.5,1.0,1.5,2.0]

list3 = [x for x in list2 if x<1.5] #[0.0,0.5,1.0]


```
8、列表方法

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/列表方法.jpg)

9、将字符串分成列表

```python
items = "jane john peter".split() #['jane','john','peter']

items = "05/23/2019".split("/") #['05','23','2019']
```

10、输入列表

```python
lst = []
print("Enter 10 numbers:")

for i in range(10):
	lst.append(eval(input()))


s = input("Enter 10 numbers separated by space")
items = s.split()
lst = [eval(x) for x in items]
```

#### 2）多维列表

```python
matrix = [
	[1,2,3,4,5],
	[6,7,8,9,0],
	[0,1,1,1,1],
	[1,0,0,0,0],
	[0,0,1,0,0]
]
```
1、初始化多维列表
```python
matrix = [] # 创建空列表

numOfRows = eval(input("Enter the rows:"))
numOfColumns = eval(input("Enter the Columns:"))

for row in range(numOfRows)
	matrix.append([]) #添加空白行
	for Columns in range(numOfColumns)
		value = eval(input("Enter the elements:"))
		matrix[row].append(value)

print(matrix)

```

2、列表元素求和
```python
matrix = [[1,2,3],[4,5,6],[7,8,9]] # 创建列表

total = 0

for row in matrix
	for value in row
		total += value

print(total)

```

3、列表元素按列求和

```python
matrix = [[1,2,3],[4,5,6],[7,8,9]] # 创建列表

for Columns in range(len(matrix[0])) # 3列
	total = 0
	for row in range(len(matrix)) #3行
		total += matrix[row][Columns]
	print(total)
```

4、列表元素行和最大

```python
matrix = [[1,2,3],[4,5,6],[7,8,9]] # 创建列表

maxRow = sum(matrix[0])
indexOfMaxRow = 0
for row in range(len(matrix)) # 3列
	if sum(matrix[row])>maxRow
		maxRow = sum(matrix[row])
		indexOfMaxRow = row

print(indexOfMaxRow,maxRow)
```

#### 3）继承与多态

1、父类与子类

从现有类定义新类叫继承，通用类（现有类）属于父类，特定类（新类）属于子类。

GeometricObject.py
```python
class GeometricObject:
	def __init__(self,color = "green",filled = True):
		self.__color = color
		self.__filled = filled

	def getColor(self):
		return self.__color

	def setColor(self,color):
		self.__color = color

	def isFilled(self):
		return self.__filled

	def setFilled(self,filled):
		self.__filled = filled

	def __str__(self):
		return "color:" + self.__color + \
			"and filled:" + str(self.__filled)
```
CircleFromGeometricObject.py
```python
from GeometricObject import GeometricObject
import math

class Circle(GeometricObject):
	def __init__(self,radius):
		super().__init__()
		self.__radius = radius

	def getRadius(self):
		return self.__radius

	def setRadius(self,radius):
		self.__radius = radius

	def getArea(self):
		return self.__radius * self.__radius * math.pi

	def getDiameter(self):
		return 2 * self.__radius

	def getPerimeter(self):
		return 2 * self.__radius * math.pi
	
	def printCircle(self):
		print(self.__str__() + "radius:" + \
			str(self.__radius))
```

2、多态

假设对象o是类C1、C2、...Cn的实例，C1是C2的子类，C2是C3的子类，Cn是object类，如果o调用一个方法P,那么会在C1、C2、...Cn按顺序找，直到找到为止。

3、isinstance函数

用来看对象是否为一个类的实例

### 2.4 2019-5-24

#### 1）文本输入输出

```python
fileVariable = open(filename,mode)
```
mode:
![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/文件模式.jpg)

#### 2）写入数据

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/写入数据.jpg)


### 2.3 2019-5-26（实战）

#### 1）模块导入
```python

#例1 导入整个datatime库
import datatime  
print(datatime.datatime.now())

#例2 从datatime库中导入datatime类
form datatime import datatime
print(datatime.now())

#例3 给datatime库起个别名
import datatime as dt
print(dt.datatime.now())
```

#### 2）append

```python
vec = []

vec.append(1,2) #[1,2]

vec.append([3]) #[1,2,[3]]

```

#### 3）numpy库

```python
import numpy as np

np.zeros((2,2)) #[[0,0],[0,0]]

net = np.dot(wh,h)+np.dot(wx,x)+b # wh * h + wx * x + b

```
[更多可以看这里](https://www.cnblogs.com/cwp-bg/p/9493583.html)


### 2.5 2019-9-12PyTorch入门

————————————————
版权声明：本文为CSDN博主「Liam Coder」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/out_of_memory_error/article/details/81258809

#### 1）基本数据类型

1、Tensor（张量）

Tensor（张量），它表示的其实就是一个多维矩阵，并有矩阵相关的运算操作。在使用上和numpy是对应的，它和numpy唯一的不同就是，pytorch可以在GPU上运行，而numpy不可以。所以，我们也可以使用Tensor来代替numpy的使用。当然，二者也可以相互转换。

Tensor的基本数据类型有五种：

32位浮点型：torch.FloatTensor。pyorch.Tensor()默认的就是这种类型。
64位整型：torch.LongTensor。
32位整型：torch.IntTensor。
16位整型：torch.ShortTensor。
64位浮点型：torch.DoubleTensor。

张量的定义方法：

```python
import torch
# 导包
 
a = torch.Tensor([[1, 2], [3, 4], [5, 6]])
print(a)

```

不过在项目之中，更多的做法是以特殊值或者随机值初始化一个矩阵，就像下面这样：

```python
import torch
 
# 定义一个3行2列的全为0的矩阵
b = torch.zeros((3, 2))
 
# 定义一个3行2列的随机值矩阵
c = torch.randn((3, 2))
 
# 定义一个3行2列全为1的矩阵
d = torch.ones((3, 2))
 
print(b)
print(c)
print(d)

```

Tensor和numpy.ndarray之间还可以相互转换，其方式如下：

Numpy转化为Tensor：torch.from_numpy(numpy矩阵)
Tensor转化为numpy：Tensor矩阵.numpy()

范例：

```python
import torch
import numpy as np
 
# 定义一个3行2列的全为0的矩阵
b = torch.randn((3, 2))
 
# tensor转化为numpy
numpy_b = b.numpy()
print(numpy_b)
 
# numpy转化为tensor
numpy_e = np.array([[1, 2], [3, 4], [5, 6]])
torch_e = torch.from_numpy(numpy_e)
 
print(numpy_e)
print(torch_e)

```

之前说过，numpy与Tensor最大的区别就是在对GPU的支持上。Tensor只需要调用cuda()函数就可以将其转化为能在GPU上运行的类型。

我们可以通过torch.cuda.is_available()函数来判断当前的环境是否支持GPU，如果支持，则返回True。所以，为保险起见，在项目代码中一般采取“先判断，后使用”的策略来保证代码的正常运行，其基本结构如下：

```python
import torch
 
# 定义一个3行2列的全为0的矩阵
tmp = torch.randn((3, 2))
 
# 如果支持GPU，则定义为GPU类型
if torch.cuda.is_available():
    inputs = tmp.cuda()
# 否则，定义为一般的Tensor类型
else:
    inputs = tmp

```

2、Variable(变量)

Pytorch里面的Variable类型数据功能更加强大，相当于是在Tensor外层套了一个壳子，这个壳子赋予了前向传播，反向传播，自动求导等功能，在计算图的构建中起的很重要的作用。Variable的结构图如下：

![jpg](https://github.com/neuzhaoxin/neuzhaoxin.github.io/raw/master/_posts/pictures/PythonLearning/pytorch_variable.jpg)

其中最重要的两个属性是：data和grad。Data表示该变量保存的实际数据，通过该属性可以访问到它所保存的原始张量类型，而关于该 variable（变量）的梯度会被累计到.grad 上去。

在使用Variable的时候需要从torch.autograd中导入。下面通过一个例子来看一下它自动求导的过程：

```python
import torch
from torch.autograd import Variable
 
# 定义三个Variable变量
x = Variable(torch.Tensor([1, 2, 3]), requires_grad=True)
w = Variable(torch.Tensor([2, 3, 4]), requires_grad=True)
b = Variable(torch.Tensor([3, 4, 5]), requires_grad=True)
 
# 构建计算图，公式为：y = w * x^2 + b
y = w * x * x + b
 
# 自动求导，计算梯度
y.backward(torch.Tensor([1, 1, 1]))
 
print(x.grad)
print(w.grad)
print(b.grad)

#上述代码的计算图为y = w * x^2 + b。
#对x, w, b分别求偏导为：
#x.grad = 2wx，
#w.grad=x^2，
#b.grad=1。
#代值检验可得计算结果是正确的。

```

#### 2）一维线性回归模型

1、

#### 3）多项式回归模型

#### 4）逻辑回归模型进行分类

#### 5）全连接神经网络

全连接神经网络是一种最基本的神经网络结构，英文为Full Connection，所以一般简称FC。

FC的准则很简单：神经网络中除输入层之外的每个节点都和上一层的所有节点有连接。

神经网络的第一层为输入层，最后一层为输出层，中间所有的层都为隐藏层。在计算神经网络层数的时候，一般不把输入层算做在内。

```python
from torch import nn

class simpleNet(nn.Module):
    """
    定义了一个简单的三层全连接神经网络，每一层都是线性的
    """
    def __init__(self, in_dim, n_hidden_1, n_hidden_2, out_dim):
        super(simpleNet, self).__init__()
        self.layer1 = nn.Linear(in_dim, n_hidden_1)
        self.layer2 = nn.Linear(n_hidden_1, n_hidden_2)
        self.layer3 = nn.Linear(n_hidden_2, out_dim)
 
    def forward(self, x):
        x = self.layer1(x)
        x = self.layer2(x)
        x = self.layer3(x)
        return x

class Activation_Net(nn.Module):
    """
    在上面的simpleNet的基础上，在每层的输出部分添加了激活函数
    """
    def __init__(self, in_dim, n_hidden_1, n_hidden_2, out_dim):
        super(Activation_Net, self).__init__()
        self.layer1 = nn.Sequential(nn.Linear(in_dim, n_hidden_1), nn.ReLU(True))
        self.layer2 = nn.Sequential(nn.Linear(n_hidden_1, n_hidden_2), nn.ReLU(True))
        self.layer3 = nn.Sequential(nn.Linear(n_hidden_2, out_dim))
        """
        这里的Sequential()函数的功能是将网络的层组合到一起。
        """
 
    def forward(self, x):
        x = self.layer1(x)
        x = self.layer2(x)
        x = self.layer3(x)
        return x


class Batch_Net(nn.Module):
    """
    在上面的Activation_Net的基础上，增加了一个加快收敛速度的方法——批标准化
    """
    def __init__(self, in_dim, n_hidden_1, n_hidden_2, out_dim):
        super(Batch_Net, self).__init__()
        self.layer1 = nn.Sequential(nn.Linear(in_dim, n_hidden_1), nn.BatchNorm1d(n_hidden_1), nn.ReLU(True))
        self.layer2 = nn.Sequential(nn.Linear(n_hidden_1, n_hidden_2), nn.BatchNorm1d(n_hidden_2), nn.ReLU(True))
        self.layer3 = nn.Sequential(nn.Linear(n_hidden_2, out_dim))
 
    def forward(self, x):
        x = self.layer1(x)
        x = self.layer2(x)
        x = self.layer3(x)
        return x

```



#### 6）卷积神经网络

#### 7）循环神经网络