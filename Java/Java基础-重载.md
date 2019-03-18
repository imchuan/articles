
在C语言中，要求为每个函数提供一个独一无二的名称，所以不能用print()函数打印一个整数，又用名为print()的函数打印一个字符串，可以理解为这个print的动作，指定了不同的词汇，略显繁琐。所以在java中，有了非常便捷的**方法重载**，使描述一种行为变得简洁、清晰。
# 定义
**方法重载也就是，几个方法的方法名称相同，形式参数不同**。
**需要注意的是：**
**1) 每个方法都有独一无二的参数类型列表**

	void print(int input){
	
	}
	void print(String input){
	
	}

**2) 方法名称相同、参数类型一致，而返回值不同的方法，不叫重载**

	void process(int input){
	
	}
	String process(int input){
		return "";
	}
	// 这两个方法不叫重载，会编译报错

**3) 通过参数顺序，也可以区分两个方法，但是不建议这么做，因为会引起代码混淆**

    public void f1(int x, String y){
    
    }
    public void f1(String y, int x){
    
    }

# 构造函数重载

	class Dog{
		void Dog(){
	    	// 默认无参构造函数
	    }
	    void Dog(String name){
	
	    }
	}
	
	new Dog();
	new Dog("阿黄");







