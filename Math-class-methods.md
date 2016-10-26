Compound-Interest

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

Math-class-methods

Μαθηματικές Συναρτήσεις

public static void main(String args[]){
System.out.println(Math.abs(-7.4)); //dinei to apoluto
System.out.println(Math.ceil(7.4));//strogulopoiei panw
System.out.println(Math.floor(7.6));//strogulopoiei katw
System.out.println(Math.max(5, 17));//megisto
System.out.println(Math.min(5, 17));//elaxisto
System.out.println(Math.pow(5, 3));//5^3
System.out.println(Math.sqrt(9));//riza tou 9

}
Random number generator for dice

Γενήτρια τυχαίον αριθμών ζαριού

public static void main(String args[]){
    Random dice = new Random();
    int number;
    for(int counter=1;counter<=10;counter++){
        number = 1 + dice.nextInt(6);
        System.out.println(number);
    }
}
Variable Length Arguments

Δημιουργεία μεθόδου που δεν γνωρίζω ποσα στοιχεία θα πάρει

public static void main(String args[]){
    System.out.println(average(5,6,7,8));
}

public static int average(int ... numbers){
    int total = 0;
    for(int x:numbers){
        total+=x;
    }
    return total/numbers.length;        
}
