###第四周java内容store
————————————database的内容——————————————

package dome;

import java.util.ArrayList;

public class Database {
//	private ArrayList<CD> listCD = new ArrayList<CD>();
//	private ArrayList<DVD> listDVD = new ArrayList<DVD>();
	private ArrayList<Item> listItem = new ArrayList<Item>();
	
//	public void add(CD cd) {
//		listCD.add(cd);
//	}
//	
//	public void add(DVD dvd) {
//		listDVD.add(dvd);
//	}
	public void add(Item item) {
		listItem.add(item);
	}
	
	public void list() {
//		for( CD cd : listCD )
//		{
//			cd.print();
//		}
//		for( DVD dvd : listDVD )
//		{
//			dvd.print();
//		}
		for( Item item : listItem )
		{
			item.print();
		}
	}
	
	public static void main(String[] args) {
		Database db = new Database();
		db.add(new CD("abc","abc",4,10,"good"));
		db.add(new CD("def","def",4,10,"good"));
		db.add(new DVD("xxx","aaa",60,"nice"));
		db.list();
	}

}



————————————CD的内容——————————————

package dome;

public class CD extends Item {
	private String title;
	private String artist;
	private int numofTracks;
	private int playTime;
	private boolean gotIt = false;
	private String comment;
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

	public CD(String title, String artist, int numofTracks, int playTime,
			String comment) {
//		super();
		this.title = title;
		this.artist = artist;
		this.numofTracks = numofTracks;
		this.playTime = playTime;
		this.comment = comment;
	}

	public void print() {
		// TODO Auto-generated method stub
		System.out.println("CD: "+title+":"+artist);
	}

}


————————————DVD的内容——————————————

package dome;

public class DVD extends Item {
	private String title;
	private String director;
	private int playTime;
	private boolean gotIt = false;
	private String comment;
	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}
	public void print() {
		// TODO Auto-generated method stub
		System.out.println("DVD: "+title+":"+director);
	}
	
	public DVD(String title, String director, int playTime, String comment) {
		super();
		this.title = title;
		this.director = director;
		this.playTime = playTime;
		this.comment = comment;
	}

}



————————————Item的内容——————————————

package dome;

public class Item {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

	public void print() {
		
	}

}

