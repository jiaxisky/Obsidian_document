### 38加号的使用

![image-20221011205257311](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011205257311.png)

###  39数据类型

#### ==01需要背==

![image-20221011210044969](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011210044969.png)

### 40整型使用



![image-20221011210511899](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011210511899.png)

![image-20221011210437554](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011210437554.png)

### 41整型细节

![image-20221011215349006](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011215349006.png)

![image-20221011212810133](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011212810133.png)



### 41浮点使用

![image-20221011212331974](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011212331974.png)

注释：Ctrl+/

### Java API 文档  

![image-20221011222057215](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011222057215.png)





##### 码工具-代码编辑工具箱

https://www.matools.com/

![image-20221011231856848](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221011231856848.png)

#### 在线编程网站

https://c.runoob.com/compile/10/

### 53自动类型换砖细节2

byte 、short、char三者参与运算时首先转换成==int型==

==boolean==不参与类型的自动转换

自动提升原则：表达式结果的类型自动提升为操作数中的最大类型。

### 54强制类型转换

```java
public class hello {
    public static void main(String args[]){
        int n1 = (int)1.9;
        System.out.println("n1="+n1);//造成数据精度损失
        int n2 = 2000;
        byte b1 = (byte)n2;
        System.out.println("b1="+b1);//造成数据溢出
}}

```

### 58 String和基本类型转换

语法：将基本数据类型+" "即可；

```java
public class hello {
	 public static void main(String args[]){
            int n1 = 100;
            Sting = n1 + "";//转成字符串
}}
```

将 String 类型转成 基本数据类型时， 要确保String类型能够转成有效的数据， 比如 我们可以把 "123" , 转成一个整数， 但是不能把 "hello" 转成一个整数  。

### 60作业

![image-20221012225601271](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221012225601271.png)

```java
public class hello {
    public static void main(String args[]){
        char c1 = '\n';
        char c2 = '\t';
        char c3 = '\r';
        char c4 = '\\';
        char c5 = '1';
        char c6 = '2';
        char c7 = '3';
        System.out.println(c1) ;
        System.out.println(c2) ;
        System.out.println(c3) ;
        System.out.println(c4) ;
        System.out.println(c5) ;
        System.out.println(c6) ;
        System.out.println(c7) ;
}}
```



![image-20221012225532913](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221012225532913.png)

```java

public class hello {
    public static void main(String args[]){
        String book1 = "天龙八部";
        String book2 = "笑傲江湖";
        System.out.println(book1+book2) ;
       //性别应该是使用char保存
        char c1 = '男';
        char c2 = '女';
        System.out.println(c1+c2) ;//得到 男 字符码值 + 女 字符码值
       //保存两本书的价格
        double price1 = 123.56;
        double price2 = 100.11;
        System.out.println(price1+price2) ;//就是123.56+100.11
}}
//输出：
//天龙八部笑傲江湖
//52906
//223.67000000000002
```

### 63算术运算符使用

#### 取模的本质

在 % 的本质 看一个公式!!!! ==a % b = a - a / b * b==

#### 复合赋值运算符会进行类型转换 

```java
//复合赋值运算符会进行类型转换  
byte b = 3;
b += 2; // 等价 b = (byte)(b + 2);
b++; // b = (byte)(b+1);  
```

### 三元运算符

#### 1.求三个数的最大值

```java
public class HelloWorld {
    public static void main(String []args) {
      int n1 = 55;
		int n2 = 33;;
		int n3 = 123;
		int max1 = n1> n2 ? n1:n2;
		int max2 = max1 > n3 ? max1:n3;
		System.out.println(max2);
		
    }
}
```



### 键盘输入

```Java
import java.util.Scanner;
public class HelloWorld {
    public static void main(String []args) {
		Scancer myScancer = new Scancer(System.in);
		System.out.println("输入用户名字");
		String name = myScancer.next();
		System.out.println("输入用户年龄");
		int age = myScancer.nextInt();
		System.out.println("输入用户薪水");
		double sal = myScancer.nextDouble();
		System.out.println("名字="+name+"年龄"+age+"薪水"+sal);
    }
}
```

###  原码、 反码、 补码(重点 难点)  

![image-20221014203852040](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221014203852040.png)

  

要把==字符串转成int型==应该用一个包装类，如下：

```java
int num1 = Integer.parseInt("18")
```

byte b = 19;//19在byte范围内，是正确的。

### 101.作业：写出将String转换成double类型的语句，以及将char转换成String的语句

```Java
String str = "18.8";//注意，字符串要可以被转换成double
double d1 = Double.parseDouble(str);

char c1 = '韩';
String str2 = c1 + "";
```

### 109.作业:判断闰年（通过输入的方式）

```java
import java.util.Scanner;
public class hello {
    public static void main(String args[]){
       System.out.println("请输入年份：");
        Scanner  year = new Scanner(System.in);
        int years = year.nextInt();//把year保存到一个变量 int years
        if(years%4==0&&years%100!=0||years%400==0){
            System.out.println(years+"年是闰年" );
        }else {
            System.out.println(years+"年不是闰年");
        }
}}
```

### 111.作业:判断芝麻信用分（通过输入的方式）

```java
import java.util.Scanner;
public class hello {
    public static void main(String args[]){
       System.out.println("请输入芝麻信用分（1-100）：");
       Scanner  score = new Scanner(System.in);
       int scores = score.nextInt();
       //先对输入的信用分进行一个范围的有效判断1-100，否则提示输入错误
       if(scores>=1&&scores<=100) {
           if (scores == 100) {
               System.out.println("信用极好");
           } else if (scores >= 80 && scores <= 99) {
               System.out.println("信用优秀");
           } else if (scores >= 60 && scores < 80) {
               System.out.println("信用一般");
           } else {
               System.out.println("信用不及格");
           }
       }else {
           System.out.println("信用分需要在1-100之间，请重新输入：");
       }
}}
```

