###通过对两个类DVD,CD所拥有的共同属性进行合并，得到父类Item-->主要讨论了继承，向上造型等
####Project名为Dome，Package名为dome，有四个类，名字分别为：Database,CD,DVD,Item


————————————————————Database————————————————————

package dome;

import java.util.ArrayList;

public class Database { 
	// private ArrayList<CD> listCD= new ArrayList<CD>(); 
	// private ArrayList<DVD> listDVD= new ArrayList<DVD>(); 
	private ArrayList<Item> listItem = new ArrayList<Item>();

//	 public void add(CD cd) { 
//		  listCD.add(cd);   
//	 }
//	 
//	 public void add(DVD dvd) { 
//		  listDVD.add(dvd); 
//	 }
	 
	 public void add(Item item) { 
		 listItem.add(item); 
	 }

	 public void list() {
//		  for( CD cd : listCD ) {
//			  cd.print(); 
//		  } 
//		  for( DVD dvd : listDVD ) {
//			   dvd.print(); 
//		  }
		  for( Item item : listItem ) {
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

————————————————————CD————————————————————

package dome;

public class CD extends Item { 
	private String artist; 
	private int numofTracks; 

	public CD(String title, String artist, int numofTracks, int playTime,
        String comment) {
		super(title,playTime,false,comment); 
		this.artist = artist; 
		this.numofTracks = numofTracks; 
//		this.playTime = playTime; 
//		this.comment = comment; 
	}

	public void print() {
    System.out.print("CD: ");
    super.print();
    System.out.println(artist);
	}
}

————————————————————DVD————————————————————

package dome;

public class DVD extends Item { 
	private String director; 
	
	public void print() {
	    System.out.print("DVD: ");
	    super.print();
	    System.out.println(director);
	}

	public DVD(String title, String director, int playTime, String comment) {
	    super(title,playTime,false,comment);
//	    this.title = title;
	    this.director = director;
//	    this.playTime = playTime; 
//		this.comment = comment; 
	}
}

————————————————————Item————————————————————

package dome;

public class Item {
	private String title;
	private int playTime; 
	private boolean gotIt = false; 
	private String comment;
	

	public Item(String title, int playTime, boolean gotIt, String comment) {
		super();
		this.title = title;
		this.playTime = playTime;
		this.gotIt = gotIt;
		this.comment = comment;
	}

	public void print() {
		System.out.print(title);
	}
	

}
