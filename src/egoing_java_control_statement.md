## JAVA 제어문

- 2 Boolean Datatype
    - Boolean은 두 가지 타입으로 지정되어 있음.

  ⇒ true , false 이 두 개는 변수로 지정할 수 없음.

    - ???.contains(값) 은 변수 ???에 ‘값’이 포함되어 있다면 true, 포함되어 있지 않다면 false를 return한다.

    ```java
    public class BooleanApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println("One");
    		System.out.println(1);
    		
    		System.out.println(true);
    		System.out.println(false);
    		
    		String foo = "Hello world";
    		// String true = "Hello world"; reserved word
    		
    		
    		System.out.println(foo.contains("world")); // true
    		System.out.println(foo.contains("hyun")); // false
    	}
    
    }
    ```

- 3 비교연산자
    - 비교연산자는 왼쪽에 있는 값과 오른쪽에 있는 값을 비교해서 그 결과가 무엇이냐에 따라서 true , false 둘 중에 하나의 값을 만들어내는 연산자

    ```java
    public class ComparisonOperatorApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println(1 > 1); // false
    		System.out.println(1 == 1); // true
    		System.out.println(1 < 1); // false
    		System.out.println(1 >= 1); // true
    
    	}
    
    }
    ```

- 4.1 조건문 형식
    - 조건문(비교연산자) - Conditional Statement
    - if와 else → 조건문은 그 안에다가 계속 쓸 수 있음.

    ```java
    public class IfApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println("a");
    //		if(false) {
    //			System.out.println(1);
    //		} else {
    //			if(true) {
    //				System.out.println(2);
    //			} else {
    //				System.out.println(3);
    //			}
    //		}
    		if(false) {
    			System.out.println(1);
    		} else if(true) {
    			System.out.println(2);
    		} else {
    			System.out.println(3);
    		}
    		
    		System.out.println("b");
    
    	}
    
    }
    ```

- 4.2 조건문 응용
    - 왜 if(inputId == id) 이게 아니고 if(inputId.equals(id)) 이것이 되어야 하는가?

    ```java
    public class AuthApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println(args[0]);
    		
    		String id = "egoing";
    		String inputId = args[0];
    		
    		System.out.println("Hi.");
    		
    		//if(inputId == id) {
    		if(inputId.equals(id)) {
    			System.out.println("Master!");
    		} else {
    			System.out.println("Who are you?");
    		}
    
    	}
    
    }
    ```

- 4.3 조건문 응용
    - 드래그하고 Ctrl + / ⇒ 드래그한 부분 주석처리.
    - if(a && b) {?} → a와b 두 값 모두 true라면 ?를 실행.

    ```java
    public class AuthApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println(args[0]);
    		
    		String id = "egoing";
    		String inputId = args[0];
    		
    		String pass = "1111";
    		String inputPass = args[1];
    		
    		System.out.println("Hi.");
    		
    		//if(inputId == id) {
    //		if(inputId.equals(id)) {
    //			if(inputPass.equals(pass)) {
    //				System.out.println("Master!");
    //			} else {
    //				System.out.println("Wrong password!");
    //			}
    //		} else {
    //			System.out.println("Who are you?");
    //		}
    		
    		if(inputId.equals(id) && inputPass.equals(pass)) {
    			System.out.println("Master!");
    		} else {
    			System.out.println("Who are you?");
    		}
    	}
    
    }
    ```

- 5 == vs equals
    - 데이터 타입은 크게 두 가지로 나뉨.

  ⇒ 원시데이터 타입 (primitive) 과 원시데이터 타입이 아닌 데이터 타입.

  ⇒ 원시 데이터 타입 : boolean , int , double , short , long , float , char

  ⇒ non 원시 데이터 타입 : String , Array , Date , File …

    - 원시 데이터 타입은 == 연산자를 사용한다. → 값이 같은 곳에 저장됐다는 의미
    - non 원시 데이터 타입은 equals를 사용한다. → 저장위치와 관계없이 내용이 같다는 의미

    - *문자열은 new로 값을 만들었을 때는 equals를 사용해야 함.

  ⇒ String a = new String(”java”);

    - String a = “java”; 이런 식의 변수는 원시 데이터 타입처럼 동작. == 연산자 사용 가능