```java
char name = myScancer1.next().charAt(0);//输入字符
```

### 114.嵌套分支课后练习

![image-20221015124534860](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221015124534860.png)

```java
import java.util.Scanner;
public class hello {
    public static void main(String args[]){
       Scanner  score = new Scanner(System.in);
        Scanner  age = new Scanner(System.in);
        System.out.println("请输入月份（1-12）：");
       int month = score.nextInt();
        System.out.println("请输入年龄：");
        int ages = age.nextInt();
       //先对输入的月份进行一个范围的有效判断1-12，否则提示输入错误
       if(month>=1&&month<=12) {
           if (month>=4&&month<= 10) {
               if(ages>=18&&ages<=60){
                   System.out.println("票价为60元");
               }else if(ages<18){
                   System.out.println("半价");
               }else {
                   System.out.println("票价为1/3");
               }
           } else if (ages>=18) {
               System.out.println("票价为40元");
           } else {
               System.out.println("票价为20元");
           }
       }else {
           System.out.println("月份需要在1-12之间，请重新输入：");
       }
}}
```

### 120.switch-作业：

#### 根据用于指定月份， 打印该月份所属的季节。 3,4,5 春季 6,7,8 夏季 9,10,11 秋季 12, 1, 2 冬季 [课堂练习, 提示 使用穿透 ]  

```java
import java.util.Scanner;
public class hello {
    public static void main(String args[]){
       Scanner  myScanner = new Scanner(System.in);
        System.out.println("请输入一个月份（1-12）：");
        int months = myScanner.nextInt();
       switch (months){
           case 3,4,5:
           System.out.println("春季");
           break;
           case 6,7,8:
           System.out.println("夏季");
           break;
           case 12,1,2:
           System.out.println("夏季");
           break;
           default:
               System.out.println("输入错误");
       }
}}

```



### 135.多重循环练习

##### 1) 统计 3 个班成绩情况， 每个班有 5 名同学， 求出各个班的平均分和所有班级的平均分[学生的成绩从键盘输入]。

##### 2) 统计三个班及格人数， 每个班有 5 名同学。  

```Java
import java.util.Scanner;
public class hello {
    public static void main(String args[]) {
        Scanner myScancer = new Scanner(System.in);
        double totalScore = 0;
        int passNum = 0;
        for (int i = 1; i <= 3; i++) {
            double sum = 0;
            for (int j = 1; j <= 5; j++) {
                System.out.println("请输入第" + i + "个班的第" + j + "个学生的成绩");
                double score = myScancer.nextDouble();
                if (score>=60){
                    passNum++;
                }
                sum += score;
                System.out.println("成绩为" + score);
            }
            System.out.println("sum=" + sum + "平均分=" + (sum / 5));
            totalScore += sum;
        }
        System.out.println("三个班总分=" + totalScore + "平均分=" + totalScore / 15);
        System.out.println("及格人数为" + passNum);
    }
}
```

### 143实现登录验证， 有 3 次机会， 如果用户名为"丁真" ,密码"666"提示登录成功， 否则提示还有几次机会， 请使用 for+break完成  

```Java
import java.util.Scanner;
public class hello {
    public static void main(String args[]) {
        Scanner myScancer = new Scanner(System.in);
        String name ="";
        String passwd ="";
        int chance=3;//登陆一次，就减少一次
        for (int i =1;i<=3;i++){//3次登录机会
            System.out.println("请输入你的姓名：");
            name = myScancer.next();//输入名字
            System.out.println("请输入密码：");
            passwd = myScancer.next();
            //比较输入的名字有和密码是否正确
            //补充说明：字符串的内容 比较 使用的方法  equal
            if ("丁真".equals(name)&&"666".equals(passwd))
            {
                System.out.println("登录成功");
                break;
            }
            chance--;
            System.out.println("您还有"+chance+"次登录机会");
        }
    }
}
```

### 146跳转控制语句-return  

return 使用在方法， 表示跳出所在的方法  注意：如果 return 写在 main 方法， 退出程序 

### 149输出1-100之间的不能被5整除的数，每5个一行

```Java
public class hello {
    public static void main(String args[]) {
        int a =1;
        int i = 0;
        for (;a<=100;a++){
            if (a%5!=0){
                i++;
                System.out.print(a+"\t");
                if (i%5==0){
                    System.out.println();
                }
            }
        }
    }
}
```

### 151.输出小写的a-z,及大写的Z-A

```java
public class hello {
    public static void main(String args[]) {
        //输出小写的a-z,及大写的Z-A
        int a =1;
        int i = 0;
        for (char c1 = 'a';c1<='z';c1++){
                System.out.print(c1+"");
                }
        System.out.println("============");
        for (char c2 = 'Z';c2>='A';c2--){
            System.out.print(c2+"");
        }
            }
        }
```

### 153.求1+（1+2）+（1+2+3）+...+（1+2+3+...+100）的结果

```java
public class hello {
    public static void main(String args[]) {
        //求1+（1+2）+（1+2+3）+...+（1+2+3+...+100）的结果
        //1.一共有100项相加
        //2.每一项的数字在逐渐增加
        //3.i可以表示第几项，同时也是当前项的最后一个数
        //4.使用sum进行累加
        int sum=0;
        for (int i = 1;i<=100;i++){
            for (int j = 1;j<=i;j++){//内层对1-i进行循环
                sum+=j;
            }
        }
        System.out.print("sum="+sum);
    }
}
```

