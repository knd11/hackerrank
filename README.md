[TOC]



# Java

## Scanner的使用

[4](#4.Java Stdin and Stdout II)	[9](#9. Java End-of-file)	

已知：Scanner scan = new Scanner(System.in);

```java
scan.nextInt() //输入内容的下一个整数，下一个指用空格隔开的下一个
scan.nextDouble()//输入内容的下一个浮点数，下一个指用空格隔开的下一个
scan.next() //输入内容的下一个字符串，下一个指用空格隔开的下一个
scan.nextLine()//输入内容的下一行
scan.hasNext() //判断是否还有下一个输入
```

## 控制输出

[5](#5. Java Output Formatting)

`System.out.printf("%-15s%03d\n",s1,x);`

控制字符串长度为15，数字长度为3

## String 和 int 间的转换

[11](#11. Java Int to String)

```java
int n = in .nextInt();
String s = String.valueOf(n);//int --> String
int n1 = Integer.parseInt(s);//String --> int
```

## 时间

[12](#12. Java Date and Time)

```java
calendar.set(year,month-1,day);
int n = calendar.get(Calendar.DAY_OF_WEEK);
String[] Day ={"SUNDAY","MONDAY","TUESDAY","WEDNESDAY","THURSDAY","FRIDAY","SATURDAY"};
System.out.println(Day[n - 1]);
```

注意set的顺序，年月日，month要==减1==







## 例题

### 4.Java Stdin and Stdout II

![java_1](pic/java_4.png)

```java
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int i = scan.nextInt();
        double d = scan.nextDouble();

        scan.nextLine();
        String s = scan.nextLine();

        System.out.println("String: " + s);
        System.out.println("Double: " + d);
        System.out.println("Int: " + i);
    }
}
```

### 5. Java Output Formatting

![java_1](pic/java_5.png)

```java
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
            Scanner sc=new Scanner(System.in);
            System.out.println("================================");

            for(int i=0;i<3;i++)
            {
                String s1=sc.next();
                int x=sc.nextInt();
                //Complete this line
                System.out.printf("%-15s%03d\n",s1,x);

                
            }
            System.out.println("================================");

    }
}
```

### 7. Java Loops II

![java_7](pic/java_7.png)

```java
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int t=in.nextInt();  
        int j;    

        for(int i=0;i<t;i++){
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();
            double temp = 0;

            for (j = 0; j < n; j++) {
                temp = temp + Math.pow(2,j)*b;
                System.out.print(a + (int)temp + " ");
            } 
            System.out.print("\n");
        }

        in.close();
    }
}
```



### 9. Java End-of-file

![java_9](pic/java_9.png)

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner scan = new Scanner(System.in);
        int i = 0;

        while(scan.hasNext()){
            String text = scan.nextLine();
            i++;
            System.out.println( i + " " + text);
        }
    }
}
```

### 10. Java Static Initializer Block

![java_10](pic/java_10.png)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

static boolean flag = true; 
static int B,H;

static{ 
    Scanner sc = new Scanner(System.in);
    
    B = sc.nextInt();
    H = sc.nextInt();
    boolean flag = true;
    
    if(B<=0||H<=0){
        System.out.println("java.lang.Exception: Breadth and height must be positive");
        flag = false; System.exit(0); 
    }
}

public static void main(String[] args){
		if(flag){
			int area=B*H;
			System.out.print(area);
		}
		
	}//end of main

}//end of class
```

### 11. Java Int to String

![java_11](pic/java_11.png)

```java
String s = String.valueOf(n);//int --> String
```



### 12. Java Date and Time

```java
public static String findDay(int month, int day, int year) {
      Calendar calendar = Calendar.getInstance();
      calendar.set(year,month-1,day);
      int n = calendar.get(Calendar.DAY_OF_WEEK);
      String[] Day ={"SUNDAY","MONDAY","TUESDAY","WEDNESDAY","THURSDAY","FRIDAY","SATURDAY"};
        return Day[n - 1];
}
```



# 30 Days of Code

## 0. Hello,World

![0](pic/0.png)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
public class Solution {
	public static void main(String[] args) {
        // Create a Scanner object to read input from stdin.
		Scanner scan = new Scanner(System.in); 
		
		// Read a full line of input from stdin and save it to our variable, inputString.
		String inputString = scan.nextLine(); 

		// Close the scanner object, because we've finished reading 
        // all of the input from stdin needed for this challenge.
		scan.close(); 
      
		// Print a string literal saying "Hello, World." to stdout.
		System.out.println("Hello, World.");
        System.out.println(inputString);
	    // TODO: Write a line of code here that prints the contents of inputString to stdout.
	}
}
```

## 1. Data Types

![1](pic/1.png)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
	
    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";
		
        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */

        /* Read and save an integer, double, and String to your variables.*/
        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.
        
        /* Print the sum of both integer variables on a new line. */

        /* Print the sum of the double variables on a new line. */
		
        /* Concatenate and print the String variables on a new line; 
        	the 's' variable above should be printed first. */
        
        int In1 = 0;
        double In2 = 0.0;
        String In3 = "";

        In1 = scan.nextInt();
        System.out.println(In1 + i);

        In2 = scan.nextDouble();
        System.out.println(In2 + d);

        In3 = s;
        while (scan.hasNextLine()) {
            In3 = In3 + scan.nextLine();
        }
        System.out.println(In3);

 
        scan.close();
    }
}
```

## 2. Operators

![2](pic/2.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the solve function below.
    static void solve(double meal_cost, int tip_percent, int tax_percent) {
        double Res = meal_cost*(1 + tip_percent/100.0 + tax_percent/100.0);
        System.out.print((int)Math.round(Res));
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        double meal_cost = scanner.nextDouble();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int tip_percent = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int tax_percent = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        solve(meal_cost, tip_percent, tax_percent);
        scanner.close();
    }
}

```

## 3. Intro to Conditional Statements

![3](pic/3.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {


    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int N = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
        if(N%2==1)
            System.out.print("Weird");
        else{
            if(N>=2 && N<5)
                System.out.print("Not Weird");
            else if(N>=6 && N<=20)
                System.out.print("Weird");
            else if(N>20)
                System.out.print("Not Weird");
        }
        scanner.close();
    }
}

```

## 4. Class vs. Instance

![4](pic/4.png)

```java
import java.io.*;
import java.util.*;

public class Person {
    private int age;	

	public Person(int initialAge) {
  		// Add some more code to run some checks on initialAge
        if(initialAge<0 || initialAge>30)
        {
            initialAge = 0;
            System.out.println("Age is not valid, setting age to 0.");
        }
        age = initialAge;
	} 

	public void amIOld() {
  		// Write code determining if this person's age is old and print the correct statement:
        if(age<13)
            System.out.println("You are young.");   
        else if(age>=13 && age<18)
            System.out.println("You are a teenager.");  
        else
            System.out.println("You are old.");
	}

	public void yearPasses() {
  		// Increment this person's age.
          age++;
	}


	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int T = sc.nextInt();
		for (int i = 0; i < T; i++) {
			int age = sc.nextInt();
			Person p = new Person(age);
			p.amIOld();
			for (int j = 0; j < 3; j++) {
				p.yearPasses();
			}
			p.amIOld();
			System.out.println();
        }
		sc.close();
    }
}
```

## 5. Loops

![5](pic/5.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
        for(int i=1;i<=10;i++){
            System.out.println(n + " x " + i + " = " + n*i);
        }
        scanner.close();
    }
}

```

## 6. Let's Review

![6](pic/6.png)

```python
# Enter your code here. Read input from STDIN. Print output to STDOUT

def ss_print(string):
    s_odd = s_even = ''
    for i in range(0,len(string)):
        if i%2 != 0 :
            s_odd = s_odd + string[i]
        if i%2 == 0 or i == 0:
            s_even = s_even + string[i]
        i = i + 1
    print(s_even + " " + s_odd)

ii = int(input())
for j in range(0,ii):
    s = input()
    ss_print(s)
```

## 7. Arrays

![7](pic/7.png)

```Java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int[] arr = new int[n];

        String[] arrItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < n; i++) {
            int arrItem = Integer.parseInt(arrItems[i]);
            arr[n-i-1] = arrItem;
        }

        for(int j=0;j<n;j++){
            System.out.print(arr[j] + " ");
        }
        scanner.close();
    }
}
```

## 8.  Dictionaries and Maps

![8](pic/8.png)

```java
//Complete this code or write your own from scratch
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        HashMap<String,Integer> map = new HashMap();
        int n = in.nextInt();
        for(int i = 0; i < n; i++){
            String name = in.next();
            int phone = in.nextInt();
            // Write code here
            map.put(name,phone);
        }
        while(in.hasNext()){
            String s = in.next();
            // Write code here
            if (map.containsKey(s)){
                System.out.println(s + "=" + map.get(s));
            }
            else
                System.out.println("Not found");
        }
        in.close();
    }
}

