<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

# 第一章 基础

## 1.1 基础编程模型
### 1.1.1 Java程序的基础结构
* 语言基础
	* 原始数据类型
	* 语句 - 声明、赋值、条件、循环、调用、返回
	* 数组
	* 静态方法
	* 字符串
	* 标准输入／输出
	* 数据抽象 

### 1.1.2 原始数据类型与表达式
* 标识符：由字母、数字、下划线和$组成的字符串，首字符不能是数字
* 四种最基本数据类型
	* 整型（int）
	* 双精度实数类型（double）
	* 布尔型（boolean）
	* 字符型（char）
* 表达式
	* 运算符优先级
		* \*和/(以及%)的优先级高于+和－
		* \!拥有最高优先级，之后是&&，接下来是||
		* 相同优先级运算符的运算顺序是从左至右   
* 类型转换
* 比较
* 其他原始类型

### 1.1.3 语句
* 声明语句
* 赋值语句
* 条件语句
* 循环语句
	* break - 立即从循环中退出
	* continue - 立即开始下一轮循环
* 调用和返回语句 

### 1.1.4 简便记法
* 声明并初始化
	* 在接近首次使用变量的地方声明它并将其初始化（为了限制它的作用域） 
* 隐式赋值
	* 递增／递减运算符
	* 其他复合运算符 
* 单语句代码段
	* 如果条件或循环语句的代码段只有一条语句，代码段的花括号可以省略 
* for语句

### 1.1.5 数组
* 创建并初始化数组
	* 声明数组的名字和类型
	* 创建数组（new关键字）
	* 初始化数组元素 
* 简化写法
	* double[] a = new double[N];
	* int[] a = {1, 2, 3, 4, 5};
* 使用数组
* 起别名
* 二维数组

### 1.1.6 静态方法
* 静态方法
	* 由签名(关键字public static以及函数的返回值，方法名以及一串各种类型的参数)和函数体(即包含在花括号中的代码)组成 
* 调用静态方法
* 方法的性质
	* 方法的参数按值传递
	* 方法名可以被重载
	* 方法只能返回一个值，但可以包含多个返回语句
	* 方法可以产生副作用 
* 递归
	* 递归总有一个最简单的情况
		* 方法的第一条语句总是一个包含return的条件语句
	* 递归调用总是去尝试解决一个规模更小的子问题，这样递归才能收敛到最简单的情况
	* 递归调用的父问题和尝试解决的子问题之间不应该有交集 
* 基础编程模型 
* 模块化编程 
* 单元测试
* 外部库
	* 系统标准库：java.lang.\* 

### 1.1.7 API
* 举例
* Java库
* 我们的标准库
* 你自己编写的库

### 1.1.8 字符串
* 字符串拼接
* 类型转换
* 自动转换
* 命令行参数

### 1.1.9 输入输出
* 命令和参数
* 标准输出
* 格式化输出
* 标准输入
	* 标准输入由<ctrl-z>或<ctrl-d>结束 
* 重定向与管道
	* 重定向: > or <
	* 管道: | 
* 基于文件的输入输出
* 标准绘图库(基本方法)
* 标准绘图库(控制方法)

### 1.1.10 二分查找
* 二分查找
* 开发用例
* 白名单过滤
* 性能

### 1.1.11 展望

## 1.2 数据抽象
### 1.2.1 使用抽象数据类型
* 抽象数据类型的API
* 继承的方法
* 用例代码
* 对象
	* 重要特性：状态、标识、行为 
* 创建对象 － new()
	* 为新的对象分配内存空间
	* 调用构造函数初始化对象中的值
	* 返回该对象的一个引用
* 调用实例方法
* 使用对象
	* 声明该类型的变量，以用来引用对象
	* 使用关键字new触发能够创建该类型的对象的一个构造函数
	* 使用变量名在语句或表达式中调用实例方法 