### 156.可以通过   数组名.length    得到数组的长度

### 157数组的使用

```java
import java.util.Scanner;
public class hello {
    public static void main(String args[]) {
        Scanner myScancer = new Scanner(System.in);
        double scores[]=new double[5];
         for (int i = 0 ; i<scores.length;i++){
             System.out.println("请输入第"+(i+1)+"个元素的值");
             scores[i] = myScancer.nextDouble();
          }
         for (int i=0;i<scores.length;i++){
             System.out.println("第"+(i+1)+"个元素的值=" + scores[i]);
         }
    }
}
```

### 162数组练习

#### 162.1创建一个 char 类型的 26 个元素的数组， 分别 放置'A'-'Z'。 使用 for 循环访问所有元素并打印出来。 提示： char 类型数据运算 'A'+2 -> 'C'   

```java
//import java.util.Scanner;
public class hello {
    public static void main(String args[]) {
        char chars[] =new char[26];
        for (int i = 0;i < chars.length;i++){
            chars[i] =(char)('A'+i);//'A'+i是int;需要强制转换
        }
        System.out.println("=====chars数组=====");
        for (int i=0;i<chars.length;i++){
            System.out.print(chars[i]+" ");
        }
    }
}
```

#### 162.2请求出一个数组 int[]的最大值 {4,-1,9, 10,23}， 并得到对应的下标。  

```java
public class hello {
    public static void main(String args[]) {
        //请求出一个数组 int[]的最大值 {4,-1,9, 10,23}， 并得到对应的下标
        //思路分析
        //1. 定义一个 int 数组 int[] arr = {4,-1,9, 10,23};
        //2. 假定 max = arr[0] 是最大值 , maxIndex=0;
        //3. 从下标 1 开始遍历 arr， 如果 max < 当前元素， 说明 max 不是真正的
        // 最大值, 我们就 max=当前元素; maxIndex=当前元素下标
        //4. 当我们遍历这个数组 arr 后 , max 就是真正的最大值， maxIndex 最大值
        // 对应的下标
        int[] arr = {4,-1,9,10,23};
        int max = arr[0];//假定第一个元素就是最大值
        int maxIndex = 0; //
        for(int i = 1; i < arr.length; i++) {//从下标 1 开始遍历 arr
            if(max < arr[i]) {//如果 max < 当前元素
                max = arr[i]; //把 max 设置成 当前元素
                maxIndex = i;
            }
        }
        //当我们遍历这个数组 arr 后 , max 就是真正的最大值， maxIndex 最大值下标
        System.out.println("max=" + max + " maxIndex=" + maxIndex);
    }
}
```

### 167.数组翻转

```java
public class hello {
    public static void main(String args[]) {
             int arr[] = {1,2,3,4,5};
              int temp = 0;
              int len = arr.length;//计算数组的长度
              for (int i =0;i<len/2;i++){
                  temp = arr[len-1-i];
                  arr[len-1-i]=arr[i];
                  arr[i]=temp;
              }
              for (int i =0; i < arr.length;i++)
              System.out.print(arr[i]+"\t");
            }
}
```

### 180.二维数组练习

#### 遍历该二维数组，并得到和

```java
public class hello {
    public static void main(String args[]) {
        /*int arr[][]= {{4,6},{1,4,5,7},{-2}};遍历该二维数组，并得到和
        思路
        1.遍历二维数组，并将各个值累积到int sum
        */
        int arr[][] =  {{4,6},{1,4,5,7},{-2}};
        int sum= 0;
        for (int i =0;i< arr.length;i++){
            //遍历每一个一维数组
          for (int j = 0;j<arr[i].length;j++){
              sum+=arr[i][j];
          }
        }
        System.out.print("sum="+sum);
    }
}
```

### 212只要调用一个方法就会产生一个新栈

### 223走迷宫算法

```java
public class hello {
    public static void main(String args[]) {
        //思路
        //1. 先创建迷宫， 用二维数组表示 int[][] map = new int[8][7];
        //2. 先规定 map 数组的元素值: 0 表示可以走 1 表示障碍物
        int[][] map = new int[8][7];
        //3. 将最上面的一行和最下面的一行， 全部设置为 1
        for(int i = 0; i < 7; i++) {
            map[0][i] = 1;
            map[7][i] = 1;
        }
        //4.将最右面的一列和最左面的一列， 全部设置为 1
        for(int i = 0; i < 8; i++) {
            map[i][0] = 1;
            map[i][6] = 1;
        }
        map[3][1] = 1;
        map[3][2] = 1;
        map[2][2] = 1; //测试回溯

        //输出当前的地图
        System.out.println("=====当前地图情况======");
        for(int i = 0; i < map.length; i++) {
                for(int j = 0; j < map[i].length; j++) {
                    System.out.print(map[i][j] + " ");//输出一行
                }
                System.out.println();
        }
        //使用 findWay 给老鼠找路
        T t1 = new T();
        //下右上左
        t1.findWay(map, 1, 1);
        System.out.println("\n====找路的情况如下=====");
        for(int i=0;i < map.length;i++) {
             for(int j = 0; j < map[i].length; j++) {
                 System.out.print(map[i][j] + " ");//输出一行
            }
             System.out.println();
        }
}
}
class T {
    //使用递归回溯的思想来解决老鼠出迷宫
    //老韩解读
    //1. findWay 方法就是专门来找出迷宫的路径
    //2. 如果找到， 就返回 true ,否则返回 false
    //3. map 就是二维数组， 即表示迷宫
    //4. i,j 就是老鼠的位置， 初始化的位置为(1,1)
    //5. 因为我们是递归的找路， 所以我先规定 map 数组的各个值的含义
    // 0 表示可以走 1 表示障碍物 2 表示可以走 3 表示走过， 但是走不通是死路
    //6. 当 map[6][5] =2 就说明找到通路,就可以结束， 否则就继续找.
    //7. 先确定老鼠找路策略 下->右->上->左
    public boolean findWay(int[][] map, int i, int j) {
        if (map[6][5] == 2) {//说明已经找到
            return true;
        } else {
            if (map[i][j] == 0) {//当前这个位置 0,说明表示可以走
                //我们假定可以走通
                map[i][j] = 2;
                //使用找路策略， 来确定该位置是否真的可以走通
                //下->右->上->左
                if (findWay(map, i + 1, j)) {//先走下
                    return true;
                } else if (findWay(map, i, j + 1)) {//右
                    return true;
                } else if (findWay(map, i - 1, j)) {//上
                    return true;
                } else if (findWay(map, i, j - 1)) {//左
                    return true;
                } else {
                    map[i][j] = 3;
                    return false;
                }
            } else { //map[i][j] = 1 , 2, 3
                return false;
            }
        }
    }
}
```