```

## 9. Recursion 3

![9](pic/9.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the factorial function below.
    static int factorial(int n) {
        int result = 1;
        if(n>1)
        {
            result = n*factorial(n-1);
        }

        return result;
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int result = factorial(n);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedWriter.close();

        scanner.close();
    }
}

```

## 10. Binary Numbers

![10](pic/10.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int temp = n;
        int count = 1;
        int count_max = 1;
        String res = "";
        

        while(temp!=0)
        {
            res = res + temp%2;
            temp = temp/2;  
        }
        

        for(int i=1;i<res.length();i++)
        {
            if(res.charAt(i)=='1' && res.charAt(i)==res.charAt(i-1))
                ++count;         
            else
                count = 1;
            
            if(count>count_max)
                count_max = count;
        }
            
        System.out.print(count_max);
        scanner.close();
    }
}

```



## 11. 2D Arrays

![11](pic/11.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int[][] arr = new int[6][6];
        // int[][] hG = new int[(6-2)*3][(6-2)*3];
        int SUM = 0;
        int SUM_MAX = -9*7;//注意不能初始化为0，因为和可能为负数

        for (int i = 0; i < 6; i++) {
            String[] arrRowItems = scanner.nextLine().split(" ");
            scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

            for (int j = 0; j < 6; j++) {
                int arrItem = Integer.parseInt(arrRowItems[j]);
                arr[i][j] = arrItem;
            }
        }

        for(int m = 1; m < 5; m++)
        {
            for(int n =1; n<5; n++){
                // hG[3*(m-1)][3*(n-1)] = arr[m-1][n-1];
                // hG[3*(m-1)][3*(n-1)] = arr[m-1][n];
                // hG[3*(m-1)][3*(n-1)] = arr[m-1][n+1];
                // hG[3*(m-1)][3*(n-1)] = arr[m][n];
                // hG[3*(m-1)][3*(n-1)] = arr[m+1][n-1];
                // hG[3*(m-1)][3*(n-1)] = arr[m+1][n];
                // hG[3*(m-1)][3*(n-1)] = arr[m+1][n+1];
                SUM = arr[m-1][n-1] + arr[m-1][n] + arr[m-1][n+1] + arr[m][n] + arr[m+1][n-1] + arr[m+1][n] + arr[m+1][n+1];
                if(SUM >= SUM_MAX)
                    SUM_MAX = SUM; 
            }
        }

        System.out.print(SUM_MAX);

        scanner.close();
    }
}
```

