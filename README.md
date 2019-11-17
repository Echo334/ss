# ss
计181 申森 2018310747
一、实验目的
   掌握字符串String及其方法的使用
   掌握异常处理结构
二、实验要求
  内容：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。
  功能：1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
        2.允许提供输入参数，统计古诗中某个字或词出现的次数
        3.考虑操作中可能出现的异常，在程序中设计异常处理程序
  输入：
  汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行<未完，待续>
  输出：
    汉皇重色思倾国，御宇多年求不得。
    杨家有女初长成，养在深闺人未识。
    天生丽质难自弃，一朝选在君王侧。
    回眸一笑百媚生，六宫粉黛无颜色。
    春寒赐浴华清池，温泉水滑洗凝脂。
    侍儿扶起娇无力，始是新承恩泽时。
    云鬓花颜金步摇，芙蓉帐暖度春宵。
    春宵苦短日高起，从此君王不早朝。
…………
三、实验过程
   首先，需要建立一个package命名为“实验四”。定义一个字符串，并输入要求的《长恨歌》。调用string buffer，定义一个新的字符串，可进行更改。对字符串中的每一个对象进行循环判断，每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”使用StringTokenizer找出所求文字出现的次数。然后新建test，对输入字符串进行try exception操作进行试错。
四、实验流程图
  ![image text](https://github.com/Echo334/ss/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
五、核心代码及注释
   public Changhenge(String j)
	{
		String c = j;
		for(int i = last - 7; i > 0; i-=7) 
		{
			if(i%14==0)
			{
				s.insert(i,'。');
				s.insert(i+1,'\n');
			}
			else s.insert(i,'，');
			}
		
		
		StringTokenizer a = new StringTokenizer(d,c);
		int number = a.countTokens();
		while(a.hasMoreTokens()) 
		{
			String k = a.nextToken();
      
		}
		if(c.equals("行"))
		{
			number = number;
		}
		else if(c.equals("汉")) 
		{
			number = number;
		}
		else 
		{
			number=number -1;
		}
		 g = number;
	}//加入标点符号
  public static void main(String args[]) throws NewException
	{
		Changhenge changhenge;

		String write;
		write = "不";
		try {
		changhenge = new Changhenge(write);
		if(write == "") 
		{
			throw new NewException("不能输入空字符");
		}
		else 
		
			System.out.print(changhenge);
		}
		catch (NewException e) 
		{
			e.printStackTrace();
		}

		finally 
		{
			System.out.print("程序运行结束");
		}

	}//试错，判断输入的字符串的类型
public class NewException extends Exception{
	public NewException(){
		
 	}
	public NewException(String str){ 
            super(str);
 	}
}//对错误类型进行定义
六、运行结果
   ![image text](https://github.com/Echo334/ss/blob/master/%E7%B3%BB%E7%BB%9F%E6%8A%A5%E9%94%99.png)
   ![image text](https://github.com/Echo334/ss/blob/master/%E8%BF%90%E8%A1%8C%E7%BB%93%E6%9E%9C.png)
七、心得体会
   此次实验，对于课上所讲述的try expection进行了练习。同时，运用了基本的循环操作，又加上string buffer，对字符串进行增添，让我对Java的学习更深了一点。
