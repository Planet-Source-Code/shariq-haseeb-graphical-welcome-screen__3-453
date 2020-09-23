<div align="center">

## GRAPHICAL WELCOME SCREEN


</div>

### Description

GRAPHICAL WELCOME FOR ANY PROGRAM OR PROGRAMMER,

WHO WANT'S TO IMPRESS HIS USER, MAY IT BE A CLASS

PROJECT OR A PROFESSONAL PRESENTATION.
 
### More Info
 
NONE AL ALL

A BAR AROUNT THE SEREEN, WITH A RED BACKGROUND, WITH SOUND

A WELC ME, THAT BECOMES THICKER.

THEN THE 'O' STARTS TO APPEAR FROM A DOT.

TWO CIRCLES RACE ACROSS THE SCREEN

NONE


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[SHARIQ HASEEB](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/shariq-haseeb.md)
**Level**          |Advanced
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |C
**Category**       |[Graphics/ Sound](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics-sound__3-15.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/shariq-haseeb-graphical-welcome-screen__3-453/archive/master.zip)





### Source Code

```
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#include<dos.h>
#include<graphics.h>
   /*Declaration of Functions*/
   /*************************/
	 void draw_bar(void);
	 void draw_bar3d(void);
	 void draw_line(void);
	 void draw_pieslice(void);
   /**************************/
  void main(void)
 {
	  int k,i;
  /* request auto detection */
	int gdriver = DETECT, gmode, errorcode;
   /* initialize graphics mode */
  initgraph(&gdriver, &gmode, "");
 /*  Color Setup   */
 /* -------------------*/
   setbkcolor(RED);
   setcolor(GREEN);
 /*  Call To Functions 0 */
 /************************/
   draw_bar();
   draw_line();
   draw_bar3d();
   draw_pieslice();
 /***********************/
	  getch();
 /*Ends All Graphic Jobs*/
    closegraph();
}
/*Function Employed in Drawing a Bars*/
  /*********************************************/
    void draw_bar(void)
 {
	  int i;
	  setfillstyle(CLOSE_DOT_FILL,YELLOW);
	  for(i=0;i<=640;i+=10)
   {
	  bar(0,0,i,50);
	   delay(3);
		sound(200+i);
	  delay(100);
	   nosound();
    }
	    for(i=50;i<=480;i+=10)
	  {
		  bar(590,50,640,i);
		   delay(50);
			sound(400+i);
		    delay(100);
			 nosound();
	  }
	 for(i=590;i>=0;i-=10)
   {
		 bar(590,430,i,480);
		  delay(50);
		   sound(600+i);
			delay(100);
			 nosound();
   }
		 for(i=430;i>=50;i-=10)
	  {
		  bar(0,430,50,i);
		   delay(50);
		    sound(800+i);
			 delay(100);
			  nosound();
	  }
	   for(i=70;i<=140;i+=10)
   {
		setfillstyle(SOLID_FILL,GREEN);
		  bar(430,70,440,140);
		   delay(100);
			sound(1000+i);
			  delay(100);
			   nosound();
   }
		 for(i=70;i<=140;i+=10)
	   {
			 bar(460,70,470,140);
			  delay(100);
			   sound(1000+i);
			    delay(100);
			  nosound();
	   }
 }
/*Function Employed in Drawing Lines*/
  /*********************************************/
   void draw_line(void)
 {
	  setfillstyle(CLOSE_DOT_FILL,YELLOW);
			 int i;
	    for(i=70;i<=140;i+=10)
    {
		 line(70,70,80,i);
		  delay(50);
		   sound(1000+i);
		    delay(100);
		  nosound();
    }
		    for(i=140;i>=90;i-=10)
		{
			   line(80,140,100,i);
				delay(50);
				 sound(1000+i);
				  delay(100);
				    nosound();
		}
	  for(i=90;i<=140;i+=10)
    {
		 line(100,90,120,i);
		   delay(50);
		    sound(1000+i);
			 delay(100);
			  nosound();
    }
		   for(i=140;i>=70;i-=10)
	   {
			  line(120,140,130,i);
			   delay(50);
				 sound(1000+i);
			   delay(100);
				 nosound();
	   }
	 for(i=70;i<=105;i+=5)
   {
	  line(440,70,450,i);
	    delay(50);
		 sound(1000+i);
	    delay(100);
		 nosound();
    }
		  for(i=105;i>=70;i-=5)
	  {
			 line(450,105,460,i);
			  delay(50);
			   sound(1000+i);
			  delay(100);
			   nosound();
	   }
 }
 /*Function Employed in Drawing a Three Dimensional Bars*/
  /*********************************************/
	 void draw_bar3d(void)
  {
	  int i;
	  setfillstyle(CLOSE_DOT_FILL, YELLOW);
		 for(i=0;i<=5;i++)
	 {
			bar3d(150,70,170,140,5,3);
			 delay(100);
			   bar3d(170,70,200,90,5,3);
			    delay(100);
			 bar3d(170,95,190,115,5,3);
			  delay(100);
			   bar3d(170,120,200,140,5,3);
				delay(100);
			  sound(1000+i);
			   delay(100);
				nosound();
			  bar3d(220,70,240,140,i,3);
			   delay(100);
				bar3d(240,120,280,140,i,3);
				 delay(100);
			  bar3d(300,70,320,140,i,2);
			   delay(100);
			  bar3d(320,70,350,90,i,3);
			   delay(100);
			  bar3d(320,120,350,140,i,2);
			   delay(100);
			  bar3d(480,70,500,140,i,3);
			   delay(100);
			  bar3d(500,70,530,90,i,2);
			   delay(100);
			  bar3d(500,95,520,115,i,2);
			   delay(100);
			  bar3d(500,120,530,140,i,2);
			   delay(100);
	 }
  }
/*******************************************************/
	/*Function Employed in Drawing a Pieslices*/
  /*********************************************/
   void draw_pieslice(void)
  {
	int i;
	setfillstyle(CLOSE_DOT_FILL,YELLOW);
	    for(i=5;i<=30;i++)
		 {
			pieslice(390,105,0,360,i);
			  delay(100);
			   setfillstyle(EMPTY_FILL,YELLOW);
			 pieslice(390,105,0,360,15);
			  sound(1000+i);
			    delay(100);
				 nosound();
		  }
	  for(i=40;i<=480;i+=40)
	{
		 setfillstyle(CLOSE_DOT_FILL,CYAN);
		    pieslice(60+i,240,0,360,40);
			 delay(100);
			  setfillstyle(CLOSE_DOT_FILL,LIGHTGREEN);
		    pieslice(60+i,320,0,360,40);
			 delay(100);
			  sound(1000+i);
			   delay(100);
			    nosound();
	}
  }
/*!!!!!!!!!!!!!!!!!!!!!!!!!!PROGRAM ENDS HERE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!*/
```