## 12. Inheritance

![12](pic/12.png)

```java
import java.util.*;

class Person {
	protected String firstName;
	protected String lastName;
	protected int idNumber;
	
	// Constructor
	Person(String firstName, String lastName, int identification){
		this.firstName = firstName;
		this.lastName = lastName;
		this.idNumber = identification;
	}
	
	// Print person data
	public void printPerson(){
		 System.out.println(
				"Name: " + lastName + ", " + firstName 
			+ 	"\nID: " + idNumber); 
	}
	 
}

class Student extends Person{
	private int[] testScores;
    private int id;
    /*	
    *   Class Constructor
    *   
    *   @param firstName - A string denoting the Person's first name.
    *   @param lastName - A string denoting the Person's last name.
    *   @param id - An integer denoting the Person's ID number.
    *   @param scores - An array of integers denoting the Person's test scores.
    */
    // Write your constructor here

    public Student(String firstName,String lastName,int id,int[] scores){
        super(firstName,lastName,id);
        testScores = scores;
    } 

    /*	
    *   Method Name: calculate
    *   @return A character denoting the grade.
    */
    // Write your method here
    

    public char calculate(){
        int total = 0;
        for(int i = 0; i < testScores.length; i++)
            total = total + testScores[i];

        total = total/testScores.length;
        return ( total > 89 ? 'O' : 
                total > 79 ? 'E' : 
                total > 69 ? 'A' : 
                total > 54 ? 'P' :
                total > 39 ? 'D' : 'T' );
    }
}

class Solution {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		String firstName = scan.next();
		String lastName = scan.next();
		int id = scan.nextInt();
		int numScores = scan.nextInt();
		int[] testScores = new int[numScores];
		for(int i = 0; i < numScores; i++){
			testScores[i] = scan.nextInt();
		}
		scan.close();
		
		Student s = new Student(firstName, lastName, id, testScores);
		s.printPerson();
		System.out.println("Grade: " + s.calculate() );
	}
}
```



