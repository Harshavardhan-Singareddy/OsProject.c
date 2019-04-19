#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
int main()
{
	int a,b,c,i;
	int student_id0=2132,student_id1=2102,student_id2=2453;
	int  b0=2,b1=4,b2=8;
	int completion_time[3];
	int turn_around_time[3];
	int waiting_time[3];
    int avg_turn_around_time=0;
    int avg_waiting_time=0;
	int time=0;
	printf("The Students priority is as given below:  \n ");
	printf("Student b is having highest priority  \n");
	printf("Student a is having the next priority after b  \n");
	printf("Student c is having the least priority   \n");
	printf("student c will be processing \n ");
    for(time=0;time<=4; time++ )
    {
    	
    	completion_time[2]=b2-4;
    	
	}
	printf("student b will be processing \n");
	for(time=5;time<=8;time++)
	{
		
		completion_time[1]=b1+completion_time[2];
		turn_around_time[1]=completion_time[1]-0;
		waiting_time[1]=turn_around_time[1]-b1;
		
	}
	for(time=9;time<=10;time++)
	{
		completion_time[2]=completion_time[1]+2;
		
	}
	for(time=11;time<=12;time++)
	{
		completion_time[0]=completion_time[2]+b0;
		turn_around_time[0]=completion_time[0]-0;
    	waiting_time[0]=turn_around_time[0]-b0;
		
	}
    for(time=13;time<=14;time++)
    {
    	completion_time[2]=completion_time[0]+2;
    	turn_around_time[2]=completion_time[2]-0;
    	waiting_time[2]=turn_around_time[2]-b1;
	}
	    printf("  **************Gantt chart************** \n");
	    printf("  __________________________________________\n ");
	    printf(" |   c      |     b    |   c  |   a  |   c  |\n");
	     printf("  |__________|__________|______|______|______|\n");
	    printf("  0         4           8     10     12     14 \n");
	    printf("********************************************\n");
		printf("process \t     burst time            completion time      turn around time          waiting time \n");
	    printf("p0\t\t\t %d \t\t\t %d \t\t\t %d \t\t\t %d \n",b0,completion_time[0],turn_around_time[0],waiting_time[0]);
	    printf("p1\t\t\t %d \t\t\t %d \t\t\t %d \t\t\t %d \n",b1,completion_time[1],turn_around_time[1],waiting_time[1]);
	    printf("p2\t\t\t %d \t\t\t %d \t\t\t %d \t\t\t %d \n",b2,completion_time[2],turn_around_time[2],waiting_time[2]);
	     avg_turn_around_time=(float)(turn_around_time[0]+turn_around_time[1]+turn_around_time[2])/3;
	     avg_waiting_time=(float)(waiting_time[0]+waiting_time[1]+waiting_time[2])/3;
	     printf("*********************************************\n");
	     printf("The average turn around time is :%d \n",avg_turn_around_time);
	     printf("The average waiting time is :%d \n",avg_waiting_time);
	     
}
Chat conve
