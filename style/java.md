# Java 编程风格

**目录**

<!-- vim-markdown-toc GFM -->
* [命名](#命名)
	* [包](#包)
	* [类](#类)
	* [接口](#接口)
	* [方法](#方法)
	* [对象成员](#对象成员)
	* [类成员](#类成员)
	* [局部变量/方法参数](#局部变量方法参数)
	* [控件](#控件)
	* [XML](#xml)
		* [文件名](#文件名)
		* [控件 ID](#控件-id)
		* [字符串](#字符串)

<!-- vim-markdown-toc -->

## 命名

基本原则：

1. 表意清楚，不使用无意义的 `a`、`b` 等命名。

2. 不乱用简写，约定俗成的部分写法除外。

### 包

全小写，无连接线。

如： `deviceinfo`

### 类

每个单词的首字母大写。

如：`PackageManager`

### 接口

以大写 `I` 开头，每个单词首字母大写。

如：`ICallback`

### 方法

第一个单词的全小写，后续首字母大写。

如：`handleMessage`

### 对象成员

`m` 开头，后面每个单词的首字母大写。

如：`mNumForegroundProcesses`

### 类成员

`s` 开头，后面每个单词的首字母大写。

如：`sGlobalLock`

### 局部变量/方法参数

第一个单词全小写，后面每个单词的首字母大写。

如：`numProcesses`

如果需要表达的意思是以数字开头，限于变量名不能以数字开头，使用 `_` 开头。

如：`_1MB`

### 控件

Java 代码里的控件名遵循上面的原则。如果需要在变量名中体现控件类型，将类型放在最后。

如：`mCancelButton`

### XML

#### 文件名

**Layout**

Layout 文件命名为 `类型_功能.xml`。

如：`activity_main.xml`、`dialog_confirm.xml`、`listitem_city.xml`

包含项 Layout 命名为 `include_模块.xml`。

如：`include_head.xml`

**图片**

图片资源命名为 `前缀_功能模块[_状态].png`。

如：`bg_main_search_normal.png`、`btn_back_pressed`

selector 不带状态后缀。

#### 控件 ID

控件 id 以下划线连接的小写字母命名，命名表意清楚，一般不包含类型。

如：`android:id="@+id/junk_list"`

#### 字符串

命名里不含 title、dialog、button 等，直接用英文含义。

如：

```xml
<string name="ok">确定</string>
<string name="welcome_to_user">欢迎使用</string>
```
