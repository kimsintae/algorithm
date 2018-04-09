	알파벳 소문자로만 이루어진 단어 S가 주어진다. 각각의 알파벳에 대해서, 
	단어에 포함되어 있는 경우에는 처음 등장하는 위치를, 포함되어 있지 않은 경우에는 -1을 출력하는 프로그램을 작성하시오.
	

	
	public static void main(String[] args) {
		 
		 String word = "kimsintae";

		 String alpha="abcdefghijklmnopqrstuvwxyz";
		 
		 for (int i = 0; i < alpha.toCharArray().length; i++) {
			 System.out.print(word.indexOf(alpha.charAt(i))+" ");
		 }//for
		 
	}//main
	
	
	
	결과 :
	7 -1 -1 -1 8 -1 -1 -1 1 -1 0 -1 2 5 -1 -1 -1 -1 3 6 -1 -1 -1 -1 -1 -1 