## 13. Abstract Classes

![13](pic/13.png)

```java
import java.util.*;

abstract class Book {
    String title;
    String author;
    
    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }
    
    abstract void display();
}

class MyBook extends Book{

    private int Price;

    MyBook(String title, String author, int price){
        super(title,author);
        Price = price;
    }

    public void display(){
        System.out.print("Title: " + title + "\nAuthor: " + author + "\nPrice: " + Price);
    } 
}
// Declare your class here. Do not use the 'public' access modifier.
    // Declare the price instance variable
    
    /**   
    *   Class Constructor
    *   
    *   @param title The book's title.
    *   @param author The book's author.
    *   @param price The book's price.
    **/
    // Write your constructor here
    
    /**   
    *   Method Name: display
    *   
    *   Print the title, author, and price in the specified format.
    **/
    // Write your method here
    
// End class

public class Solution {
   
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String title = scanner.nextLine();
        String author = scanner.nextLine();
        int price = scanner.nextInt();
        scanner.close();

        Book book = new MyBook(title, author, price);
        book.display();
    }
}
```



## 14. Scope

![14](pic/14.png)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;


class Difference {
  	private int[] elements;
  	public int maximumDifference;

	// Add your code here
    Difference(int[] a){
        elements = a;
    }

    public int computeDifference(){
        int min=100;
        int max=1;

        for(int i=0;i<elements.length;++i)
        {
            if(elements[i]<min){min=elements[i];}
            if(elements[i]>max){max=elements[i];}
        }
        maximumDifference=max-min;
        return maximumDifference;
    }
    
} // End of Difference class

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] a = new int[n];
        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }
        sc.close();

        Difference difference = new Difference(a);

        difference.computeDifference();

        System.out.print(difference.maximumDifference);
    }
}
```

## 15.  Linked List

![15](pic/15.png)

```java
import java.io.*;
import java.util.*;

class Node {
	int data;
	Node next;
	Node(int d) {
        data = d;
        next = null;
    }
}

class Solution {

    public static  Node insert(Node head,int data) {
        //Complete this method
        if(head == null)
            return new Node(data);
        else if(head.next == null)
            head.next = new Node(data);
        else
            insert(head.next,data);

        return head;                
            
    }

	public static void display(Node head) {
        Node start = head;
        while(start != null) {
            System.out.print(start.data + " ");
            start = start.next;
        }
    }

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        Node head = null;
        int N = sc.nextInt();

        while(N-- > 0) {
            int ele = sc.nextInt();
            head = insert(head,ele);
        }
        display(head);
        sc.close();
    }
}
```

## 16. Exceptions - String to Integer

![16](pic/16.png)



try to print String2Integer,if failed,turn to catch.

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String S = in.next();

        try{
            System.out.print(Integer.parseInt(S));
        }
        catch(Exception e){
            System.out.print("Bad String");
        }
    }
}
```

## 17. More Exceptions

![17](pic/17.png)

```java
import java.util.*;
import java.io.*;

//Write your code here
class Calculator {
    public int power(int n, int p)throws Exception{
        if(n < 0 || p < 0) {
           throw new Exception("n and p should be non-negative");
        }
        return (int)Math.pow(n, p);
    }
}

class Solution{

    public static void main(String[] args) {
    
        Scanner in = new Scanner(System.in);
        int t = in.nextInt();
        while (t-- > 0) {
        
            int n = in.nextInt();
            int p = in.nextInt();
            Calculator myCalculator = new Calculator();
            try {
                int ans = myCalculator.power(n, p);
                System.out.println(ans);
            }
            catch (Exception e) {
                System.out.println(e.getMessage());
            }
        }
        in.close();
    }
}
```

## 18. Queues and Stacks

![18](pic/18.png)

