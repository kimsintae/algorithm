 
 N개의 수가 주어졌을 때, 이를 오름차순으로 정렬하는 프로그램을 작성하시오.
 
 
 
 
 
 public static void main(String[] args) {
		 
		 Scanner scanner = new Scanner(System.in);
		 
		 int num = scanner.nextInt();
		 List<Integer> numArry = new ArrayList<Integer>();
		 java.util.Random ran = new java.util.Random();
		
		 while(numArry.size()<num){
			 int ranNum = ran.nextInt(num)+1;
			 if(numArry.contains(ranNum)==false){
				 numArry.add(ranNum); 
			 }
		 }
		 
		 
		 
		 System.out.println("오름차순 정렬 되기 전 : " + numArry.toString());
		 
		 int temp = 0;
		 for (int i = 0; i < numArry.size(); i++) {
			 for (int j = 0; j < numArry.size(); j++) {
				 if(j+1 < num){
					 //a와 b 두 값을 비교
					 if(numArry.get(j) < numArry.get(j+1)){}else{
					    //j 가 큰 경우
						 
						 //임시 변수에 변경할 값을 넣는다.
						 temp = numArry.get(j);
						 
						 //j에 작은 숫자를 써넣는다.
						 numArry.set(j, numArry.get(j+1));
						 
						 //임시 변수에 저장되있던 숫자를 넣는다.
						 numArry.set(j+1, temp);
						 
					}//if ~ else
				 }
			}//for j
		}// for i
		 
		 
		 System.out.println("오름차순 정렬 되기 후 : " + numArry.toString());
		 
		 
	}//main
  
  
  
  
  
결과 :   
12
오름차순 정렬 되기 전 : [5, 6, 2, 10, 9, 12, 4, 3, 8, 7, 1, 11]
오름차순 정렬 되기 후 : [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
  
  
  
