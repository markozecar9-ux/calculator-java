# Izveštaj o testiranju (TEST-RESULTS)

## 1. Sistemsko / Black-box testiranje (Prihvatljivost i funkcionalnost)

Prilikom sistemskog testiranja aplikacije iz ugla krajnjeg korisnika unošeni su različiti aritmetički izrazi radi provere funkcionalnosti i prioriteta računskih operacija:

- *Test scenario 1:* Unos jednostavnog izraza 4 + 5
  - *Očekivani rezultat:* 9
  - *Stvarno ponašanje:* Aplikacija ispravno izračunava vrednost 9.

- *Test scenario 2:* Provera prioriteta operacija 10 + 5 * 4 + 3
  - *Očekivani rezultat:* 10 + 20 + 3 = 33
  - *Detektovani propust / Bug:* Aplikacija računa operacije sledećim redosledom s leva na desno bez poštovanja prioriteta množenja, što rezultira netačnim ishodom.

- *Test scenario 3:* Deljenje sa nulom 10 / 0
  - *Očekivani rezultat:* Prikaz poruke o grešci ili izuzetka ArithmeticException.
  - *Detektovani propust / Bug:* Aplikacija ne prijavljuje grešku već vraća Infinity.

---

## 2. Jedinično testiranje (Unit Testing)

Kreiran je unit test u klasi CalculatorTest.java koji proverava funkcionisanje metode Calculate() za izračunavanje aritmetičkih izrata.

### Primer napisanog Unit test koda:
```java
@Test
public void testCalculateSimpleExpression() {
    Calculator calc = new Calculator();
    double expected = 9.0;
    double actual = calc.Calculate("4 + 5");
    assertEquals(expected, actual, 0.001);
}