```java
import java.io.*;
import java.util.*;

public class Solution {
    // Write your code here.
    Stack<Character> stack = new Stack<>();
    Queue<Character> queue = new LinkedList<>();

    void pushCharacter(Character ch) {
        stack.push(ch);
    }

    void enqueueCharacter(char ch) {
        queue.add(ch);
    }

    char popCharacter(){
        return stack.pop();
    }

    char dequeueCharacter() {
        return queue.remove();
    }
    
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String input = scan.nextLine();
        scan.close();

        // Convert input String to an array of characters:
        char[] s = input.toCharArray();

        // Create a Solution object:
        Solution p = new Solution();

        // Enqueue/Push all chars to their respective data structures:
        for (char c : s) {
            p.pushCharacter(c);
            p.enqueueCharacter(c);
        }

        // Pop/Dequeue the chars at the head of both data structures and compare them:
        boolean isPalindrome = true;
        for (int i = 0; i < s.length/2; i++) {
            if (p.popCharacter() != p.dequeueCharacter()) {
                isPalindrome = false;                
                break;
            }
        }

        //Finally, print whether string s is palindrome or not.
        System.out.println( "The word, " + input + ", is " 
                           + ( (!isPalindrome) ? "not a palindrome." : "a palindrome." ) );
    }
}
```



## 19. Interfaces

![19](pic/19.png)

```java
import java.io.*;
import java.util.*;

interface AdvancedArithmetic{
   int divisorSum(int n);
}
class Calculator implements AdvancedArithmetic {
    public int divisorSum(int n) {
        int sum = 0;
        for(int i=1;i<=n;i++){
            for(int j=i;j<=n;j++){
                if(i*j==n){
                    if(i==j)
                        sum = sum + i;
                    else
                        sum = sum + i + j;  
                }      
            }
        }
    return sum;    
    }
}

class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        scan.close();
        
      	AdvancedArithmetic myCalculator = new Calculator(); 
        int sum = myCalculator.divisorSum(n);
        System.out.println("I implemented: " + myCalculator.getClass().getInterfaces()[0].getName() );
        System.out.println(sum);
    }
}
```

## 20. Sorting

![20](pic/20.png)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int[] a = new int[n];
        for(int a_i=0; a_i < n; a_i++){
            a[a_i] = in.nextInt();
        }
        // Write Your Code Here
        int temp = 0;
        int swap = 0;
        for(int i=0;i<n;i++){
            for(int j=0;j<n-1;j++){
                if(a[j]>a[j+1]){
                    temp = a[j];
                    a[j] = a[j+1];
                    a[j+1] = temp;
                    swap++;
                }   
            }
        }
        System.out.println("Array is sorted in " + swap +  " swaps.");
        System.out.println("First Element: " + a[0]);
        System.out.print("Last Element: " + a[n-1]);
    }
}
```



## 21. Generics

![21](pic/21.png)

```java
import java.util.*;

class Printer <T> {

    /**
    *    Method Name: printArray
    *    Print each element of the generic array on a new line. Do not return anything.
    *    @param A generic array
    **/
    
    // Write your code here
    public static <E> void printArray(E[] generic){
        for(E element : generic) {
            System.out.println(element); 
        }
    }

}

public class Generics {
    
    public static void main(String args[]){
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        Integer[] intArray = new Integer[n];
        for (int i = 0; i < n; i++) {
            intArray[i] = scanner.nextInt();
        }

        n = scanner.nextInt();
        String[] stringArray = new String[n];
        for (int i = 0; i < n; i++) {
            stringArray[i] = scanner.next();
        }
        
        Printer<Integer> intPrinter = new Printer<Integer>();
        Printer<String> stringPrinter = new Printer<String>();
        intPrinter.printArray( intArray  );
        stringPrinter.printArray( stringArray );
        if(Printer.class.getDeclaredMethods().length > 1){
            System.out.println("The Printer class should only have 1 method named printArray.");
        }
    } 
}
```

## 22.  Binary Search Trees

![22](pic/22.png)

```java
import java.util.*;
import java.io.*;
class Node{
    Node left,right;
    int data;
    Node(int data){
        this.data=data;
        left=right=null;
    }
}
class Solution{

	public static int getHeight(Node root){
      //Write your code here
      if(root == null)  return -1;
      
      int left = 1 + getHeight(root.left);
      int right = 1 + getHeight(root.right);
      
      return Math.max(left, right);
    }

