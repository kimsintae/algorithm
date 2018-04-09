	 public static void main(String[] args) {
		 
		 String word = "kimsintae";

		 String alpha="abcdefghijklmnopqrstuvwxyz";
		 
		 for (int i = 0; i < alpha.toCharArray().length; i++) {
			 System.out.print(word.indexOf(alpha.charAt(i))+" ");
		 }//for
		 
	}//main