- 6 논리 연산자

    ```java
    public class LogicalOperatorApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println(1 == 1); // true
    		
    		// AND 연산자
    		System.out.println(true && true); // true
    		System.out.println(true && false); // false
    		System.out.println(false && true); // false
    		System.out.println(false && false); // false
    		
    		// OR 연산자
    		System.out.println(true || true); // true
    		System.out.println(true || false); // true
    		System.out.println(false || true); // true
    		System.out.println(false || false); // false
    		
    		// not 연산자
    		System.out.println(!true); // false
    		System.out.println(!false); // true
    	}
    
    }
    ```

    - 응용

    ```java
    public class AuthApp2 {
    
    	public static void main(String[] args) {
    		
    		System.out.println(args[0]);
    		
    		String id = "egoing";
    		String inputId = args[0];
    		
    		String pass = "1111";
    		String pass2 = "2222";
    		String inputPass = args[1];
    		
    		System.out.println("Hi.");
    		boolean isRightPass = (inputPass.equals(pass) || inputPass.equals(pass2));
    		
    		if(inputId.equals(id) && isRightPass ) {
    			System.out.println("Master!");
    		} else {
    			System.out.println("Who are you?");
    		}
    	}
    
    }
    ```

- 7.1 반복문
    - while문은 자유도가 높은 반복문
    - for문은 간편화되어있음.
    - for(int i=0; i < 3; i++) {}

  ⇒ for문은 첫번째 i=0을 단 한 번만 실행함. 그 후로 두 번째 i < 3과 i++를 순서대로 한 번씩 계속 반복함.

    ```java
    public class LoopApp {
    
    	public static void main(String[] args) {
    		
    		System.out.println(1);
    		System.out.println("=== while ===");
    		int i = 0;
    		while(i < 3) {
    			System.out.println(2);
    			System.out.println(3);
    //			i = i + 1;
    			i++;
    		}
    		System.out.println("=== for ===");
    		for(int j=0; j < 3; j++) {
    			System.out.println(2);
    			System.out.println(3);
    		}
    		
    		System.out.println(4);
    
    	}
    
    }
    ```

- 7.2 배열
    - users[0] 의 0은 index라고 부름.
    - [0]에 맞는 egoing이란 값은 element(이 배열을 이루고 있는 원소)라고 부름.

    ```java
    public class ArrayApp {
    
    	public static void main(String[] args) {
    		
    		// egoing , jinhuck , youbin
    //		String users = "egoing , jinhuck , youbin";
    		String[] users = new String[3];
    		users[0] = "egoing";
    		users[1] = "jinhuck";
    		users[2] = "youbin";
    		
    		System.out.println(users[1]);
    		System.out.println(users.length);
    		
    		int[] scores = {10, 100, 100};
    		System.out.println(scores[1]);
    		System.out.println(scores.length);
    		
    		
    	}
    
    }
    ```

- 7.3 반복문 + 배열

    ```java
    public class LoopArray {
    
    	public static void main(String[] args) {
    		/*
    		 * <li>egoing</li>
    		 * <li>jinhuck</li>
    		 * <li>youbin</li>
    		 */
    		
    		String[] users = new String[3];
    		users[0] = "egoing";
    		users[1] = "jinhuck";
    		users[2] = "youbin";
    		
    		for(int i=0; i<users.length; i++) {
    			System.out.println(users[i]+",");
    		}
    		
    	}
    
    }
    ```

- 8.1 종합응용 1
    - arguments 에 옳은 아이디값을 넣었다면 Hi, Master!! 를,

  틀린 아이디값을 넣었다면 Hi, Who are you?를 출력하는 코드

    ```java
    public class AuthApp3 {
    
    	public static void main(String[] args) {
    		
    		String[] users = {"egoing", "jinhuck", "youbin"};
    		String inputId = args[0];
    		
    		boolean isLogined = false;
    		for(int i=0; i<users.length; i++) {
    			String currentId = users[i];
    			if(currentId.equals(inputId)) {
    				isLogined = true;
    				break;
    			}
    		}
    		System.out.println("Hi,");
    		if(isLogined) {
    			System.out.println("Master!!");
    		} else {
    			System.out.println("Who are you?");
    		}
    
    	}
    
    }
    ```

- 8.2 종합응용 2과 수업을 마치며
  - 옳은 아이디와 비밀번호를 입력해야 Hi,Master!! 가 출력되는 코드

    ```java
    public class AuthApp3 {
    
    	public static void main(String[] args) {
    		
    		//String[] users = {"egoing", "jinhuck", "youbin"};
    		String[][] users = {
    				{"egoing", "1111"},
    				{"jinhuck", "2222"},
    				{"youbin", "3333"}
    		};
    		String inputId = args[0];
    		String inputPass = args[1];
    		
    		boolean isLogined = false;
    		for(int i=0; i<users.length; i++) {
    			String[] current = users[i];
    			if(
    					current[0].equals(inputId) &&
    					current[1].equals(inputPass)
    			) {
    				isLogined = true;
    				break;
    			}
    		}
    		System.out.println("Hi,");
    		if(isLogined) {
    			System.out.println("Master!!");
    		} else {
    			System.out.println("Who are you?");
    		}
    
    	}
    
    }
    ```
