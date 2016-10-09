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

#Methods with Arrays
	public static void main(String args[]){
		int stef[]= {9,10,22,34};//dhmiourgeia pinaka
		
		change(stef);//kalei th methodo
		
		for(int y : stef){//enhanced loop diaforetikos tropos loop gia pinakes
			System.out.println(y);
		}		
	}
	
	public static void change(int x[]){//methodos
		
		for(int counter=0; counter<x.length; counter++){
			x[counter]+=5;			
		}		
	}
#Print multidimational array with method

	public static void main(String args[]){
		int stef1 [][] ={{8,9,10,11},{12,13,14,15}};//dhmiourgeia tou poludiastatou pinaka me grammes
		int stef2 [][] ={{30,31,32,33},{43},{4,5,6}};
		
		System.out.println("This is the first array...");
		display(stef1);//kaleite h methodos display
		
		System.out.println("This is the second array...");
		display(stef2);
	}
	public static void display(int x[][]){
		for(int row = 0; row < x.length; row++){//gia th grammh 1
			for(int column = 0; column < x[row].length; column++){//gia th sthlh 1-4 (8,9,10,11)
				System.out.print(x[row][column]+"\t");// "/t":gia apostash metaksei ton arithmwn
			}
			System.out.println();
		}
	}

#To String Method and Composition
 Μέθοδος To String και Composition
 
		 public class apples {
			public static void main(String args[]){
				potpie potpieobject =new potpie(4 , 5 , 6);
				tuna tunaobject = new tuna("Stefanos" , potpieobject );
				System.out.println(tunaobject);
			} 
		}
		
		public class tuna {
		private String name;
		private potpie birthday;//reference sto potpie object

		public tuna (String thename ,potpie theday){		
			name =  thename;
			birthday = theday;
		}
		public String toString(){
			return String.format("My name is %s my birthday is %s", name, birthday);// to name tha mpei kanonika afou einai 			//string
			//to birthday einai reference to an object paei sth klash potpie kai paei sthn toString methodo ths kai meta
			//dinei tis plhrofories pou xreiazetai
			}
		}
		public class potpie {
		private int month;
		private int day;
		private int year;

		public potpie(int m,int d,int y){
			month = m;
			day = d;
			year = y;
			System.out.printf("The constractor for this is %s\n", this);//to this shmatodotei oti thelei ena string 
			//anaferetai sto shgkekrimeno object uponoei oti xrieazetai ena string kai afou to xriazetai
			//gi auto tou dinetai apo katw hh to String.		

		}

		public String toString(){
			return String.format("%d/%d/%d", month, day, year);
		}

	}
