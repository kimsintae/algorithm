다장조는 c d e f g a b C, 총 8개 음으로 이루어져있다. 이 문제에서 8개 음은 다음과 같이 숫자로 바꾸어 표현한다. c는 1로, d는 2로, ..., C를 8로 바꾼다.

1부터 8까지 차례대로 연주한다면 ascending, 8부터 1까지 차례대로 연주한다면 descending, 둘 다 아니라면 mixed 이다.

연주한 순서가 주어졌을 때, 이것이 ascending인지, descending인지, 아니면 mixed인지 판별하는 프로그램을 작성하시오.

====================================================================================================================

	public static void main(String[] args) {
		//음계 8자리
		List<Integer> scale = new ArrayList<Integer>();
		Integer num=0;
		
		String result = null;
		
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("음계를 입력하세요");
		for (int i = 1; i <= 8; i++) {
			
			//입력한 음계를 리스트에 담기
			num = scanner.nextInt();
			scale.add(num);
		}
		
		if(scale.get(0)==1){
			//오름차순일 확률이 높은 경우
			for (int i = 1; i <= 8; i++) {
				if(!(i==scale.get(i-1))){
						result="Mixed!";
						break;
					}else{
						result="Ascending!";
					}
			}
		}else if(scale.get(0)==8){
			//내림차순일 확률이 높은 경우
			for (int i=8; i >= 1; i--) {
					if(!(i==scale.get(8-i))){
						result="Mixed!";
						break;
					}else{
						result="Decending!";
					}
			}
		}else{
			result="Mixed!";
		}

		System.out.println("입력한 음계 = "+scale.toString());
		System.out.println("결과 = "+ result);
	}//main
