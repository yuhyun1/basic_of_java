## JAVA Method

- 2 이미 익숙한 메소드

    ```java
    public class FirstMethod {
    
    	public static void main(String[] args) {   // 메인 메소드(함수)
    		
    		System.out.println("Hello Method"); // Hello Method라고 화면에 출력하는 메소드(함수
    		System.out.println(Math.floor(1.1)); // 1이라고 출력하는 메소드(함수)
    
    	}
    
    }
    ```

- 3 메소드의 기본 형식
    - 여러 개의 반복적이고 복잡한 코드를 한 개의 구별하기 쉬운 함수로 나타내는 힘
    - Refactor → Extract Method   ⇒   Alt + Shift + M

    ```java
    public class WhyMethod {
    
    	public static void main(String[] args) {
    		
    		// 100000000
    		printTwoTimesA();
    		// 100000000
    		printTwoTimesA();
    		// 100000000
    		printTwoTimesA();
    
    	}
    
    	public static void printTwoTimesA() {
    		System.out.println("-");
    		System.out.println("a");
    		System.out.println("a");
    	}
    
    }
    ```

- 4 메소드의 입력
    - 매개변수를 두 개를 주고 한 개씩 쓸 수도 있네

    ```java
    public class WhyMethod {
    
    	public static void main(String[] args) {
    		
    					//인자, argument (a,-)
    		printTwoTimes("a", "-");
    		// 100000000
    		printTwoTimes("a", "*");
    		// 100000000
    		printTwoTimes("a", "&");
    		printTwoTimes("b", "!");
    
    	}
    									//매개변수,parameter (text,delimiter)
    	public static void printTwoTimes(String text, String delimiter) {
    		System.out.println(delimiter);
    		System.out.println(text);
    		System.out.println(text);
    	}
    
    }
    ```

- 5 메소드의 출력
    - void = 리턴값이 없을 때 사용.

    ```java
    import java.io.FileWriter;
    import java.io.IOException;
    
    public class WhyMethod {
    
    	public static void main(String[] args) throws IOException {
    		
    		System.out.println(twoTimes("a","-"));
    		FileWriter fw = new FileWriter("out.txt");
    		fw.write(twoTimes("a","*"));
    		fw.close();
    //		Email.send("egoing@a.com", "two times a", twoTimes("a","&"));
    
    	}
    	public static String twoTimes(String text, String delimiter) {
    		String out = "";
    		out = out + delimiter + "\n";
    		out = out + text + "\n";
    		out = out + text + "\n";
    		return out;
    	}
    
    }
    ```

- 6 메소드의 활용

    ```java
    public class AccountingApp {
    	//공급가액
    	public static double valueOfSupply = 10000.0;
    			
    	//부가가치세율
    	public static double vatRate = 0.1;
    	
    	public static double getVAT() {
    		return valueOfSupply * vatRate;
    	}
    	public static double getTotal() {
    		return valueOfSupply + getVAT();
    	}
    	public static void main(String[] args) {
    		
    		System.out.println("Value of supply : "+valueOfSupply);
    		System.out.println("VAT : "+ getVAT() );
    		System.out.println("Total : "+ getTotal() );
    		
    	}
    
    }
    ```

- 8 부록 - access level modifiers
    - private은 같은 클래스 안에서만 사용할 수 있음

    ```java
    class Greeting{
    	//public, protected, default, private
    		public static void hi() {
    			System.out.println("Hi");
    		}
    	
    }
    public class AccessLevelModifiersMethod {
    
    	public static void main(String[] args) {
    		
    		Greeting.hi();
    
    	}
    
    }
    ```

- 9 부록 - static
    - static이 붙은 메소드는 class 메소드다.
    - static이 없는 메소드는 instance 메소드다.

    ```java
    class Print{
    	public String delimiter;
    	public void a() {
    		System.out.println(this.delimiter);
    		System.out.println("a");
    		System.out.println("a");
    	}
    	public void b() {
    		System.out.println(this.delimiter);
    		System.out.println("b");
    		System.out.println("b");
    		
    	}
    	public static void c(String delimiter) {
    		System.out.println(delimiter);
    		System.out.println("b");
    		System.out.println("b");
    	}
    }
    public class staticMethod {
    	
    	public static void main(String[] args) {
    //		Print.a("-");
    //		Print.b("-");
    		
    		// instance
    		Print t1 = new Print();
    		t1.delimiter = "-";
    		t1.a();
    		t1.b();
    		Print.c("$");
    		
    		
    		
    //		Print.a("*");
    //		Print.b("*");
    		
    		Print t2 = new Print();
    		t2.delimiter = "*";
    		t2.a();
    		t2.b();
    	}
    
    }
    ```
