# 📜 LogicFlow - Interpretor de Pseudocod

## 📌 Descriere
Interpretorul de pseudocod este o aplicație web destinată elevilor care doresc să învețe informatică și să înțeleagă mai bine structura algoritmilor. Acesta oferă o sintaxă prietenoasă, inspirată din pseudocodul utilizat în manuale și la examenul de bacalaureat.

Această aplicație poate fi utilă în:
- Studiul algoritmilor în limbaj de pseudocod.
- Pregătirea pentru examenul de bacalaureat, în special pentru subiectul II.
- Convertirea intuitivă a pseudocodului în limbaje de programare reale.
- Învățarea tranziției de la algoritmi la implementare în C++.

---

## 🚀 Utilizare
1. Scrieți pseudocodul în editorul text.
2. Apăsați pe butonul **„Run"** pentru a executa codul.
3. Rezultatul va fi afișat în consolă.
4. Input-ul este luat prin casete de `prompt()`.
5. Vedeți transpilarea automată în C++ în panoul din dreapta.
6. Personalizați editorul din secțiunea **Setări**.
7. Activați **Modul AI Asistat** pentru a corecta automat erorile de sintaxă.

---

## 🔥 Features

### Interpretor și Editor
✅ **Editor text avansat**: syntax highlighting și auto-complete. <br>
✅ **Interpretor scris de la zero**, optimizat pentru limbajul de pseudocod.<br>
✅ **Analiză contextuală** a instrucțiunilor și expresiilor.<br>
✅ **Detectarea blocurilor logice** pentru controlul fluxului și al buclelor.<br>
✅ **Mesaje de eroare explicite** pentru debugging mai ușor.<br>
✅ **Configurare avansată** a editorului și a interpretorului.<br>

### Transpiler C++
✅ **Transpilare automată** a pseudocodului în cod C++ funcțional.<br>
✅ **Generare de headeruri** și declarații în funcție de tipurile detectate.<br>
✅ **Mapare corectă** a construcțiilor de limbaj din pseudocod în C++.<br>
✅ **Actualizare în timp real** a codului C++ la modificările pseudocodului.<br>

### Evaluator
✅ **Evaluare eficientă** a expresiilor și instrucțiunilor.<br>
✅ **Suport pentru variabile** de tip număr, boolean și șiruri de caractere.<br>
✅ **Limite de iterații** configurabile pentru prevenirea buclelor infinite.<br>
✅ **Execuție pas cu pas** a pseudocodului pentru înțelegere clară.<br>

### AI Asistat
✅ **Asistență AI** pentru corectarea automată a erorilor de sintaxă.<br>
✅ **Sugestii inteligente** pentru îmbunătățirea codului.<br>
✅ **Interfață de analiză comparativă** între codul original și cel corectat de AI.<br>
✅ **Selectare granulară** a modificărilor propuse de AI prin interfața de merge.<br>
✅ **Păstrarea contextului** și a intenției algoritmice în corectările propuse.<br>

---

## 🛠 Tehnologii folosite
- **[Vite](https://vitejs.dev/)** - build tool rapid și modern
- **[React.js](https://react.dev/)** - pentru interfața utilizator
- **[TailwindCSS](https://tailwindcss.com/)** - pentru un UI responsive și modern
- **JavaScript** - pentru interpretarea codului
- **[OpenAI API](https://openai.com/)** - pentru asistența AI în corectarea codului
- **[Monaco Editor](https://microsoft.github.io/monaco-editor/)** - editor de cod performant

---

## 🏗 Instalare locală
Dacă vrei să rulezi proiectul pe propriul computer, urmează pașii:

```bash
# Clonează repository-ul
git clone https://github.com/danielmitrache/Pseudocode_Interpreter

# Intră în folderul proiectului
cd Pseudocode_Interpreter

git checkout logicflow

# Instalează dependențele
npm install

# Creează un fișier .env pentru cheile API necesare (AI-assisted mode)
echo "VITE_OPENAI_API_KEY=your_openai_api_key_here" > .env

# Rulează aplicația local
npm run dev
```

Aplicația va fi disponibilă pe `http://localhost:5173/` (sau alt port specificat de Vite).

---

## 🧩 Cum funcționează

### Fluxul de interpretare a pseudocodului:
1. **Lexer** - Tokenizarea codului sursă în structuri primitive
2. **Parser** - Construirea arborelui de sintaxă abstractă (AST)
3. **Evaluator** - Execuția AST-ului și manipularea variabilelor
4. **Transpiler** - Convertirea opțională în cod C++ echivalent
5. **AI Assistant** - Corectarea erorilor de sintaxă (când e activat)

### Fluxul de corectare asistat de AI:
1. **Detectarea erorilor** - Identificarea problemelor de sintaxă în cod
2. **Refactorizare AI** - Trimiterea codului către API-ul OpenAI pentru corectare
3. **Analiză comparativă** - Prezentarea diferențelor între codul original și cel corectat
4. **Merge interactiv** - Interfață pentru acceptarea selectivă a modificărilor propuse
5. **Aplicare** - Integrarea modificărilor selectate în editor

---

## 📊 Exemplu comparativ

### Pseudocod:
```
citeste n
suma = 0
pentru i = 1, n executa {
    citeste x
    suma = suma + x
}
scrie "Suma este: ", suma
```

### C++ generat:
```cpp
#include <iostream>
#include <string>

using namespace std;

int main() {
    int n;
    int suma;
    int i;
    int x;
    
    cin >> n;
    suma = 0;
    for (i = 1; i <= n; i++) {
        cin >> x;
        suma = suma + x;
    }
    cout << "Suma este: " << suma << endl;
    
    return 0;
}
```