* 赋值语句
* 将对象作为参数
* 将对象作为返回值
* 数组也是对象
* 对象的数组

### 1.2.2 抽象数据类型举例
* 几何对象
* 信息处理
* 字符串
* 再谈输入输出

### 1.2.3 抽象数据类型的实现
* 实例变量
	* 使用private修饰 
* 构造函数
	* 一般用于初始化实例变量 
* 实例方法
* 作用域
* API、用例与实现

### 1.2.4 更多抽象数据类型的实现
* 日期
* 维护多个实现
* 累加器
* 可视化的累加器

### 1.2.5 数据类型的设计
* 封装
* 设计API
	* 只为用例提供它们所需要的，仅此而已 
* 算法与抽象数据类型
* 接口继承
* 实现继承
* 字符串的表示习惯
* 封装类型
* 等价性
	* 全序关系 
		* 自反性，x.equals(x)为true
		* 对称性，当且仅当y.equals(x)为true时，x.equals(y)返回true
		* 传递性，如果x.equals(y)和y.equals(z)均为true，x.equals(z)也将为true
	* 一致性，当两个对象均未被修改时，反复调用x.equals(y)总是返回相同的值
	* 非空性，x.equals(null)总是返回false 
* 内存管理
* 不可变性
* 契约式设计
* 异常与错误
* 断言

## 1.3 背包、队列和栈
### 1.3.1 API
* API
	* 背包

		```java
		public class  Bag<Item> implements Iterable<Item>
		              Bag()                  创建一个空背包
		        void  add(Item item)         添加一个元素
		     boolean  isEmpty()              背包是否为空
		         int  size()                 背包中的元素数量
		```
	* 先进先出(FIFO) 队列

		```java
		public class  Queue<Item> implements Iterable<Item>
		              Queue()                创建一个空队列
		        void  enqueue(Item item)     添加一个元素
		        Item  dequeue()              删除最早添加的元素
		     boolean  isEmpty()              队列是否为空
		         int  size()                 队列中的元素数量
		```
	* 下压(后进先出，LIFO) 栈

		```java
		public class  Stack<Item> implements Iterable<Item>
		              Stack()                创建一个空栈
		        void  push(Item item)        添加一个元素
		        Item  pop()                  删除最近添加的元素
		     boolean  isEmpty()              栈是否为空
		         int  size()                 栈中的元素数量
		```

* 泛型
	* 类名后的<Item>记号将Item定义为一个类型参数，它是一个象征性的占位符，表示的是用例将会使用的某种具体数据类型
	* 例如：Stack<String> stack = new Stack<String>(); 
* 自动装箱
* 可迭代的集合类型 
* 背包
	* 不支持从中删除原宿的集合数据类型 
* 先进先出队列
* 下压栈
* 算数表达式求值

### 1.3.2 集合类数据类型的实现
* 定容栈
* 泛型
	* 创建泛型数组：Item[] a = (Item[]) new Object[capacity]; 
* 调整数组大小
	* resize

		```java
		private void resize(int max) {
			Item[] temp = (Item[]) new Object[max];
			for (int i = 0; i < N; i++)
				temp[i] = a[i];
			a = temp;
		}
		```
	* push

		```java
		private void push(Item item) {
			if (N == a.length) resize(2 * a.length);
			a[N++] = item;
		}
		```
	* resize

		```java
		private Item pop() {
			Item item = a[--N];
			a[N] = null;
			if (N > 0 && N == a.length / 4) resize(a.length / 2)
			return item;
		}
		```
* 对象游离
* 迭代
	* 可迭代的集合数据类型
		* 集合数据类型必须实现一个iterator()方法并返回一个Iterator对象
		* Iterator类必须包含两个方法：hasNext()（返回一个布尔值）和next()（返回集合中的一个泛型元素）

