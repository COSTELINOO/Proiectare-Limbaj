
# Proiect: Limbaj de Programare Original folosind YACC/BISON

## Instrucțiuni de Compilare

1. Se deschide un terminal în directorul cu fișierele proiectului.
2. Pentru compilarea proiectului, se utilizează comanda:
   ```bash
   ./compile.sh limbaj
   ```
3. Pentru verificarea limbajului propriu, se utilizează o comandă de tipul:
   ```bash
   ./limbaj "fisier.txt"
   ```
   Unde `fisier.txt` poate fi unul dintre următoarele exemple:
   - `inp_ok.txt` (exemplu de intrare corectă)
   - `input_gresit.txt` (exemplu de intrare cu erori)
   - `input_propriu.txt` (exemplu personalizat)

---

## Descrierea Proiectului

Acest proiect constă în proiectarea și implementarea unui limbaj de programare original utilizând **YACC/BISON** și **C++**, destinat să demonstreze concepte esențiale de parsing, analiza semantică și interpretare a expresiilor. Limbajul este structurat să includă caracteristici avansate precum declarațiile de tipuri, clase, funcții, expresii aritmetice și booleene, și să ofere suport pentru o ierarhie de simboluri bazată pe scope-uri.

## Caracteristici principale

### 1. Sintaxă și Structură
- Sprijin pentru tipuri predefinite: `int`, `float`, `char`, `string`, `bool`.
- Suport pentru tipuri de date complexe, cum ar fi array-uri și clase.
- Declarații de variabile și funcții, inclusiv o funcție principală care servește drept punct de intrare.
- Control al fluxului cu instrucțiuni `if`, `for`, și `while`.
- Funcții predefinite:
  - `Print(expr)` pentru a afișa valoarea și tipul unei expresii.
  - `TypeOf(expr)` pentru a afișa doar tipul unei expresii.

### 2. Tabela de Simboluri
- Implementarea unei tabele de simboluri pentru fiecare scope:
  - **Scope global**: variabile, funcții și clase accesibile în întreaga programare.
  - **Scope de bloc**: definit de `if`, `for`, și `while`.
  - **Scope de funcție**: definit de corpurile funcțiilor.
  - **Scope de clasă**: pentru membri și metode ale claselor.
- Gestionarea ierarhică a scope-urilor utilizând pointeri către tabela părinte.

### 3. Analiză Semantică
- Verificarea corectitudinii utilizării variabilelor și funcțiilor:
  - Declarațiile înainte de utilizare.
  - Verificarea dublurilor în același scope.
- Controlul tipurilor:
  - Operanzii expresiilor trebuie să aibă același tip.
  - Tipurile din atribuiri și apeluri de funcții trebuie să fie conforme cu definițiile.
- Gestionarea și raportarea erorilor cu mesaje detaliate.

### 4. Evaluarea Expresiilor
- Construirea și evaluarea arborilor de sintaxă abstractă (AST) pentru:
  - Expresii aritmetice și booleene.
  - Funcții și atribuiri.
- Integrarea evaluării AST în funcțiile predefinite și în atribuiri.
- Afișarea valorii și tipului unei expresii utilizând AST.


## Scop și Beneficii

Proiectul pune accent pe înțelegerea profundă a conceptelor de parsing și analiză semantică, oferind totodată o experiență practică în definirea și evaluarea expresiilor folosind AST-uri. Este conceput să ofere flexibilitate și extensibilitate pentru cerințe suplimentare și modificări în timpul prezentării.

---
