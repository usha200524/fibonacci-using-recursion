import java.util.Arrays;
public class Main {
    static int fib(int n,int[] memo){
        if(memo[n]!=-1){
            return memo[n];
        }
        if(n<=1){
            memo[n]=n;
        }
        else{
            memo[n]=fib(n-1,memo)+fib(n-2,memo);
        }
        return memo[n];
    }
    public static void main(String[] args) {
        int n=5;
        int[] memo=new int[n+1];
        for(int i=0;i<=n;i++){
            memo[i]=-1;
        }
        int x=fib(n,memo);
        System.out.println(x);
        
       
    }
}