### 236可变参数练习

```java
public class hello {
    public static void main(String args[]) {
        HspMethod m = new HspMethod();
        System.out.println(m.showScore("li lei",8,9,10));
    }
}
class HspMethod{
    public String showScore(String name,double...scores){
        double totalScore = 0;
        for (int i=0;i<scores.length;i++){
            totalScore+=scores[i];
        }
        return name + "有"+scores.length+"门课的成绩总分为="+totalScore;
    }
}
```



### 276包

1.包的命名规则：只能包含数字、字母、下划线、小圆点、但是不能用数字开头，不能是关键字及保留字。

demo.class.exec1//错误class是关键字

demo.12a//错误12a是数字开头的

2.命名规范

一般是小写字母+小圆点，一般是com.公司名.项目名.业务模块名

比如：com.hspedu.oa.model;

com.sina.crm.user//用户模块

com.sina.crm.order//订单模块

### 281封装

#### 封装的好处：

1、隐藏实现细节 方法（连接数据库）2、可对数据进行验证，保证安全合理。

#### 封装实现步骤(三步)：

1）将属性进行私有化private；

2）提供一个公共的（public）set方法，用于对属性判断并赋值

```java
public void setXxx(类型 参数名){//Xxx表示某个属性
//加入数据验证的业务逻辑
属性 = 参数名；
}
```

3）提供一个公共的（public）get方法，用于获取属性的值

```java
public 数据类型 getXxx(){//权限判断
return xx;
}
```

### 283封装快速入门



```java
package cha;

public class pag {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("jacktomcat你好吗");
        person.setAge(150);
        person.setSalary(10000);
        System.out.println(person.info());
    }
}

class Person {
    public String name;
    private int age;
    private double salary;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        //加入对数据的校验，相当于增加了业务逻辑
        if (name.length() >= 2 && name.length() <= 6) {
            this.name = name;
        } else {
            System.out.println("名字的长度不对需要（2-6）个字符，默认名字");
            this.name = "无名人";

        }
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age >= 1 && age <= 120)
            this.age = age;
        else {
            System.out.println("你设置的年龄不对，年龄需要在1-120，给默认年龄18");
            this.age = 18;
        }
    }

    public double getSalary() {
        //可以在这里增加当前对象的权限判断
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    //写一个方法，返回属性信息
    public String info() {
        return "信息为name=" + name + " age = " + age + " salary=" + salary;
    }

}

```

#### 2.构造器和setXxx结合

```java
package cha;

public class pag {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("jacktomcat你好吗");
        person.setAge(150);
        person.setSalary(10000);
        System.out.println(person.info());
        System.out.println("====smith的信息=====");
        //如果我们自己使用构造器指定属性
        Person smith = new Person("smith", 25, 100000);
        System.out.println(smith.info());
    }
}

class Person {
    public String name;
    private int age;
    private double salary;

    public Person() {//无参构造器
    }

    public Person(String name, int age, double salary) {
        //有三个属性的构造器
//        this.name = name;
//        this.age = age;
//        this.salary = salary;
        //我们可以将set方法写在构造器中，这样仍然可以验证
        setName(name);//和this.setName(name)等价
        setSalary(salary);
        setAge(age);
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        //加入对数据的校验，相当于增加了业务逻辑
        if (name.length() >= 2 && name.length() <= 6) {
            this.name = name;
        } else {
            System.out.println("名字的长度不对需要（2-6）个字符，默认名字");
            this.name = "无名人";

        }
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age >= 1 && age <= 120)
            this.age = age;
        else {
            System.out.println("你设置的年龄不对，年龄需要在1-120，给默认年龄18");
            this.age = 18;
        }
    }

    public double getSalary() {
        //可以在这里增加当前对象的权限判断
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    //写一个方法，返回属性信息
    public String info() {
        return "信息为name=" + name + " age = " + age + " salary=" + salary;
    }

}

```

### 300.super与this的区别

![image-20221031223225959](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221031223225959.png)

### 314动态绑定机制

java的动态绑定机制

1.当调用==对象方法==的时候，该方法会和==该对象的内存地址/运行类型==绑定

2.当调用==对象属性==时，没有动态绑定机制，哪里声明，哪里使用

### 461 包装类练习题

