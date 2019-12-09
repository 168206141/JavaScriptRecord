JSON：JavaScriptObjectNotation（JavaScript对象表示法）
JSON是存储和交换文本信息的语法，类似XML。
JSON比XML更小、更快、更易解析。
JSON文本格式在语法上与创建JavaScript对象的代码相同。
由于这种相似性，无需解析器，JavaScript程序能够使用内建的eval()函数，用JSON数据生成原生的JavaScript对象。

1.与XML异同点
与XML相同点：   *JSON是纯文本  
                          *JSON具有“自我描述性”（人类可读）
	          *JSON具有层级结构（值中存在值） 
	          *JSON可通过JavaScript进行解析  
	          *JSON数据可使用AJAX进行传输
与XML不同之处：* 没有结束标签
	          *更短
	          *读写数度更快
	          *能够使用内建的JavaScript eval() 方法进行解析
	          *使用数组
	          *不使用保留字
对于AJAX应用程序来说，JSON比XML更快更容易使用。

2.JSON语法
JSON语法是JavaScript对象表示语法的子集：
	          *数据在名称/值对中
	          *数据由逗号分隔
	          *大括号保存对象
	          *中括号保存数组
文件类型是“.json”

3.JSON对象
JSON对象使用在大括号（{}）中书写
对象可以包含多个key/value（键/值）对
key必须是字符串，value可以是合法的JSON数据类型（字符串，数字，对象，数组，布尔值或null）
key和value中使用冒号（：）分割
每个key/value对使用逗号（，）分开

4.JSON数组
JSON数组在中括号中书写
JSON中数组值必须是合法的JSON数据类型（字符串，数字，对象，数组，布尔值或null）
JavaScript中数组值可以是以上的数据类型，也可以是JavaScript的表达式，包括函数，日期，及undefined

5.JSON.parse()
JSON通常用于与服务端交换数据
在接收服务器数据时一般是字符串
我们可以使用JSON.parse() 方法将数据转换为JavaScript对象
语法：JSON.parse(text[, reviver])
参数说明： *text：必需，一个幼小的JSON字符串
  	 *reviver：可选，一个转换结果的函数，将对象的每个成员调用此函数

6.JSON.stringify()
JSON通常用于与服务端交换数据
再向服务端发送数据时一般是字符串
我们可以使用JSON.stringify() 方法将JavaScript对象转化为字符串
语法： JSON.stringify(value[, replacer[,space]])
参数说明： *value：必需，要转换的JavaScript值（通常为对象或数组）
  	 *replacer：可选，用于转换结果的函数或数组；如果replacer为函数，则JSON.stringify将调用函数，并传入每个成员的键和值
                                  使用返回值而不是原始值；如果此函数返回undefined，则排除成员；跟对象的键是一个空字符串：""。
                                 如果replacer是一个数组，则仅转换该数组中具有键值得成员；成员的转换顺序与键在数组的顺序一样；
		 当value参数也为数组时，将忽略replacer数组。
	 *space： 可选，文本添加缩进、空格和换行符，如果space是一个数字，则返回值文本在每个级别缩进指定数目的空格，
                                如果space大于10，则文本缩进10个空格；space也可以使用非数字，入：\t。
