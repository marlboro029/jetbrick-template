Version 1.1.1 (2013-12-08)
-----------------------------

* [新增] #28 增强 asDefault() 方法扩展，支持设置默认值
* [新增] #30 增强 #put，一次支持多个变量的传递
* [新增] #31 增加 Spring FactoryBean 的集成支持
* [新增] #35 增加 #tag block(name) 默认实现，配合 #include 实现多个内容块的 layout
* [增强] #39 增强 #tag layout 功能，允许添加自定义参数给 layout 模板
* [修复] #20 The column of error line is wrong when the line contains '\t'
* [修复] #24 三元表达式如果使用 Interface 或者 Primitive Class 作为选项，会出现 NullPointerException
* [修复] #25 #if #else #end 语句后面貌似丢了一个换行
* [修复] #27 #set指令创建double型字面变量时，小数点后面跟0则不能通过编译
* [修复] #29 如果没有 #if 只有独立的 #else 或者 #end，没有报错，且剩余内容会被省略掉
* [修复] #33 属性安全调用问题？
* [修复] #34 拼写错误: #tag layout 中的实现用的是 bodyContext, 文档中描述的是 bodyContent，不一致
* [修复] #37 throw NullPointerException when method parameter is null.
* [修复] #40 #form 和 #for 指令冲突，编译失败
* [修复] #41 从 request uri 中获取模板路径存在问题，会出现404错误
* [修复] #42 include() 函数和 #tag layout() 传的 Map 参数出现编译错误

Version 1.1.0 (2013-12-02)
-----------------------------

* [新增] #12 增加自定义 Tag 功能
* [新增] #13 增加 #macro 宏定义
* [新增] #15 增加对类的静态字段和静态方法的直接访问
* [新增] #18 增加默认的 layout Tag 实现
* [新增] #19 与Nutz集成，实现JetTemplateView (Thanks wendal1985@gmail.com)
* [修复] #14 如果运算符的操作数的返回值是 void, 那么就会出现编译错误* [修复] #20 The column of error line is wrong when the line contains '\t'
* [修复] #21 NumberUtils.format(123) should be "123.00".
* [修复] #22 对于 ${bean.property}，优先使用 getXXX()
* [修复] #23 Fixed request uri in JetTemplateServlet/JetTemplateFilter

Version 1.0.2 (2013-11-22)
-----------------------------

* [新增] #10 增加选项：compile.always 第一次访问模板强制编译
* [新增] #16 允许 import 一个单独的 Class, 避免出现冲突
* [新增] #17 增加 iterator(start,stop,step) 代替 range(…) 函数
* [增强] #9 如果 compile.path 对应的目录非法或者没有权限不可写, 应该启动Engine时就报错
* [修复] #8 jetx 模板生成的 java 文件名可能会产生冲突
* [修复] #11 模板的路径如有使用 “../../file.jetx” 那么就会访问到 template.path 路径的外面

Version 1.0.1 (2013-11-20)
-----------------------------

* [新增] #1 支持 Servlet 2.x
* [新增] #4 增加指令注释支持，如： <!-- #if (...) --> 增强对可视化编辑器的友好度* [修复] #2 trim.directive.line 选项，如果指令两边为非空格，也会被 trim 
* [修复] #3 compile.debug 默认应该为 false
* [修复] #6 JDK 6 can't load the template class compiled using JDK 7.
* [修复] #7 JetTemplateServlet 和 JetTemplateFilter 默认可能输出错误的 contentType. 

Version 1.0.0 (2013-11-18)
-----------------------------

* 支持类似与 Velocity 的多种指令
* 支持静态编译
* 支持编译缓存
* 支持热加载
* 支持类型推导
* 支持泛型
* 支持可变参数方法调用
* 支持方法重载
* 支持类似于 Groovy 的方法扩展
* 支持函数扩展
* first public release
