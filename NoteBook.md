###模拟一个笔记本，运用了泛型类ArrayList和集合Set

package notebook;

import java.util.ArrayList;
import java.util.HashSet;

class Value {
	private int i;
	public void set(int i) {
		this.i = i;
	}
	public int get() {
		return i;
	}
	public String toString() {
		return "" + i;
	}
}

public class NoteBook {
	private ArrayList<String> notes = new ArrayList<String>();
	
	public void add(String s) {
		notes.add(s);		//ArrayList里本来就有一个用于添加的函数add()
	}
	
	public void add(String s, int location) {		//在location这个位置前添加字符串s，就相当于新的字符串替换了i的位置
		notes.add(location, s);
	}
	
	public int getSize() {
		return notes.size();
	}
	
	public String getNote(int index) {
		return notes.get(index);
	}
	
	public void removeNote(int index) {
		notes.remove(index);
	}
	
	public String[] list() {
		String[] a = new String[notes.size()];
//		for(int i=0; i<notes.size(); i++)
//		{
//			a[i] = notes.get(i);
//		}
		notes.toArray(a);
		return a;
	}
	
	public static void main(String[] args) {
		Value v = new Value();
		v.set(10);
		System.out.println("v="+v);
		
		System.out.println("---------------");
		
		NoteBook nb = new NoteBook();
		nb.add("first");
		nb.add("second");
		nb.add("first");
		String[] a = nb.list();
		for( String s:a )
		{
			System.out.println(s);
		}
		
		System.out.println("---------------");
		
		HashSet<String> s = new HashSet<String>();
		s.add("first");
		s.add("second");
		s.add("first");
		for( String k:s )
		{
			System.out.println(k);
		}
	}

}

