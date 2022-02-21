# Bestdori!自制谱社区和BanG Dream!官方谱面

此类目下面的功能均与**Bestdori!自制谱社区**和**BanG Dream!官方谱面**有关。

### 搜索官方歌曲（谱面）

*注：这个命令只能在和纱夜私聊时使用。*

#### 用途

通过提供的关键词，搜索BanG Dream!官方歌曲（谱面）。

#### 书写格式

`(搜索官方谱面|搜索官方谱|搜索官谱|官谱|official) [(-p|-page) 页码] <关键词1> [关键词2] ...`

其中：

`-p 页码`是当搜索结果有多页时，您通过输入它，指定返回的结果页码的一个参数。这个参数通常在您进行了一次查询后，发现当前页没有您想要的结果，再次使用相同的命令时附加的。

`关键词`包含两类：1. 您要搜索的官谱的关键词，可以输入任意关键词；2. 一个表达式，用于查询包含了符合该表达式的难度的谱面的歌曲名。关于表达式的写法，请您参考[附录：表达式的写法](appendix#附录：表达式的写法)。

*注意：此命令中关键词是“和”关系——这意味着，您查询到的结果一定是**符合您提供的所有限定条件的**；换句话说，如果您**提供了冲突的关键词，您不会查询到任何结果**。*

#### 返回内容

最多同时返回10个结果。包含对应歌曲的ID和歌曲名。

#### 示例

> official poppin =28

查询曲名或乐队名中包含**poppin**，并且有28难度谱面的歌曲。

> 官谱 bring it on

查询曲名或乐队名中包含**bring**、**it**和**on**的歌曲。

### 搜索自制谱面

*注：这个命令只能在和纱夜私聊时使用。*

#### 用途

通过提供的关键词，搜索Bestdori!自制谱社区的谱面。

#### 书写格式

`(搜索自制谱面|搜索自制谱|搜索自制|自制|community) [(-p|-page) 页码] [(-a|-升序)] <关键词1> [关键词2] ...`

其中：

`-p 页码`与[搜索官方歌曲（谱面）](bestdori-chart#搜索官方歌曲（谱面）)中的同名参数一致。

`-a`表示返回的结果按照发布时间从早到晚的顺序排列；不加则表示按照默认的发布时间从晚到早的顺序排列。

`关键词`是您要查询的谱面的曲名、艺术家等。

*注意：此命令中关键词是“和”关系——这意味着，您查询到的结果一定是**符合您提供的所有限定条件的**；换句话说，如果您**提供了冲突的关键词，您不会查询到任何结果**。*

#### 返回内容

最多同时返回10个结果。包含对应歌曲的ID、歌曲名和发布者。

#### 示例

> community conflict >=27

查询曲名或艺术家中包含**conflict**，并且难度大于或等于27的谱面。

> 自制 Brionac ~Lugh Lamhfhata~

查询曲名或艺术家中包含**Brionac**、**~Lugh**和**Lamhfhata~**的歌曲。

### 查询谱面基本信息

#### 用途

查询对应的官谱，或是Bestdori!自制谱社区谱面的基本信息。

#### 书写格式

`(看看谱|查查谱|kkp|ccp) <谱面id>`

其中：

`谱面id`是您所要查询的谱面的ID，有两种方式查询：1. 对于官方谱面来说，您可以在Bestdori!对应的歌曲详情页面，看到该歌曲的ID；对于自制谱面来说，您需要打开对应谱面详情页面，然后观察地址栏，其格式应该为`bestdori.com/community/charts/xxx...`，其中的`xxx`即为该谱面的ID，它应当是一个正整数；2. 使用[搜索官方歌曲（谱面）](bestdori-chart#搜索官方歌曲（谱面）)或[搜索自制谱面](bestdori-chart#搜索自制谱面)查询。

#### 返回内容

包含歌曲名、艺术家、谱面作者、难度名、难度、详情页链接和游玩链接。

#### 示例

> kkp 128 sp

查询ID为**128**的歌曲的信息。

> 看看谱 19078

查询ID为**19078**的谱面信息。

### 计算谱面难度

*该功能由**@稳音绫与6QHTSK**提供。*

*如果您想要体验完整功能，欢迎前往[彩绫的工具站](https://ayachan.fun)*。

#### 用途

使用定级器为指定的谱面估算各方面的难度等级。

#### 书写格式

`(难度查询|难度|difficulty|diff) <谱面id> [难度]`

其中：

`谱面id`与[查询谱面基本信息](bestdori-chart#查询谱面基本信息)中的同名参数一致。

`难度`是当您查询官方谱面时，可选择提供的额外参数。您可以填写`easy`、`normal`、`hard`、`expert`或`special`，亦可填写对应的简称：`ez`、`nm`、`hd`、`ex`、`sp`。如果不填写，则默认为`expert`。

#### 返回内容

以一张图片的形式呈现，包含歌曲的封面、歌曲名、艺术家、谱面作者、难度名、标定难度及各方面的难度信息。

#### 示例

> diff 1 sp

查询ID为**1**的歌曲的**special**难度的谱面难度信息。

> 难度 28994

查询ID为**28994**的谱面难度信息。

### 生成谱面预览

#### 用途

生成一张谱面的预览图片。

*注：如果谱面过长，生成可能会失败。*

#### 书写格式

`(预览谱面|预览|preview|pre) <谱面id> [难度]`

其中：

`谱面id`与[查询谱面基本信息](bestdori-chart#查询谱面基本信息)中的同名参数一致。

`难度`与[计算谱面难度](bestdori-chart#计算谱面难度)中的同名参数一致。

#### 返回内容

以一张图片的形式呈现，包含歌曲的封面、歌曲名、艺术家、谱面作者、难度名、标定难度及谱面的预览。

#### 示例

> pre 1 sp

生成ID为**1**的歌曲的**special**难度的谱面预览图。

> 预览 28994

生成ID为**28994**的谱面预览图。

### 查询音源

#### 用途

查询指定歌曲或谱面的音源链接。

#### 书写格式

`(查询音源|音源|audio|cxyy) <谱面id>`

其中：

`谱面id`与[查询谱面基本信息](bestdori-chart#查询谱面基本信息)中的同名参数一致。

#### 返回内容

为被查询的谱面的音源链接。

#### 示例

> cxyy 8

查询ID为**8**的歌曲的音源链接。

### 查询封面

#### 用途

查询指定歌曲或谱面的封面链接。

#### 书写格式

`(查询封面|封面|cover|cxfm) <谱面id>`

其中：

`谱面id`与[查询谱面基本信息](bestdori-chart#查询谱面基本信息)中的同名参数一致。

#### 返回内容

为被查询的谱面的封面链接。

#### 示例

> cxyy 8

查询ID为**8**的歌曲的封面链接。