![image-20221120140643789](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221120140643789.png)

 

### 串行化

串行化是指该对象既可以网络传输，也可以保存在文件中

### 488 Date应用实例

```java
package date_;

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

public class Date01 {
    public static void main(String[] args) throws ParseException {
        Date d1 = new Date();
        Date d2 = new Date(923465);
        System.out.println("d2 = "+d2);
        System.out.println("当前时间"+d1);
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日 hh:mm:ss:SS E");
        String format = sdf.format(d1);
        System.out.println("当前日期= "+format);
        String s = "2022年11月24日 02:43:14:494 周四";
        Date parse = sdf.parse(s);
        System.out.println("parse = "+parse);
    }
}
//输出：
//d2 = Thu Jan 01 08:15:23 CST 1970
//当前时间Thu Nov 24 14:45:48 CST 2022
//当前日期= 2022年11月24日 02:45:48:997 周四
//parse = Thu Nov 24 02:43:14 CST 2022


```

### 0491 第三代日期方法

```java
import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.LocalTime;

public class LocalDate_ {
    public static void main(String[] args) {
        LocalDateTime ldt = LocalDateTime.now();
        System.out.println(ldt);
        System.out.println("年="+ldt.getYear());
        System.out.println("月="+ldt.getMonth());
        System.out.println("月="+ldt.getMonthValue());
        System.out.println("日 = "+ldt.getDayOfMonth());

        LocalDate now = LocalDate.now();//可以获取到年月日
        System.out.println(now.getYear());

        LocalTime now2 = LocalTime.now();//获取时分秒
        System.out.println(now2);
    }
}
/*输出：
2022-11-24T17:47:50.682874800
年=2022
月=NOVEMBER
月=11
日 = 24
2022
17:47:50.690854100*/

```

### 0493 String翻转

1.编程题

（1）将字符串中指定部分进行反转，比如将"abcde"反转为"aedcbf"

（2）编写public static String reverse (String str,int start,int end )搞定

```java
public class Homework01 {
    public static void main(String[] args) {
        String str = "abcdef";
        System.out.println("===交换前===");
        System.out.println(str);
        try {
            str = reverse(str,1,4);
        } catch (Exception e) {
            System.out.println(e.getMessage());;
            return;
        }
        System.out.println("===交换后===");
        System.out.println(str);
    }
    public static String reverse (String str,int start,int end ){
        /*对输入的参数做一个验证
        //重要的编程技巧！！！！
        //（1）写出正确的情况
          （2）然后取反即可
        */
        if (!(str!=null && start>=0 && end>start && end<str.length())){
            throw new RuntimeException("参数不正确");
        }

        char[] chars = str.toCharArray();
        char temp = ' ';
        for (int i = start,j=end;i<j;i++,j--){
            temp = chars[i];
            chars[i] = chars[j];
            chars[j] =  temp;
        }
        return new String(chars);
    }
}
/*
输出：
===交换前===
abcdef
===交换后===
aedcbf
*/
```

### 0494注册处理题

```java
package date_;

public class Homework02 {
    public static void main(String[] args) {
        String name = "abc";
        String pwd ="123456";
        String email = "jack@shouhu.com";
        try {
            userRegister(name,pwd,email);
            System.out.println("恭喜你，注册成功");
        } catch (Exception e) {
            System.out.println(e.getMessage());
        }
    }
    /*
    (1)先编写方法userRegister(String name, String pwd,String email){}
    (2)针对输入的内容进行校验，如果发现有问题就抛出异常，给出提示
    (3)单独写一个方法，判断密码是否全部是数字字符 boolean
     */
    public static void userRegister(String name, String pwd,String email){
          /*
          (1)用户名长度为2或3或4
          (2)密码的长度为6，要求全为数字 isDigital
          (3)邮箱中包含@和.并且@在.的前面
           */
        //再加入一些校验
        if (!(name!=null && pwd!=null&&email!=null)){
            throw new RuntimeException("参数不能为null");
        }

        int userLength = name.length();
        if (!(userLength>=2&&userLength<=4)){
            throw new RuntimeException("用户名长度为2或3或4");
        }
        if (!(pwd.length()==6 && isDigital(pwd))){
            throw new RuntimeException("密码的长度为6，要求全为数字");
        }
        //邮箱中包含@和.并且@在.的前面
        int i = email.indexOf('@');
        int j = email.indexOf('.');
        if (!( i > 0 && j>i )){
            throw new RuntimeException("邮箱中要包含@和.并且@在.的前面");
        }
    }
    public static  boolean isDigital(String str){
        char[] chars = str.toCharArray();
        for (int i = 0; i < chars.length; i++) {
            if (chars[i]<'0'||chars[i]>'9'){//0-9的ASCII
                return false;
            }
        }
        return true;
    }

}

```

### 0495 字符串统计

![image-20221125193602178](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221125193602178.png)

```java
package date_;

import java.util.Locale;

public class Homework03 {
    public static void main(String[] args) {
        String name = "han shun ping ";
        printName(name);

    }
    public static void printName(String str){
        if (str==null){
            System.out.println("str 不能为空");
            return;
        }
        String[] names = str.split(" ");
        if (names.length!=3){
            System.out.println("输入的字符串格式不对");
            return;
        }
        String format = String.format("%s,%s.%c", names[2], names[0], names[1].toUpperCase().charAt(0));
        System.out.println(format);
    }
}

```

#### 输入字符串，判断里面有多少个大写字母，多少个小写字母，多少个数字

