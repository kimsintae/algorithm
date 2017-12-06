#Get smaller number than x
#정수 N개로 이루어진 수열 A와 정수 X가 주어진다. 이 때, A에서 X보다 작은 수를 모두 출력하는 프로그램을 작성하시오.

#첫째 줄에 N과 X가 주어진다. (1 ≤ N, X ≤ 10,000)
#둘째 줄에 수열 A를 이루는 정수 N개가 주어진다. 주어지는 정수는 모두 1보다 크거나 같고, 10,000보다 작거나 같은 정수이다.

```java
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		int num;
		int num2;
		//it is not stored in order
		Set<Integer> set = new LinkedHashSet<Integer>();
		
		num = scan.nextInt();
		num2 = scan.nextInt();
	
		System.out.println(num +" "+ num2);
		int ran= 0 ;
		boolean flag = true;
		while(flag){
			ran =(int)(Math.random()*num)+1;
			set.add(ran);
			if(set.size()>=num){
				flag = false;
			}
		}
		System.out.println(set.toString());
		Iterator<Integer> itr = set.iterator(); 
		while(itr.hasNext()){
			int num3 = itr.next();
			if(num3<num2){
				System.out.print(num3+" ");
			};
		}
	}
```