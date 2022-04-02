# Write-a-program-that-allows-input-of-an-integer-n-n-1000-
Write a program that allows input of an integer n ( n &lt; 1000 )
import java.util.Scanner;

public class BaiTapJavaCoBan8 {
   public static void main(String[] args)
   {
      int n;
      boolean soNguyenTo = false;
      System.out.println("Enter Integer:");
      Scanner sc = new Scanner(System.in);

      n = sc.nextInt();

      // 1, 2 are 2 default prime numbers, no need to consider.
      System.out.print("1 2 ");
      for (int i = 3; i <= n; i++) // iterate all elements from 1-20
      {
         /**
          * Assign to soNguyenTo true
          * If after exiting the loop j
          * if it is still true then the number is prime
          */
         soNguyenTo = true;
         for (int j = 2; j < i; j++)
         {
            if (i % j == 0)
               /**
                * Assign to soNguyenTo false
                * when it is divisible by any number less than
                * it's between 3 - n
                */
               soNguyenTo = false;
         }
         if (soNguyenTo == true)
            System.out.print(i + " ");
      }
   }
}