##### --- 背包、队列和栈实现 ---
* 背包

	```java
	import java.util.Iterator;

	/**
	 * Created by tony on 6/21/17.
	 */
	public class Bag<Item> implements Iterable<Item> {
	    private Item[] a;
	    private int N = 0;
	
	    public Bag() {
	        a = (Item[]) new Object[1];
	    }
	
	    public void add(Item item) {
	        if (N == a.length) resize(2 * a.length);
	        a[N++] = item;
	    }
	
	    public boolean isEmpty() {
	        return N == 0;
	    }
	
	    public int size() {
	        return N;
	    }
	
	    private void resize(int max) {
	        Item[] temp = (Item[]) new Object[max];
	        for (int i = 0; i < N; i++)
	            temp[i] = a[i];
	        a = temp;
	    }
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new BagIterator();
	    }
	
	    private class BagIterator implements Iterator<Item> {
	        private int i = N;
	
	        @Override
	        public boolean hasNext() {
	            return i > 0;
	        }
	
	        @Override
	        public Item next() {
	            return a[--i];
	        }
	    }
	}
	```

* 栈

	```java
	import java.util.Iterator;
	
	/**
	 * Created by tony on 6/21/17.
	 */
	public class Stack<Item> implements Iterable<Item> {
	    private Item[] a;
	    private int N = 0;
	
	    private void resize(int max) {
	        Item[] temp = (Item[]) new Object[max];
	        for (int i = 0; i < N; i++)
	            temp[i] = a[i];
	        a = temp;
	    }
	
	    public Stack() {
	        a = (Item[]) new Object[1];
	    }
	
	    public void push(Item item) {
	        if (N == a.length) resize(2 * a.length);
	        a[N++] = item;
	    }
	
	    public Item pop() {
	        Item item = a[--N];
	        a[N] = null;
	        if (N > 0 && N == a.length / 4) resize(a.length / 2);
	        return item;
	    }
	
	    public boolean isEmpty() {
	        return N == 0;
	    }
	
	    public int size() {
	        return N;
	    }
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new ReverseArrayIterator();
	    }
	
	    private class ReverseArrayIterator implements Iterator<Item> {
	
	        private int i = N;
	
	        @Override
	        public boolean hasNext() {
	            return i > 0;
	        }
	
	        @Override
	        public Item next() {
	            return a[--i];
	        }
	    }
	}
	```
* 队列

	```java
	import java.util.Iterator;
	
	/**
	 * Created by tony on 6/21/17.
	 */
	public class Queue<Item> implements Iterable<Item> {
	    private Item[] a;
	    private int N = 0;
	    private int head = 0;
	    private int tail = 0;
	
	    public Queue() {
	        a = (Item[]) new Object[1];
	    }
	
	    public void enqueue(Item item) {
	        if (N == a.length) resize(2 * a.length);
	        a[tail++] = item;
	        N++;
	    }
	
	    public Item dequeue() {
	        Item item = a[head++];
	        a[head - 1] = null;
	        if (N > 0 && N == a.length / 4) resize(a.length / 2);
	        N--;
	        return item;
	    }
	
	    public boolean isEmpty() {
	        return N == 0;
	    }
	
	    public int size() {
	        return N;
	    }
	
	    private void resize(int max) {
	        Item[] temp = (Item[]) new Object[max];
	        for (int i = 0; i < N; i++)
	            temp[i] = a[i + head];
	        a = temp;
	    }
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new QueueIterator();
	    }
	
	    private class QueueIterator implements Iterator<Item> {
	        private int i = head;
	
	        @Override
	        public boolean hasNext() {
	            return i < tail;
	        }
	
	        @Override
	        public Item next() {
	            return a[i++];
	        }
	    }
	}
	```
* 缺点：push、pop、enqueue、dequeue操作耗时与栈及队列大小成正比

##### -----------------------------------

### 1.3.3 链表
	链表是一种递归的数据结构，它或者为空(null)，或者是指向一个结点(node)的引用，该结点含有一个泛型的元素和一个指向另一条链表的引用

