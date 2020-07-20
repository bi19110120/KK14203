abstract class Cake {
String n;
String [] topping;
String [] toppingselection;
double pricesmall;
double pricemedium;
double pricebig;
double totalprice; 
int size;
double sizeprice;
String sizetype;
int quantity;

Cake (String cakeName){
n = cakeName ; 
}

String getCake () {
return n;
}

String [] getTopping () {
return topping ;
}

String [] getToppingselection () {
return toppingselection;
}

double getPriceSmall () {
return pricesmall;
}

double getPriceMedium () {
return pricemedium;
}

double getPriceBig () {
return pricebig;
}

int getquantity () {
return quantity;
}

abstract void setCake (String[] t, double s, double m, double b);

void orderCake (String[] toppingselection, int quantity, int size) {
this.toppingselection = toppingselection;
this.quantity=quantity;
this.size=size;
}

double getsizeprice (int size, double pricesmall, double pricemedium, double pricebig) {
if(size==1){
sizeprice = pricesmall;
}
else if (size==2){
sizeprice = pricemedium;
}
else if(size==3){
sizeprice = pricebig;
}
return sizeprice;
}

double gettotalprice () {
double totalprice = getsizeprice(size,pricesmall,pricemedium,pricebig) * quantity + (toppingselection.length*10);
return totalprice;
}

String getsize (int size){
if(size==1) {
sizetype = "Small" ;
}
if(size==2) {
sizetype = "Medium";
}
if(size==3) {
sizetype = "Big";
}
return sizetype;
}

void printCake () {
System.out.println ("----------------------------------");
System.out.println("             Cake Menu             ");
System.out.println("-----------------------------------");
System.out.println( n + " with available toppings : " );
int i = 0;
while (i < topping.length ) {
System.out.println((i+1)+")"+topping[i]);
i++;
}
System.out.println("\nPrice : ");
System.out.println( "[1] Small   :  RM " +getPriceSmall());
System.out.println( "[1] Medium   : RM " +getPriceMedium());
System.out.println( "[1] Big   :  RM  " +getPriceBig());
}

void printOrder () {
System.out.println("\nCake Order Detail : " ) ;
System.out.println("-------------------------------");
System.out.print("Topping : ");
  int i = 0;
  while (i<toppingselection.length) {
  System.out.print ((i+1)+")"+toppingselection[i]+ " ");
  i++;
  }
System.out.println("\nSize : " + getsize (size));
System.out.println("---------------------------------");
System.out.println("Total Price : RM " +gettotalprice());
}
}

class BlackForest extends Cake { 

BlackForest (String n) {
super (n);
}

 void setCake (String[] x, double s, double m, double b) {
 topping = x;
 pricesmall = s;
 pricemedium = m;
 pricebig = b;
}
}

public class TestCake1{
 public static void main(String args[]){
 Cake c = new BlackForest("BlackForest");
 String[] topping = {"Chocolate", "Cherries", "Whipped Cream"};
 c.setCake(topping, 45.00, 65.00, 80.00);
 c.printCake();

 String[] order = {"Chocolate", "Cherries"};
 c.orderCake(order, 1, 2);
 c.printOrder();
 }
}
                
