<div align="center">

<h1>🎨 CSS — powtórka do INF.03</h1>

<p><strong>Praktyczne podsumowanie stylowania stron internetowych — od selektorów i modelu pudełkowego po Flexbox oraz responsywność.</strong></p>

<p>
  <img src="https://img.shields.io/badge/INF.03-powtórka-0A66C2" alt="INF.03 — powtórka">
  <img src="https://img.shields.io/badge/CSS3-stylowanie-1572B6" alt="CSS3 — stylowanie">
  <img src="https://img.shields.io/badge/demo-kopiuj_i_uruchom-2EA44F" alt="Demo — kopiuj i uruchom">
</p>

<p><em>Rozwijaj przykłady, kopiuj kod do osobnych plików i obserwuj zmiany na bieżąco w przeglądarce.</em></p>

</div>

<hr>

<h2>📌 Spis treści</h2>

<ol>
  <li><a href="#czym-jest-css">Czym jest CSS?</a></li>
  <li><a href="#dolaczanie">Sposoby dołączania CSS</a></li>
  <li><a href="#selektory">Selektory</a></li>
  <li><a href="#kolory">Kolory i jednostki</a></li>
  <li><a href="#box-model">Model pudełkowy</a></li>
  <li><a href="#tekst">Tekst i czcionki</a></li>
  <li><a href="#tlo-obramowanie">Tło, obramowanie i zaokrąglenia</a></li>
  <li><a href="#display">Display, widoczność i przepełnienie</a></li>
  <li><a href="#flexbox">Flexbox</a></li>
  <li><a href="#pozycjonowanie">Pozycjonowanie elementów</a></li>
  <li><a href="#pseudoklasy">Pseudoklasy i pseudoelementy</a></li>
  <li><a href="#formularze-tabele">Stylowanie formularzy i tabel</a></li>
  <li><a href="#responsywnosc">Responsywność i media queries</a></li>
  <li><a href="#kaskada">Kaskada, dziedziczenie i specyficzność</a></li>
  <li><a href="#bledy">Najczęstsze błędy na INF.03 / CKE</a></li>
  <li><a href="#sciaga">Krótka ściąga właściwości</a></li>
  <li><a href="#dema">Gotowe dema do uruchomienia w przeglądarce</a></li>
  <li><a href="#zadanie">Mini zadanie powtórkowe</a></li>
</ol>

<hr>

<a id="czym-jest-css"></a>
<h2>1. Czym jest CSS?</h2>

<p><strong>CSS</strong> (<em>Cascading Style Sheets</em>) to język arkuszy stylów. Określa wygląd elementów HTML: kolory, rozmiary, odstępy, obramowania oraz układ strony.</p>

<blockquote>
  <p>💡 HTML opisuje <strong>co znajduje się na stronie</strong>, a CSS określa <strong>jak ta treść wygląda</strong>.</p>
</blockquote>

<table>
  <thead>
    <tr><th>Fragment</th><th>Nazwa</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>p</code></td><td>Selektor</td><td>Wskazuje elementy, które zostaną ostylowane</td></tr>
    <tr><td><code>color</code></td><td>Właściwość</td><td>Określa cechę, którą zmieniamy</td></tr>
    <tr><td><code>navy</code></td><td>Wartość</td><td>Określa ustawienie właściwości</td></tr>
    <tr><td><code>color: navy;</code></td><td>Deklaracja</td><td>Para „właściwość: wartość” zakończona średnikiem</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — anatomia reguły CSS</strong></summary>
  <br>
  <pre><code>p {
  color: navy;
  font-size: 18px;
}</code></pre>
  <p>Reguła wybiera wszystkie akapity <code>&lt;p&gt;</code>, ustawia granatowy kolor tekstu i rozmiar czcionki równy <code>18px</code>.</p>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="dolaczanie"></a>
<h2>2. Sposoby dołączania CSS</h2>

<table>
  <thead>
    <tr><th>Sposób</th><th>Miejsce</th><th>Typowe zastosowanie</th></tr>
  </thead>
  <tbody>
    <tr><td>Zewnętrzny</td><td>Osobny plik <code>.css</code></td><td>Najlepszy wybór dla całej witryny</td></tr>
    <tr><td>Wewnętrzny</td><td>Znacznik <code>&lt;style&gt;</code> w <code>&lt;head&gt;</code></td><td>Mała lub demonstracyjna strona</td></tr>
    <tr><td>Liniowy</td><td>Atrybut <code>style</code> elementu</td><td>Pojedynczy wyjątek; zwykle należy go unikać</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — zewnętrzny arkusz stylów</strong></summary>
  <br>
  <p><strong>Plik <code>index.html</code>:</strong></p>
  <pre><code>&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Moja strona&lt;/title&gt;
  &lt;link rel="stylesheet" href="styl.css"&gt;
&lt;/head&gt;</code></pre>
  <p><strong>Plik <code>styl.css</code>:</strong></p>
  <pre><code>body {
  background-color: #f4f6f8;
  color: #222222;
}</code></pre>
</details>