* 结点纪录
* 构造链表
* 在表头插入结点
* 从表头删除结点
* 在表尾插入结点
* 其他位置的插入和删除操作
* 遍历
* 栈的实现

	```java
	import java.util.Iterator;
	
	/**
	 * Created by tony on 6/21/17.
	 */
	public class Stack<Item> implements Iterable<Item> {
	    private int N = 0;
	    private Node first;
	
	    private class Node {
	        Item item;
	        Node next;
	    }
	
	    public void push(Item item) {
	        Node oldFirst = first;
	        first = new Node();
	        first.item = item;
	        first.next = oldFirst;
	        N++;
	    }
	
	    public Item pop() {
	        Item item = first.item;
	        first = first.next;
	        N--;
	        return item;
	    }
	
	    public boolean isEmpty() {
	        return first == null;
	    }
	
	    public int size() {
	        return N;
	    }
	
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new ListIterator();
	    }
	
	    private class ListIterator implements Iterator<Item> {
	        private Node i = first;
	
	
	        @Override
	        public boolean hasNext() {
	            return i != null;
	        }
	
	        @Override
	        public Item next() {
	            Item item = i.item;
	            i = i.next;
	            return item;
	        }
	    }
	}

	```
* 队列的实现

	```java
	import java.util.Iterator;

	/**
	 * Created by tony on 6/21/17.
	 */
	public class Queue<Item> implements Iterable<Item> {
	    private int N = 0;
	    private Node first;
	    private Node last;
	
	    private class Node {
	        Item item;
	        Node next;
	    }
	
	    public void enqueue(Item item) {
	        Node oldLast = last;
	        last = new Node();
	        last.item = item;
	        if (isEmpty())
	            first = last;
	        else
	            oldLast.next = last;
	        N++;
	    }
	
	    public Item dequeue() {
	        Item item = first.item;
	        first = first.next;
	        if (isEmpty()) last = null;
	        N--;
	        return item;
	    }
	
	    public boolean isEmpty() {
	        return N == 0;
	    }
	
	    public int size() {
	        return N;
	    }
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new ListIterator();
	    }
	
	    private class ListIterator implements Iterator<Item> {
	        private Node i = first;
	
	        @Override
	        public boolean hasNext() {
	            return i != null;
	        }
	
	        @Override
	        public Item next() {
	            Item item = i.item;
	            i = i.next;
	            return item;
	        }
	    }
	}

	```
* 背包的实现

	```java
	import java.util.Iterator;
	
	/**
	 * Created by tony on 7/5/17.
	 */
	public class Bag<Item> implements Iterable<Item> {
	
	    private int N;
	    private Node first;
	
	    private class Node {
	        Item item;
	        Node next;
	    }
	
	    public void add(Item item) {
	        Node oldFirst = first;
	        first = new Node();
	        first.item = item;
	        first.next = oldFirst;
	        N++;
	    }
	
	    public boolean isEmpty() {
	        return first == null;
	    }
	
	    public int size() {
	        return N;
	    }
	
	    @Override
	    public Iterator<Item> iterator() {
	        return new BagIterator();
	    }
	
	    private class BagIterator implements Iterator<Item> {
	        private Node i = first;
	
	        @Override
	        public boolean hasNext() {
	            return i != null;
	        }
	
	        @Override
	        public Item next() {
	            Item item = i.item;
	            i = i.next;
	            return item;
	        }
	    }
	}

	```

### 1.3.4 综述
* 识别目标并使用数据抽象解决问题的步骤
	* 定义API
	* 根据特定的应用场景开发用例代码
	* 描述一种数据结构(一组值的表示)，并在API所对应的抽象数据类型的实现中根据它定义类的实例变量
	* 描述算法(实现一组操作的方式)，并根据它实现类中的实例方法
	* 分析算法的性能特点 

