
"OOXXOXXOOO"와 같은 OX퀴즈의 결과가 있다. O는 문제를 맞은 것이고, X는 문제를 틀린 것이다. 문제를 맞은 경우 그 문제의 점수는 그 문제까지 연속된 O의 개수가 된다. 예를 들어, 10번 문제의 점수는 3이 된다.

"OOXXOXXOOO"의 점수는 1+2+0+0+1+0+0+1+2+3 = 10점이다.

OX퀴즈의 결과가 주어졌을 때, 점수를 구하는 프로그램을 작성하시오.

=============================================================

public static void main(String[] args) {
		
		String[] arry = {"O","X"};
		
		Random ran = new Random();
		List<String> list = new ArrayList<String>();
		List<Integer> sumArry = new ArrayList<>();
		int count = 0;
		int sum = 0 ;
		//5면 for문 5번 돌려서 배열 5개를 생성한다.
		for(int z = 0 ; z < 5 ; z++){
			String str = "";
			//O,X 문자열 만들기
			//문자크기 판단 숫자
			for(int i =1 ; i <= ran.nextInt(80)+1 ; i++){
				 //O,X 판단 숫자
				String flag = arry[ran.nextInt(2)];
				
				 str += flag;
				 if(flag.equals("O")){
					 count+=1;
					 sum+=count;
				 }else if(flag.equals("X")){
					 count = 0;
				 }
			}
			
			sumArry.add(sum);
			list.add(str);
		    sum=0;
		    count=0;
		}//for
		
		//미리 만들어 놓은 ox배열에서 랜덤 숫자로 뽑아낸다 
		System.out.println(list.toString());
		System.out.println(sumArry.toString());
	}
  
  
  
  
  
  결과
  
[OOOOO, OXXO, OXOXXXXOOOX, XOXOO, OOXXOXOXOXX]
[15, 2, 8, 4, 6]
