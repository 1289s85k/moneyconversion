# moneyconversion
import java.util.*;
import java.util.Scanner;
public class moneyCoversion{

public static void main(String[] args){

Scanner sc = new Scanner(System.in);

System.out.println("Input money:");
String money = sc.nextLine;

String Rupee="";
String Paisa="";

int n = money.length();
int f=0,j=0;

for(int i=0; i<=n; i++)
 {
  if(money.charAt(i)==".")
   {
    f=1;
    continue;
    }
  else
  {
   if(f==0)
   {
     Rupee.charAt(i)=money.charAt(i);
     }
     else
     {
     Paisa.charAt(j)=money.charAt(i);
       j++;
       }
    }
  }
 int l=n-Rupee.length();
 n=n-l;
 j=Integer.parseInt(Rupee);
 f=Intger.parseInt(Paisa);
 
public String[] ones = { "", "One", "Two", "Three", "Four",
"Five", "Six", "Seven", "Eight", "Nine", "Ten", "Eleven", "Twelve",
"Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen",
"Eighteen", "Nineteen" };

public String[] tens = { 
        "", "", "Twenty", "Thirty", "Forty", "Fifty", "Sixty", "Seventy", "Eighty", "Ninety"    
};
i=0;
int a;
String[] convert;

if(n>7)
{
a=j/10^7;
if(a>19)
{
b=a%10;
a=a/10;
convert[i] = tens[a] + ones[b] + "Crore";
}

else
{
convert[i] = ones[a] + "Crore";
}
j=j%10^7;
i++;
n=n-2;
}

if(n>5)
{
a=j/10^5;
if(a>19)
{
b=a%10;
a=a/10;
convert[i] = tens[a] + ones[b] + "Lac";
}

else
{
convert[i] = ones[a] + "Lac";
}
j=j%10^5;
i++;
n=n-2;
}

if(n>3)
{
a=j/10^3;
if(a>19)
{
b=a%10;
a=a/10;
convert[i] = tens[a] + ones[b] + "Thousand";
}

else
{
convert[i] = ones[a] + "Thousand";
}
j=j%10^3;
i++;
n=n-1;
}
if(n>2)
{
a=j/10^2;
if(a>19)
{
b=a%10;
a=a/10;
convert[i] = tens[a] + ones[b] + "Hundred";
}

else
{
convert[i] = ones[a] + "Hundred";
}
j=j%10^2;
i++;
n=n-1;
}

if(a>19)
{
b=a%10;
a=a/10;
convert[i] = tens[a] + ones[b];
}


else
{
convert[i] = ones[a];
}

for(i=0;i<=convert.length;i++)
{
System.out.print(convert[i]);
}
System.out.print(f/10^l);
}
