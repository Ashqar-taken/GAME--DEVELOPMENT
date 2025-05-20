# EX 3 : Circle Drawing Algorithm

**AIM :**

To  implement the Bresenham’s  algorithm for circle using a c coding.


**ALGORITHM :**

Step 1 : Start.
    
Step 2 : Initialize the graphics header files and functions.
   
Step 3 : Declare the required variables and functions.
 
Step 4 : Get the co-ordinates and radius of the circle.

Step 5 : Draw the circle using the algorithm.

Step  6 : Display the output.
  
Step 7 : stop.

**Program :**
```
Developed By: Ashqar Ahamed S.T
Register No: 212224240018
```
```
#include <stdio.h>
#include <graphics.h>
#include <math.h>

int plot(int xcenter,int ycenter,int x,int y);
void main()
{
	int i,gm=DETECT,gd;
	int xcenter,ycenter,x,y,r,p;
	
	initgraph(&gm,&gd,"c://turboc3/bgi");
	printf("Enter the center x and y of the circle: ");
	scanf("%d %d",&xcenter,&ycenter);
	printf("Enter the radius of the circle ");
	scanf("%d",&r);
	
	x = 0;
	y =r;
	
	p = 1 -r;
 
	while(x<y)
	{
		if(p<0)
		{	
			x = x+1;
			p = p + 2*x +1;
		}
		else
		{
			x = x+1;
			y = y-1;
			p = p +2*x +1 - 2*y;
		}
	plot(xcenter,ycenter,x,y);
	}
	getch();
	closegraph();
}
int plot(int xcenter, int ycenter,int x,int y)
{
	putpixel(xcenter+x,ycenter+y,1);
	putpixel(xcenter-x,ycenter+y,1);
	putpixel(xcenter+x,ycenter-y,1);
	putpixel(xcenter-x,ycenter-y,1);
	putpixel(xcenter+y,ycenter+x,1);
	putpixel(xcenter-y,ycenter+x,1);
	putpixel(xcenter+y,ycenter-x,1);
	putpixel(xcenter-y,ycenter-x,1);
	return 0;
}
```


**Output :**

![Screenshot 2025-05-20 141346](https://github.com/user-attachments/assets/ff0a1c59-5df5-4a77-97c8-d6dcbae660a9)


**Result :**
The Bresenham's algorithm for drawing a circle is implemented successfully using a C code.