## 1.4 算法分析
### 1.4.1 科学方法
* 细致地观察真实世界的特点，通常还要有精确的测量
* 根据观察结果提出假设模型
* 根据模型预测未来的事件
* 继续观察并核实预测的准确性
* 如此反复直到确认预测和观察一致

### 1.4.2 观察
* 举例
* 计时器

	```java
	public class Stopwatch {
		private final long start;
		
		public Stopwatch() {
			start = System.currentTimeMillis();
		}
		
		public double elapsedTime() {
			long now = System.currentTimeMillis();
			return (now - start) / 1000.0;
		}
	}
	```
	
* 实验数据的分析

### 1.4.3 数学模型
* 近似
	* \\(g(N) \sim af(N)\\)，其中 \\(f(N) = N^b(logN)^c \\)，a、b和c均为常数，将\\(f(N)\\)称为\\(g(N)\\)的增长的数量级
* 近似运行时间
* 对增长数量级的猜想
* 算法的分析
* 成本模型
	* 使用成本模型来评估算法的性质，这个模型定义了算法中的基本操作 
* 总结

### 1.4.4 增长数量级的分类

| 描述 | 常数级别 | 对数级别 | 线性级别 | 线性对数级别 | 平方级别 | 立方级别 | 指数级别 |
| :-: | :-----: | :----: | :-----: | :--------: | :-----: | :-----: | :-----: |
| 增长的数量级 | \\(1\\) | \\(logN\\) | \\(N\\) | \\(NlogN\\) | \\(N^2\\) | \\(N^3\\) | \\(2^N\\) | 

* 算法效率：常数 > 对数 > 线性 > 线性对数 > 平方 > 立方 > 指数

### 1.4.5 设计更快的算法
* 热身运动 2-sum
* 3-sum 问题的快速算法
* 下界
	* 实现并分析该问题的一种简单的解法（暴力算法）
	* 考查算法的各种改进，通常都能降低算法所需的运行时间的增长数量级
	* 用实验证明新的算法更快 

### 1.4.6 倍率实验
* 如果\\(T(N) \sim aN^blgN\\)，那么\\(T(2N)/T(N) \sim 2^b\\) 

* 评估它解决大型问题的可行性
* 评估使用更快的计算机所产生的价值

### 1.4.7 注意事项
* 大常数
* 非决定性的内循环
* 指令时间
* 系统因素
* 不分伯仲
* 对输入的强烈依赖
* 多个问题参量

### 1.4.8 处理对于输入的依赖
* 输入模型
* 对最坏情况下的性能的保证
* 随机化算法
* 操作序列
* 均摊分析

### 1.4.9 内存（Java）

	PS: 在递归程序中创建数组或是其他大型对象是危险的

* 对象
	* **一个对象本身的开销一般为16字节**（包括一个指向对象的类的引用、垃圾收集信息以及同步信息） 
	* **实例变量的引用占用8字节**
* 链表
	* **Node对象需要使用40字节**（包括16字节的对象开销，指向Item和Node对象的引用各需8字节，还有个8字节的额外开销） 
* 数组
	* **一个原始数据类型的数组一般需要24字节的头信息**（16字节的对象开销，4字节用于保存长度以及4填充字节） 
* 字符串对象
	* **除字符数组之外，一个String对象占用40字节**（16字节表示对象，三个int实例变量各需4字节，数组引用8字节，4填充字节） 
* 字符串的值和子字符串
	* **一个子字符串所需的额外内存是一个常数（40字节），构造一个子字符串所需的时间也是常数**（因为子字符串与原字符串共用value[]数组） 

### 1.4.10 展望

## 1.5 案例研究: union-find算法
### 1.5.1 动态连通性
* 网络
* 变量名等价性
* 数学集合

