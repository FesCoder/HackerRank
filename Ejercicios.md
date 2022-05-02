# Ejercicios prácticos de HackerRank
Primer ejercicio:

~~~
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int t=in.nextInt();
        for(int i=0;i<t;i++){
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();

            // Mi codigo
            int[] resultado = new int[n];
            StringBuilder res = new StringBuilder();
            for(int j=0;j<n;j++){
                resultado[j] = a;
                for (int k = 0; k < j+1; k++) {
                    resultado[j]+= Math.pow(2,k)*b;
                }
                res.append(String.valueOf(resultado[j])).append(" ");
            }
            System.out.println(res);
        }
        in.close();
    }
}
~~~
// a + 2^0*b
// a + 2^0*b + 2^1*b
// a + 2^0*b + 2^1*b + 2^2*b
// a + 2^0*b + 2^1*b + 2^2*b + 2^3*b

Link enlace de format number 
https://javiergarciaescobedo.es/programacion-en-java/29-trucos/113-formato-de-numeros-monedas-y-porcentajes2#:~:text=La%20clase%20NumberFormat%20de%20Java,de%20moneda%20o%20valores%20porcentuales.