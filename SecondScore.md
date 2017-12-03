#한줄에 세 점수를 입력 후  두번쩨 점수에 해당하는 값을 출력 
#50 23 1  > 23

```java
	public static void main(String[] args) {
		
		/*
		 * 한줄에 세 점수를 입력 후  두번쩨 점수에 해당하는 값을 출력 
		 * 50 23 1  > 23
		 * 
		 */
		
		Scanner scanner = new Scanner(System.in);
		String str = scanner.nextLine();
		System.out.println(str.substring(str.indexOf(" ")+1, str.lastIndexOf(" ")));
	}
```	