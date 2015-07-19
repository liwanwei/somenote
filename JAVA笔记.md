java 笔记

## length函数 ##
1. java 中的length属性是针对数组说的,比如说你声明了一个数组,想知道这个数组的长度则用到了length这个属性.
2. java 中的length()方法是针对字符串String说的,如果想看这个字符串的长度则用到length()这个方法.
3. java中的size()方法是针对泛型集合说的,如果想看这个泛型有多少个元素,就调用此方法来查看!

这个例子来演示这两个方法和一个属性的用法

	 public static void main(String[] args) {
	        String []list={"ma","cao","yuan"};
	        String a="macaoyuan";
	        System.out.println(list.length);
	        System.out.println(a.length());
		
	        List<Object> array=new ArrayList();
	        array.add(a);
	        System.out.println(array.size());
	    }

输出的值为:

	3	
	9	
	1

## 数据类型转换 ##

1. 简单数据类型之间的转换  
	1. 自动类型转换  
		低级变量可以直接向高级变量转换  
		**(byte, short, char)--int--long--float--double;**

		    byte b; int i=b; long l=b; float f=b; double d=b;

		**NB.**  byte, short, char 是相同级别的，不能相互自动转换，但是可以通过强制类型转换。
		
		    short i = 99; cahr c =(char)i; System.out.println("output: "+c);
	2. 强制类型转换
		将高级变量转换为低级变量，可使用强制类型转换  
		    
		    int i = 99; byte b = (byte)i; char c = (char)i;
		NB. 这种转换可能会导致溢出或精度下降。
	3. 包装类过度类型转换
		JAVA 共有6个包装类Boolean、 Character、Integer、Long、Float和Double。

		将Float转换为Double型时：
		
		    float f1 = 100.00f;
			Float F1 = new float(f1);
			Double d1 = F1.doubleValue();

	4. 将字符型直接作为数值型转换为其他数据类型
		getNumericValue(Char ch)

P41 面试例题3 解析：  
1. short s=s+1会出现编译错误。s+1的时候，结果会被“升格”为int类型。把int赋给short当然编译错误。  
2. s+=1 对于“+=”操作，系统会自动执行类型转换操作，等价于s=(short)s+1。

## 三目运算符的类型转换问题 ##

	public class Test{
		public static void main(String[] args){
			int a = 5;
			System.out.println("value is "+((a < 5) ? 10.9 : 9));
		}		
	}
输出结果为9.0
注意到(a < 5) ? 10.9 : 9)后面有一个10.9,，而后跟了一个9，这是java会根据运算符的精度类型进行自动类型转换。由于前面有一个10.9，因此后面的9也会自动变成9.0。


## &&与&的却别，||与|的区别 ##

 `&&`与`&`二者都是布尔逻辑与，只是`&&`与`||`是短路的，而`&`与`|`是非短路的。  
就是一旦`&&`前面的是false，`&&`后面的内容便不会执行，而`&`后面的任然会执行；而一旦`||`前面是true，`||`后面的便不会执行，而`|`后面的仍然会执行。

## 移位操作符 ##
？？P47 面试例题6

## finally ##
try{}里有一个return语句，那么紧跟在这个try后的finally{}里地code在什么时候被执行？  
> 函数return后就会销毁，因此在return前执行finally。

7/17/2015 4:45:10 PM 

## 传递和引用 ##
Java中是传值还是传引用？  

对于基本类型变量，Java是传值的副本；对于一切对象型变量，Java都是传引用的副本。
> - 不管Java参数的类型是什么，一律传递参数的副本。  
> - 基本的类型变量有:int、long、double、float、byte、boolean、char。  
> - 传引用副本的实质是复制指向地址的指针，只不过Java不想C++中有显著的\*和&符号。
> - String 类型也是对象型变量。




代码输入的结果是什么？为什么？

	package PassingAndCall;
	
	class Value { 
		public int i = 15; 
	} 
	public class P64_2 {
		public static void main(String[] args) {
			P64_2 t = new P64_2(); 
			t.first(); 
		}
		public void first() {
			int i = 5; 
			Value v = new Value();
			v.i = 25; 
			second(v, i);
			System.out.println("in first : v.i-->"+v.i);
		}
		public void second(Value v, int i) {
			i = 0;
			v.i = 20; //为什么是这个。。。
			Value val = new Value();
			v = val;
			System.out.println("in second : v.i-->"+v.i+", i = "+i);
		}
	}

结果为：

	in second : v.i-->15, i = 0
	in first : v.i-->20

**??为什么是20？？**

