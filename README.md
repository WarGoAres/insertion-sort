# insertion-sort
insertion  sort

#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#define number 100000




void insertionsort(int data[],int len){//insertion sort  algorithm
	
	int i;
	int j;
	int key;
	
	for(i=0;i<len;i++){
		
		j=i;
		key=data[i];
		
		
		while(j>0 && data[j-1]>key){
			
			data[j]=data[j-1];
			j--;
			
		}	
		data[j]=key;	
	}		
		//0.000077  sec
}		
		


int main(void ) {
	
	  
    double start,end;
    
    
    
    start = clock();  
      
    int i;  	
	int data[16]={1,7,6,8,7,4,5,9,78,42,13,14,15,16,77,99};//order(n*n)
	int len = sizeof(data) / sizeof(data[0]);
    
    insertionsort(data,len); 
    
    for(int i = 0; i < len; ++i) {
     
	 	
     printf("%d\n",data[i] )	;
    	
	}
	
   
  
    
     
    end = clock();  
  

    double diff = end - start; // ms 
    printf(" %f  ms" , diff);
    printf(" %f  sec", diff / CLOCKS_PER_SEC );
  



    
	
    return 0; 
    
}    
    
    
    
   
     
    
	


