# JAVA-Basic-exercise
Java基础学习有关练习
public class P238_17 {
	public static void main(String[] args) {
		String [] m = {"a","b","c"};
		double [] n = {85,92,60};
		Selection(m,n);
	}
	public static void Selection(String [] m,double [] n){
		for(int i = 0;i<n.length-1;i++){
			double max = n[i];
			int maxIndex = i;
			String sMax = m[i];
			int sMaxIndex = i;
			for(int j = i+1;j<n.length;j++){
				if(max<n[j]){
					max = n[j];
					maxIndex = j;
					sMax = m[j];
					sMaxIndex = j;
				}
			}
			if(maxIndex!=i){
				n[maxIndex] = n[i];
				n[i] = max;
				m[sMaxIndex] = m[i];
				m[i] = sMax;
			}
		}
		System.out.println(java.util.Arrays.toString(m)+"  "+java.util.Arrays.toString(n));
	}