<details>
  <summary><strong>▶ Demo kodu — styl wewnętrzny i liniowy</strong></summary>
  <br>
  <pre><code>&lt;head&gt;
  &lt;style&gt;
    h1 {
      color: darkgreen;
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Nagłówek stylowany wewnętrznie&lt;/h1&gt;
  &lt;p style="color: crimson;"&gt;Styl liniowy.&lt;/p&gt;
&lt;/body&gt;</code></pre>
</details>

<blockquote>
  <p>⚠️ Na egzaminie sprawdź dokładną nazwę i położenie arkusza. Zapis <code>href="styl.css"</code> zadziała tylko wtedy, gdy pliki HTML i CSS znajdują się w tym samym katalogu.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="selektory"></a>
<h2>3. Selektory</h2>

<table>
  <thead>
    <tr><th>Selektor</th><th>Przykład</th><th>Co wybiera?</th></tr>
  </thead>
  <tbody>
    <tr><td>Elementu</td><td><code>p</code></td><td>Wszystkie elementy <code>&lt;p&gt;</code></td></tr>
    <tr><td>Klasy</td><td><code>.ważne</code></td><td>Elementy z <code>class="ważne"</code></td></tr>
    <tr><td>Identyfikatora</td><td><code>#kontakt</code></td><td>Element z <code>id="kontakt"</code></td></tr>
    <tr><td>Uniwersalny</td><td><code>*</code></td><td>Wszystkie elementy</td></tr>
    <tr><td>Grupowy</td><td><code>h1, h2</code></td><td>Wszystkie wskazane typy elementów</td></tr>
    <tr><td>Potomka</td><td><code>nav a</code></td><td>Linki znajdujące się wewnątrz <code>&lt;nav&gt;</code></td></tr>
    <tr><td>Dziecka</td><td><code>ul &gt; li</code></td><td>Elementy <code>&lt;li&gt;</code> będące bezpośrednimi dziećmi listy</td></tr>
    <tr><td>Atrybutu</td><td><code>input[type="email"]</code></td><td>Pola <code>input</code> konkretnego typu</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — najważniejsze selektory</strong></summary>
  <br>
  <pre><code>/* Wszystkie akapity */
p {
  line-height: 1.6;
}

/* Elementy należące do klasy */
.ważne {
  color: red;
  font-weight: bold;
}

/* Jeden element o unikalnym id */
#kontakt {
  background-color: lightyellow;
}

/* Linki wewnątrz nawigacji */
nav a {
  text-decoration: none;
}

/* Pola wymagane */
input[required] {
  border: 2px solid orange;
}</code></pre>
</details>

<blockquote>
  <p>🧠 Kropka <code>.</code> oznacza klasę, krzyżyk <code>#</code> oznacza identyfikator, a sam zapis <code>p</code> wskazuje element HTML.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="kolory"></a>
<h2>4. Kolory i jednostki</h2>

<h3>Sposoby zapisu koloru</h3>

<table>
  <thead>
    <tr><th>Zapis</th><th>Przykład</th><th>Informacja</th></tr>
  </thead>
  <tbody>
    <tr><td>Nazwa</td><td><code>navy</code></td><td>Czytelna, ale ograniczona paleta</td></tr>
    <tr><td>HEX</td><td><code>#1e40af</code></td><td>Popularny sześciocyfrowy zapis szesnastkowy</td></tr>
    <tr><td>RGB</td><td><code>rgb(30, 64, 175)</code></td><td>Składowe czerwona, zielona i niebieska</td></tr>
    <tr><td>RGBA</td><td><code>rgba(30, 64, 175, 0.5)</code></td><td>RGB z kanałem przezroczystości</td></tr>
    <tr><td>HSL</td><td><code>hsl(224, 71%, 40%)</code></td><td>Odcień, nasycenie i jasność</td></tr>
  </tbody>
</table>

<h3>Najczęstsze jednostki</h3>

<table>
  <thead>
    <tr><th>Jednostka</th><th>Rodzaj</th><th>Zastosowanie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>px</code></td><td>Bezwzględna</td><td>Obramowania i precyzyjne wartości</td></tr>
    <tr><td><code>%</code></td><td>Względna</td><td>Wartość zależna od elementu nadrzędnego</td></tr>
    <tr><td><code>em</code></td><td>Względna</td><td>Zależna od rozmiaru czcionki elementu</td></tr>
    <tr><td><code>rem</code></td><td>Względna</td><td>Zależna od rozmiaru czcionki elementu głównego</td></tr>
    <tr><td><code>vw</code></td><td>Względna</td><td>Procent szerokości okna przeglądarki</td></tr>
    <tr><td><code>vh</code></td><td>Względna</td><td>Procent wysokości okna przeglądarki</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — kolory i jednostki</strong></summary>
  <br>
  <pre><code>body {
  background-color: #f1f5f9;
  color: rgb(30, 41, 59);
  font-size: 16px;
}

main {
  width: 80%;
  min-height: 50vh;
}

h1 {
  font-size: 2rem;
}

