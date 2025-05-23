
# Nieograniczony problem plecakowy – Aplikacja Java

## 📌 Opis projektu
Projekt realizowany w ramach laboratorium **Platformy Programistyczne .NET i Java (Lab 5)**. Celem jest implementacja aplikacji konsolowej rozwiązującej **nieograniczony problem plecakowy** z użyciem algorytmu zachłannego (Dantzig, 1957) w języku **Java**.

## 📂 Struktura klas

### ✅ `Item.java`
Reprezentuje pojedynczy przedmiot.

#### Atrybuty:
- `int value` – wartość przedmiotu.
- `int weight` – waga przedmiotu.

#### Metody:
- Konstruktor `Item(int value, int weight)` – inicjalizuje wartości.
- `getValue()` – zwraca wartość.
- `getWeight()` – zwraca wagę.
- `toString()` – reprezentacja tekstowa przedmiotu.

---

### ✅ `Problem.java`
Reprezentuje instancję problemu plecakowego.

#### Atrybuty:
- `List<Item> items` – lista przedmiotów.
- `int n, seed, lowerBound, upperBound` – dane generatora.

#### Metody:
- Konstruktor `Problem(int n, int seed, int lowerBound, int upperBound)` – generuje `n` przedmiotów z zakresu.
- `List<Item> getItems()` – zwraca listę przedmiotów.
- `Result solve(int capacity)` – implementuje algorytm zachłanny.
- `toString()` – reprezentacja problemu.

---

### ✅ `Result.java`
Zawiera wynik rozwiązania problemu.

#### Atrybuty:
- `Map<Item, Integer> quantities` – mapa: przedmiot → ilość.
- `int totalWeight` – łączna waga.
- `int totalValue` – łączna wartość.

#### Metody:
- `add(Item item, int quantity)` – dodaje przedmiot do wyniku.
- `toString()` – reprezentacja wyniku.

---

### ✅ `Main.java`
Punkt wejściowy programu.

#### Metody:
- `main(String[] args)` – tworzy problem i rozwiązuje go, wypisując wynik.

---

### ✅ `ProblemTest.java`
Zestaw testów jednostkowych klasy `Problem`.

#### Metody testowe:
- Test generowania dokładnej liczby przedmiotów.
- Test dla plecaka o pojemności 0.
- Test poprawności sumy wag/wartości.
- Test gdy żaden przedmiot się nie mieści.

## 🛠️ Technologie
- Java 17+
- Maven
- IntelliJ IDEA
- JUnit 5

## 📈 Algorytm
Użyto algorytmu zachłannego sortującego przedmioty według opłacalności (wartość/waga), dodając je do plecaka dopóki pozwala na to pojemność.

## 🧪 Testowanie
Zastosowano bibliotekę **JUnit 5** do testów jednostkowych.
