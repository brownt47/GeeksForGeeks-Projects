Rahul wanted to purchase vegetables mainly brinjal, carrot and tomato. There are N different vegetable sellers in a line. Each vegetable seller sells all three vegetable items, but at different prices. Rahul, obsessed by his nature to spend optimally, decided not to purchase same vegetable from adjacent shops. Also, Rahul will purchase exactly one type of vegetable item (only 1 kg) from one shop. Rahul wishes to spend minimum money buying vegetables using this strategy. Help Rahul determine the minimum money he will spend.

Input:
First line indicates number of test cases T. Each test case in its first line contains N denoting the number of vegetable sellers in Vegetable Market. Then each of next N lines contains three space separated integers denoting cost of brinjal, carrot and tomato per kg with that particular vegetable seller.

Output:
For each test case, output the minimum cost of shopping taking the mentioned conditions into account in a separate line.

Constraints:
1 <= T <= 10
1 <= N <= 100000
Cost of each vegetable(brinjal/carrot/tomato) per kg does not exceed 10^4

Example
Input:
1
3
1 50 50
50 50 50
1 50 50
Output:
52
Explanation:
There are two ways, each one gives 52 as minimum cost. One way is buy brinjals from first shop, carrots from second shop and brinjals from third shop or he can buy brinjals from first shop, tomatoes from second shop and brinjals from third shop.
Both ways , cost comes up to 1 + 50 + 1 = 52

##Solution:

import java.util.*;
import java.lang.*;
import java.io.*;

class GFG {
    public static long dfs(long mat[][], long arr[][], int i ,int j){
        int n = arr.length;
        if(i==n)
        return 0;
        if(mat[i][j]!=-1)
        return mat[i][j];
        long val1 =1000000000;
        long val2=1000000000;
        long val3 =1000000000;
        if(j!=0)
        val1= dfs(mat,arr,i+1,0);
        if(j!=1)
        val2= dfs(mat,arr,i+1,1);
        if(j!=2)
        val3= dfs(mat,arr,i+1,2);
        mat[i][j]=arr[i][j]+Math.min(val1,Math.min(val2,val3));
        return mat[i][j];
    }
	public static void main (String[] args) {
		//code
		Scanner in = new Scanner(System.in);
		int t = in.nextInt();
		for(int f =0;f<t;f++){
		    int n = in.nextInt();
		   long arr[][]= new long [n][3];
		   long mat[][] = new long [n][3];
		    for(int i =0;i<n;i++)
		     for(int j =0;j<3;j++)
		      {
		          arr[i][j]= in.nextLong();
		          mat[i][j]=-1;
		      }
		  long val1= dfs(mat,arr,0,0);
		  long val2= dfs(mat,arr,0,1);
		  long val3= dfs(mat,arr,0,2);
		  long val4 = Math.min(val1,Math.min(val2,val3));
		  System.out.println(val4);
		}
	}
}
