# lightning
int x = (float)(Math.random()*400);
int y = 0;

void setup() {
  size(500, 400);
  background(10,0,10);
}

public void drawLightning() {

  int a = (float)((Math.random()*20)+ x-7);
  int b = (float)((Math.random()*25)+ y);
  int sw = (float)((Math.random()*3)+3);
  
  strokeWeight(sw+15);
  stroke(255,180,255,5);
  line(x,y,a,b);

  stroke(228,180,255,80);
  strokeWeight(sw);
  line(x,y,a,b);

  strokeWeight(sw-2);
  stroke(255,180,255,100);
  line(x,y,a,b);

  x = a;
  y = b;

    if(y>=2000){
    x = (float)(Math.random()*400);
    y = 0;
    a = (float)((Math.random()*20)+ x-7);
    b = (float)((Math.random()*25)+ y);
    sw = (float)((Math.random()*3)+3);
    }

}


void draw() {

fill(10,0,10,10);
rect(0,0,500,400);

drawLightning();


  noStroke();
  fill(20,9,15,85);
  ellipse(30,20,230,180);
  ellipse(125,55,160,150);
  ellipse(75,100,70,40);
  ellipse(200,50,150,110);

  ellipse(310,30,180,170);  
  ellipse(380,40,130,110);
  ellipse(460,55,140,120);


  fill(25,9,20,90);
  ellipse(30,20,220,170);
  ellipse(125,55,150,140);
  ellipse(75,100,60,30);
  ellipse(200,50,140,100);
  
  ellipse(310,30,170,160);
  ellipse(380,40,120,100);
  ellipse(460,55,130,110);

}
