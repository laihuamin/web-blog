## mongodb基础概念

### 文档
文档是mongodb中的基础单元，非常类似于传统数据库中的行的概念，但是更具表现力

### 集合
集合就相当于传统数据库中的表，是一个拥有动态模式的表

### mongodb
mongodb是一个实例可以拥有多个相对独立的数据库，每个数据库可以拥有自己的集合

### _id
每个文档都有一个唯一且特殊的键——_id

### shell
mongodb自带javascript shell便于管理数据库

### 数据特点
在mongodb中不仅区分大小写，还区分类型

### 文档的注意点
1.mongodb的文档中不能有重复的键名
2.在mongodb中顺序不同是不同的，比如
```
{x:1,y:2} {y:2,x:1}
```

### 动态模式
意味着一个集合中的文档可以是各式各样的

### 集合的意义
1.方便使用特定类型的查找，加快速度
2.查询一个集合不如分开查询多个来的快捷
3.创建索引的时候，需要使用文档的附加结构，索引是根据集合来定义的

### 集合的命名
1.不能是空字符串
2.集合名不能使用\0字符
3.集合名不能以system.开头
4.创建集合不能在里面包含保留字$

### 子集合
按照惯例，子集合是在集合后面加上'.'，举个例子
```
集合是blog
子集合可以是blog.posts和blog.authors等
```

### 数据库的命名
1.不能是空字符串
2.不能含有/、\、.、"、*、<、>、:、|、?、$、\0，基本上只能使用字母和数字
3.数据库区分大小写
4.数据库名最多64个字节

### admin
有一些保留的数据库，admin就是其中之一，这个是管理身份的数据库，可以添加用户和删除用户

### local
保留数据库其中之一，这台数据库永远不能复制，且一台服务器上的所有的本地集合都可以存储在这个数据库中

### config
保留数据库其中之一，mongodb用于分片设置时，分片信息会存储在config数据库中