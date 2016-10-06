# Compound-Interest
Υπολογισμός κάτι σαν επιτόκιο

public class apples {
		
	public static void main(String args[]){
		double amount;
		double principal = 10000;
		double rate = 0.1;
		for(int day=1; day<=20; day++){
			
			amount = principal*Math.pow(1 + rate , day);
			
			System.out.println(day + "   "+ amount);
			
		}
	}
}
#Arrays Elements as counters
Δημιουργεία πίνακα με στοιχεία μετρητές

	public static void main(String args[]){
		
		Random rand = new Random();		
		int freq[] = new int[7]; //bazoume 7 giati ksekinaei na metraei apo to 0-5 kai tha to ftiaksoume etsi na 
		//bazei apo to 1 mexri to 6
		
		for(int roll = 1; roll <= 1000; roll++){			
			++freq[1 + rand.nextInt(6)];
			//1 + rand.nextInt(6):mas dinei tous arithmous apo 1 mexri 6
			//++freq:An to zari gurisei kai erthei 3 tote sth thesh 2(3-1)tou freq mpainei 1 k.o.k.
			//Ola einai arxikopoihmena sto 0 			
		}
		System.out.println("Face \t Frequency");
		for(int face=1;face<=freq.length;face++){//to face ksekinaei apo to 1 den mas endeiaferei to 0
			System.out.println(face + "\t" + freq[face]);//emfanizei thn suxnothta 			
		}
	}
