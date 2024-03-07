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
