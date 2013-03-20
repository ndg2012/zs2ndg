zs2ndg
======

Przykladowy projekt publiczny.
Początek pracy z GitHub-em.
Wklejaj akapity, obrazki, linki czy też kawałki kodu...
GitHub nie korzysta z HTML (zbyt skomplikowane kodowanie) - Grubber wprowadził MarkDown (opis strony język prostym językiem).

# Przykładowy tytuł
znak '#' oznacza nagłówek pierwszego rzędu

Przykładowy link: [Wirtualna](http://wp.pl)

Przykladowy obrazek:  ![Kotek](http://c.wrzuta.pl/wi10415/cf984b07001ff42c4a4cba50/kotek)

składnia: nawiasy[Opis_tekst] nawiasy(link_do_)

patrz na dole strony-dokumentation: (link)
http://github.github.com/github-flavored-markdown/

Scieżka lokalna: link rozpoczyna się od slasha[sciezka_lokalna](/dodany_drugi_plik)

Jak wpisywać obrazki?

```markdown
[odwrotne apostrofy pod tyldą]
![tytuł-tekst](link)
```


#Przykład w C++

```c
int main(){
   return 0 
}
```

Teraz inny przykład

#Przykład w Pascalu

```pas
Program Pasek;
 
 Uses Crt;
 
 Var                        //deklaracja zmiennych
   i, j, k :Byte;
    
begin
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Write('Nic nie robię');
   Readln;                  //czekam na naciśnięcie klawisza ENTER
end.                        // end z kropką kończy program
```
-
-
-
-
-
... dla tych, którzy jednak chca cos robic......
-
-
-
-




Metodyka Top-Down Design
========================
Metodyka Top-Down Design polega na konstruowaniu programu "od góry" (TOP) do dolu (DOWN)
czyli od ogólu do szczególu...
- 
## Przykład: Top-Down (T-D...) w Pascalu

```pas
PROGRAM Top_Down_1;          // przykad zastosowania metodyki Top-Down
 
 Uses Crt;
 
 Var                        //deklaracja zmiennych
   i, j, k :Byte;
    
BEGIN                       // Top_Down_1 
   InformacjaCoRobiProgram;
   CzytajDane;
   Oblicz;
   DrukujWynik;
   Poczekaj;
END.                        // end z kropką kończy program Top_Down
```
-

###Niestety, taki program nie zadziala.
###Trzeba poinformować kompilator, co oznaczaja instrukcje pomiedzy BEGIN i END.
###tzn.: trzeba tylko napisać, że nazwy miedzy BEGIN i END to nazwy procedur:
- 
## Przykład: Top-Down (T-D...) w Pascalu ...cd:

```pas
PROGRAM Top_Down_1;          // przykad zastosowania metodyki Top-Down
 
 Uses Crt;
 
 Var                        //deklaracja zmiennych
   i, j, k :Byte;
    
   Procedure InformacjaCoRobiProgram;
      begin     //nawiasy instrukcyjne begin-end; to wymóg formalny definicji procedury
      end;      // miedzy nimi umieszczamy kolejne instrukcje wykonywane po wywolaniu procedury

   Procedure CzytajDane;
      begin
      end;

   Procedure Oblicz;
      begin
      end;
      
   Procedure DrukujWynik;
      begin
      end;
      
   Procedure Poczekaj;
      begin
      end;

BEGIN                       // Top_Down_1 
   InformacjaCoRobiProgram;
   CzytajDane;
   Oblicz;
   DrukujWynik;
   Poczekaj;
END.                        // end z kropką kończy program Top_Down
```
-
##schodzimy niżej (DOWN) - do szczególów - opisujemy kolejne instrukcje, które maja być wykonane po wywolaniu każdej z procedur zdefiniowanych w programie:
- 
## Przykład: Top-Down (T-D...) w Pascalu ...cd:

```pas
PROGRAM Top_Down_1;          // przykad zastosowania metodyki Top-Down
 
 Uses Crt;
 
 Var                        //deklaracja zmiennych
   i, j : Byte;
   suma : Integer;
    
   Procedure InformacjaCoRobiProgram;
      begin
         Writeln('Program przykladowy. Pokaz strukturalnej budowy programu.');
         Writeln('Metodyka: Top-Down - obliczanie sumy swóch liczb wprowadzonych przez użytkownika.');
         Writeln;
      end;

   Procedure CzytajDane;
      begin
         Write('Wpisz dodatnia liczbe calkowita (max. 255): i = ');
         Readln(i);
         Write('Wpisz dodatnia liczbe calkowita (max. 255): j = ');
         Readln(j);
      end;

   Procedure Oblicz;
      begin
         suma := i+j;
      end;
      
   Procedure DrukujWynik;
      begin
         Writeln;
         Writeln('Obliczylem wartosc sumy wprowadzonych liczb.');
         Writeln;
         Writeln('Suma liczb: ',i,' + ',j,' = ', suma);
      end;
      
   Procedure Poczekaj;
      begin
         Writeln;
         Write('Po nacisnieciu klawisza ENTER program zakonczy dzialanie');
         Readln;            // Oczekiwanie na nacisniecie klawisza ENTER
      end;

BEGIN                       // Top_Down_1 
   InformacjaCoRobiProgram;
   CzytajDane;
   Oblicz;
   DrukujWynik;
   Poczekaj;
END.                        // end z kropką kończy program Top_Down
```
-
-
-
ZADANIA
=======
### 1. Narysuj schemat blokowy powyzszego programu przykladowego.
### 2. Skonstruuj program wykonujacy te same operacje bez podzialu na procedury.

