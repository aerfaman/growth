###stub###

 - Stub是一种状态确认
 - Stub用简单的行为来替换复杂的行为

###mock###

 - Mock是一种行为确认
 - Mock模拟行为

###stub &amp;&amp; mock###
 - Stub从某种程度上来说，会返回我们一个特定的结果，用代码替换来方法。
 - Mock确保这个方法被调用。

###理解下的stub与mock###
stub从字面意义上来说是存根，存根可以理解为我们保留了一些预留的结果。这个时候我们相当于构建了这样一个特殊的测试场景，用于替换诸如网络或者IO口调度等高度不可预期的测试。如当我们需要去验证某个api被调用并返回了一个结果，举例在最小物联网系统设计中返回的json，我们可以在本地构建一个[{"id":1,"temperature":14,"sensors1":15,"sensors2":12,"led1":1}]的结果来当我们预期的数据，也就是所谓的存根。那么我们所要做的也就是解析json，并返回预期的结果。当我们依赖于网络时，此时测试容易出现问题。

mock从字面意义上来说是模仿，也就是说我们要在本地构造一个模仿的环境，而我们只需要验证我们的方法被调用了。