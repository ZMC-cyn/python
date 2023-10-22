# 实验三 Python列表

班级： 21计科04

学号： B20210302425

姓名： 陈宥男

Gitte地址：https://gitee.com/ZMC_cyn
GitHub地址：https://github.com/ZMC-cyn/py_work

---

## 实验目的

1. 学习Python的简单使用和列表操作
2. 学习Python中的if语句

## 实验环境

1. Git
2. Python 3.10
3. VSCode
4. VSCode插件

## 实验内容和步骤

### 第一部分

Python列表操作

完成教材《Python编程从入门到实践》下列章节的练习：

- 第3章 列表简介
- 第4章 操作列表
- 第5章 if语句

---

### 第二部分

在[Codewars网站](https://www.codewars.com)注册账号，完成下列Kata挑战：

---

#### 第一题：3和5的倍数（Multiples of 3 or 5）

难度： 6kyu

如果我们列出所有低于 10 的 3 或 5 倍数的自然数，我们得到 3、5、6 和 9。这些数的总和为 23. 完成一个函数，使其返回小于某个整数的所有是3 或 5 的倍数的数的总和。此外，如果数字为负数，则返回 0。

注意：如果一个数同时是3和5的倍数，应该只被算一次。

**提示：首先使用列表解析得到一个列表，元素全部是3或者5的倍数。
使用sum函数可以获取这个列表所有元素的和.**

代码提交地址：
<https://www.codewars.com/kata/514b92a657cdc65150000006>

---

#### 第二题： 重复字符的编码器（Duplicate Encoder）

难度： 6kyu

本练习的目的是将一个字符串转换为一个新的字符串，如果新字符串中的每个字符在原字符串中只出现一次，则为"("，如果该字符在原字符串中出现多次，则为")"。在判断一个字符是否是重复的时候，请忽略大写字母。

例如:

```python
"din"      =>  "((("
"recede"   =>  "()()()"
"Success"  =>  ")())())"
"(( @"     =>  "))(("
```

代码提交地址:
<https://www.codewars.com/kata/54b42f9314d9229fd6000d9c>

---

#### 第三题：括号匹配（Valid Braces）

难度：6kyu

写一个函数，接收一串括号，并确定括号的顺序是否有效。如果字符串是有效的，它应该返回True，如果是无效的，它应该返回False。
例如：

```python
"(){}[]" => True 
"([{}])" => True
 "(}" => False
 "[(])" => False 
"[({})](]" => False
```

**提示：
python中没有内置堆栈数据结构，可以直接使用`list`来作为堆栈，其中`append`方法用于入栈，`pop`方法可以出栈。**

代码提交地址
<https://www.codewars.com/kata/5277c8a221e209d3f6000b56>

---

#### 第四题： 从随机三元组中恢复秘密字符串(Recover a secret string from random triplets)

难度： 4kyu

有一个不为你所知的秘密字符串。给出一个随机三个字母的组合的集合，恢复原来的字符串。

这里的三个字母的组合被定义为三个字母的序列，每个字母在给定的字符串中出现在下一个字母之前。"whi "是字符串 "whatisup "的一个三个字母的组合。

作为一种简化，你可以假设没有一个字母在秘密字符串中出现超过一次。

对于给你的三个字母的组合，除了它们是有效的三个字母的组合以及它们包含足够的信息来推导出原始字符串之外，你可以不做任何假设。特别是，这意味着秘密字符串永远不会包含不出现在给你的三个字母的组合中的字母。

测试用例：

```python
secret = "whatisup"
triplets = [
  ['t','u','p'],
  ['w','h','i'],
  ['t','s','u'],
  ['a','t','s'],
  ['h','a','p'],
  ['t','i','s'],
  ['w','h','s']
]
test.assert_equals(recoverSecret(triplets), secret)
```

代码提交地址：
<https://www.codewars.com/kata/53f40dff5f9d31b813000774/train/python>

提示：

- 利用集合去掉`triplets`中的重复字母，得到字母集合`letters`，最后的`secret`应该由集合中的字母组成，`secret`长度也等于该集合。

```python
letters = {letter for triplet in triplets for letter in triplet }
length = len(letters)
```

- 创建函数`check_first_letter(triplets, first_letter)`，检测一个字母是不是secret的首字母，返回True或者False。
- 创建函数`remove_first_letter(triplets, first_letter)`,  从三元组中去掉首字母，返回新的三元组。
- 遍历字母集合letters，利用上面2个函数得到最后的结果`secret`。

---

#### 第五题： 去掉喷子的元音（Disemvowel Trolls）

难度： 7kyu

喷子正在攻击你的评论区!
处理这种情况的一个常见方法是删除喷子评论中的所有元音(字母：a,e,i,o,u)，以消除威胁。
你的任务是写一个函数，接收一个字符串并返回一个去除所有元音的新字符串。
例如，字符串 "This website is for losers LOL!"   将变成 "Ths wbst s fr lsrs LL!".

注意：对于这个Kata来说，y不被认为是元音。
代码提交地址：
<https://www.codewars.com/kata/52fba66badcd10859f00097e>

提示：

- 首先使用列表解析得到一个列表，列表中所有不是元音的字母。
- 使用字符串的join方法连结列表中所有的字母，例如：

```python
last_name = "lovelace"
letters = [letter for letter in last_name ]
print(letters) # ['l', 'o', 'v', 'e', 'l', 'a', 'c', 'e']
name = ''.join(letters) # name = "lovelace"
```

### 第三部分

使用Mermaid绘制程序流程图

安装VSCode插件：

- Markdown Preview Mermaid Support
- Mermaid Markdown Syntax Highlighting

使用Markdown语法绘制你的程序绘制程序流程图（至少一个），Markdown代码如下：

![程序流程图](/Experiments/img/2023-08-05-22-00-00.png)

显示效果如下：

```mermaid
flowchart LR
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]
```

查看Mermaid流程图语法-->[点击这里](https://mermaid.js.org/syntax/flowchart.html)

使用Markdown编辑器（例如VScode）编写本次实验的实验报告，包括[实验过程与结果](#实验过程与结果)、[实验考查](#实验考查)和[实验总结](#实验总结)，并将其导出为 **PDF格式** 来提交。

## 实验过程与结果

请将实验过程与结果放在这里，包括：

- [第一部分 Python列表操作和if语句](#第一部分)
- [第二部分 Codewars Kata挑战](#第二部分)
#### 第一题：3和5的倍数（Multiples of 3 or 5）
```python
def solution(number):
    pass
    if number < 0:
        return 0
    multiples = [x for x in range(number) if x % 3 == 0 or x % 5 == 0]
    return sum(multiples)
```
![](a.png)
#### 第二题： 重复字符的编码器（Duplicate Encoder）
```python
def duplicate_encode(word):
    #your code here
    word = word.lower()  # 将字符串转换为小写字母形式
    result = ""
    for char in word:
        if word.count(char) > 1:
            result += ")"
        else:
            result += "("
    return result
```
![](b.png)

#### 第三题：括号匹配（Valid Braces）
```python
def valid_braces(string):
    stack = []
    mapping = {")": "(", "}": "{", "]": "["}
    for char in string:
        if char in mapping.values():
            stack.append(char)
        elif char in mapping.keys():
            if not stack or stack[-1] != mapping[char]:
                return False
            stack.pop()
    return not stack
```
![](c.png)
---
#### 第四题： 从随机三元组中恢复秘密字符串(Recover a secret string from random triplets)
```python
def recoverSecret(triplets):
    res = []
    while triplets:
        t = list(zip(*triplets))
        big = list(set(t[0]) - set(t[1] + t[2]))
        if not big:
            break
        res.extend(big)
        for item in triplets:
            if big[0] == item[0]:
                item.pop(0)
                item.append(0)
    return ''.join(res)
```
![](d.png)
#### 第五题： 去掉喷子的元音（Disemvowel Trolls）
```python
def disemvowel(string_):

    vowels = 'aeiouAEIOU'
    result = ""
    for char in string_:
        if char not in vowels:
            result += char
    return result
```
![](e.png)
- [第三部分 使用Mermaid绘制程序流程图](#第三部分)

```mermaid
flowchart LR
A(开始) --> B[定义字符串s包含所有要移除的字符] 
 B --> C[遍历字符串中的每个字符char] 
C --> D{char是否在字符串s中?}
 D--是--> E[从字符串中移除char]
D否 -->F[保留char]
E-->C
F-->C
C-->G{是否还有符要处理?}
G--是-->C
G--否-->H[返回处理后的字符串]
H -->I[结束]
```
![](f.png)
注意代码需要使用markdown的代码块格式化，例如Git命令行语句应该使用下面的格式：

![Git命令](/Experiments/img/2023-07-26-22-48.png)

显示效果如下：

```bash
git init
git add .
git status
git commit -m "first commit"
```

如果是Python代码，应该使用下面代码块格式，例如：

![Python代码](/Experiments/img/2023-07-26-22-52-20.png)

显示效果如下：

```python
def add_binary(a,b):
    return bin(a+b)[2:]
```

代码运行结果的文本可以直接粘贴在这里。

**注意：不要使用截图，Markdown文档转换为Pdf格式后，截图可能会无法显示。**

## 实验考查

请使用自己的语言并使用尽量简短代码示例回答下面的问题，这些问题将在实验检查时用于提问和答辩以及实际的操作。

1. Python中的列表可以进行哪些操作？
增加元素：使用append()、extend()、insert()等方向列表中添加元素。
删除元素：使用remove()、pop()、del等方法从列表中删除元素。
访问元素：通过索引来访问列表中的元素，如list[index]。
切片：使用切片操作来获取列表的子集。
查找元素：使用in运算符来检查元素是否在列表中。
迭代：通过for循环遍历列表中的元素。
排序：使用sort()方法对列表进行排序。
反转：使用reverse()方法或切片操作来反转列表。
合并：使用+运算符或extend()方法合并多个列表。
获取长度：使用len()函数获取列表的长度。
复制：使用copy()方法或切片来复制列表。

2. 哪两种方法可以用来对Python的列表排序？这两种方法有和区别？
sort()方法：该方法在原地对列表进行排序，改变了列表本身，不返回新的列表。效率较高，适用于对
原列表进行排序。
sorted()函数：该函数返回一个新的排序后的列表，不改变原列表。适用于需要保留原列表的情况。

3. 如何将Python列表逆序打印？
my_list = [1, 2, 3, 4, 5]
my_list.reverse()
print(my_list)


4. Python中的列表执行哪些操作时效率比较高？哪些操作效率比较差？是否有类似的数据结构可以用来替代列表？
访问元素：由于列表是基于数组的数据结构，通过索引访问元素的操作非常高效。
增加元素：使用append()方法在列表末尾添加元素的操作通常很快。
Python中的列表执行以下操作时效率相对较低：
删除元素：使用remove()方法或del操作涉及元素的删除操作，可能需要移动其他元素，效率较低。
插入元素：使用insert()方法在列表中间插入元素，可能需要移动其他元素，效率也较低。
如果需要更高效的操作，可以考虑使用其他数据结构，如collections.deque（双端队列）用于高效的元
素插入和删除，或numpy数组用于数值计算。

5. 阅读《Fluent Python》Chapter 2. An Array of Sequence - Tuples Are Not Just Immutable Lists小节（p30-p35）。总结该小节的主要内容。

Python中的不同序列类型，包括列表、元组和字符串，以及它们的特性。
元组与列表的区别，主要是元组是不可变的，而列表是可变的。
列表的各种操作，如切片、拼接等。
使用元组作为记录的示例，以及元组拆包和命名元组的应用。
字符串的一些基本操作和格式化方法

## 实验总结
能够掌握使用列表操作