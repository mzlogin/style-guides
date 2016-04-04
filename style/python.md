# Python 编程风格

Reference: [Python 风格规范][1]

## 命名

**tip**

module\_name, package\_name, ClassName, method\_name, ExceptionName, function\_name, GLOBAL\_VAR\_NAME, instance\_var\_name, function\_parameter\_name, local\_var\_name.

**应该避免的名称**

1. 单字符名称，除了计数器和迭代器。
2. 包 / 模块名中的连字符 (-)
2. 双下划线开头并结尾的名称 (Python 保留，例如、_\_init\_\_)

**命名约定**

1. 所谓"内部 (Internal)"表示仅模块内可用，或者，在类内是保护或私有的。
2. 用单下划线 (\_) 开头表示模块变量或函数是 protected 的（使用 import * from 时不会包含）.
3. 用双下划线 (\_\_) 开头的实例变量或方法表示类内私有。
4. 将相关的类和顶级函数放在同一个模块里。不像 Java, 没必要限制一个类一个模块。
5. 对类名使用大写字母开头的单词（如 CapWords, 即 Pascal 风格）, 但是模块名应该用小写加下划线的方式（如 lower\_with\_under.py). 尽管已经有很多现存的模块使用类似于 CapWords.py 这样的命名，但现在已经不鼓励这样做，因为如果模块名碰巧和类名一致，这会让人困扰。

**Python 之父 Guido 推荐的规范**

| Type                       | Public               | Internal                                                                 |
|----------------------------|----------------------|--------------------------------------------------------------------------|
| Modules                    | lower\_with\_under   | \_lower\_with\_under
| Packages                   | lower\_with\_under   |                                                                          |
| Classes                    | CapWords             | \_CapWords                                                               |
| Exceptions                 | CapWords             |                                                                          |
| Functions                  | lower\_with\_under() | \_lower\_with\_under()                                                   |
| Global/Class Constants     | CAPS\_WITH\_UNDER    | \_CAPS\_WITH\_UNDER                                                      |
| Global/Class Variables     | lower\_with\_under   | \_lower\_with\_under                                                     |
| Instance Variables         | lower\_with\_under   | \_lower\_with\_under (protected) or \_\_lower\_with\_under (private)     |
| Method Names               | lower\_with\_under() | \_lower\_with\_under() (protected) or \_\_lower\_with\_under() (private) |
| Function/Method Parameters | lower\_with\_under   |                                                                          |
| Local Variables            | lower\_with\_under   |                                                                          |

[1]: http://zh-google-styleguide.readthedocs.org/en/latest/google-python-styleguide/python_style_rules/