```java
package date_;

public class Homework04 {
    public static void main(String[] args) {
        String str= "abcdh AEFF0eh 155";
        countStr(str);

    }
    /*
    *输入字符串，判断里面有多少个大写字母，多少个小写字母，多少个数字
    * 思路分析：
    * （1）遍历字符串，如果char在'0'-'9' 就是一个数字
    * （2）如果在'a'-'z'就是一个小写字母
    * （3）如果在'A'-'z'就是一个大写字母
    * （4）使用三个变量来记录统计结果
     */
    private static void countStr(String str){
        if (str==null){
            System.out.println("输入不能为空");
            return;
        }
        int strLen = str.length();
        int numCount =0;
        int lowerCount = 0;
        int upperCount = 0;
        int otherCount = 0;
        for (int i = 0; i < strLen; i++) {
            if (str.charAt(i)>='0'&&str.charAt(i)<='9'){
                numCount++;
            }else if (str.charAt(i)>='a'&&str.charAt(i)<='z'){
                lowerCount++;
            }else if (str.charAt(i)>='A'&&str.charAt(i)<='Z'){
                upperCount++;
            }else {
                otherCount++;
            }
        }
        System.out.println("数字有："+numCount);
        System.out.println("小写字母有："+lowerCount);
        System.out.println("大写字母有："+upperCount);
        System.out.println("其他字符有："+otherCount);
    }
}

```

### 0500 Collection方法

> 1. add:添加单个元素
> 2. remove:删除
> 3. contains:查找元素是否存在
> 4. size:获取元素的个数 
> 5.  isEmpty:判断是否为空
> 6.  clear:清空
> 7.  addAll:添加多个元素
> 8. containsAll:查找多个元素是否都存在
> 9.  removeAll:删除多个元素



```java
package com.hspedu.collection;

import java.util.ArrayList;

import java.util.List;

public class Collection_ {
    public static void main(String[] args) {
        List list = new ArrayList();//创建ArrayList对象，使用List对象接收
        //add:添加单个元素
        list.add("jack");
        list.add(10);//是对象了，不再是基本数据类型；本质为：list.add(new Integer(10)),下同
        list.add(true);
        System.out.println("list="+list);
        //remove:删除
       // list.remove(0);//删除第一个元素
        //list.remove("jack");//指定删除某个元素
        System.out.println("list = "+list);
        //contains:查找元素是否存在
        System.out.println(list.contains("jack"));
        //size:获取元素的个数
        System.out.println(list.size());
        //isEmpty:判断是否为空
        System.out.println(list.isEmpty());
        //clear:清空
        list.clear();
        //addAll:添加多个元素
       ArrayList list2 =  new ArrayList();
       list2.add("红楼梦");
       list2.add("三国演义");
       list.addAll(list2);
        System.out.println("list = "+list);
        //containsAll:查找多个元素是否都存在
        System.out.println(list.containsAll(list));
        //removeAll:删除多个元素
        list.add("聊斋");
        list.removeAll(list2);
        System.out.println("lst = "+list);

    }
}
/*输出：
list=[jack, 10, true]
list = [jack, 10, true]
true
3
false
list = [红楼梦, 三国演义]
true
lst = [聊斋]
*/

```

### 0501 迭代器遍历

```java
package com.hspedu.collection;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;

public class CollectionIterator {
    @SuppressWarnings({"all"})
    public static void main(String[] args) {
        Collection col = new ArrayList();
        col.add(new Book("三国演义","罗贯中",10.1));
        col.add(new Book("小李飞刀","古龙",5.1));
        col.add(new Book("红楼梦","曹雪芹",36.4));
        System.out.println("col="+col);
        //遍历集合
        //1.先得到col对应的迭代器
        Iterator iterator = col.iterator();
        //2.使用while循环遍历
        while (iterator.hasNext()){//判断是否还有数据
            //返回下一个元素，类型为Object
            Object obj = iterator.next();
            System.out.println("obj="+obj);
        }
        //3.当退出while循环后，这是iterator迭代器，指向最后的元素
        //iterator.next();//NoSuchElementException
        //4.如果希望再次遍历，需要重置迭代器
        iterator = col.iterator();
        System.out.println("===第二次遍历===");
        while (iterator.hasNext()){//判断是否还有数据
            //返回下一个元素，类型为Object
            Object obj = iterator.next();
            System.out.println("obj="+obj);
        }


    }
}
class Book{
    private String name;
    private String author;
    private double price;

    public Book(String name, String author, double price) {
        this.name = name;
        this.author = author;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getAuthor() {
        return author;
    }

    public void setAuthor(String author) {
        this.author = author;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    @Override
    public String toString() {
        return "Book{" +
                "name='" + name + '\'' +
                ", author='" + author + '\'' +
                ", price=" + price +
                '}';
    }
}
/*输出
col=[Book{name='三国演义', author='罗贯中', price=10.1}, Book{name='小李飞刀', author='古龙', price=5.1}, Book{name='红楼梦', author='曹雪芹', price=36.4}]
obj=Book{name='三国演义', author='罗贯中', price=10.1}
obj=Book{name='小李飞刀', author='古龙', price=5.1}
obj=Book{name='红楼梦', author='曹雪芹', price=36.4}
===第二次遍历===
obj=Book{name='三国演义', author='罗贯中', price=10.1}
obj=Book{name='小李飞刀', author='古龙', price=5.1}
obj=Book{name='红楼梦', author='曹雪芹', price=36.4}

 */
```

### 0502 集合增强

