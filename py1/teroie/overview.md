# 🐍 Ghid complet de bază Python – pentru examen 10/10

## 1️⃣ Tipuri de date din Python

| Tip de date | Exemplu         | Descriere                   |
| ----------- | --------------- | --------------------------- |
| `int`       | `x = 5`         | numere întrege              |
| `float`     | `x = 3.14`      | numere reale                |
| `str`       | `"Hello"`       | șiruri de caractere         |
| `bool`      | `True`, `False` | valori logice               |
| `list`      | `[1, 2, 3]`     | colecție de valori ordonate |
| `NoneType`  | `None`          | absența unei valori         |

### Conversii de tip

```python
int("5")        # -> 5
float("3.14")   # -> 3.14
str(42)         # -> "42"
bool(0)         # -> False
```

### Verificarea tipului

```python
type(3.14)      # <class 'float'>
```

---

## 2️⃣ Printare și lucru cu stringuri

### Printare

```python
print("Hello World")
print("Line1\nLine2")              # newline
print("Name:", name, "Age:", age)  # mai multe valori
```

### Concatenare și formatare

```python
print("Hello " + name)
print("My name is %s" % name)
print("I am %d years old" % age)
```

### Funcții utile pentru stringuri

| Funcție                           | Scop                           | Exemplu                                |
| --------------------------------- | ------------------------------ | -------------------------------------- |
| `.upper()`                        | majuscule                      | `"cat".upper()` → `"CAT"`              |
| `.lower()`                        | minuscule                      | `"DOG".lower()` → `"dog"`              |
| `.title()`                        | majuscule la început de cuvânt | `"hello world".title()`                |
| `.capitalize()`                   | prima literă mare              | `"hi".capitalize()`                    |
| `.replace(a,b)`                   | înlocuiește caractere          | `"cat".replace("c","r")`               |
| `.split()`                        | împarte textul                 | `"a,b,c".split(",")` → `["a","b","c"]` |
| `.find("e")`                      | poziția primei apariții        | `"tree".find("e")` → `1`               |
| `.count("a")`                     | număr de apariții              | `"banana".count("a")` → `3`            |
| `.startswith(x)` / `.endswith(x)` | verifică început/sfârșit       | `"Hello".startswith("H")`              |

---

## 3️⃣ Operatorii

### Aritmetici

| Operator | Descriere          | Exemplu       |
| -------- | ------------------ | ------------- |
| `+`      | adunare            | `2 + 3 = 5`   |
| `-`      | scădere            | `5 - 2 = 3`   |
| `*`      | înmulțire          | `4 * 2 = 8`   |
| `/`      | împărțire          | `5 / 2 = 2.5` |
| `//`     | împărțire întreagă | `5 // 2 = 2`  |
| `%`      | restul împărțirii  | `7 % 4 = 3`   |
| `**`     | putere             | `3 ** 2 = 9`  |

### De atribuire

```python
x = 5
x += 1   # x = 6
x -= 2   # x = 4
x *= 3   # x = 12
x /= 2   # x = 6.0
```

### De comparație

| Operator    | Exemplu  | Rezultat |
| ----------- | -------- | -------- |
| `==`        | `5 == 5` | `True`   |
| `!=`        | `4 != 5` | `True`   |
| `>` / `<`   | `7 > 2`  | `True`   |
| `>=` / `<=` | `5 >= 5` | `True`   |

### Logici

```python
and, or, not
```

Exemplu:

```python
if age > 18 and country == "Romania":
    print("Adult român")
```

### Apartenență și identitate

```python
"x" in "text"      # True
5 is 5             # True (aceeași valoare în memorie)
```

---

## 4️⃣ Structuri de control: `if`, `elif`, `else`

```python
if x > 0:
    print("Pozitiv")
elif x == 0:
    print("Zero")
else:
    print("Negativ")
```

### Exemple utile

