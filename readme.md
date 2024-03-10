# Klasy i obiekty
## wstęp

#### Co to są klasy i obiekty?
- **Klasa** jest pewnym **wzorcem** lub **szablonem**, który definiuje **strukturę** obiektu. np. mamy plan domy ale nie znamy konkretnych detali.
- **klasa** składa się z **pól**(takie inne zmienne) i z **metod**(takie inne funkcje).
- **Obiekt** to **konkretny egzemplarz** danej **klasy**. np. Na pdostawie **klasy** `House` możemy stworzyć **obiekt** reprezentujący rzeczywisty dom.


## Składnia tworzenia klasy w Javie:
- **Każda** klasa w Javie zaczyna się od słowa kluczowego `class`, a następnie podajemy nazwę klasy. Na przykład:

```java
public class MojaKlasa {
    // Ciało klasy
}
```
***Pamiętaj, że nazwy klas zwykle zaczynamy z wielkiej litery.***

## Modyfikatory dostępu:
Modyfikatory dostępu określają, jakie części składowe klasy (np. pola, metody) są widoczne dla innych klas i kodu.
- public: Dostępne dla wszystkich klas i kodu.
- private: Dostępne tylko wewnątrz tej samej klasy.
- protected: Dostępne wewnątrz tej samej klasy oraz dla podklas.
  ![alt text](https://i.redd.it/lyd5md4v3q351.jpg)
  ***Modyfikatory dostępu piszemy przed typem danego pola/metody***
  `public static void test`

## Definiowanie pól (zmiennych) w klasie:
- Pola klas to zmienne, które opisują stan obiektów danej klasy.
- Definiujemy je wewnątrz klasy, poza metodami.
- Przykład:

```java
public class Samochod {
    private String kolor; // Pole prywatne
    public int predkosc; // Pole publiczne

    // Metody, konstruktory itp.
}
```
## Metoda w programowaniu obiektowym:
- **Metoda** to **podprogram** zdefiniowany wewnątrz klasy, który wykonuje określone zadania na rzecz obiektów danej klasy.
- Działanie metody może obejmować manipulację polami obiektu lub wykonywanie innych operacji.
- Metody pozwalają na **hermetyzację** (ukrycie) logiki wewnątrz klasy, co ułatwia zarządzanie kodem.
  aha spoko ale czym jest hermetyzacja?

## Deklarowanie metody:

- Metodę deklarujemy wewnątrz klasy, podając jej nazwę, typ zwracanej wartości (jeśli istnieje), oraz listę parametrów (jeśli potrzebujemy przekazać dane). np
``` java
public class Samochod {
    public void uruchomSilnik() {
        // Logika uruchamiania silnika
    }
}

```


## Parametry metody i ich przekazywanie:
- Parametry metody to dane, które przekazujemy do metody w momencie jej wywołania.
- Parametry są określane w nawiasach okrągłych po nazwie metody.
  Przykład z metodą przyjmującą parametr:

```java
    public class Kalkulator {
        public int dodaj(int a, int b) {
            return a + b;
        }
    }

```


## Zwracanie wartości z metody:

- Słowo kluczowe `return` służy do zwracania wartości z metody.
- W przykładzie powyżej metoda `dodaj` zwraca sumę dwóch liczb.
- Jeśli metoda nie ma wartości do zwrócenia (np. jest typu `void`), używamy `return` bez żadnej wartości.



## Hierarchia klas:
- **Dziedziczenie** pozwala na tworzenie **hierarchii klas**, gdzie klasy pochodne dziedziczą cechy (pola i metody) po klasach bazowych.
- Przykład: Mamy klasę bazową `Zwierzę`, a po niej dziedziczą klasy `Ssak`, `Ptak`, `Ryba`.

## Dziedziczenie i nadpisywanie metod:
- **Dziedziczenie** umożliwia klasom pochodnym korzystanie z metod zdefiniowanych w klasach bazowych.
- **Nadpisywanie metod** pozwala na dostosowanie dziedziczonych metod do specyfiki klasy pochodnej.
- Przykład: Klasa `Kot` dziedziczy po klasie `Ssak` i może nadpisać metodę dzwiek().

## Polimorfizm - wielopostaciowość:
- **Polimorfizm** oznacza, że obiekty danej klasy mogą być traktowane jako obiekty innej klasy.
- Pozwala na wywoływanie tych samych metod na różnych obiektach.
- Przykład: Możemy wywołać metodę `dzwiek()` na obiekcie `Kot` lub `Ptak`.