```java
package com.hspedu.collection;

import java.util.ArrayList;
import java.util.Collection;

public class CollectionFor {
    @SuppressWarnings({"all"})
    public static void main(String[] args) {
        Collection col = new ArrayList();
        col.add(new Book("三国演义","罗贯中",10.1));
        col.add(new Book("小李飞刀","古龙",5.1));
        col.add(new Book("红楼梦","曹雪芹",36.4));
        //1.使用增强for循环在Collection集合上
        //2.使用for，底层仍然是迭代器
        //3.增强for可以理解为简化版本的迭代器
        //4.快捷键I      
        for (Object book:col){
            System.out.println("book = "+book);
        }
        //增强for循环,不仅可以用在集合也可以用在数组上
        int[] num = {1,9,8,15};
        for (int i:num){
            System.out.print(" i="+i);
        }

    }

}
/*
book = Book{name='三国演义', author='罗贯中', price=10.1}
book = Book{name='小李飞刀', author='古龙', price=5.1}
book = Book{name='红楼梦', author='曹雪芹', price=36.4}
 i=1 i=9 i=8 i=15
 */
```

### 0505 List接口练习

<img src="https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221126154432141.png" alt="image-20221126154432141" style="zoom:100%;" />

```java
package com.hspedu.list_;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class ListExercise {
    public static void main(String[] args) {
        List list = new ArrayList();
        for (int i = 0; i < 12; i++) {
            list.add("hello"+i);
        }
        System.out.println("list="+list);
        list.add(1,"韩顺平教育");
        System.out.println("list="+list);
        System.out.println("第5个元素="+list.get(4));
        System.out.println("删除第6个元素="+list.remove(5));
        list.set(6,"三国演义");
        System.out.println("list ="+list);
        //使用迭代器遍历集合
        Iterator iterator = list.iterator();
        while (iterator.hasNext()) {
            Object obj =  iterator.next();
            System.out.println("obj="+obj);
            
        }
    }
}
/*list=[hello0, hello1, hello2, hello3, hello4, hello5, hello6, hello7, hello8, hello9, hello10, hello11]
list=[hello0, 韩顺平教育, hello1, hello2, hello3, hello4, hello5, hello6, hello7, hello8, hello9, hello10, hello11]
第5个元素=hello3
删除第6个元素=hello4
list =[hello0, 韩顺平教育, hello1, hello2, hello3, hello5, 三国演义, hello7, hello8, hello9, hello10, hello11]
obj=hello0
obj=韩顺平教育
obj=hello1
obj=hello2
obj=hello3
obj=hello5
obj=三国演义
obj=hello7
obj=hello8
obj=hello9
obj=hello10
obj=hello11
```



### 0506 三种遍历方式

#### 方式1.迭代器

#### 方式2.增强for

#### 方式3.普通for循环

```java
package com.hspedu.list_;

import java.util.*;

public class ListFor {
    @SuppressWarnings({"all"})
    public static void main(String[] args) {
        //三种方式都可以
//        List list = new ArrayList();
        List list = new LinkedList();
//        List list = new Vector();
        list.add("jack");
        list.add("tom");
        list.add("北京烤鸭");
        list.add("鱼香肉丝");
        //鱼香肉丝
        //方式1.迭代器
        Iterator iterator = list.iterator();
        while (iterator.hasNext()) {
            Object obj =  iterator.next();
            System.out.println(obj);            
        }
        System.out.println("===增强for===");
        //方式2.增强for
        for (Object o:list) {
            System.out.println("o="+o);
        }
        //方式3.普通for循环
        System.out.println("===普通for==");
        for (int i = 0; i < list.size(); i++) {
            System.out.println("对象="+list.get(i));

        }
    }
}

```

### 0507 List排序练习

![image-20221126170740340](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221126170740340.png)

```java
package com.hspedu.list_;

import java.awt.print.Book;
import java.util.ArrayList;
import java.util.List;

public class ListExercise02 {
    @SuppressWarnings({"all"})
    public static void main(String[] args) {
        List list = new ArrayList();
        list.add(new Book1("红楼梦","曹雪芹",100));
        list.add(new Book1("西游记","吴承恩",10));
        list.add(new Book1("水浒传","施耐庵",19));
        list.add(new Book1("三国","罗贯中",80));
       // list.add(new Book1("西游记","吴承恩",10));
        //遍历
        for (Object o:list){
            System.out.println(o);
        }
        //调用冒泡排序
        sort(list);
        System.out.println("===排序后===");
        for (Object o:list){
            System.out.println(o);
        }

    }
    //静态方法
    public static void sort(List list){
        int listSize = list.size();
        for (int i = 0; i < listSize-1; i++) {
            for (int j = 0; j < listSize-1-i; j++) {
                //取出对象Book1
                Book1 book1 =  (Book1)list.get(j);//向下转型
                Book1 book2 =  (Book1)list.get(j+1);
                if (book1.getPrice()>book2.getPrice()){//交换
                    list.set(j,book2);
                    list.set(j+1,book1);
                }
            }

        }
    }
}
class Book1{
    private String name;
    private String author;
    private double price;

    public Book1(String name, String author, double price) {
        this.name = name;
        this.author = author;
        this.price = price;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getAuthor() {
        return author;
    }

    public void setAuthor(String author) {
        this.author = author;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    @Override
    public String toString() {
        return "名称:" + name + "\t\t 价格："+price+ "\t\t作者："+ author;

    }
}
```

#### 0516 ArratList和LinkedList都是线程不安全的

---

### 0543 HMap源码解读

1. 执行构造器 new HashMap()

   初始化加载因子loadfactor = 0.75

   hashMap$Node[ ] table =null

2. 执行put,调用hash方法，计算key的hash值（(h = key.hashCode()) ^ (h >>> 16)）

   ```Java
   public V put(K key, V value) {
           return putVal(hash(key), key, value, false, true);
       }
   ```