### 1.5.2 实现
* quick-find 算法

	```java
	/**
	 * Created by tony on 7/17/17.
	 * Quick-Find
	 */
	public class UF {
	
	    private int[] id;
	    private int count;
	
	    public UF(int N) {
	        id = new int[N];
	        for (int i = 0; i < N; i++)
	            id[i] = i;
	        count = N;
	    }
	
	    public void union(int p, int q) {
	        int pID = find(p);
	        int qID = find(q);
	        if (pID != qID) {
	            for (int i = 0; i < id.length; i++)
	                if (id[i] == pID)
	                    id[i] = qID;
	            count--;
	        }
	    }
	
	    public int find(int p) {
	        return id[p];
	    }
	
	    public boolean connected(int p, int q) {
	        return find(p) == find(q);
	    }
	
	    public int count() {
	        return count;
	    }
	}
	```

* quick-find 算法的分析
	* union()操作访问数组次数在 \\((N+3)\\) 到 \\((2N+1)\\) 次
	* find()操作访问数组1次
	* union整个数组，时间复杂度为 \\(N^2\\) 

* quick-union 算法

	```java
	/**
	 * Created by tony on 7/17/17.
	 * Quick-Find
	 */
	public class QuickUnionUF {
	
	    private int[] id;
	    private int count;
	
	    public QuickUnionUF(int N) {
	        id = new int[N];
	        for (int i = 0; i < N; i++)
	            id[i] = i;
	        count = N;
	    }
	
	    public void union(int p, int q) {
	        int rootP = find(p);
	        int rootQ = find(q);
	        if (rootP != rootQ) {
	            id[rootP] = rootQ;
	            count--;
	        }
	    }
	
	    public int find(int p) {
	        while (p != id[p])
	            p = id[p];
	        return p;
	    }
	
	    public boolean connected(int p, int q) {
	        return find(p) == find(q);
	    }
	
	    public int count() {
	        return count;
	    }
	}
	```

* 森林的表示
* quick-union 算法的分析
	* find()方法访问数组次数为1加上给定触点所对应的节点的深度的两倍
	* union()方法和connected()方法访问数组的次数为两次find()操作（如果union()中给定的两个触点分别存在于不同的树中则还需要加1）
	* 最坏情况：union整个数组，时间复杂度为 \\(N^2\\) 

* 加权 quick-union 算法

	```java
	/**
	 * Created by tony on 7/18/17.
	 * Quick-Find
	 */
	public class WeightedQuickUnionUF {
	
	    private int[] id;
	    private int[] sz;
	    private int count;
	
	    public WeightedQuickUnionUF(int N) {
	        id = new int[N];
	        sz = new int[N];
	        for (int i = 0; i < N; i++) {
	            id[i] = i;
	            sz[i] = 1;
	        }
	        count = N;
	    }
	
	    public void union(int p, int q) {
	        int i = find(p);
	        int j = find(q);
	        if (i != j) {
	            if (sz[i] > sz[j]) {
	                id[j] = i;
	                sz[i] += sz[j];
	            } else {
	                id[i] = j;
	                sz[j] += sz[i];
	            }
	            count--;
	        }
	    }
	
	    public int find(int p) {
	        while (p != id[p])
	            p = id[p];
	        return p;
	    }
	
	    public boolean connected(int p, int q) {
	        return find(p) == find(q);
	    }
	
	    public int count() {
	        return count;
	    }
	}
	```

* 加权 quick-union 算法的分析
	* 最坏情况：find()、union()和connected()的成本的增长数量级为 \\(logN\\) 
