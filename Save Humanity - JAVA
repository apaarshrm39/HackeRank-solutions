import java.io.*;
import java.math.*;
import java.text.*;
import java.util.*;
import java.util.regex.*;

public class Solution {

    /*
     * Complete the virusIndices function below.
     */
    static void virusIndices(String p, String v) {
         String output = "";
        
        int i;
        int k;
        boolean hasMatch;
 
        hasMatch = false;
        
        int N_Diff;
        
        
        int p_length = p.length();
        int v_length = v.length();
        
        for (i=0; i<=p_length - v_length;i++)
        {
            N_Diff = 0;
            
            for (k = i; k <= i + v_length - 1; k++)
            {
                if (p.charAt(k) != v.charAt(k-i))
                {
                    N_Diff++;
                
                    if (N_Diff >= 2)
                        break;
                }
            }
            
            if (N_Diff < 2)
            {
                output = output.concat(i+ " ");
                hasMatch = true;
            }

        }
      
        if (!hasMatch)
            output = "No Match!";
        
        System.out.println(output);
        return;
        
    
    }

    private static final Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        int t = Integer.parseInt(scanner.nextLine().trim());

        for (int tItr = 0; tItr < t; tItr++) {
            String[] pv = scanner.nextLine().split(" ");

            String p = pv[0];

            String v = pv[1];

            virusIndices(p, v);
        }
    }
}
