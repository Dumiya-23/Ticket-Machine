#include<stdio.h>

	int i,j,x,y,z,a,b,c,d;
	char A[3][25]={"Starting station","Stopping station","\tDistances"};
	int B[21][3]={{1,2,15},{1,3,40},{1,4,55},{1,5,65},{1,6,85},{1,7,103},{2,3,25},{2,4,40},{2,5,50},{2,6,70},{2,7,88},{3,4,15},{3,5,25},{3,6,45},{3,7,63},{4,5,10},{4,6,30},{4,7,48},{5,6,20},{5,7,38},{6,7,18}};
	char C[7][25]={"Kurunagala","Narammala","Giriulla","Meerigama","Dulapitiya","Ja-ela","Colombo"};

void main(){

	printf("\n\t***** Rathna Express *****\n");
	printf("\n\n\tPlease Enter Your Choice\n\n");
	printf("\t1 :- Search for distance\n");
	printf("\t2 :- Issue a ticket\n\n");
	printf("\tSelect Your Choice  -  ");
	scanf("%d",&b);
	
	switch(b){
		
	case 1:
		destinations();
		table();
	
	
	
	case 2:
		destinations();
		data();
		ticket();
		select();
	break;  
	   	
	}
	
	}
	 
	 
	//table about distances
int table(){
	
	printf("\n\n\t~~~~~~ Distances ~~~~~~\n\n\n");
	for(i=0;i<3;i++){
		printf("  %3s\t",A[i]);
		
}
   printf("\n\n");
	for(i=0;i<21;i++){
	for(j=0;j<3;j++){
		printf("\t%3d\t\t",B[i][j]);
	}
    printf("\n");	
}
} 
	 
		 
	 
//destinations
 int destinations(){
     printf("\n\n\n\tDestinations\t:\n\n");
     for(i=0;i<7;i++){
     printf("\t %d  -  %s \n",i+1,C[i]);
}
}




//input information
int data(){

	printf("\n\n\n\tStarting station\t -  ");
	scanf("%d",&x);
	printf("\tDestination\t\t -  ");
	scanf("%d",&y);
	printf("\tNumber of passengers\t -  ");
	scanf("%d",&z);
	
}


//issue a ticket
int ticket(){
    printf("\n\n\n       =========================");
    printf("\n\t\t TICKET");
    printf("\n       =========================");
    printf("\n\n");
   
    printf("\n\t\tKurunegala");
    printf("\n    BN:NA-4221 Normal CN:GP-78 RT#:50");
    printf("\n\t    Ref: 654568254785");
    printf("\n\t D: 02-05-21   \t T: 07:45:36\n");
    printf("\t\tROUTE :05");
    printf("\n\t    Kurunegala-Colombo\n\n");
   	
 
}
 
 
 //calculation
 int select(){
 	int e=7;  // fare for 1km
 	for(i=0;i<21;i++){
 		for(j=0;j<2;j++){
 			if(x==B[i][j]){
 				c=1;
 		         for(d=0;d<2;d++){
 			if(y==B[i][d]){
 				a=1;
 				printf("\n\n\t  %s - %s",C[x-1],C[y-1]);
 				printf("\n\t    (Journey - %d KM)",B[i][2]);
   	printf("\n\t  FULL : %.f * Rs.%.2f ",(float)z,(float)e*B[i][2]);
   	printf("\n\t     TOTAL = Rs.%.2f ",(float)z*e*B[i][2]);
 				
			 }
			 else{
			 	a=0;
			 }
			 
			 }
 			
			 } 
			 else{
			 	c=0;
			 }
 		}	
	 } printf("\n\n\tDepot Hotline : 0372247621");
    printf("\n\n      ____________________");
 }
