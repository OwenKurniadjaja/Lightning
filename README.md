int startX = 0;
int startY = 150;
int endX = 0;
int endY = 150;
int counter = 0;

void setup()
{
  size(300,300);
  background(0);
  strokeWeight(5);
}
void draw()
{
stroke((int)(Math.random()*260),(int)(Math.random()*260),(int)(Math.random()*260));
while(endX < 300)
{
  endY = startX +(int)(Math.random()+10);
  endX = startY +(int)(Math.random()*19)-9;
  line(startX,startY,endX,endY);
  startX = endX;
  startY = endY;
}
}
void mousePressed()
{
startX = (int)(Math.random()*256);
startY = (int)(Math.random()*256);
endX = 0;
endY = 50;
counter = counter + 1;
if (counter > 5){
  background(0);
  counter = 0;
}
}
