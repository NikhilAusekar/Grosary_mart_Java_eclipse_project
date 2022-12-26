# Grosary_mart_Java_eclipse_project
Grocery Shop Project with Java using Eclipse , Build a shopping list of components and divided them into 5 categories user can sellect multiple products and if cost is above 3000rupes he will get 5% discount when customer exit bill of his details is generaged
package pack1;
import java.util.Scanner;
import java.time.format.DateTimeFormatter;  
import java.time.LocalDateTime; 

public class Store

{	int total;
	double finalbill;
	
	double nextBill = finalbill;

	Scanner sc = new Scanner(System.in);
		
	int n = sc.nextInt();
	
	//Calculating Bill
	
 int bill(int a , int b) {
	int bill = (a * b);
System.out.println("If Your Bill Is Above 3000Rs "
			+ "You will get 5% disocunt..!!");
	
	 return (bill);
 }
	
 // Calculating total bill
 
 int totalbill(int a)
 {
	 if (a>=3000)
			{
		 
	float discount = (float)(a*5)/100;
	int dis = (int)discount;
	//Calling method to take data from user
	
	
	
	
	//calling method to gate the date
	
	
	System.out.println("===============================");
	System.out.println("====Digital Store ====");
	System.out.println("final bill is "+( finalbill = a - dis));
	System.out.println("Your Discount "+dis +"Rs");
	System.out.println(this.user());
	System.out.println("thank You for shoppoing with us");
	System.out.println("===============================");
				
			
			}		
				
else {
	System.out.println("===============================");
	System.out.println("====Digital Store ====");
	System.out.println(this.user());
	System.out.println("your Final Bill is "+ a);
	System.out.println("Thank you for shopping with us");
	System.out.println("===============================");			
			}
	return 1; 
	
 }
 
//Generating Date on Bill
 public void date() {
	 
	 
	 DateTimeFormatter dtf = DateTimeFormatter.ofPattern("yyyy/MM/dd HH:mm:ss");  
	   LocalDateTime now = LocalDateTime.now();  
	   System.out.println(dtf.format(now));  
	   this.items();
	   
 }
 
 //Customer Details
 public String user () 
 
 {
	 Scanner st = new Scanner(System.in);
	 
		System.out.println("Enter Your Name" );
		String ok = st.next() ;
		ok+= st.nextLine();
		System.out.println("Your Name is:"+ok); 
		 
		
		System.out.println("Enter Your Address");
		String	 addr = st.nextLine();
		System.out.println("Your Address Is:"+addr);
		
		
		System.out.println("Enter Your number");
		long numb = st.nextLong();
		System.out.println("Your Number Is:"+numb);
		
		this.date();
		st.close();
		return ok;
		
 }
 
 
 // Store Product Details
static 
{
	  System.out.println("===============================");

	  System.out.println("Welcome to Digital Store ");

	  System.out.println("===============================");
	  System.out.println(" 1) Cosmetics products");
	  System.out.println(" 2) Electoronices Products");
	  System.out.println(" 3) Vegitables");
  	  System.out.println(" 4) Furniture");
  	  System.out.println(" 5) Jwellary produts");
  	  System.out.println(" 6) Clothing Products");
  	  System.out.println("===============================");
  	  System.out.println(" To Select Option Enter The Number..!!");
  	  System.out.println("===============================");
}
	
  // Selecting different items
  void items()
    {
   if(n==1)
       {
	   System.out.println("===============================");
     System.out.println("You Selected Cosmetics, Below is list of products ");
     System.out.println("===============================");
   			this.cosmetics();
       }
        
   else if(n==2)
   {
        System.out.println("Your Selected Electoronices Products");
            this.elec();
        }
   else if(n==3)
   {
        System.out.println("Your Selected Vegitables");
            this.vegi();
        }
   else if(n==4)
   {
        System.out.println("Your Selected Furneature");
            this.furn();
        }
   else if(n==5)
   {
        System.out.println("Your Selected Jwellary produts");
            this.jwel();
        }
   else if(n==6)
   {
        System.out.println("Your Selected Clothing Products");
        this.clot();
    }
 
   else
   {
    System.out.println("---Please Select Valid Input---");
    main(null);
    
   }
   }  
   
