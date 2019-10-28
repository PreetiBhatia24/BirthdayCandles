# BirthdayCandles
Count  the max height of Birthday Candles in Java

import java.util.*;

public class Solution {

    static int birthdayCakeCandles(int[] ar) {
         int temp =0;
            int max = ar[0];
            for(int j=1;j<ar.length;j++)
            {
                if(ar[j]>=max)
                {
                    max = ar[j];
                }
                
            }
            for(int i=0;i<ar.length;i++)
            {
                if(ar[i]==max)
                {
                    temp++;
                }
            }
            return temp;
        
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arCount = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int[] ar = new int[arCount];

        String[] arItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < arCount; i++) {
            int arItem = Integer.parseInt(arItems[i]);
            ar[i] = arItem;
        }

        int result = birthdayCakeCandles(ar);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedWriter.close();

        scanner.close();
    }
}

