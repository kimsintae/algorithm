	
  
  위의 그림과 같이 육각형으로 이루어진 벌집이 있다. 
  그림에서 보는 바와 같이 중앙의 방 1부터 시작해서 이웃하는 방에 돌아가면서 1씩 증가하는 번호를 주소로 매길 수 있다. 
  숫자 N이 주어졌을 때, 벌집의 중앙 1에서 N번 방까지 최소 개수의 방을 지나서 갈 때 몇 개의 방을 지나가는지(시작과 끝을 포함하여)를 계산하는 프로그램을 작성하시오. 
  예를 들면, 13까지는 3개, 58까지는 5개를 지난다.
  
  
  
  
  
 * 접근방법 
 
  1. 무조건 주어진 수(N)에 있어서 중앙(1)에서 바깥으로 이동시 생성되는 둘레를 하나의 방으로 가정.
     (18일 경우 1에서부터 3번째에 위치한 둘레 이기 때문에 3번째 방)
  
  2. 각 둘레들의 시작과 끝에 대한 범위 규칙을 찾기.
     
     이  동 : 1  2  3  4  5  6
     -------------------------
     시  작 : 1  2  08 20 38 62
     
     종  료 : 1  7  19 37 61 91
     
     
     즉, 
     방(둘레)을 한칸씩 이동 할때 마다 
     시작은 종료값의 +1씩 증가하고 종료값은 6의 배수를 더한 만큼 증가하고 있다는 것.
     
     시작은 종료+1  
     종료는 이동*6
     
  3. 코드 작성
		 
		
	public static void main(String[] args) {	
		
		Scanner scanner = new Scanner(System.in);
		 
		 int n = scanner.nextInt();
		 int move = 1;
		 int start = 1;
		 int end = 1;

		 while(move>0){			 
			 for (int i = start; i <= end; i++) {
				 if(n==i){
					 System.out.println("이동한 방 : "+move);
					 move=-1;
				 };
			 };
			 //다음 범위 시작값
			 start=end+1;
			//다음 범위 끝 값
			 end+=(move*6);
			 //칸 이동수
			 move++;
		 }//while		 
		 

	}//main