3. 执行putVal

   ```java
   final V putVal(int hash, K key, V value, boolean onlyIfAbsent,
                      boolean evict) {
           Node<K,V>[] tab; Node<K,V> p; int n, i;//辅助变量
       //如果底层的table数组为null||（n=tab.length）==0，就扩容到16
           if ((tab = table) == null || (n = tab.length) == 0)
               n = (tab = resize()).length;
       //取出hash值对应的table表的索引位置的Node,如果为null，就直接把加入的k-v创建成一个Node,加入该位置即可。
           if ((p = tab[i = (n - 1) & hash]) == null)
               tab[i] = newNode(hash, key, value, null);
           else {
               Node<K,V> e; K k;//辅助变量
               //如果table表的索引位置的key的hash值和新的key的hash相同，并满足（table现有的结点的key和准备添加的key是同一个对象||equals返回真），就认为不能加入新的k-v
               if (p.hash == hash &&
                   ((k = p.key) == key || (key != null && key.equals(k))))
                   e = p;
               else if (p instanceof TreeNode)//如果当前的table的已有的Node 是红黑树，就按照红黑树的方式处理
                   e = ((TreeNode<K,V>)p).putTreeVal(this, tab, hash, key, value);
               else {
                   //如果找到的结点，后面是链表，就循环比较
                   for (int binCount = 0; ; ++binCount) {//死循环
                       if ((e = p.next) == null) {//如果整个链表，没有和他相同的，就加到该链表的最后
                           p.next = newNode(hash, key, value, null);
                           //加入后判断当前链表的个数，是否已经到8个，到达8个后就调用treeifyBin方法进行红黑树的转换
                           if (binCount >= TREEIFY_THRESHOLD - 1) // -1 for 1st
                               treeifyBin(tab, hash);
                           break;
                       }
                       if (e.hash == hash &&//在循环比较过程中，发现有相同，就break，就只是替换value
                           ((k = e.key) == key || (key != null && key.equals(k))))
                           break;
                       p = e;
                   }
               }
               if (e != null) { // existing mapping for key
                   V oldValue = e.value;
                   if (!onlyIfAbsent || oldValue == null)
                       e.value = value;//替换key对应的值
                   afterNodeAccess(e);
                   return oldValue;
               }
           }
           ++modCount;//每增加一个Node,就size++
           if (++size > threshold)//如果size>临界值，就扩容
               resize();
           afterNodeInsertion(evict);
           return null;
       }
   ```

   4. 关于树化（转成红黑树）

   - 如果table为null，或者大小还没有到64，暂时不树化，而是进行扩容（MIN_TREEIFY_CAPACITY默认为64）

   ```Java
   final void treeifyBin(Node<K,V>[] tab, int hash) {
           int n, index; Node<K,V> e;
           if (tab == null || (n = tab.length) < MIN_TREEIFY_CAPACITY)
               resize();
           else if ((e = tab[index = (n - 1) & hash]) != null) {
               TreeNode<K,V> hd = null, tl = null;
               do {
                   TreeNode<K,V> p = replacementTreeNode(e, null);
                   if (tl == null)
                       hd = p;
                   else {
                       p.prev = tl;
                       tl.next = p;
                   }
                   tl = p;
               } while ((e = e.next) != null);
               if ((tab[index] = hd) != null)
                   hd.treeify(tab);
           }
       }
   ```

   

   

### 0542集合选型规则

根据业务操作特点选择集合实现类特性进行选择，分析如下：

1. 先判断存储的类型（一组对象[单列]或一组键值对[双列]）
2. 一组对象[单列]：Collection接口

   - 允许重复：List
     - 增删多：LinkedList(底层维护了一个双向链表)
     - 改查多：ArrayList(底层维护Object类型的可变数组)			

   - 不允许重复：Set
     - 无序：HashSet[底层是HashMap,维护了一个哈希表，即（数组+链表+红黑树）]
     - 排序：TreeSet
     - 插入和取出顺序一致：LinkedHashSet，维护数组+双向链表
3. 一组键值对[双列]：Map
   - 键无序：HashMap[底层是：哈希表 jdk7:数组+链表，jdk8:数组+链表+红黑树]
   - 键排序：TreeMap
   - 键插入和取出顺序一致：LinkedHashMap
   - 读取文件 ：Properties

### 0550 分析HashSet和TreeSet分别是如何实现去重的

![image-20221202214038893](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20221202214038893.png)

### 0561 接口中的成员属性最终都是[==公共静态常量==](https://blog.csdn.net/a755199443/article/details/90402480?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167007139016800182726115%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167007139016800182726115&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-1-90402480-null-null.142^v67^pc_rank_34_queryrelevant25,201^v3^control,213^v2^t3_control1&utm_term=%E6%8E%A5%E5%8F%A3%E4%B8%AD%E7%9A%84%E6%88%90%E5%91%98%E9%83%BD%E6%98%AF%E9%9D%99%E6%80%81%E7%9A%84&spm=1018.2226.3001.4187)

接口的成员特点：
1:成员变量 只能是常量。默认修饰符 public [static](https://so.csdn.net/so/search?q=static&spm=1001.2101.3001.7020) final
2:成员方法 只能是[抽象方法](https://so.csdn.net/so/search?q=抽象方法&spm=1001.2101.3001.7020)。默认修饰符 public abstract

### 0750 启动MySQL

![image-20230131221643490](https://raw.githubusercontent.com/jiaxisky/obsidian_image/master/image-20230131221643490.png)

