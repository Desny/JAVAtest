###使用HashMap来代替switch-case
package Coin;

import java.util.HashMap;
import java.util.Scanner;

public class CoinName {
	private HashMap<Integer, String> coinnames = new HashMap<Integer, String>();
	
	public CoinName() {
		coinnames.put(1, "penny");
		coinnames.put(10, "dime");
		coinnames.put(25, "quarter");
		coinnames.put(50, "half-dollar");
		System.out.println(coinnames.keySet().size());
		System.out.println(coinnames);		//第一种输出形式
		
		for( Integer k:coinnames.keySet() )    //第二种输出形式
		{
			String s = coinnames.get(k);
			System.out.println(s);
		}
	}
	public String getName( int amount ) {
		return coinnames.get(amount);
	}

	public static void main(String[] args) {
		Scanner in = new Scanner(System.in);
		int amount = in.nextInt();
		CoinName coin = new CoinName();
		String name = coin.getName(amount);
		System.out.println(name);
	}
}
