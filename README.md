# Izveštaj - Metrika, pregled i statička analiza

## 1. Metrika (LOC - Lines of Code)
- Ukupan LOC za kompletan projekat: 105 linija
- LOC po fajlovima:
  - Calculator.java: 52 linije
  - Start.java: 21 linija
  - CalculatorTest.java: 32 linije

## 2. Neformalni pregled koda i statička analiza

### Fajl: Calculator.java
- Broj linije koda: 14
  - Zapažanje / Code Smell: Nedostaje provera deljenja sa nulom u metodi divide(double a, double b). Ukoliko je $b = 0$, metoda vraća Infinity umesto da baci odgovarajući izuzetak (ArithmeticException).
- Broj linije koda: 22–28
  - Zapažanje / Code Smell: Postoje neiskorišćene lokalne promenljive i nepotrebni proračuni koji se nigde ne upotrebljavaju.
- Broj linije koda: 35
  - Zapažanje / Code Smell: Loša konvencija imenovanja promenljivih (korišćena su neopisna, jednoslovna imena poput x, y, z).
- Broj linije koda: 42
  - Zapažanje / Code Smell: Dupliranje koda (kôd za sabiranje se ponavlja umesto da se iskoristi već postojeća metoda add).

### Fajl: Start.java
- Broj linije koda: 8–12
  - Zapažanje / Code Smell: Postoji zakomentarisan kôd (Dead Code) koji narušava čitljivost fajla.
- Broj linije koda: 15
  - Zapažanje / Code Smell: Direktno štampanje na System.out umesto korišćenja standardnog logera (Logger).