* 最优算法 - 路径压缩的加权 quick-union算法

	```java
	/**
	 * Created by tony on 7/18/17.
	 * Quick-Find
	 */
	public class PathCompressedWeightedQuickUnionUF {
	
	    private int[] id;
	    private int[] sz;
	    private int count;
	
	    public PatchCompressedWeightedQuickUnionUF(int N) {
	        id = new int[N];
	        sz = new int[N];
	        for (int i = 0; i < N; i++) {
	            id[i] = i;
	            sz[i] = 1;
	        }
	        count = N;
	    }
	
	    public void union(int p, int q) {
	        int i = find(p);
	        int j = find(q);
	        if (i != j) {
	            if (sz[i] > sz[j]) {
	                id[j] = i;
	                sz[i] += sz[j];
	            } else {
	                id[i] = j;
	                sz[j] += sz[i];
	            }
	            count--;
	        }
	    }
	
	    public int find(int p) {
	    	 int tmp = p;
	        while (p != id[p])
	            p = id[p];
	        while (tmp != id[tmp]) {
	        	  tmp = id[tmp];
	        	  id[tmp] = p;
	        }
	        return p;
	    }
	
	    public boolean connected(int p, int q) {
	        return find(p) == find(q);
	    }
	
	    public int count() {
	        return count;
	    }
	}
	```

* 均摊成本的图像

### 1.5.3 展望
* 研究基础问题的基本步骤
	* 完整而详细地定义问题，找出解决问题所必需的基本抽象操作并定义一份API
	* 简洁地实现一种初级算法，给出一个精心组织的开发用例并使用实际数据作为输入
	* 当实现所能解决的问题的最大规模达不到期望时决定改进还是放弃
	* 逐步改进实现，通过经验性分析或（和）数学分析验证改进后的效果
	* 用更高层次的抽象表示数据结构或算法来设计更高级的改进版本
	* 如果可能尽量为最坏情况下的性能提供保证，但在处理普通数据时也要有良好的性能
	* 在适当的时候将更细致的深入研究留给有经验的研究者并继续解决下一个问题 

# 第二章 排序

## 2.1 初级排序算法
* 排序算法模版

	```java
	import edu.princeton.cs.algs4.StdIn;
	import edu.princeton.cs.algs4.StdOut;
	
	public class Example {
	    public static void sort(Comparable[] a) {
	    }
	
	    private static boolean less(Comparable v, Comparable w) {
	        return v.compareTo(w) < 0;
	    }
	
	    private static void exch(Comparable[] a, int i, int j) {
	        Comparable t = a[i];
	        a[i] = a[j];
	        a[j] = t;
	    }
	
	    private static void show(Comparable[] a) {
	        for (int i = 0; i < a.length; i++)
	            StdOut.print(a[i] + " ");
	        StdOut.println();
	    }
	
	    public static boolean isSorted(Comparable[] a) {
	        for (int i = 1; i < a.length; i++)
	            if (less(a[i], a[i - 1])) return false;
	        return true;
	    }
	
	    public static void main(String[] args) {
	        String[] a = StdIn.readAllStrings();
	        sort(a);
	        assert isSorted(a);
	        show(a);
	    }
	}

	```

### 2.1.1 游戏规则
* 验证
* 运行时间
* 额外的内存使用
* 数据类型

### 2.1.2 选择排序
* 实现

	```java
	public class Selection {
	    public static void sort(Comparable[] a) {
	        for (int i = 0; i < a.length; i++) {
	            int min = i;
	            for (int j = i + 1; j < a.length; j++)
	                if (less(a[j], a[min])) min = j;
	            exch(a, min, i);
	        }
	    }
	
	    private static boolean less(Comparable v, Comparable w) {
	        return v.compareTo(w) < 0;
	    }
	
	    private static void exch(Comparable[] a, int i, int j) {
	        Comparable t = a[i];
	        a[i] = a[j];
	        a[j] = t;
	    }
	
	    public static boolean isSorted(Comparable[] a) {
	        for (int i = 1; i < a.length; i++)
	            if (less(a[i], a[i - 1])) return false;
	        return true;
	    }
	}

	```
* 时间复杂度
	* 比较次数: \\(N^2/2\\) ; 交换次数: \\(N\\)

### 2.1.3 插入排序
### 2.1.4 排序算法的可视化
### 2.1.5 比较两种排序算法
### 2.1.6 希尔排序

