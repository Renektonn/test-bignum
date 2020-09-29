class Main {
  static String longAdd(String a , String b){
    char [] cha =new char[201];
    for(int i=a.length()-1 ; i>=0 ; i--){
      cha[a.length()-i] += a.charAt(i);
    }
    for(int i=b.length()-1 ; i>=0 ; i--){
      cha[b.length()-i] += b.charAt(i);
    }
    for(int i=1 ; i<=199 ; i++){
      if(cha[i]>=10){
        cha[i+1]++;
        cha[i]-=10;
      }
    }
    char [] reCha = new char[201];
    for(int i=200;i>0;i--){
      if(cha[i]!='0'){
        int start=0;
        while(i>0){
          
          reCha[start]=cha[i];
          start++;
          i--;
        }
      } 
    }
    String str=String.valueOf(reCha);

    
    return str;
  }
  
  //static String DP(String n,String [] f){
    //if(f[n]!=-1) return f[n];
    //else
      //if(n.equal("0")) {
        //f[n]="0";
        //return "0";
      //}
      //else
        //if(n==1 || n==2) {
          //f[n]=1;
          //return "1";
        //}
        //else{
          //f[n]=DP(n-1,f)+DP(n-2,f);
          //return DP(n-1,f)+DP(n-2,f);
        //}
  //}
  
  public static void main(String[] args) {
    String [] f =new String [201];
    for(int i=1;i<=200;i++){
      //f[i]=-1;
    }
    System.out.println(longAdd("123","123"));
    //System.out.println(DP(152,f));
    //int [] DP={0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144};
  }
}