    public static Node insert(Node root,int data){
        if(root==null){
            return new Node(data);
        }
        else{
            Node cur;
            if(data<=root.data){
                cur=insert(root.left,data);
                root.left=cur;
            }
            else{
                cur=insert(root.right,data);
                root.right=cur;
            }
            return root;
        }
    }
	 public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int T=sc.nextInt();
        Node root=null;
        while(T-->0){
            int data=sc.nextInt();
            root=insert(root,data);
        }
        int height=getHeight(root);
        System.out.println(height);
    }
}
```



## 23. BST Level-Order Traversal

![23](pic/23.png)

```java
import java.util.*;
import java.io.*;
class Node{
    Node left,right;
    int data;
    Node(int data){
        this.data=data;
        left=right=null;
    }
}
class Solution{

static void levelOrder(Node root){
      //Write your code here
        //生成一个队列
        Queue<Node> q = new LinkedList<>();
        q.add(root);  //根结点入队
        //循环遍历整个队列
        while (!q.isEmpty()) {
        //获取队列头部的元素，并删除该元素
        Node cur = q.remove();
        System.out.print(cur.data + " ");
        //左结点非空则入队，右结点非空则入队
        if (cur.left != null)
            q.add(cur.left);
        if (cur.right != null)
            q.add(cur.right);
        }
        
    }

public static Node insert(Node root,int data){
        if(root==null){
            return new Node(data);
        }
        else{
            Node cur;
            if(data<=root.data){
                cur=insert(root.left,data);
                root.left=cur;
            }
            else{
                cur=insert(root.right,data);
                root.right=cur;
            }
            return root;
        }
    }
    public static void main(String args[]){
            Scanner sc=new Scanner(System.in);
            int T=sc.nextInt();
            Node root=null;
            while(T-->0){
                int data=sc.nextInt();
                root=insert(root,data);
            }
            levelOrder(root);
        }	
}
```

## 24. More Linked Lists

![24](pic/24.png)

```java
import java.io.*;
import java.util.*;
class Node{
	int data;
	Node next;
	Node(int d){
        data=d;
        next=null;
    }
	
}
class Solution
{

    public static Node removeDuplicates(Node head) {
      //Write your code here
        if(head==null || head.next==null)
            return head;
        
        if(head.data == head.next.data){
            head.next = head.next.next;
            removeDuplicates(head);
        }
        else{
            removeDuplicates(head.next);
        }
        return head;
    }

	 public static  Node insert(Node head,int data)
     {
        Node p=new Node(data);			
        if(head==null)
            head=p;
        else if(head.next==null)
            head.next=p;
        else
        {
            Node start=head;
            while(start.next!=null)
                start=start.next;
            start.next=p;

        }
        return head;
    }
    public static void display(Node head)
        {
              Node start=head;
              while(start!=null)
              {
                  System.out.print(start.data+" ");
                  start=start.next;
              }
        }
        public static void main(String args[])
        {
              Scanner sc=new Scanner(System.in);
              Node head=null;
              int T=sc.nextInt();
              while(T-->0){
                  int ele=sc.nextInt();
                  head=insert(head,ele);
              }
              head=removeDuplicates(head);
              display(head);

       }
    }
```

## 25. Running Time and Complexity

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        
        for(int i=0;i<n;i++){
            String str = " ";
            int number = scan.nextInt();
            for(int j=2;j<=Math.sqrt(number);j++){
                if(number%j==0){
                    str = "Not prime";
                }
            }
            if(str == "Not prime" || number == 1)
                System.out.println("Not prime");
            else
                System.out.println("Prime");

        }
    }
}


```

## 26. Nested Logic

![26](pic/26.png)

```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner scan = new Scanner(System.in);

        int Aday = scan.nextInt();
        int Amonth = scan.nextInt();
        int Ayear = scan.nextInt();

        int Dday = scan.nextInt();
        int Dmonth = scan.nextInt();
        int Dyear = scan.nextInt();
        scan.close();

        int daylate = Aday - Dday;
        int monthlate = Amonth - Dmonth;
        int yearlate = Ayear- Dyear;

        System.out.println(yearlate>0?10000:monthlate>0 && yearlate==0?500*monthlate:daylate>0 && monthlate==0 && yearlate==0?15*daylate:0);

    }
}
```

## 27. Testing

![27](pic/27.png)