.informacja {
  background-color: rgba(59, 130, 246, 0.2);
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="box-model"></a>
<h2>5. Model pudełkowy</h2>

<p>Każdy element HTML można traktować jak prostokąt złożony z czterech warstw.</p>

<table>
  <thead>
    <tr><th>Warstwa</th><th>Właściwość</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td>Zawartość</td><td><code>width</code>, <code>height</code></td><td>Tekst, obraz lub inna treść</td></tr>
    <tr><td>Wypełnienie</td><td><code>padding</code></td><td>Odstęp wewnątrz elementu</td></tr>
    <tr><td>Obramowanie</td><td><code>border</code></td><td>Linia otaczająca element</td></tr>
    <tr><td>Margines</td><td><code>margin</code></td><td>Odstęp na zewnątrz elementu</td></tr>
  </tbody>
</table>

<blockquote>
  <p>🧠 <strong>Padding</strong> to przestrzeń wewnątrz pudełka, a <strong>margin</strong> oddziela pudełko od sąsiednich elementów.</p>
</blockquote>

<details>
  <summary><strong>▶ Demo kodu — model pudełkowy</strong></summary>
  <br>
  <pre><code>* {
  box-sizing: border-box;
}

.karta {
  width: 320px;
  padding: 24px;
  border: 2px solid #2563eb;
  margin: 20px;
}</code></pre>
  <p><code>box-sizing: border-box</code> sprawia, że podana szerokość obejmuje zawartość, wypełnienie i obramowanie.</p>
</details>

<details>
  <summary><strong>▶ Demo kodu — skrócony zapis odstępów</strong></summary>
  <br>
  <pre><code>/* Wszystkie strony */
padding: 20px;

/* Góra/dół oraz lewo/prawo */
padding: 10px 20px;

/* Góra, lewo/prawo, dół */
margin: 10px 20px 30px;

/* Góra, prawa, dół, lewa — zgodnie z ruchem wskazówek zegara */
margin: 10px 20px 30px 40px;</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="tekst"></a>
<h2>6. Tekst i czcionki</h2>

<table>
  <thead>
    <tr><th>Właściwość</th><th>Zastosowanie</th><th>Przykład</th></tr>
  </thead>
  <tbody>
    <tr><td><code>color</code></td><td>Kolor tekstu</td><td><code>color: #222;</code></td></tr>
    <tr><td><code>font-family</code></td><td>Krój pisma</td><td><code>font-family: Arial, sans-serif;</code></td></tr>
    <tr><td><code>font-size</code></td><td>Rozmiar tekstu</td><td><code>font-size: 18px;</code></td></tr>
    <tr><td><code>font-weight</code></td><td>Grubość tekstu</td><td><code>font-weight: bold;</code></td></tr>
    <tr><td><code>font-style</code></td><td>Styl tekstu</td><td><code>font-style: italic;</code></td></tr>
    <tr><td><code>text-align</code></td><td>Wyrównanie</td><td><code>text-align: center;</code></td></tr>
    <tr><td><code>text-decoration</code></td><td>Dekoracja, np. podkreślenie</td><td><code>text-decoration: none;</code></td></tr>
    <tr><td><code>text-transform</code></td><td>Zmiana wielkości liter</td><td><code>text-transform: uppercase;</code></td></tr>
    <tr><td><code>line-height</code></td><td>Wysokość wiersza</td><td><code>line-height: 1.6;</code></td></tr>
    <tr><td><code>letter-spacing</code></td><td>Odstęp między znakami</td><td><code>letter-spacing: 1px;</code></td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — czytelna typografia</strong></summary>
  <br>
  <pre><code>body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #1f2937;
}

h1 {
  font-size: 2rem;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
}

