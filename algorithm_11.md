

public class Apartment {

	public static void main(String[] args) {
		
		Scanner scanner = new Scanner(System.in);
		int H = scanner.nextInt();
		int W = scanner.nextInt();
		int N = scanner.nextInt();
		int cnt = 1;
		
			for (int i = 1; i <= W; i++) {
				for (int j = 1; j <= H; j++) {
					//층수
					if(cnt==N){
						System.out.print((j*100)+i);
					}
					cnt++;
				}
			}//for
	}
}
