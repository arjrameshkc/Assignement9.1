# Assignement9.1
package collectionsdemos;

public class Hdtv implements Comparable <Hdtv>{

	 String brandName;
	 int size;
	public Hdtv(String brandName, int size) {
		super();
		this.brandName = brandName;
		this.size = size;
	}
	@Override
	public String toString() {
		return "Hdtv [brandName=" + brandName + ", size=" + size + "]";
	}
	@Override
	public int compareTo(Hdtv o) {
		// TODO Auto-generated method stub
		return this.size - o.size;
	}
	
}
package collectionsdemos;
import java.util.*;

public class Arraylist {
	String brandName;
	int size;
	public static void main(String[] args) {	
	

	Hdtv objOne =  new Hdtv("DISH TV",20);
	Hdtv objTwo =  new Hdtv("TATA SKY",25);
	Hdtv objThree =  new Hdtv("SUN",30);
	
	ArrayList<Hdtv> hashSet = new ArrayList<Hdtv>();
	
	hashSet.add(objOne);
	hashSet.add(objTwo);
	hashSet.add(objThree);

	System.out.println(hashSet);
	System.out.println("*************************************************************");
	
	ListIterator<Hdtv> iterator = hashSet.listIterator();
	
	while(iterator.hasNext()){
		Hdtv str = (Hdtv) iterator.next();
		System.out.println(str);
	}
		
}
}
