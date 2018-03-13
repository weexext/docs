#java classLoader机制解析 [博客](http://blog.csdn.net/xbynet/article/details/51036892)
##前言:
java的由.class文件从加载,运行,卸载整个声明周期:加载 连接[校验 准备 解析 初始化] 使用 卸载
###双亲委派模型
bootstrpClassLoader extensionClassLoader appClassLoader
1.如何保障加载的class在内存中唯一性  
2.命名空间
3.每个class文件对应自己classloader
java中不是每个classloader加载自己class 流程:appclassloader检查缓存中是否用class文件 ==>extclassloader ==bootstrpclassloader 这样可以保证java的核心类库linkedlist hashMap等基础类库在虚拟机中只被加载唯一加载
其次 class.getParent()只是语法上定义 关系不是继承关系

###应用场景
1.动态加载 可用通过自定义classloader实现在虚拟运行的动态替换

