```java
import java.util.*;

public class Solution {

    public static int minimum_index(int[] seq) {
        if (seq.length == 0) {
            throw new IllegalArgumentException("Cannot get the minimum value index from an empty sequence");
        }
        int min_idx = 0;
        for (int i = 1; i < seq.length; ++i) {
            if (seq[i] < seq[min_idx]) {
                min_idx = i;
            }
        }
        return min_idx;
    }

    static class TestDataEmptyArray {
        public static int[] get_array() {
            // complete this function
            int arr[] = {};
            return arr;
        }
    }

    static class TestDataUniqueValues {
        static int[] arr = {1,2,3,4};

        public static int[] get_array() {
            // complete this function
            return arr; 
        }
        public static int get_expected_result() {
            // complete this function
            return 0;
        }
    }

    static class TestDataExactlyTwoDifferentMinimums {
         static int[] arr = {0,0,1}; 

        public static int[] get_array() {
            // complete this function
            return arr;
        }

        public static int get_expected_result() {
            // complete this function
            return 0;
        }
    }

    
	public static void TestWithEmptyArray() {
        try {
            int[] seq = TestDataEmptyArray.get_array();
            int result = minimum_index(seq);
        } catch (IllegalArgumentException e) {
            return;
        }
        throw new AssertionError("Exception wasn't thrown as expected");
    }

    public static void TestWithUniqueValues() {
        int[] seq = TestDataUniqueValues.get_array();
        if (seq.length < 2) {
            throw new AssertionError("less than 2 elements in the array");
        }

        Integer[] tmp = new Integer[seq.length];
        for (int i = 0; i < seq.length; ++i) {
            tmp[i] = Integer.valueOf(seq[i]);
        }
        if (!((new LinkedHashSet<Integer>(Arrays.asList(tmp))).size() == seq.length)) {
            throw new AssertionError("not all values are unique");
        }

        int expected_result = TestDataUniqueValues.get_expected_result();
        int result = minimum_index(seq);
        if (result != expected_result) {
            throw new AssertionError("result is different than the expected result");
        }
    }

    public static void TestWithExactlyTwoDifferentMinimums() {
        int[] seq = TestDataExactlyTwoDifferentMinimums.get_array();
        if (seq.length < 2) {
            throw new AssertionError("less than 2 elements in the array");
        }

        int[] tmp = seq.clone();
        Arrays.sort(tmp);
        if (!(tmp[0] == tmp[1] && (tmp.length == 2 || tmp[1] < tmp[2]))) {
            throw new AssertionError("there are not exactly two minimums in the array");
        }

        int expected_result = TestDataExactlyTwoDifferentMinimums.get_expected_result();
        int result = minimum_index(seq);
        if (result != expected_result) {
            throw new AssertionError("result is different than the expected result");
        }
    }

    public static void main(String[] args) {
        TestWithEmptyArray();
        TestWithUniqueValues();
        TestWithExactlyTwoDifferentMinimums();
        System.out.println("OK");
    }
}
```

## 28. RegEx, Patterns, and Intro to Databases

![28](pic/28-1575782754828.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int N = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
        List<String> list = new ArrayList();
        
        for (int NItr = 0; NItr < N; NItr++) {
            String[] firstNameEmailID = scanner.nextLine().split(" ");

            String firstName = firstNameEmailID[0];

            String emailID = firstNameEmailID[1];
            
            // This will match a sequence of 1 or more uppercase and lowercase English letters as well as spaces
        String emailRegEx = ".+@gmail\\.com$";;

        // Create a Pattern object (compiled RegEx) and save it as 'p'
        Pattern p = Pattern.compile(emailRegEx);

        // We need a Matcher to match our compiled RegEx to a String
        Matcher m = p.matcher(emailID);

        // if our Matcher finds a match
        if( m.find() ) {
            list.add(firstName);
        }
        }
        Collections.sort(list);
        for (String name : list){
            System.out.println(name);
        }
        scanner.close();
        
    }
}
```

## 29. Bitwise AND

![29](pic/29.png)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {



    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int t = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int tItr = 0; tItr < t; tItr++) {
            String[] nk = scanner.nextLine().split(" ");

            int n = Integer.parseInt(nk[0]);

            int k = Integer.parseInt(nk[1]);

            
            if(((k-1)|k) > n && k%2==0)
                System.out.println(k-2);
            else
                System.out.println(k-1);

        }
        scanner.close();
    }
}
```









