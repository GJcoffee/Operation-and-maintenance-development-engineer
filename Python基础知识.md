# 第六章 字典

概念：字典是一系列的键值对，每个键都与一个值相关联，你可以使用键来访问与之相关联的值。

## 访问字典中的值

访问字典中的值，可依次指定字典名和放在方括号内的键:

```
alien_0 = {'color': 'green'} 
print(alien_0['color'])
```

## 添加键—值对

字典是一种动态结构，可随时在其中添加键—值对。要添加键—值对，可依次指定字典名、用方括号括起的键和相关联的值。

```
alien_0 = {'color': 'green', 'points': 5}
print(alien_0)
alien_0['x_position'] = 0 
alien_0['y_position'] = 25 
print(alien_0)
```

## 删除键值对

可使用del将相应的键--值对彻底删除。使用del语句时必须指定字典名和要删除的键。

```
alien_0 = {'color': 'green', 'points': 5}
print(alien_0)
del alien_0['points'] 
print(alien_0)
```

## 遍历字典

遍历所有的键值对：

```
user_0 = {
    'username': 'efermi',
    'first': 'enrico',
    'last': 'fermi',
    }
for key, value in user_0.items():
	print("\nKey:"+key)
	print("Value:"+value)
```

遍历字典中所有键：

```
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
    }
for name in favorite_languages.keys():
	print(name.title())
```



方法keys()并非只能用于遍历；实际上该方法返回一个列表，其中包含字典中的所有键。

```
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
    }
if 'erin' not in favorite_languages.keys():
	print("Erin,please take out poll")
```

按顺序遍历字典中的所有键:

```
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
    }
for name in sorted(favorite_languages.keys()):
    print(name.title()+", thank you for taking the poll.")
```

遍历字典中的所有值:

可使用方法values()，它返回一个值列表，而不包含任何键

```
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
    }
print("The following languages have been mentioned:")
for language in favorite_languages.values():
    print(language.title())
```

# 第7章 用户输入和while循环

求模运算符:处理数值信息时，求模运算符（%）是一个很有用的工具，它将两个数相除并返回

```
>>>4 % 3
1
>>>5 % 3
2
>>>6 % 3
0
>>>7 % 3
1
```

# 第9章类

1.方法__init__()

类中的函数称为方法；你前面学到的有关函数的一切都适用于方法，就目前而言，唯一重要的差别是调用方法的方式。❸处的方法__init__()是一个特殊的方法，每当你根据Dog类创建新实例时，Python都会自动运行它。在这个方法的名称中，开头和末尾各有两个下划线，这是一种约定，旨在避免Python默认方法与普通方法发生名称冲突。

创建和使用类

```
class Dog():❶
    """一次模拟小狗的简单尝试""" ❷
    def __init__(self,name,age):❸
        """初始化属性name和age"""
        self.name = name ❹
        self.age = age
    def sit(self):❺
        """模拟小狗被命令时蹲下"""
        print(self.name.title()+" is now sitting.")
    def roll_over(self):
        """模拟小狗被命令时打滚"""
        print(self.name.title()+" rolled over!")
```



# 测试代码：

单元测试用于核实函数的某个方面没有问题；

测试用例是一组单元测试，这些单元测试一起核实函数在各种情形下的行为都符合要求。

全覆盖式测试用例包含一整套单元测试，涵盖了各种可能的函数使用方式。
