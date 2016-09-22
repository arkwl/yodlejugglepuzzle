package yodlejuggler;

import java.io.File;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class CircuitParser {

	private ArrayList<Circuit> circuits;
	private Scanner in;
	private int count;
	
	public CircuitParser(String filename) throws IOException{
		circuits = new ArrayList<Circuit>();
		count = 0;
		in = new Scanner(new File(filename));
		while (in.hasNext()) {
		    String line = in.nextLine();
		    //if the line starts with J
		    if(line.length() > 0){
		    	if((line.substring(0,1)).equals("C")){
		    		String[] parts = line.split("\\s+");
		    		
		    		int h_cir = Integer.parseInt((parts[2].substring(2)));
		    		int e_cir = Integer.parseInt((parts[3].substring(2)));
		    		int p_cir = Integer.parseInt((parts[4].substring(2)));
		    		
		    		circuits.add(new Circuit(h_cir, e_cir, p_cir));
		    	}
		    }
		}
		in.close();
	}
	
	int getCount(){
		return count;
	}
	
	ArrayList<Circuit> getCircuits(){
		if (circuits.size() != 0){
			return circuits;
		}
		else{
			return null;
		}
		
	}
}
