# Project-Switch

### Naredba SWITCH

Kako bismo zaobišli **neprekidno korištenje** `if..else`, možemo koristiti naredbu SWITCH.
Naredba `SWITCH` odabire jedan od ponuđenih blokova koje će se izvršiti.

Primjer:
```
switch (izraz){
  case 1:
    // blok naredbi 1
    break;
  case 2:
    // blok naredbi 1
    break;
  default:
    // blok naredbi koji se izvrši ako nijedan prije nije izvršen
}
```

Izraz pod `SWITCH` naredbom je ispitan samo jednom.

Ispitana vrijednost je tada uspoređena sa vrijednošću u svakom zadanom slučaju `CASE` Ako postoji podudaranje , blok naredbi povezan sa tim slučajem će se izvesti.

```
int dan=4;
switch(dan){
case 1:
  printf(ponedjeljak);
  break;
case 2:
  printf(utorak);}
  break;
case 3:
  printf(srijeda);}
  break;
case 4:
  printf(cetvrtak);}
  break;
case 5:
  printf(petak);}
  break;
}
//izvrsava se ispis cetvrtak(dan 4)
```

### Naredba DEFAULT

Dopušten je i poseban blok koji ne određuje nijednu vrijednost i koji počinje ključnom riječju **default** umjesto ključnom riječju **case**.

Ako je blok **default** prisutan i ako nijedna od **case** naredbi unutar **switch** petlje nije izvršena, tada se izvršava naredba koja slijedi nakon ključne riječi **default**.

Primjer:
```
switch(izraz){
  case 1:
      printf("Broj je pozitivan.");
      break; //Ukoliko je broj pozitivan izvršiti će se naredba pod ovim slučajem
  case 2:
      printf("Broj je negativan.");
      break; //Ukoliko je broj negativan izvršiti će se naredba pod ovim slučajem
  default;
      printf("Broj je nula.");
      //Ukoliko broj nije ni pozitivan ni negativan izvršiti će se naredba nakon default
}
```

//Uvesti još nešto prije "Moguće izvedbe naredbe switch" (obrisati komentar nakon unosa)
### Moguće izvedbe naredbe switch
  Naredba koja omogućuje izbor ispisa između niza radnji. Možemo je koristit u "raznim" oblicima.
  
Kao na primjer:
A) Naredba switch koja ide u beskonačnost (loop)
```
int a;
scanf("%d", &a);
switch (a){
  case 1: printf("Ovo");
  case 2: printf("ide");
  case 3: printf("u");
  case 4: printf("beskonačnost");
  case 5: printf("!!");
}
```
B) Naredba switch sa ispisom niza i krajnjim izvodom (naredba default)
```
int a;
scanf("%d", &a);
switch (a){
  case 1: printf("1");
  case 2: printf("2");
  case 3: printf("3");
  case 4: printf("4");
  case 5: printf("5");
  default:
printf("Zna brojati do 5.");
}
```
C) Naredba switch sa prekidima (naredba break)
```
int a;
scanf("%d", &a);
switch (a){
  case 1: printf("1");
  break;
  case 2: printf("2");
  break;
  case 3: printf("3");
  break;
  case 4: printf("4");
  break;
  case 5: printf("5");
  break;
}
```
D) Naredba switch sa pojedinim ispisom iz niza
```
int a;
scanf("%d", &a);
switch (a){
  case 1: printf("1");
  break;
  case 2: printf("2");
  break;
  case 3: printf("3");
  break;
  case 4: printf("4");
  break;
  case 5: printf("5");
  break;
  default:
printf("Probaj manji broj.");
}
```
### Alternativni načini korištenja

Alternativni načini za postizanje sličnog efekta kao **switch** naredba uključuje upotrebu **if-else** naredbi ili čak tablice pokazivača na funkcije za složenije slučajeve.
Primjer:
```
int broj = 2;
if (broj == 1) {
  // Kod ako je broj 1
} else if (broj == 2) {
  // Kod ako je broj 2
} else if (broj == 3) {
    // Kod ako je broj 3
} else {
    // Kod za sve ostale slučajeve
}
```
Korištenje tablice pokazivača na funkcije:
```
#include <stdio.h>

void slucaj_1() {
    printf("Slucaj 1\n");
}

void slucaj_2() {
    printf("Slucaj 2\n");
}

void slucaj_3() {
    printf("Slucaj 3\n");
}

int main() {
    int broj = 2;
    void (*pokazivac_na_funkciju)() = NULL;
    
    // Inicijalizacija tablice pokazivača na funkcije
    void (*tablica[3])() = {slucaj_1, slucaj_2, slucaj_3};
    
    if (broj >= 1 && broj <= 3) {
        pokazivac_na_funkciju = tablica[broj - 1];
        pokazivac_na_funkciju();
    } else {
        printf("Nepoznat slucaj\n");
    }
    
    return 0;
}
```
Ovaj primjer radi slično kao i **switch** naredba. Međutim, **switch** naredba je često čišća i može biti efikasnija za čitanje i pisanje koda kada imamo više uslova koje testiramo na istoj varijabli.






