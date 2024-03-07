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
