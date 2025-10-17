# 🐍 Python Cheatsheet – Modul 2

## 1️⃣ Funcții (`def`)

**Ce sunt:** blocuri de cod reutilizabile care pot primi date (parametri) și returnează un rezultat.

### Exemplu

```python
def salut(nume):
    print("Salut,", nume)

def aduna(a, b):
    return a + b

salut("Andrei")
print(aduna(3, 4))
```

**Explicație:**

- `def` definește funcția.
- `return` trimite rezultatul înapoi.
- Poți apela funcția oricând după definire.

---

## 2️⃣ Funcții recursive

**Ce sunt:** funcții care se apelează pe ele însele. Se folosesc pentru probleme repetitive care se “micșorează” la fiecare pas.

### Exemplu (factorial)

```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

**Explicație:**

- Condiția `if n <= 1` este cazul de oprire.
- Recursia continuă până când `n` devine 1.

---

## 3️⃣ Comprehensiune de listă

**Ce este:** o formă scurtă de a crea liste fără a folosi bucle lungi.

### Exemplu

```python
# listă cu pătratele primelor 5 numere
patrate = [x**2 for x in range(1, 6)]
print(patrate)  # [1, 4, 9, 16, 25]

# doar numere pare
pare = [x for x in range(10) if x % 2 == 0]
print(pare)  # [0, 2, 4, 6, 8]
```

**Explicație:**

- `[x**2 for x in range(1, 6)]` = “pune în listă pătratul fiecărui `x` între 1 și 5”.
- Poți adăuga condiții după `if`.

---

## 4️⃣ Matrici (liste de liste)

**Ce sunt:** liste în care fiecare element este o altă listă (ca un tabel 2D).

### Exemplu

```python
matrice = [[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]]

# accesarea elementelor
print(matrice[1][2])  # 6

# parcurgere
for rand in matrice:
    print(rand)
```

**Explicație:**

- `matrice[1][2]` = elementul din rândul 2, coloana 3.
- Poți parcurge matricea cu bucle imbricate.

---

## 5️⃣ Tuple

**Ce sunt:** colecții ordonate care **nu pot fi modificate** după creare.

### Exemplu

```python
coordonate = (10, 20)
x, y = coordonate
print(x, y)  # 10 20

culori = ("roșu", "verde", "albastru")
print(culori[0])  # roșu
```

**Explicație:**

- Se folosesc pentru date care nu trebuie schimbate.
- Poți “despacheta” valorile ușor: `x, y = coordonate`.

---

## 6️⃣ Fișiere

**Citire și scriere din fișiere text**

### Exemplu

```python
# scriere
with open("exemplu.txt", "w", encoding="utf-8") as f:
    f.write("Salut lume!\n")

# citire
with open("exemplu.txt", "r", encoding="utf-8") as f:
    continut = f.read()
    print(continut)
```

**Explicație:**

- `with open()` deschide fișierul și îl închide automat.
- Moduri: `r` (citire), `w` (scriere), `a` (adăugare).

---

## 7️⃣ Operații pe biți

**Ce sunt:** metode de a lucra cu reprezentarea binară a numerelor.

### Exemplu

```python
a = 5   # 0b0101
b = 3   # 0b0011

print(a & b)   # AND -> 1
print(a | b)   # OR  -> 7
print(a ^ b)   # XOR -> 6
print(a << 1)  # SHIFT LEFT -> 10
print(a >> 1)  # SHIFT RIGHT -> 2
```

**Explicație:**

- `&` = ambele 1 → 1
- `|` = oricare 1 → 1
- `^` = doar unul 1 → 1
- `<<` și `>>` deplasează biții la stânga/dreapta.

---

## 8️⃣ Module Python

**Ce sunt:** fișiere care conțin cod reutilizabil. Se folosesc cu `import`.

#### `math` – calcule matematice

```python
import math
print(math.sqrt(9))   # 3.0
print(math.pi)        # 3.1415...
```

#### `random` – valori aleatorii

```python
import random
x = random.randint(1, 10)
print(x)
```

#### `turtle` – desen grafic

```python
import turtle

t = turtle.Turtle()
for _ in range(4):
    t.forward(100)
    t.right(90)

turtle.exitonclick()
```

#### `os` – lucrul cu fișiere

```python
import os
os.remove("fisier.txt")
```

## Module folosite și funcțiile importante

#### math – calcule matematice

- math.sqrt(x) – rădăcina pătrată.
- math.pi, math.e – constante utile.
- math.factorial(n) – calculează factorialul.

- random – generare aleatorie
- random.randint(a, b) – număr întreg între a și b.
- random.choice(lista) – alege un element aleator.
- random.shuffle(lista) – amestecă elementele din listă.

#### turtle – desen grafic

_turtle.Turtle() – creează “stiloul”.
_.forward(px), .right(deg) – mișcare și rotație.
*.color(), .begin_fill(), .end_fill() – culoare și umplere.
*turtle.exitonclick() – închide fereastra la click.

#### os – lucrul cu fișiere și directoare

- os.path.join(fisier1, fisier2) – creează o cale completă.
- os.remove(fisier) – șterge fișierul dat.

#### pygame – dezvoltare jocuri 2D

*pygame.display.set_mode() – fereastra jocului.
*pygame.image.load() – încarcă imagini.
*pygame.Rect() – creează obiecte dreptunghiulare.
*pygame.key.get_pressed() – verifică taste apăsate.
\*pygame.mixer.Sound() – redă efecte sonore.

#### pandas – manipulare de date (CSV)

_pd.read_csv('fisier.csv') – citește fișier CSV.
_.head() – afișează primele rânduri.
_.drop() – elimină coloane.
_.fillna() – înlocuiește valori lipsă.

#### matplotlib.pyplot – grafice

*plt.pie() – grafic circular.
*plt.barh() – grafic cu bare orizontale.
\*plt.show() – afișează graficul.

#### numpy – calcule numerice

*np.mean(lista) – media valorilor.
*np.max(lista) – valoarea maximă.
*np.array() – creează un tablou numeric.

---

## 9️⃣ Exemplu complet – recapitulare

```python
import random

def genereaza_numere():
    return [random.randint(1, 10) for _ in range(5)]

def calculeaza_media(lista):
    return sum(lista) / len(lista)

numere = genereaza_numere()
print("Numere:", numere)
print("Media:", calculeaza_media(numere))
```

**Ce combină:**

- Funcții proprii (`def`)
- Modul extern (`random`)
- Comprehensiune de listă
- Calcul numeric cu funcții integrate (`sum`, `len`)

---

✅ **Rezumat final:**

- **Funcții** → organizează codul.
- **Recursie** → funcție care se apelează singură.
- **Comprehensiuni** → creare rapidă de liste.
- **Matrici** → liste în liste.
- **Tuple** → colecții fixe.
- **Fișiere** → citire/scriere date externe.
- **Operații pe biți** → lucrul cu reprezentări binare.
- **Module** → cod reutilizabil importat cu `import`.

---
