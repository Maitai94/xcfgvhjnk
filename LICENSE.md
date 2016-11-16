

int LEDRED = 7;
int LEDGREEN = 8;
int LEDBLUE = 9;


void setup()
{

pinMode (LEDRED, OUTPUT);
pinMode (LEDGREEN, OUTPUT);
pinMode (LEDBLUE, OUTPUT);
pinMode (53, INPUT);
Serial.begin(9600);  
}

void loop ()
{
for ( int r=0; r <= 255; r=r+5)
{
 Serial.println("erste for: ");
  Serial.println(r);
 analogWrite (LEDRED,r);
 analogWrite (LEDGREEN,255-r);
  delay(10);
}
for ( int r=0; r <= 255; r=r+5)
{
 Serial.println("zweite for: ");
  Serial.println(r);
 analogWrite (LEDBLUE,r);
 analogWrite (LEDGREEN,46+(r*0,8) );
  delay(10);
}
for ( int r=0; r <= 255; r=r+5)
{
 Serial.println("dritte for: ");
  Serial.println(r);
 analogWrite (LEDRED,155);
 analogWrite (LEDGREEN,r);
  delay(10);
}
}

