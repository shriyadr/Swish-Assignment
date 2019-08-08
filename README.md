/*# Swish-Assignment
The coffee shop that you use often has a service that is limited today.  - When purchasing coffee, the price for the next purchase will be P% off. - Truncation after decimal point in each price reduction  You have noticed that the price cuts are cumulative. If you drink coffee many times, you will be able to drink coffee for free.  You want to drink coffee for free, so you will calculate how many INR you can pay for later.  Let's actually write a program and calculate it.*/
import java.util.*;
import java.io.*;
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        int p = sc.nextInt();
        int sum = x;
        int r; 
        int count;
        r = (x*p)/100;
        count = x - r; 
        sum += count;
        x = count;
        while(count > 1){
            r = (x*p)/100;
            count = x - r; 
            sum += count;
            x = count;
        }
        System.out.println(sum);
    }
}
