Izraz pod SWITCH naredbom je ispitan samo jednom.

Ispitana vrijednost je tada uspoređena sa vrijednošću u svakom zadanom slučaju CASE
Ako postoji podudaranje , blok naredbi povezan sa tim slučajem će se izvesti.
int main(void){
int dan=4;
switch (dan){
  case 1:
   printf("ponedjaljak");
    break;
  case 2:
    printf("utorak");
    break;
case 3:
    printf("srijeda");
case 4:
    printf("cetvrtak");
}
// izvrsava se ispis cetvrtak
return 0;}