```python
# Sistem de note
if grade >= 90:
    print("A")
elif grade >= 75:
    print("B")
else:
    print("C")
```

---

## 5️⃣ Bucla `while`

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

- Rulează atâta timp cât condiția este `True`
- Poate conține `break` (ieșire) sau `continue` (trecere la următoarea iterație)

Exemplu: numără cifrele dintr-un număr

```python
num = 9845
count = 0
while num != 0:
    num //= 10
    count += 1
print(count)
```

---

## 6️⃣ Bucla `for`

```python
for i in range(5):
    print(i)
```

### Exemple

```python
# pe șiruri
for c in "Hello":
    print(c)

# pe liste
for n in [1, 2, 3]:
    print(n)
```

### Cu `range(start, stop, step)`

```python
for i in range(2, 10, 2): print(i)  # 2, 4, 6, 8
```

---

## 7️⃣ Liste (list)

### Creare și acces

```python
names = ["Anna", "George", "Tom"]
print(names[0])     # primul
print(names[-1])    # ultimul
```

### Operații de bază

```python
names.append("Bob")
names.insert(1, "Amy")
names.remove("Tom")
names.pop(0)
print(len(names))
```

### Slicing

```python
names[1:3]   # elementele de la 1 la 2
names[:2]    # primele două
names[::2]   # din 2 în 2
```

### Alte metode

| Metodă       | Explicație                     |
| ------------ | ------------------------------ |
| `.count(x)`  | numărul de apariții            |
| `.index(x)`  | poziția elementului            |
| `.sort()`    | sortează lista                 |
| `.reverse()` | inversează ordinea             |
| `.extend()`  | adaugă elemente din altă listă |

---

## 8️⃣ Numere și funcții matematice

```python
abs(-3)       # 3
min(1, 2, 3)  # 1
max(4, 7, 2)  # 7
sum([1,2,3])  # 6
```

### Exemple utile

- **Fibonacci:**

  ```python
  a, b = 0, 1
  for i in range(10):
      print(a)
      a, b = b, a + b
  ```

- **CMMDC (GCD):**

  ```python
  for i in range(1, min(a,b)+1):
      if a % i == 0 and b % i == 0:
          gcd = i
  ```

- **CMMMC (LCM):**

  ```python
  lcm = max(a,b)
  while not (lcm % a == 0 and lcm % b == 0):
      lcm += 1
  ```

---

## 9️⃣ Funcții și funcții predefinite importante

| Funcție                            | Scop                           |
| ---------------------------------- | ------------------------------ |
| `len()`                            | lungimea unui șir/listă        |
| `type()`                           | tipul datelor                  |
| `str()`, `int()`, `float()`        | conversii de tip               |
| `input()`                          | citește de la tastatură        |
| `print()`                          | afișează                       |
| `range()`                          | generează o secvență de numere |
| `append()`, `insert()`, `remove()` | modifică liste                 |
| `min()`, `max()`, `sum()`          | funcții matematice rapide      |

---

## 🔠 Exemple de aplicații logice

- **Jocuri:** ghicirea unui număr, hangman, tic-tac-toe
- **Probleme matematice:** CMMDC, CMMMC, număr prim, sumă, produs
- **Manipulare de text:** înlocuire, numărare vocale, codificare/decriptare
- **Liste:** sortare, filtrare, găsire valori comune, eliminare duplicate

---

## ✅ Sfaturi pentru examen

- Indentarea corectă este obligatorie (`if`, `for`, `while` trebuie să aibă spații corecte)
- Convertește tipurile când combini text și numere (`str()` / `int()`)
- Repetă conceptele cheie: `if/elif/else`, `for`, `while`, `list.append()`, `range()`, `input()`
- Înelege diferența între:

  - `append` – adaugă un singur element
  - `extend` – adaugă mai multe elemente

- Exersează mini-programe:

  - Căutarea celui mai mare număr
  - Numărarea aparițiilor unui element
  - Ghicirea unui număr secret