   public void cosmetics() 
   {
	   System.out.println(" 101) Lipsticks 	 "+"180Rs");
	   System.out.println(" 102) Lotion    	 "+"150Rs");
	   System.out.println(" 103) Eyeshadow 	"+" 250Rs");
	   System.out.println(" 104) Powder   	 "+"100Rs");
	   System.out.println(" 105) Nail Polish	"+" 80Rs");
	   
	   
	   
	   int ap = sc.nextInt();
	  
	   
	   
	   switch (ap){
	   
	   case 101:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Lipstick");
		   System.out.println(" Enter Quantity--");
		   System.out.println("===============================");
		   int qu = sc.nextInt();
		 System.out.print(total=this.bill( qu, 180));
		 
		 System.out.println("===============================");
		 System.out.println("Rs your bill");
		   System.out.println("Press 1 to continue Shoping");
		   System.out.println("Press 0 to Exit");
		   int f = sc.nextInt();
		   if (f==1) {
			 //  total = total +total;
			   this.cosmetics();
		   }
		   else if(f ==0){
			//   this.user();
			   System.out.println(this.totalbill(total));
			   this.user();
		   }
		   
		  
		   
		   break;
		   
	   case 102:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Lotion");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");  
		   int qu1 = sc.nextInt();
			 System.out.print(total=this.bill( qu1, 120));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   
			   int f1 = sc.nextInt();
			   if (f1==1) {
				   this.cosmetics();
			   }
			   else if(f1 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
	   case 103:
		   System.out.println("===============================");
		   System.out.println("Your Selected Eyeshadow");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");   
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2, 250));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.cosmetics();
			   }
			   else if(f2 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 104:
		   System.out.println("===============================");
		   System.out.println("Your Selected powder");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");   
		   
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3, 100));  
			 System.out.println("Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f3 = sc.nextInt();
			   if (f3==1) {
				   this.cosmetics();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 105:
		   System.out.println("===============================");
		   System.out.println("Your Selected Nail polish");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4, 80));  
			 System.out.println("Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.cosmetics();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
		   
	   default:
		   
System.out.println("----Please select a valid Option---");
	 this.cosmetics();
			   
		   
			   
	   }
   }
  
   
   public void elec() 
   {
	   System.out.println(" 201) Mobile     "+"20180Rs");
	   System.out.println(" 202) Hand Watch "+"2150Rs");
	   System.out.println(" 203) Laptop    " +"50250Rs");
	   System.out.println(" 204) Headphone "+ "1100Rs");
	   System.out.println(" 205) BT Speaker"+ "2080Rs");
	   
	   int ap = sc.nextInt();
	     
	   int total;
	   switch (ap){
	   
	   case 201:
		   System.out.println("===============================");
		   System.out.println(" Your Selected mobile");
		   System.out.println(" Enter Quantity--");
		   System.out.println("===============================");
		   int qu = sc.nextInt();
		 System.out.print(total=this.bill( qu, 20180));  
		 System.out.println(" Rs your bill");
		 System.out.println("===============================");
		   System.out.println("Press 1 to continue");
		   System.out.println("Press 0 to Exit");
		   int f = sc.nextInt();
		   if (f==1) {
			   this.elec();
		   }
		   else if(f ==0){
			   System.out.println(this.totalbill(total));
		   }
		   break;
	   case 202:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Hand Watch");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		  
		   int qu1 = sc.nextInt();
			 System.out.print(total=this.bill( qu1, 20180));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			 
				   System.out.println(this.totalbill(total));
				   int f1 = sc.nextInt();
				   if (f1==1) {
					   this.elec();
				   }
				   else if(f1 ==0){
					   System.out.println(this.totalbill(total));
				   }
		   break;
		   
	   case 203:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Laptop");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2, 20180));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.elec();
			   }
			   else if(f2 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 204:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Headphone");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3, 20180));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   
			   int f3 = sc.nextInt();
			   if (f3==1) {
				   this.elec();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 205:
		   System.out.println("===============================");
		   System.out.println(" Your Selected BT Speaker");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4, 20180));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			  
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.elec();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
	  
		   
		   default:
			   System.out.println("----Please select a valid Option---");
			   this.cosmetics();	   
	   }
   } 
   public void vegi() 
   {
	   System.out.println(" 301) Apples "+" 120Rs perKg");
	   System.out.println(" 302) Carrots "+"80Rs  perKg");
	   System.out.println(" 303) Spinach "+"30Rs  perKg");
	   System.out.println(" 304) Tomato "+" 20Rs  perKg");
	   System.out.println(" 305) Chilli "+" 80Rs  perKg");
	   
	   int ap = sc.nextInt();
		  
	   int total;
	   switch (ap){
	   
	   case 301:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Apples");
		   System.out.println(" Enter Quantity--");
		   System.out.println("===============================");
		   int qu = sc.nextInt();
		 System.out.print(total=this.bill( qu, 120));  
		 System.out.println(" Rs your bill");
		   System.out.println("Press 1 to continue");
		   System.out.println("Press 0 to Exit");
		   System.out.println("===============================");
		   int f = sc.nextInt();
		   if (f==1) {
			   this.vegi();
		   }
		   else if(f ==0){
			   System.out.println(this.totalbill(total));
		   }
		   break;
	   case 302:
		   System.out.println("===============================");
		   System.out.println(" Your Selected Carrots");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		 
		   int qu1 = sc.nextInt();
			 System.out.print(total=this.bill( qu1, 120));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f1 = sc.nextInt();
			   if (f1==1) {
				   this.vegi();
			   }
			   else if(f1 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   
		   break;
	   case 303:
		   System.out.println("===============================");
		   System.out.println(" Your Selected spinach");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2, 120));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.vegi();
			   }
			   else if(f2 ==0){
				   
				   System.out.println(this.totalbill(total));
			   }
		   
		   break;
	   case 304:
		   System.out.println("===============================");
		   System.out.println(" Your Selected tomato");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3, 120));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f3 = sc.nextInt();
			   if (f3==1) {
				 this.vegi();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   
		   break;
	   case 305:
		   System.out.println("===============================");
		   System.out.println(" Your Selected chilli");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(80);
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4, 120));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.vegi();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   
		   break;
		   
	   
		   
		   default:
			   System.out.println("----Please select a valid Option---");
			   this.vegi();
			   
		  
			   
	   }
   }
  
   
   
   public void furn() 
   {
	   System.out.println(" 401) Sofa "+" 	20120Rs ");
	   System.out.println(" 402) Dining "+"	10080Rs  ");
	   System.out.println(" 403) wardrobe "+"	23000Rs  ");
	   System.out.println(" 404) Chair "+" 	2020Rs  ");
	   System.out.println(" 405) Table "+"	4080Rs  ");
	   
	   
	   int ap = sc.nextInt();
		  
	   int total;
	   switch (ap){
	   
	   case 401:
		   System.out.println("===============================");
		   System.out.println(" Your Selected sofa");
		   System.out.println(" Enter Quantity--");
		   System.out.println("===============================");
		   int qu = sc.nextInt();
		 System.out.print(total=this.bill( qu, 20120));  
		 System.out.println(" Rs your bill");
		 System.out.println("===============================");
		   System.out.println("Press 1 to continue");
		   System.out.println("Press 0 to Exit");
		    int f = sc.nextInt();
		   if (f==1) {
			   this.furn();
		   }
		   else if(f ==0){
			   System.out.println(this.totalbill(total));
		   }
		   break;
	   case 402:
		   System.out.println("===============================");
		   System.out.println(" Your Selected dining ");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   
		   int qu1 = sc.nextInt();
			 System.out.print(total=this.bill( qu1, 10080));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f1 = sc.nextInt();
			   if (f1==1) {
				   this.furn();
			   }
			   else if(f1 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 403:
		   System.out.println("===============================");
		   System.out.println(" Your Selected wardrobe");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		  
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2, 23000));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.furn();
			   }
			   else if(f2 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   
		   break;
	   case 404:
		   System.out.println("===============================");
		   System.out.println(" Your Selected chair");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		  
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3, 2020));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f3 = sc.nextInt();
			   if (f3==1) {
				   this.furn();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }

		   break;
	   
	   case 405:
		   System.out.println("===============================");
		   System.out.println(" Your Selected table");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		   ;
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4, 4080));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.furn();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
		   default:
			   System.out.println("----Please select a valid Option---");
			   this.furn();
			   
		  
			   
	   }
   }
  
   
   public void jwel() 
   {
	   System.out.println(" 501) Dimaond Ring "+" 30120Rs");
	   System.out.println(" 502) Necklace "+"		80080Rs  ");
	   System.out.println(" 503) Ear Rings "+"	3030Rs  ");
	   System.out.println(" 504) Bangles "+"		4520Rs  ");
	   System.out.println(" 505) Bracelete "+"	4080Rs  per");
	   
	   int ap = sc.nextInt();
		  
	   int total;
	   switch (ap){
	   
		   
	   case 501:
		   System.out.println("===============================");
		   System.out.println(" Your Selected dimaond ring");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		 //  System.out.println(120);
		   int qu = sc.nextInt();
			 System.out.print(total=this.bill( qu,30120));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f = sc.nextInt();
			   if (f==1) {
				   this.jwel();
			   }
			   else if(f ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 502:
		   System.out.println("===============================");
		   System.out.println(" Your Selected necklace");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(250);
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2,80080));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f1 = sc.nextInt();
			   if (f1==1) {
				   this.jwel();
			   }
			   else if(f1 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 503:
		   System.out.println("===============================");
		   System.out.println(" Your Selected ear rings");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		 //  System.out.println(100);
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3,3030));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.jwel();
			   }
			   else if(f2 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 504:
		   System.out.println("===============================");
		   System.out.println(" Your Selected bangels");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		 //  System.out.println(80);
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4,4520));  
			 System.out.println(" Rs your bill");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   System.out.println("===============================");
			   int f3 = sc.nextInt();
			   if (f3==1) {
				   this.jwel();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }

		   break;
		   
	   case 505:
		   System.out.println("===============================");
		   System.out.println(" Your Selected bracelate");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(200);
		   int qu5 = sc.nextInt();
			 System.out.print(total=this.bill( qu5,4080));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.jwel();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
		   default:
			   System.out.println("----Please select a valid Option---");
			   this.jwel();
			   
		  
			   
	   }
   }
  
   
   
   public void clot() 
   {
	   System.out.println(" 601) Shirts "+"	1120Rs ");
	   System.out.println(" 602) Shoes "+"	2080Rs ");
	   System.out.println(" 603) Kurtas "+"	1030Rs  ");
	   System.out.println(" 604) T-Shirts "+" 820Rs  ");
	   System.out.println(" 605) Suits "+" 	20080Rs  ");
	   
	   int ap = sc.nextInt();
		  
	   int total;
	   switch (ap){
	   
	   case 601:
		   System.out.println("===============================");
		   System.out.println(" Your Selected shirts");
		   System.out.println(" Enter Quantity--");
		   System.out.println("===============================");
		   int qu = sc.nextInt();
		 System.out.print(total=this.bill( qu, 1220));  
		 System.out.println(" Rs your bill");
		 System.out.println("===============================");
		   System.out.println("Press 1 to continue");
		   System.out.println("Press 0 to Exit");
		   int f = sc.nextInt();
		   if (f==1) {
			   this.clot();
		   }
		   else if(f ==0){
			   System.out.println(this.totalbill(total));
		   }
		   break;
	   case 602:
		   System.out.println("===============================");
		   System.out.println(" Your Selected shoes");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(120);
		   int qu1 = sc.nextInt();
			 System.out.print(total=this.bill( qu1, 2080));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f1 = sc.nextInt();
			   if (f1==1) {
				   this.clot();
			   }
			   else if(f1 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 603:
		   System.out.println("===============================");
		   System.out.println(" Your Selected kurtas");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		 //  System.out.println(250);
		   int qu2 = sc.nextInt();
			 System.out.print(total=this.bill( qu2, 1030));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f2 = sc.nextInt();
			   if (f2==1) {
				   this.clot();
			   }
			   else if(f2 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
	   case 604:
		   System.out.println("===============================");
		   System.out.println(" Your Selected t-shirts");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(100);
		   int qu3 = sc.nextInt();
			 System.out.print(total=this.bill( qu3, 820));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f3 = sc.nextInt();
			   if (f3==1) {
				   this.clot();
			   }
			   else if(f3 ==0){
				   System.out.println(this.totalbill(total));
			   }

		   break;
	   case 605:
		   System.out.println("===============================");
		   System.out.println(" Your Selected suits");
		   System.out.println("Enter Quantity");
		   System.out.println("===============================");
		//   System.out.println(80);
		   int qu4 = sc.nextInt();
			 System.out.print(total=this.bill( qu4, 20080));  
			 System.out.println(" Rs your bill");
			 System.out.println("===============================");
			   System.out.println("Press 1 to continue");
			   System.out.println("Press 0 to Exit");
			   int f4 = sc.nextInt();
			   if (f4==1) {
				   this.clot();
			   }
			   else if(f4 ==0){
				   System.out.println(this.totalbill(total));
			   }
		   break;
		   
	   
		   
   default:
 System.out.println("----Please select a valid Option---");
	this.clot();
			   

			   
	   }
   }
  
   
   
  
	public static void main(String[] args) {
	Store aobj= new Store();
	    aobj.items();
}

}