a {
  color: #1d4ed8;
  text-decoration: none;
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="tlo-obramowanie"></a>
<h2>7. Tło, obramowanie i zaokrąglenia</h2>

<details>
  <summary><strong>▶ Demo kodu — karta z tłem i obramowaniem</strong></summary>
  <br>
  <pre><code>.karta {
  background-color: #ffffff;
  border: 1px solid #cbd5e1;
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
}

.baner {
  background-image: url("obrazy/tlo.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}</code></pre>
</details>

<table>
  <thead>
    <tr><th>Właściwość</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>background-color</code></td><td>Kolor tła</td></tr>
    <tr><td><code>background-image</code></td><td>Obraz tła</td></tr>
    <tr><td><code>background-repeat</code></td><td>Sposób powtarzania obrazu</td></tr>
    <tr><td><code>background-position</code></td><td>Pozycja obrazu tła</td></tr>
    <tr><td><code>background-size</code></td><td>Rozmiar obrazu tła</td></tr>
    <tr><td><code>border</code></td><td>Skrócony zapis grubości, stylu i koloru ramki</td></tr>
    <tr><td><code>border-radius</code></td><td>Zaokrąglenie narożników</td></tr>
    <tr><td><code>box-shadow</code></td><td>Cień elementu</td></tr>
  </tbody>
</table>

<blockquote>
  <p>⚠️ Poprawny skrót obramowania to np. <code>border: 2px solid black;</code>. Musi zawierać styl linii, jeśli ramka ma być widoczna.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="display"></a>
<h2>8. Display, widoczność i przepełnienie</h2>

<table>
  <thead>
    <tr><th>Wartość</th><th>Zachowanie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>display: block</code></td><td>Element zajmuje dostępną szerokość i zaczyna nowy wiersz</td></tr>
    <tr><td><code>display: inline</code></td><td>Element pozostaje w wierszu; szerokość wynika z treści</td></tr>
    <tr><td><code>display: inline-block</code></td><td>Element pozostaje w wierszu, ale może mieć wymiary</td></tr>
    <tr><td><code>display: none</code></td><td>Element znika i nie zajmuje miejsca</td></tr>
    <tr><td><code>visibility: hidden</code></td><td>Element jest niewidoczny, ale zachowuje miejsce</td></tr>
    <tr><td><code>overflow: auto</code></td><td>Dodaje przewijanie, jeśli zawartość się nie mieści</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — block, inline-block i ukrywanie</strong></summary>
  <br>
  <pre><code>nav a {
  display: inline-block;
  padding: 10px 16px;
}

.ukryty {
  display: none;
}

.przewijany-panel {
  width: 300px;
  height: 120px;
  overflow: auto;
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="flexbox"></a>
<h2>9. Flexbox</h2>

<p>Flexbox ułatwia układanie elementów w jednym kierunku: w wierszu albo w kolumnie.</p>

<table>
  <thead>
    <tr><th>Właściwość</th><th>Gdzie?</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>display: flex</code></td><td>Kontener</td><td>Włącza Flexbox</td></tr>
    <tr><td><code>flex-direction</code></td><td>Kontener</td><td>Ustawia kierunek elementów</td></tr>
    <tr><td><code>justify-content</code></td><td>Kontener</td><td>Rozmieszcza elementy na osi głównej</td></tr>
    <tr><td><code>align-items</code></td><td>Kontener</td><td>Wyrównuje elementy na osi poprzecznej</td></tr>
    <tr><td><code>gap</code></td><td>Kontener</td><td>Ustawia odstęp między elementami</td></tr>
    <tr><td><code>flex-wrap</code></td><td>Kontener</td><td>Zezwala elementom przechodzić do kolejnego wiersza</td></tr>
    <tr><td><code>flex</code></td><td>Element potomny</td><td>Określa sposób wzrostu i zmniejszania</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — karty ułożone za pomocą Flexbox</strong></summary>
  <br>
  <pre><code>.kontener {
  display: flex;
  justify-content: center;
  align-items: stretch;
  flex-wrap: wrap;
  gap: 20px;
}

.karta {
  flex: 1 1 240px;
  max-width: 320px;
  padding: 20px;
  border: 1px solid #cccccc;
}</code></pre>
</details>

<blockquote>
  <p>🧠 Przy domyślnym <code>flex-direction: row</code> oś główna jest pozioma. <code>justify-content</code> działa wtedy poziomo, a <code>align-items</code> pionowo.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="pozycjonowanie"></a>
<h2>10. Pozycjonowanie elementów</h2>

<table>
  <thead>
    <tr><th>Wartość <code>position</code></th><th>Zachowanie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>static</code></td><td>Domyślne położenie w normalnym układzie strony</td></tr>
    <tr><td><code>relative</code></td><td>Przesunięcie względem pozycji początkowej; tworzy punkt odniesienia</td></tr>
    <tr><td><code>absolute</code></td><td>Pozycja względem najbliższego pozycjonowanego przodka</td></tr>
    <tr><td><code>fixed</code></td><td>Pozycja względem okna przeglądarki</td></tr>
    <tr><td><code>sticky</code></td><td>Łączy zachowanie zwykłe i przyklejone podczas przewijania</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — etykieta w prawym górnym rogu karty</strong></summary>
  <br>
  <pre><code>.karta {
  position: relative;
  padding: 30px;
  border: 1px solid #999999;
}

.etykieta {
  position: absolute;
  top: 8px;
  right: 8px;
  background-color: crimson;
  color: white;
  padding: 4px 8px;
}

header {
  position: sticky;
  top: 0;
  z-index: 10;
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="pseudoklasy"></a>
<h2>11. Pseudoklasy i pseudoelementy</h2>

<table>
  <thead>
    <tr><th>Zapis</th><th>Typ</th><th>Zastosowanie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>:hover</code></td><td>Pseudoklasa</td><td>Wskaźnik znajduje się nad elementem</td></tr>
    <tr><td><code>:focus</code></td><td>Pseudoklasa</td><td>Element ma fokus, np. aktywne pole formularza</td></tr>
    <tr><td><code>:first-child</code></td><td>Pseudoklasa</td><td>Element jest pierwszym dzieckiem rodzica</td></tr>
    <tr><td><code>:nth-child(2)</code></td><td>Pseudoklasa</td><td>Element jest drugim dzieckiem rodzica</td></tr>
    <tr><td><code>::before</code></td><td>Pseudoelement</td><td>Wstawia dekoracyjną treść przed zawartością</td></tr>
    <tr><td><code>::after</code></td><td>Pseudoelement</td><td>Wstawia dekoracyjną treść po zawartości</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — interakcja bez JavaScriptu</strong></summary>
  <br>
  <pre><code>a {
  color: #1d4ed8;
}

a:hover {
  color: #dc2626;
  text-decoration: underline;
}

input:focus {
  outline: 3px solid #93c5fd;
}

li:first-child {
  font-weight: bold;
}

.ważne::before {
  content: "⚠ ";
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="formularze-tabele"></a>
<h2>12. Stylowanie formularzy i tabel</h2>

<details>
  <summary><strong>▶ Demo kodu — czytelny formularz</strong></summary>
  <br>
  <pre><code>form {
  max-width: 500px;
  margin: 30px auto;
}

label {
  display: block;
  margin-top: 12px;
  font-weight: bold;
}

input,
select,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #94a3b8;
  border-radius: 6px;
  box-sizing: border-box;
}

button {
  margin-top: 16px;
  padding: 10px 20px;
  border: none;
  background-color: #2563eb;
  color: white;
  cursor: pointer;
}

button:hover {
  background-color: #1d4ed8;
}</code></pre>
</details>

<details>
  <summary><strong>▶ Demo kodu — czytelna tabela</strong></summary>
  <br>
  <pre><code>table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  padding: 10px;
  border: 1px solid #64748b;
  text-align: left;
}

th {
  background-color: #1e3a8a;
  color: white;
}

tbody tr:nth-child(even) {
  background-color: #e2e8f0;
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="responsywnosc"></a>
<h2>13. Responsywność i media queries</h2>

<p>Strona responsywna dostosowuje układ do szerokości ekranu. Podstawą jest elastyczny układ, względne rozmiary oraz zapytania medialne.</p>

<details>
  <summary><strong>▶ Demo kodu — układ zmieniany na małym ekranie</strong></summary>
  <br>
  <pre><code>.kolumny {
  display: flex;
  gap: 20px;
}

.kolumna {
  flex: 1;
}

img {
  max-width: 100%;
  height: auto;
}

@media (max-width: 700px) {
  .kolumny {
    flex-direction: column;
  }

  nav a {
    display: block;
  }
}</code></pre>
</details>

<blockquote>
  <p>📱 Nie zapomnij o znaczniku <code>&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</code> w sekcji <code>&lt;head&gt;</code>.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="kaskada"></a>
<h2>14. Kaskada, dziedziczenie i specyficzność</h2>

<p>Gdy kilka reguł dotyczy tego samego elementu i tej samej właściwości, przeglądarka musi wybrać deklarację zwycięską.</p>

<table>
  <thead>
    <tr><th>Zasada</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td>Kaskada</td><td>Łączy reguły z różnych źródeł i rozstrzyga konflikty</td></tr>
    <tr><td>Dziedziczenie</td><td>Niektóre właściwości, np. <code>color</code>, przechodzą z rodzica na dzieci</td></tr>
    <tr><td>Specyficzność</td><td>Bardziej precyzyjny selektor zwykle ma pierwszeństwo</td></tr>
    <tr><td>Kolejność</td><td>Przy tej samej specyficzności wygrywa reguła zapisana później</td></tr>
  </tbody>
</table>

<p><strong>Uproszczona kolejność siły selektorów:</strong></p>

<p><code>styl liniowy → #id → .klasa / :pseudoklasa → element</code></p>

<details>
  <summary><strong>▶ Demo kodu — która reguła wygra?</strong></summary>
  <br>
  <pre><code>p {
  color: green;
}

.opis {
  color: blue;
}

#wstęp {
  color: red;
}</code></pre>
  <pre><code>&lt;p id="wstęp" class="opis"&gt;Jaki będę mieć kolor?&lt;/p&gt;</code></pre>
  <p><strong>Odpowiedź:</strong> czerwony, ponieważ selektor identyfikatora <code>#wstęp</code> jest bardziej specyficzny.</p>
</details>

<blockquote>
  <p>⚠️ Nie rozwiązuj zwykłych problemów ze specyficznością przez częste używanie <code>!important</code>. Najpierw sprawdź selektor, kolejność reguł i poprawność dołączenia arkusza.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="bledy"></a>
<h2>15. Najczęstsze błędy na INF.03 / CKE</h2>

<table>
  <thead>
    <tr><th>❌ Błąd</th><th>✅ Jak go uniknąć?</th></tr>
  </thead>
  <tbody>
    <tr><td>Zła nazwa pliku CSS</td><td>Przepisz nazwę dokładnie, np. <code>styl.css</code>, i sprawdź rozszerzenie.</td></tr>
    <tr><td>Niepoprawna ścieżka w <code>href</code></td><td>Sprawdź położenie pliku względem dokumentu HTML.</td></tr>
    <tr><td>Brak <code>rel="stylesheet"</code></td><td>Użyj pełnego znacznika <code>&lt;link rel="stylesheet" href="styl.css"&gt;</code>.</td></tr>
    <tr><td>Selektor nie pasuje do HTML</td><td>Porównaj zapis klasy i id, łącznie z polskimi znakami oraz wielkością liter.</td></tr>
    <tr><td>Brak kropki przed klasą</td><td>Dla <code>class="karta"</code> zapisz selektor <code>.karta</code>.</td></tr>
    <tr><td>Brak <code>#</code> przed id</td><td>Dla <code>id="baner"</code> zapisz selektor <code>#baner</code>.</td></tr>
    <tr><td>Brak dwukropka lub średnika</td><td>Stosuj zapis <code>właściwość: wartość;</code>.</td></tr>
    <tr><td>Brak jednostki</td><td>Jeśli jest wymagana, zapisz np. <code>20px</code>, nie samo <code>20</code>.</td></tr>
    <tr><td>Przecinek zamiast kropki</td><td>W CSS liczby dziesiętne zapisuj z kropką, np. <code>opacity: 0.5;</code>.</td></tr>
    <tr><td>Zła ścieżka w <code>url()</code></td><td>Ścieżka jest liczona względem pliku CSS, a nie zawsze względem HTML.</td></tr>
    <tr><td>Literówka we właściwości</td><td>Przeglądarka pomija nierozpoznaną deklarację bez wyświetlania komunikatu na stronie.</td></tr>
    <tr><td>Mylenie <code>margin</code> i <code>padding</code></td><td>Pamiętaj: margin — na zewnątrz, padding — wewnątrz.</td></tr>
    <tr><td>Styl przesłonięty inną regułą</td><td>Sprawdź specyficzność i kolejność deklaracji.</td></tr>
    <tr><td>Brak zapisania pliku</td><td>Zapisuj HTML i CSS przed odświeżeniem strony.</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>✅ Lista kontrolna przed oddaniem pracy</strong></summary>
  <ul>
    <li>Sprawdź nazwy i miejsca zapisania plików.</li>
    <li>Zweryfikuj znacznik <code>&lt;link&gt;</code> i jego ścieżkę.</li>
    <li>Porównaj wszystkie wymagane wartości z arkuszem.</li>
    <li>Sprawdź jednostki, średniki, nawiasy klamrowe i dwukropki.</li>
    <li>Przetestuj linki, formularz oraz wygląd na całej stronie.</li>
    <li>Zmniejsz okno i sprawdź zachowanie układu.</li>
    <li>Zapisz wszystkie pliki, a następnie odśwież stronę.</li>
  </ul>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="sciaga"></a>
<h2>16. Krótka ściąga właściwości</h2>

<table>
  <thead>
    <tr><th>Cel</th><th>Właściwości</th></tr>
  </thead>
  <tbody>
    <tr><td>Kolory</td><td><code>color</code>, <code>background-color</code>, <code>opacity</code></td></tr>
    <tr><td>Tekst</td><td><code>font-family</code>, <code>font-size</code>, <code>font-weight</code>, <code>line-height</code>, <code>text-align</code></td></tr>
    <tr><td>Rozmiar</td><td><code>width</code>, <code>height</code>, <code>min-width</code>, <code>max-width</code></td></tr>
    <tr><td>Odstępy</td><td><code>margin</code>, <code>padding</code>, <code>gap</code></td></tr>
    <tr><td>Ramka</td><td><code>border</code>, <code>border-radius</code>, <code>box-shadow</code></td></tr>
    <tr><td>Tło</td><td><code>background-image</code>, <code>background-size</code>, <code>background-position</code></td></tr>
    <tr><td>Wyświetlanie</td><td><code>display</code>, <code>visibility</code>, <code>overflow</code></td></tr>
    <tr><td>Flexbox</td><td><code>display: flex</code>, <code>justify-content</code>, <code>align-items</code>, <code>flex-wrap</code></td></tr>
    <tr><td>Pozycja</td><td><code>position</code>, <code>top</code>, <code>right</code>, <code>bottom</code>, <code>left</code>, <code>z-index</code></td></tr>
    <tr><td>Kursor</td><td><code>cursor</code></td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — CSS w 30 sekund</strong></summary>
  <br>
  <pre><code>* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  color: #1f2937;
  background-color: #f8fafc;
}

main {
  width: 90%;
  max-width: 1100px;
  margin: 0 auto;
}

.kontener {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.karta {
  flex: 1 1 250px;
  padding: 20px;
  border: 1px solid #cbd5e1;
  border-radius: 10px;
}</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="dema"></a>
<h2>17. Gotowe dema do uruchomienia w przeglądarce</h2>

<blockquote>
  <p>🧪 <strong>Instrukcja:</strong> rozwiń przykład, skopiuj cały kod do pustego pliku o podanej nazwie, zapisz go i otwórz w przeglądarce. Zmieniaj wskazane wartości i odświeżaj stronę klawiszem <kbd>F5</kbd>.</p>
</blockquote>

<details>
  <summary><strong>▶ Demo kodu 1 — selektory, tekst i box model | plik: karta.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Karta kursu&lt;/title&gt;
  &lt;style&gt;
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 40px;
      font-family: Arial, sans-serif;
      background-color: #e2e8f0;
      color: #1e293b;
    }

    .karta {
      max-width: 420px;
      margin: 0 auto;
      padding: 24px;
      background-color: white;
      border: 2px solid #2563eb;
      border-radius: 12px;
      box-shadow: 0 6px 18px rgba(0, 0, 0, 0.15);
    }

    .karta h1 {
      margin-top: 0;
      color: #1d4ed8;
    }

    .ważne {
      padding: 10px;
      background-color: #fef3c7;
      border-left: 5px solid #f59e0b;
      font-weight: bold;
    }

    #cena {
      font-size: 24px;
      color: #15803d;
    }

    a {
      display: inline-block;
      padding: 10px 16px;
      color: white;
      background-color: #2563eb;
      text-decoration: none;
      border-radius: 6px;
    }

    a:hover {
      background-color: #1e40af;
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;article class="karta"&gt;
    &lt;h1&gt;Kurs HTML i CSS&lt;/h1&gt;
    &lt;p&gt;Poznaj podstawy tworzenia nowoczesnych stron.&lt;/p&gt;
    &lt;p class="ważne"&gt;Liczba miejsc jest ograniczona!&lt;/p&gt;
    &lt;p id="cena"&gt;Cena: 199 zł&lt;/p&gt;
    &lt;a href="#"&gt;Zapisz się&lt;/a&gt;
  &lt;/article&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>
  <p><strong>Zmiany do pokazania:</strong> modyfikuj <code>padding</code>, <code>margin</code>, <code>border-radius</code>, kolory oraz selektory. Najedź kursorem na przycisk.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 2 — Flexbox i responsywne karty | plik: oferta.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Oferta zajęć&lt;/title&gt;
  &lt;style&gt;
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f8fafc;
      color: #1f2937;
    }

    header {
      padding: 30px;
      text-align: center;
      background-color: #1e3a8a;
      color: white;
    }

    main {
      width: 90%;
      max-width: 1100px;
      margin: 30px auto;
    }

    .karty {
      display: flex;
      justify-content: center;
      align-items: stretch;
      flex-wrap: wrap;
      gap: 20px;
    }

    .karta {
      flex: 1 1 240px;
      max-width: 340px;
      padding: 20px;
      background-color: white;
      border: 1px solid #cbd5e1;
      border-radius: 10px;
    }

    .karta h2 {
      color: #1d4ed8;
    }

    @media (max-width: 600px) {
      header {
        padding: 18px;
      }

      .karty {
        flex-direction: column;
      }

      .karta {
        max-width: none;
      }
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;Oferta zajęć&lt;/h1&gt;
  &lt;/header&gt;

  &lt;main&gt;
    &lt;section class="karty"&gt;
      &lt;article class="karta"&gt;
        &lt;h2&gt;HTML&lt;/h2&gt;
        &lt;p&gt;Struktura i semantyka dokumentu.&lt;/p&gt;
      &lt;/article&gt;

      &lt;article class="karta"&gt;
        &lt;h2&gt;CSS&lt;/h2&gt;
        &lt;p&gt;Kolory, odstępy i układ strony.&lt;/p&gt;
      &lt;/article&gt;

      &lt;article class="karta"&gt;
        &lt;h2&gt;JavaScript&lt;/h2&gt;
        &lt;p&gt;Interakcje oraz dynamiczna treść.&lt;/p&gt;
      &lt;/article&gt;
    &lt;/section&gt;
  &lt;/main&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>
  <p><strong>Zmiany do pokazania:</strong> usuń <code>display: flex</code>, zmieniaj <code>justify-content</code>, wyłącz <code>flex-wrap</code> i zwężaj okno przeglądarki.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 3 — formularz i tabela | plik: zapisy.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Zapisy na zajęcia&lt;/title&gt;
  &lt;style&gt;
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f1f5f9;
      color: #1e293b;
    }

    main {
      width: 90%;
      max-width: 800px;
      margin: 30px auto;
    }

    table {
      width: 100%;
      margin-bottom: 30px;
      border-collapse: collapse;
      background-color: white;
    }

    th,
    td {
      padding: 12px;
      border: 1px solid #64748b;
      text-align: left;
    }

    th {
      background-color: #1e3a8a;
      color: white;
    }

    tbody tr:nth-child(even) {
      background-color: #e2e8f0;
    }

    form {
      padding: 24px;
      background-color: white;
      border-radius: 10px;
    }

    label {
      display: block;
      margin-top: 12px;
      font-weight: bold;
    }

    input,
    select {
      width: 100%;
      padding: 10px;
      border: 1px solid #94a3b8;
      border-radius: 5px;
    }

    input:focus,
    select:focus {
      outline: 3px solid #bfdbfe;
      border-color: #2563eb;
    }

    button {
      margin-top: 18px;
      padding: 11px 20px;
      border: none;
      border-radius: 5px;
      background-color: #15803d;
      color: white;
      cursor: pointer;
    }

    button:hover {
      background-color: #166534;
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;main&gt;
    &lt;h1&gt;Zapisy na warsztaty&lt;/h1&gt;

    &lt;table&gt;
      &lt;thead&gt;
        &lt;tr&gt;
          &lt;th&gt;Grupa&lt;/th&gt;
          &lt;th&gt;Termin&lt;/th&gt;
          &lt;th&gt;Wolne miejsca&lt;/th&gt;
        &lt;/tr&gt;
      &lt;/thead&gt;
      &lt;tbody&gt;
        &lt;tr&gt;&lt;td&gt;HTML&lt;/td&gt;&lt;td&gt;Poniedziałek&lt;/td&gt;&lt;td&gt;5&lt;/td&gt;&lt;/tr&gt;
        &lt;tr&gt;&lt;td&gt;CSS&lt;/td&gt;&lt;td&gt;Środa&lt;/td&gt;&lt;td&gt;3&lt;/td&gt;&lt;/tr&gt;
        &lt;tr&gt;&lt;td&gt;JavaScript&lt;/td&gt;&lt;td&gt;Piątek&lt;/td&gt;&lt;td&gt;8&lt;/td&gt;&lt;/tr&gt;
      &lt;/tbody&gt;
    &lt;/table&gt;

    &lt;form action="#" method="post"&gt;
      &lt;label for="imie"&gt;Imię:&lt;/label&gt;
      &lt;input type="text" id="imie" name="imie" required&gt;

      &lt;label for="email"&gt;E-mail:&lt;/label&gt;
      &lt;input type="email" id="email" name="email" required&gt;

      &lt;label for="grupa"&gt;Wybierz grupę:&lt;/label&gt;
      &lt;select id="grupa" name="grupa"&gt;
        &lt;option value="html"&gt;HTML&lt;/option&gt;
        &lt;option value="css"&gt;CSS&lt;/option&gt;
        &lt;option value="js"&gt;JavaScript&lt;/option&gt;
      &lt;/select&gt;

      &lt;button type="submit"&gt;Zapisz się&lt;/button&gt;
    &lt;/form&gt;
  &lt;/main&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>
  <p><strong>Zmiany do pokazania:</strong> usuń <code>border-collapse</code>, zmień selektor <code>:nth-child(even)</code> na <code>odd</code>, klikaj pola i modyfikuj szerokość formularza.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 4 — błędny CSS do wspólnego poprawienia | plik: znajdz-bledy.html</strong></summary>
  <br>
  <p><strong>Zadanie dla klasy:</strong> uruchom kod bez poprawiania. Poproś uczniów o znalezienie błędów i obserwujcie, które reguły przeglądarka pomija.</p>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Znajdź błędy CSS&lt;/title&gt;
  &lt;style&gt;
    body {
      backgrund-color: #eeeeee;
      font-family Arial, sans-serif;
      margin: 20;
    }

    nagłówek {
      color: blue;
    }

    karta {
      width: 300px;
      padding: 20px;
      border: 3px red;
    }

    #ważne {
      color: green;
    }

    .przycisk {
      background-color: orange
      color: white;
      padding: 10px 20px;
    }

    .przycisk hover {
      background-color: darkorange;
    }
  &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1 class="nagłówek"&gt;Warsztaty CSS&lt;/h1&gt;
  &lt;/header&gt;

  &lt;article class="karta"&gt;
    &lt;p class="ważne"&gt;Zapisy trwają do piątku.&lt;/p&gt;
    &lt;a class="przycisk" href="#"&gt;Zapisz się&lt;/a&gt;
  &lt;/article&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

  <details>
    <summary><strong>✅ Pokaż nauczycielowi listę błędów</strong></summary>
    <ol>
      <li><code>backgrund-color</code> powinno mieć zapis <code>background-color</code>.</li>
      <li>Po <code>font-family</code> brakuje dwukropka.</li>
      <li><code>margin: 20</code> nie ma jednostki <code>px</code>.</li>
      <li>Klasa <code>nagłówek</code> wymaga selektora <code>.nagłówek</code>.</li>
      <li>Klasa <code>karta</code> wymaga selektora <code>.karta</code>.</li>
      <li>W <code>border: 3px red</code> brakuje stylu, np. <code>solid</code>.</li>
      <li>HTML ma <code>class="ważne"</code>, a CSS używa selektora id <code>#ważne</code>.</li>
      <li>Po <code>background-color: orange</code> brakuje średnika.</li>
      <li>Pseudoklasę zapisuje się <code>.przycisk:hover</code>, bez spacji i z dwukropkiem.</li>
    </ol>
  </details>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="zadanie"></a>
<h2>18. Mini zadanie powtórkowe</h2>

<blockquote>
  <p><strong>Cel:</strong> ostyluj stronę szkolnego koła programistycznego zgodnie z wymaganiami przypominającymi polecenia egzaminacyjne.</p>
</blockquote>

<h3>Wymagania</h3>

<ol>
  <li>Utwórz zewnętrzny arkusz <code>styl.css</code> i poprawnie dołącz go do dokumentu HTML.</li>
  <li>Dla całej strony ustaw bezszeryfową czcionkę, jasne tło oraz usuń domyślny margines.</li>
  <li>Nagłówek i stopka mają mieć granatowe tło, biały tekst i wyśrodkowaną zawartość.</li>
  <li>Główna treść ma zajmować <code>90%</code> szerokości, maksymalnie <code>1100px</code>, i być wyśrodkowana.</li>
  <li>Trzy karty kursów ułóż obok siebie za pomocą Flexbox, z odstępem <code>20px</code>.</li>
  <li>Każda karta ma mieć białe tło, wypełnienie, obramowanie i zaokrąglone narożniki.</li>
  <li>Linki nawigacyjne mają być białe i bez podkreślenia, a po najechaniu zmieniać kolor.</li>
  <li>Tabela ma mieć połączone obramowania, kolorowy wiersz nagłówkowy i naprzemienne tła wierszy.</li>
  <li>Pola formularza mają zajmować całą szerokość i zmieniać obramowanie po uzyskaniu fokusu.</li>
  <li>Dla ekranów do <code>700px</code> karty mają układać się jedna pod drugą.</li>
</ol>

<details>
  <summary><strong>💡 Podpowiedzi</strong></summary>
  <ul>
    <li>Do wyśrodkowania głównej treści użyj <code>margin: 0 auto</code>.</li>
    <li>Kontener kart powinien mieć <code>display: flex</code> i <code>flex-wrap: wrap</code>.</li>
    <li>Do stylu aktywnego pola użyj pseudoklasy <code>:focus</code>.</li>
    <li>Naprzemienne wiersze uzyskasz przez <code>:nth-child(even)</code>.</li>
    <li>Układ mobilny umieść wewnątrz <code>@media (max-width: 700px)</code>.</li>
  </ul>
</details>

<details>
  <summary><strong>✅ Kryteria samodzielnego sprawdzenia</strong></summary>
  <ul>
    <li>Arkusz CSS jest zapisany pod właściwą nazwą i poprawnie dołączony.</li>
    <li>W konsoli narzędzi deweloperskich nie ma błędnych ścieżek do zasobów.</li>
    <li>Selektory klas rozpoczynają się kropką, a identyfikatorów znakiem <code>#</code>.</li>
    <li>Odstępy wewnętrzne i zewnętrzne są zgodne z wymaganiami.</li>
    <li>Flexbox działa na szerokim ekranie.</li>
    <li>Układ zmienia się po zwężeniu okna.</li>
    <li>Linki, pola oraz przyciski reagują na <code>:hover</code> lub <code>:focus</code>.</li>
    <li>Wszystkie wymagane kolory, rozmiary i jednostki zgadzają się z poleceniem.</li>
  </ul>
</details>

<hr>

<div align="center">

<h2>🏁 Najważniejsza zasada</h2>

<p><strong>Jeżeli styl nie działa, sprawdź kolejno: zapis pliku → znacznik link → ścieżkę → selektor → składnię deklaracji → specyficzność.</strong></p>

<p><code>element HTML → pasujący selektor → właściwość → wartość → test w przeglądarce</code></p>

<p><a href="#-spis-treści">⬆ Wróć na początek</a></p>

</div>
