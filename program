//java 7
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

public class Solution {

    // Complete the breakingRecords function below.
    static int[] breakingRecords(int[] scores) {
        int [] d=new int[2];
        int high=0,k,low=0;
        List <Integer>dd=new ArrayList<>();
        for(int i=0;i<scores.length;i++)
        {
            dd.add(scores[i]);
        }
        int length=dd.size();
        for(int j=0;j<length;j++)
        {
            for(k=0;k<length;k++)
            {
                if(j!=k)
                {
                 if(dd.get(j)<dd.get(k))
                 {
                    high++;
                    break;
                 }
                }
            }
            j=k-1;
        }
        for(int j=0;j<length;j++)
            {
            for(k=0;k<length;k++)
            {
                if(j!=k)
                {
                 if(dd.get(j)>dd.get(k))
                 {
                    low++;
                    break;
                 }
                }
            }
            j=k-1;
        }
        d[0]=high;
        d[1]=low;
        return d;


    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) throws IOException {
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int n = scanner.nextInt();
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        int[] scores = new int[n];

        String[] scoresItems = scanner.nextLine().split(" ");
        scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");

        for (int i = 0; i < n; i++) {
            int scoresItem = Integer.parseInt(scoresItems[i]);
            scores[i] = scoresItem;
        }

        int[] result = breakingRecords(scores);

        for (int i = 0; i < result.length; i++) {
            bufferedWriter.write(String.valueOf(result[i]));

            if (i != result.length - 1) {
                bufferedWriter.write(" ");
            }
        }

        bufferedWriter.newLine();

        bufferedWriter.close();

        scanner.close();
    }
}
