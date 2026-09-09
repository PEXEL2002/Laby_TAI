<div align="center">

<h1>🌐 HTML — powtórka do INF.03</h1>

<p><strong>Praktyczne podsumowanie najważniejszych znaczników, atrybutów i zasad wymaganych na egzaminie zawodowym.</strong></p>

<p>
  <img src="https://img.shields.io/badge/INF.03-powtórka-0A66C2" alt="INF.03 — powtórka">
  <img src="https://img.shields.io/badge/HTML5-podstawy-E34F26" alt="HTML5 — podstawy">
  <img src="https://img.shields.io/badge/poziom-podstawowy-2EA44F" alt="Poziom podstawowy">
</p>

<p><em>Otwieraj sekcje, analizuj przykłady i wykonaj zadanie znajdujące się na końcu.</em></p>

</div>

<hr>

<h2>📌 Spis treści</h2>

<ol>
  <li><a href="#czym-jest-html">Czym jest HTML?</a></li>
  <li><a href="#szkielet">Podstawowy szkielet dokumentu</a></li>
  <li><a href="#tekst">Nagłówki i tekst</a></li>
  <li><a href="#listy">Listy</a></li>
  <li><a href="#linki">Linki</a></li>
  <li><a href="#obrazy">Obrazy i tekst alternatywny</a></li>
  <li><a href="#tabele">Tabele</a></li>
  <li><a href="#semantyka">Semantyczne elementy HTML5</a></li>
  <li><a href="#id-class"><code>id</code> i <code>class</code></a></li>
  <li><a href="#formularze">Formularze</a></li>
  <li><a href="#bledy">Najczęstsze błędy na INF.03</a></li>
  <li><a href="#sciaga">Krótka ściąga atrybutów</a></li>
  <li><a href="#dema">Gotowe dema do uruchomienia w przeglądarce</a></li>
  <li><a href="#zadanie">Mini zadanie powtórkowe</a></li>
</ol>

<hr>

<a id="czym-jest-html"></a>
<h2>1. Czym jest HTML?</h2>

<p><strong>HTML</strong> (<em>HyperText Markup Language</em>) to język znaczników służący do opisywania <strong>struktury i znaczenia treści strony internetowej</strong>.</p>

<blockquote>
  <p>💡 HTML odpowiada za strukturę, CSS za wygląd, a JavaScript za zachowanie strony.</p>
</blockquote>

<table>
  <thead>
    <tr>
      <th>Technologia</th>
      <th>Rola</th>
      <th>Przykład</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>HTML</strong></td>
      <td>Struktura i treść</td>
      <td>Nagłówek, akapit, formularz</td>
    </tr>
    <tr>
      <td><strong>CSS</strong></td>
      <td>Wygląd</td>
      <td>Kolory, odstępy, układ</td>
    </tr>
    <tr>
      <td><strong>JavaScript</strong></td>
      <td>Interakcje</td>
      <td>Walidacja, reakcja na kliknięcie</td>
    </tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — budowa znacznika HTML</strong></summary>
  <br>
  <pre><code>&lt;p class="opis"&gt;Treść akapitu&lt;/p&gt;</code></pre>
  <ul>
    <li><code>&lt;p&gt;</code> — znacznik otwierający,</li>
    <li><code>class="opis"</code> — atrybut i jego wartość,</li>
    <li><code>Treść akapitu</code> — zawartość elementu,</li>
    <li><code>&lt;/p&gt;</code> — znacznik zamykający.</li>
  </ul>
</details>

<p><strong>Zapamiętaj:</strong> przeglądarka interpretuje znaczniki i wyświetla wynik. Użytkownik nie widzi kodu HTML, lecz utworzoną na jego podstawie stronę.</p>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="szkielet"></a>
<h2>2. Podstawowy szkielet dokumentu</h2>

<details>
  <summary><strong>▶ Demo kodu — podstawowy szkielet dokumentu</strong></summary>
  <br>
<pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Moja strona&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Witaj na stronie!&lt;/h1&gt;
  &lt;p&gt;To jest pierwszy akapit.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>
</details>

<table>
  <thead>
    <tr>
      <th>Element</th>
      <th>Znaczenie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>&lt;!DOCTYPE html&gt;</code></td>
      <td>Informuje przeglądarkę, że dokument używa HTML5.</td>
    </tr>
    <tr>
      <td><code>&lt;html lang="pl"&gt;</code></td>
      <td>Obejmuje cały dokument; <code>lang</code> określa język treści.</td>
    </tr>
    <tr>
      <td><code>&lt;head&gt;</code></td>
      <td>Zawiera informacje o stronie, których zwykle nie widać w jej treści.</td>
    </tr>
    <tr>
      <td><code>&lt;meta charset="UTF-8"&gt;</code></td>
      <td>Ustawia kodowanie znaków, m.in. poprawną obsługę polskich liter.</td>
    </tr>
    <tr>
      <td><code>&lt;title&gt;</code></td>
      <td>Ustawia tytuł karty przeglądarki.</td>
    </tr>
    <tr>
      <td><code>&lt;body&gt;</code></td>
      <td>Zawiera widoczną treść strony.</td>
    </tr>
  </tbody>
</table>

<details>
  <summary><strong>✅ Lista kontrolna dokumentu</strong></summary>
  <ul>
    <li>Czy plik ma rozszerzenie <code>.html</code>?</li>
    <li>Czy pierwszą deklaracją jest <code>&lt;!DOCTYPE html&gt;</code>?</li>
    <li>Czy ustawiono <code>lang="pl"</code>?</li>
    <li>Czy dokument ma kodowanie <code>UTF-8</code>?</li>
    <li>Czy znacznik <code>&lt;title&gt;</code> zawiera wymagany tytuł?</li>
    <li>Czy elementy widoczne na stronie znajdują się w <code>&lt;body&gt;</code>?</li>
  </ul>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="tekst"></a>
<h2>3. Nagłówki i tekst</h2>

<p>Nagłówki tworzą hierarchię dokumentu. <code>&lt;h1&gt;</code> oznacza najważniejszy nagłówek, a <code>&lt;h6&gt;</code> — nagłówek najniższego poziomu.</p>

<details>
  <summary><strong>▶ Demo kodu — nagłówki i formatowanie tekstu</strong></summary>
  <br>
<pre><code>&lt;h1&gt;Główny tytuł strony&lt;/h1&gt;
&lt;h2&gt;Nazwa sekcji&lt;/h2&gt;
&lt;h3&gt;Nazwa podsekcji&lt;/h3&gt;

&lt;p&gt;To jest zwykły akapit tekstu.&lt;/p&gt;
&lt;p&gt;To jest &lt;strong&gt;ważna informacja&lt;/strong&gt;.&lt;/p&gt;
&lt;p&gt;Ten fragment ma &lt;em&gt;szczególny akcent&lt;/em&gt;.&lt;/p&gt;</code></pre>
</details>

<table>
  <thead>
    <tr>
      <th>Znacznik</th>
      <th>Zastosowanie</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><code>&lt;h1&gt;</code>–<code>&lt;h6&gt;</code></td><td>Nagłówki kolejnych poziomów</td></tr>
    <tr><td><code>&lt;p&gt;</code></td><td>Akapit</td></tr>
    <tr><td><code>&lt;strong&gt;</code></td><td>Treść o dużym znaczeniu, zwykle pogrubiona</td></tr>
    <tr><td><code>&lt;em&gt;</code></td><td>Treść zaakcentowana, zwykle zapisana kursywą</td></tr>
    <tr><td><code>&lt;br&gt;</code></td><td>Przejście do nowego wiersza</td></tr>
    <tr><td><code>&lt;hr&gt;</code></td><td>Tematyczne oddzielenie treści</td></tr>
    <tr><td><code>&lt;sup&gt;</code></td><td>Indeks górny, np. m<sup>2</sup></td></tr>
    <tr><td><code>&lt;sub&gt;</code></td><td>Indeks dolny, np. H<sub>2</sub>O</td></tr>
  </tbody>
</table>

<blockquote>
  <p>⚠️ Nie wybieraj poziomu nagłówka tylko ze względu na jego domyślny rozmiar. Poziomy powinny przedstawiać logiczną hierarchię treści.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="listy"></a>
<h2>4. Listy</h2>

<table>
  <thead>
    <tr>
      <th>Rodzaj listy</th>
      <th>Znaczniki</th>
      <th>Kiedy używać?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Nieuporządkowana</td>
      <td><code>&lt;ul&gt;</code> + <code>&lt;li&gt;</code></td>
      <td>Gdy kolejność punktów nie ma znaczenia</td>
    </tr>
    <tr>
      <td>Uporządkowana</td>
      <td><code>&lt;ol&gt;</code> + <code>&lt;li&gt;</code></td>
      <td>Gdy kolejność jest ważna</td>
    </tr>
    <tr>
      <td>Opisowa</td>
      <td><code>&lt;dl&gt;</code> + <code>&lt;dt&gt;</code> + <code>&lt;dd&gt;</code></td>
      <td>Do par „pojęcie — opis”</td>
    </tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — listy</strong></summary>
  <br>
  <pre><code>&lt;ul&gt;
  &lt;li&gt;HTML&lt;/li&gt;
  &lt;li&gt;CSS&lt;/li&gt;
  &lt;li&gt;JavaScript&lt;/li&gt;
&lt;/ul&gt;

&lt;ol&gt;
  &lt;li&gt;Otwórz edytor.&lt;/li&gt;
  &lt;li&gt;Utwórz plik index.html.&lt;/li&gt;
  &lt;li&gt;Uruchom stronę w przeglądarce.&lt;/li&gt;
&lt;/ol&gt;

&lt;dl&gt;
  &lt;dt&gt;HTML&lt;/dt&gt;
  &lt;dd&gt;Język opisu struktury strony.&lt;/dd&gt;
&lt;/dl&gt;</code></pre>
</details>

<p><strong>Ważne:</strong> elementy listy umieszczaj w znacznikach <code>&lt;li&gt;</code>. Nie wpisuj punktów bezpośrednio do <code>&lt;ul&gt;</code> lub <code>&lt;ol&gt;</code>.</p>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="linki"></a>
<h2>5. Linki</h2>

<details>
  <summary><strong>▶ Demo kodu — linki</strong></summary>
  <br>
<pre><code>&lt;a href="https://www.cke.gov.pl/"&gt;Strona CKE&lt;/a&gt;

&lt;a href="kontakt.html"&gt;Przejdź do kontaktu&lt;/a&gt;

&lt;a href="#formularz"&gt;Przejdź do formularza&lt;/a&gt;

&lt;a href="mailto:sekretariat@example.com"&gt;Napisz wiadomość&lt;/a&gt;</code></pre>
</details>

<p>Atrybut <code>href</code> wskazuje cel odnośnika. Tekst pomiędzy <code>&lt;a&gt;</code> i <code>&lt;/a&gt;</code> powinien jasno informować, dokąd prowadzi link.</p>

<details>
  <summary><strong>🧭 Ścieżka względna czy bezwzględna?</strong></summary>
  <br>
  <table>
    <thead>
      <tr><th>Rodzaj</th><th>Przykład</th><th>Zastosowanie</th></tr>
    </thead>
    <tbody>
      <tr><td>Względna</td><td><code>podstrony/oferta.html</code></td><td>Plik wewnątrz projektu</td></tr>
      <tr><td>Względna — katalog wyżej</td><td><code>../index.html</code></td><td>Powrót o jeden poziom katalogów</td></tr>
      <tr><td>Bezwzględna</td><td><code>https://example.com</code></td><td>Zewnętrzna strona WWW</td></tr>
    </tbody>
  </table>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="obrazy"></a>
<h2>6. Obrazy i tekst alternatywny</h2>

<details>
  <summary><strong>▶ Demo kodu — obraz z tekstem alternatywnym</strong></summary>
  <br>
  <pre><code>&lt;img src="obrazy/logo.png" alt="Logo firmy KwiatPol"&gt;</code></pre>
</details>

<table>
  <thead>
    <tr><th>Atrybut</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>src</code></td><td>Ścieżka do pliku obrazu</td></tr>
    <tr><td><code>alt</code></td><td>Tekst opisujący znaczenie lub zawartość obrazu</td></tr>
    <tr><td><code>width</code></td><td>Szerokość obrazu</td></tr>
    <tr><td><code>height</code></td><td>Wysokość obrazu</td></tr>
  </tbody>
</table>

<p><strong>Dobry tekst <code>alt</code>:</strong> krótko przekazuje to, co jest istotne w obrazie. Jest używany m.in. przez czytniki ekranu i pojawia się, gdy pliku nie można wyświetlić.</p>

<details>
  <summary><strong>✅ Dobre i złe przykłady</strong></summary>
  <br>
  <table>
    <thead>
      <tr><th>Ocena</th><th>Kod</th><th>Dlaczego?</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>✅</td>
        <td><code>&lt;img src="wykres.png" alt="Wykres sprzedaży w latach 2024–2026"&gt;</code></td>
        <td>Opisuje informację przedstawioną na obrazie.</td>
      </tr>
      <tr>
        <td>❌</td>
        <td><code>&lt;img src="wykres.png" alt="obrazek"&gt;</code></td>
        <td>Tekst nie mówi, co znajduje się na obrazie.</td>
      </tr>
      <tr>
        <td>❌</td>
        <td><code>&lt;img src="wykres.png"&gt;</code></td>
        <td>Brakuje wymaganego atrybutu <code>alt</code>.</td>
      </tr>
    </tbody>
  </table>
  <p>Dla obrazu wyłącznie dekoracyjnego stosuje się pusty tekst alternatywny: <code>alt=""</code>.</p>
</details>

<blockquote>
  <p>⚠️ Na egzaminie przepisz dokładnie wskazaną nazwę pliku i wymagany tekst alternatywny. Wielkość liter oraz rozszerzenie mogą mieć znaczenie.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="tabele"></a>
<h2>7. Tabele</h2>

<p>Tabela służy do przedstawiania <strong>danych tabelarycznych</strong>, a nie do budowania układu strony.</p>

<details>
  <summary><strong>▶ Demo kodu — kompletna tabela</strong></summary>
  <br>
<pre><code>&lt;table&gt;
  &lt;caption&gt;Wyniki egzaminu próbnego&lt;/caption&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th scope="col"&gt;Uczeń&lt;/th&gt;
      &lt;th scope="col"&gt;Wynik&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;Anna&lt;/td&gt;
      &lt;td&gt;82%&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;Marek&lt;/td&gt;
      &lt;td&gt;76%&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;</code></pre>
</details>

<table>
  <thead>
    <tr><th>Znacznik / atrybut</th><th>Znaczenie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>&lt;table&gt;</code></td><td>Cała tabela</td></tr>
    <tr><td><code>&lt;caption&gt;</code></td><td>Tytuł lub opis tabeli</td></tr>
    <tr><td><code>&lt;thead&gt;</code></td><td>Sekcja nagłówkowa</td></tr>
    <tr><td><code>&lt;tbody&gt;</code></td><td>Sekcja z głównymi danymi</td></tr>
    <tr><td><code>&lt;tfoot&gt;</code></td><td>Sekcja podsumowania</td></tr>
    <tr><td><code>&lt;tr&gt;</code></td><td>Wiersz</td></tr>
    <tr><td><code>&lt;th&gt;</code></td><td>Komórka nagłówkowa</td></tr>
    <tr><td><code>&lt;td&gt;</code></td><td>Komórka danych</td></tr>
    <tr><td><code>colspan</code></td><td>Łączenie komórek w poziomie</td></tr>
    <tr><td><code>rowspan</code></td><td>Łączenie komórek w pionie</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — łączenie komórek</strong></summary>
  <br>
  <pre><code>&lt;tr&gt;
  &lt;th colspan="2"&gt;Dane kontaktowe&lt;/th&gt;
&lt;/tr&gt;
&lt;tr&gt;
  &lt;td&gt;Telefon&lt;/td&gt;
  &lt;td&gt;123 456 789&lt;/td&gt;
&lt;/tr&gt;</code></pre>
  <p><code>colspan="2"</code> oznacza, że komórka zajmuje miejsce dwóch kolumn.</p>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="semantyka"></a>
<h2>8. Semantyczne elementy HTML5</h2>

<p>Znacznik semantyczny opisuje <strong>rolę treści</strong>. Dzięki temu kod jest czytelniejszy dla programisty, wyszukiwarki i technologii wspomagających.</p>

<details>
  <summary><strong>▶ Demo kodu — semantyczny układ strony HTML5</strong></summary>
  <br>
<pre><code>&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;Kwiaciarnia Róża&lt;/h1&gt;
  &lt;/header&gt;

  &lt;nav&gt;
    &lt;a href="index.html"&gt;Start&lt;/a&gt;
    &lt;a href="oferta.html"&gt;Oferta&lt;/a&gt;
  &lt;/nav&gt;

  &lt;main&gt;
    &lt;section&gt;
      &lt;h2&gt;Aktualności&lt;/h2&gt;
      &lt;article&gt;
        &lt;h3&gt;Nowa dostawa róż&lt;/h3&gt;
        &lt;p&gt;Zapraszamy od poniedziałku.&lt;/p&gt;
      &lt;/article&gt;
    &lt;/section&gt;

    &lt;aside&gt;Promocja tygodnia&lt;/aside&gt;
  &lt;/main&gt;

  &lt;footer&gt;
    &lt;p&gt;Autor strony: Jan Kowalski&lt;/p&gt;
  &lt;/footer&gt;
&lt;/body&gt;</code></pre>
</details>

<table>
  <thead>
    <tr><th>Element</th><th>Typowa rola</th></tr>
  </thead>
  <tbody>
    <tr><td><code>&lt;header&gt;</code></td><td>Nagłówek strony lub sekcji</td></tr>
    <tr><td><code>&lt;nav&gt;</code></td><td>Główna nawigacja</td></tr>
    <tr><td><code>&lt;main&gt;</code></td><td>Główna, unikalna treść dokumentu</td></tr>
    <tr><td><code>&lt;section&gt;</code></td><td>Tematyczna sekcja treści</td></tr>
    <tr><td><code>&lt;article&gt;</code></td><td>Samodzielna treść, np. wpis lub wiadomość</td></tr>
    <tr><td><code>&lt;aside&gt;</code></td><td>Treść uzupełniająca lub poboczna</td></tr>
    <tr><td><code>&lt;footer&gt;</code></td><td>Stopka strony lub sekcji</td></tr>
    <tr><td><code>&lt;figure&gt;</code></td><td>Samodzielna ilustracja, wykres lub przykład</td></tr>
    <tr><td><code>&lt;figcaption&gt;</code></td><td>Podpis elementu <code>&lt;figure&gt;</code></td></tr>
  </tbody>
</table>

<blockquote>
  <p>💡 <code>&lt;div&gt;</code> nie niesie informacji o znaczeniu. Używaj go, gdy nie istnieje lepszy element semantyczny.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="id-class"></a>
<h2>9. <code>id</code> i <code>class</code></h2>

<table>
  <thead>
    <tr><th>Cecha</th><th><code>id</code></th><th><code>class</code></th></tr>
  </thead>
  <tbody>
    <tr><td>Przeznaczenie</td><td>Unikalny identyfikator elementu</td><td>Wspólna nazwa grupy elementów</td></tr>
    <tr><td>Powtarzanie w dokumencie</td><td>Nie — wartość powinna być unikalna</td><td>Tak</td></tr>
    <tr><td>Przykład</td><td><code>id="kontakt"</code></td><td><code>class="ważne"</code></td></tr>
    <tr><td>Odwołanie w CSS</td><td><code>#kontakt</code></td><td><code>.ważne</code></td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — zastosowanie id i class</strong></summary>
  <br>
<pre><code>&lt;section id="kontakt"&gt;
  &lt;h2&gt;Kontakt&lt;/h2&gt;
  &lt;p class="ważne"&gt;Odpowiadamy w ciągu 24 godzin.&lt;/p&gt;
&lt;/section&gt;

&lt;p class="ważne"&gt;Telefon alarmowy działa całą dobę.&lt;/p&gt;

&lt;a href="#kontakt"&gt;Przejdź do kontaktu&lt;/a&gt;</code></pre>
</details>

<details>
  <summary><strong>🧠 Sposób na zapamiętanie</strong></summary>
  <ul>
    <li><strong>ID</strong> przypomina numer dokumentu — identyfikuje konkretny element.</li>
    <li><strong>Class</strong> oznacza klasę, czyli grupę elementów o wspólnej cesze.</li>
    <li>Element może mieć kilka klas: <code>class="karta promocja"</code>.</li>
  </ul>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="formularze"></a>
<h2>10. Formularze</h2>

<details>
  <summary><strong>▶ Demo kodu — kompletny formularz</strong></summary>
  <br>
<pre><code>&lt;form action="zapisz.php" method="post"&gt;
  &lt;fieldset&gt;
    &lt;legend&gt;Formularz kontaktowy&lt;/legend&gt;

    &lt;label for="imie"&gt;Imię:&lt;/label&gt;
    &lt;input type="text" id="imie" name="imie" required&gt;

    &lt;label for="email"&gt;E-mail:&lt;/label&gt;
    &lt;input type="email" id="email" name="email" required&gt;

    &lt;label for="temat"&gt;Temat:&lt;/label&gt;
    &lt;select id="temat" name="temat"&gt;
      &lt;option value="oferta"&gt;Pytanie o ofertę&lt;/option&gt;
      &lt;option value="reklamacja"&gt;Reklamacja&lt;/option&gt;
    &lt;/select&gt;

    &lt;label for="wiadomosc"&gt;Wiadomość:&lt;/label&gt;
    &lt;textarea id="wiadomosc" name="wiadomosc" rows="5"&gt;&lt;/textarea&gt;

    &lt;input type="checkbox" id="zgoda" name="zgoda" required&gt;
    &lt;label for="zgoda"&gt;Akceptuję regulamin&lt;/label&gt;

    &lt;button type="submit"&gt;Wyślij&lt;/button&gt;
    &lt;button type="reset"&gt;Wyczyść&lt;/button&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;</code></pre>
</details>

<h3>Najważniejsze elementy formularza</h3>

<table>
  <thead>
    <tr><th>Element</th><th>Zastosowanie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>&lt;form&gt;</code></td><td>Obejmuje cały formularz</td></tr>
    <tr><td><code>&lt;label&gt;</code></td><td>Opisuje pole; <code>for</code> wskazuje jego <code>id</code></td></tr>
    <tr><td><code>&lt;input&gt;</code></td><td>Pole wejściowe różnego typu</td></tr>
    <tr><td><code>&lt;textarea&gt;</code></td><td>Wielowierszowe pole tekstowe</td></tr>
    <tr><td><code>&lt;select&gt;</code></td><td>Lista rozwijana</td></tr>
    <tr><td><code>&lt;option&gt;</code></td><td>Jedna opcja listy</td></tr>
    <tr><td><code>&lt;button&gt;</code></td><td>Przycisk wykonujący określoną akcję</td></tr>
    <tr><td><code>&lt;fieldset&gt;</code></td><td>Grupuje powiązane pola</td></tr>
    <tr><td><code>&lt;legend&gt;</code></td><td>Opisuje grupę <code>&lt;fieldset&gt;</code></td></tr>
  </tbody>
</table>

<details open>
  <summary><strong>⌨️ Przydatne typy <code>input</code></strong></summary>
  <br>
  <table>
    <thead>
      <tr><th>Typ</th><th>Przeznaczenie</th></tr>
    </thead>
    <tbody>
      <tr><td><code>text</code></td><td>Krótki tekst</td></tr>
      <tr><td><code>password</code></td><td>Hasło</td></tr>
      <tr><td><code>email</code></td><td>Adres e-mail</td></tr>
      <tr><td><code>number</code></td><td>Liczba</td></tr>
      <tr><td><code>date</code></td><td>Data</td></tr>
      <tr><td><code>radio</code></td><td>Jeden wybór z grupy</td></tr>
      <tr><td><code>checkbox</code></td><td>Niezależne pole wyboru</td></tr>
      <tr><td><code>file</code></td><td>Wybór pliku</td></tr>
      <tr><td><code>submit</code></td><td>Wysłanie formularza</td></tr>
      <tr><td><code>reset</code></td><td>Przywrócenie wartości początkowych</td></tr>
    </tbody>
  </table>
</details>

<h3><code>GET</code> a <code>POST</code></h3>

<table>
  <thead>
    <tr><th>Metoda</th><th>Co dzieje się z danymi?</th><th>Typowe użycie</th></tr>
  </thead>
  <tbody>
    <tr><td><code>GET</code></td><td>Dane trafiają do adresu URL.</td><td>Wyszukiwanie, filtrowanie, odczyt</td></tr>
    <tr><td><code>POST</code></td><td>Dane są przesyłane w treści żądania.</td><td>Logowanie, rejestracja, zapis zmian</td></tr>
  </tbody>
</table>

<blockquote>
  <p>⚠️ Pole bez atrybutu <code>name</code> nie zostanie poprawnie przesłane jako część danych formularza. Atrybut <code>id</code> służy m.in. do połączenia pola z etykietą, a <code>name</code> określa nazwę przesyłanej wartości.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="bledy"></a>
<h2>11. Najczęstsze błędy na INF.03 / CKE</h2>

<table>
  <thead>
    <tr><th>❌ Błąd</th><th>✅ Jak go uniknąć?</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>Niepoprawna nazwa lub rozszerzenie pliku</td>
      <td>Przepisz nazwę dokładnie z arkusza, np. <code>index.html</code>, a nie <code>Index.htm</code>.</td>
    </tr>
    <tr>
      <td>Zła ścieżka do obrazu albo podstrony</td>
      <td>Sprawdź strukturę katalogów i nie używaj ścieżki z własnego komputera, np. <code>C:\...</code>.</td>
    </tr>
    <tr>
      <td>Brak <code>alt</code> przy obrazie</td>
      <td>Dodaj dokładnie taki tekst alternatywny, jakiego wymaga arkusz.</td>
    </tr>
    <tr>
      <td>Brak znacznika zamykającego</td>
      <td>Kontroluj pary, np. <code>&lt;p&gt;...&lt;/p&gt;</code>.</td>
    </tr>
    <tr>
      <td>Niepoprawne zagnieżdżenie</td>
      <td>Zamykaj elementy w odwrotnej kolejności: <code>&lt;strong&gt;&lt;em&gt;tekst&lt;/em&gt;&lt;/strong&gt;</code>.</td>
    </tr>
    <tr>
      <td>Powtórzone wartości <code>id</code></td>
      <td>Każdemu identyfikatorowi przypisz tylko jeden element.</td>
    </tr>
    <tr>
      <td>Brak <code>name</code> w polu formularza</td>
      <td>Dodaj <code>name</code>, jeśli wartość pola ma zostać wysłana.</td>
    </tr>
    <tr>
      <td>Etykieta nie jest powiązana z polem</td>
      <td>Ustaw taką samą wartość w <code>for</code> etykiety i <code>id</code> pola.</td>
    </tr>
    <tr>
      <td>Użycie <code>&lt;br&gt;</code> do tworzenia odstępów</td>
      <td><code>&lt;br&gt;</code> służy do złamania wiersza; odstępy ustawia się w CSS.</td>
    </tr>
    <tr>
      <td>Wykonanie „podobnie” zamiast zgodnie z poleceniem</td>
      <td>Realizuj wymagania punkt po punkcie i używaj wskazanych elementów oraz wartości.</td>
    </tr>
  </tbody>
</table>

<details open>
  <summary><strong>📝 Kontrola przed oddaniem pracy</strong></summary>
  <ul>
    <li>Porównaj nazwy plików, katalogów i treść elementów z arkuszem.</li>
    <li>Otwórz każdą podstronę w przeglądarce.</li>
    <li>Kliknij wszystkie linki i przyciski.</li>
    <li>Sprawdź, czy każdy obraz się wyświetla.</li>
    <li>Sprawdź polskie znaki.</li>
    <li>Przetestuj formularz i jego wymagane pola.</li>
    <li>Sprawdź, czy znaczniki są poprawnie zagnieżdżone i zamknięte.</li>
    <li>Zapisz wszystkie pliki w wymaganym miejscu.</li>
  </ul>
</details>

<blockquote>
  <p>🎯 Na egzaminie najpierw spełniaj wymagania arkusza. Dodatkowe elementy nie zastępują brakującego wymaganego znacznika, tekstu lub atrybutu.</p>
</blockquote>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="sciaga"></a>
<h2>12. Krótka ściąga atrybutów</h2>

<table>
  <thead>
    <tr><th>Atrybut</th><th>Najczęściej używany z</th><th>Znaczenie / przykład</th></tr>
  </thead>
  <tbody>
    <tr><td><code>href</code></td><td><code>&lt;a&gt;</code></td><td>Cel linku: <code>href="oferta.html"</code></td></tr>
    <tr><td><code>src</code></td><td><code>&lt;img&gt;</code></td><td>Źródło zasobu: <code>src="logo.png"</code></td></tr>
    <tr><td><code>alt</code></td><td><code>&lt;img&gt;</code></td><td>Tekst alternatywny obrazu</td></tr>
    <tr><td><code>id</code></td><td>większość elementów</td><td>Unikalny identyfikator</td></tr>
    <tr><td><code>class</code></td><td>większość elementów</td><td>Jedna lub więcej klas elementu</td></tr>
    <tr><td><code>lang</code></td><td><code>&lt;html&gt;</code></td><td>Język dokumentu: <code>lang="pl"</code></td></tr>
    <tr><td><code>title</code></td><td>większość elementów</td><td>Dodatkowa informacja o elemencie</td></tr>
    <tr><td><code>type</code></td><td><code>&lt;input&gt;</code>, <code>&lt;button&gt;</code></td><td>Typ pola lub przycisku</td></tr>
    <tr><td><code>name</code></td><td>pola formularza</td><td>Nazwa przesyłanej wartości</td></tr>
    <tr><td><code>value</code></td><td>pola formularza, <code>&lt;option&gt;</code></td><td>Wartość elementu</td></tr>
    <tr><td><code>for</code></td><td><code>&lt;label&gt;</code></td><td>Wskazuje <code>id</code> opisywanego pola</td></tr>
    <tr><td><code>required</code></td><td>pola formularza</td><td>Oznacza pole wymagane</td></tr>
    <tr><td><code>placeholder</code></td><td><code>&lt;input&gt;</code>, <code>&lt;textarea&gt;</code></td><td>Krótka podpowiedź w pustym polu</td></tr>
    <tr><td><code>checked</code></td><td><code>checkbox</code>, <code>radio</code></td><td>Domyślnie zaznaczona opcja</td></tr>
    <tr><td><code>selected</code></td><td><code>&lt;option&gt;</code></td><td>Domyślnie wybrana opcja</td></tr>
    <tr><td><code>action</code></td><td><code>&lt;form&gt;</code></td><td>Adres odbierający dane formularza</td></tr>
    <tr><td><code>method</code></td><td><code>&lt;form&gt;</code></td><td>Metoda wysyłania: <code>get</code> lub <code>post</code></td></tr>
    <tr><td><code>colspan</code></td><td><code>&lt;td&gt;</code>, <code>&lt;th&gt;</code></td><td>Liczba połączonych kolumn</td></tr>
    <tr><td><code>rowspan</code></td><td><code>&lt;td&gt;</code>, <code>&lt;th&gt;</code></td><td>Liczba połączonych wierszy</td></tr>
  </tbody>
</table>

<details>
  <summary><strong>▶ Demo kodu — HTML w 30 sekund</strong></summary>
  <br>
  <pre><code>&lt;h1&gt;Najważniejszy nagłówek&lt;/h1&gt;
&lt;p&gt;Akapit z &lt;strong&gt;ważnym tekstem&lt;/strong&gt;.&lt;/p&gt;
&lt;a href="strona.html"&gt;Link&lt;/a&gt;
&lt;img src="obraz.jpg" alt="Opis obrazu"&gt;
&lt;ul&gt;&lt;li&gt;Punkt listy&lt;/li&gt;&lt;/ul&gt;
&lt;input type="text" id="nazwa" name="nazwa" required&gt;</code></pre>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="dema"></a>
<h2>13. Gotowe dema do uruchomienia w przeglądarce</h2>

<blockquote>
  <p>🧪 <strong>Jak prowadzić pokaz?</strong> Rozwiń wybrane „Demo kodu”, skopiuj całość do nowego pliku o podanej nazwie, zapisz plik i otwórz go w przeglądarce. Następnie zmieniaj kod razem z uczniami i odświeżaj stronę klawiszem <kbd>F5</kbd>.</p>
</blockquote>

<details>
  <summary><strong>▶ Demo kodu 1 — tekst, listy i linki | plik: tekst-listy.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Tekst, listy i linki&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;Koło programistyczne&lt;/h1&gt;
    &lt;p&gt;Uczymy się tworzyć &lt;strong&gt;strony internetowe&lt;/strong&gt;.&lt;/p&gt;
  &lt;/header&gt;

  &lt;main&gt;
    &lt;section&gt;
      &lt;h2&gt;Czego się uczymy?&lt;/h2&gt;
      &lt;ul&gt;
        &lt;li&gt;HTML — struktura strony&lt;/li&gt;
        &lt;li&gt;CSS — wygląd strony&lt;/li&gt;
        &lt;li&gt;JavaScript — interakcje&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/section&gt;

    &lt;section&gt;
      &lt;h2&gt;Jak dołączyć?&lt;/h2&gt;
      &lt;ol&gt;
        &lt;li&gt;Przeczytaj informacje.&lt;/li&gt;
        &lt;li&gt;Wypełnij formularz.&lt;/li&gt;
        &lt;li&gt;Przyjdź na spotkanie.&lt;/li&gt;
      &lt;/ol&gt;
      &lt;p&gt;&lt;a href="https://www.cke.gov.pl/"&gt;Odwiedź stronę CKE&lt;/a&gt;&lt;/p&gt;
    &lt;/section&gt;
  &lt;/main&gt;

  &lt;footer&gt;
    &lt;p&gt;Autor: Jan Kowalski&lt;/p&gt;
  &lt;/footer&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

  <p><strong>Zmiany do pokazania:</strong> zamień listę <code>&lt;ul&gt;</code> na <code>&lt;ol&gt;</code>, dodaj nagłówek <code>&lt;h3&gt;</code>, zmień tekst linku i utwórz drugi akapit.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 2 — obraz, tabela i semantyka | plik: oferta.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Oferta kursów&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;Akademia WWW&lt;/h1&gt;
  &lt;/header&gt;

  &lt;nav&gt;
    &lt;a href="#oferta"&gt;Oferta&lt;/a&gt; |
    &lt;a href="#plan"&gt;Plan zajęć&lt;/a&gt;
  &lt;/nav&gt;

  &lt;main&gt;
    &lt;section id="oferta"&gt;
      &lt;h2&gt;Nasza oferta&lt;/h2&gt;
      &lt;figure&gt;
        &lt;img
          src="https://www.w3.org/html/logo/downloads/HTML5_Badge_128.png"
          alt="Pomarańczowe logo HTML5"&gt;
        &lt;figcaption&gt;HTML5 — podstawa stron internetowych&lt;/figcaption&gt;
      &lt;/figure&gt;
    &lt;/section&gt;

    &lt;section id="plan"&gt;
      &lt;h2&gt;Plan zajęć&lt;/h2&gt;
      &lt;table&gt;
        &lt;caption&gt;Spotkania we wrześniu&lt;/caption&gt;
        &lt;thead&gt;
          &lt;tr&gt;
            &lt;th scope="col"&gt;Dzień&lt;/th&gt;
            &lt;th scope="col"&gt;Godzina&lt;/th&gt;
            &lt;th scope="col"&gt;Temat&lt;/th&gt;
          &lt;/tr&gt;
        &lt;/thead&gt;
        &lt;tbody&gt;
          &lt;tr&gt;
            &lt;td&gt;Poniedziałek&lt;/td&gt;
            &lt;td&gt;15:00&lt;/td&gt;
            &lt;td&gt;Podstawy HTML&lt;/td&gt;
          &lt;/tr&gt;
          &lt;tr&gt;
            &lt;td&gt;Środa&lt;/td&gt;
            &lt;td&gt;16:00&lt;/td&gt;
            &lt;td&gt;Formularze&lt;/td&gt;
          &lt;/tr&gt;
        &lt;/tbody&gt;
      &lt;/table&gt;
    &lt;/section&gt;
  &lt;/main&gt;

  &lt;footer&gt;
    &lt;p&gt;Akademia WWW — 2026&lt;/p&gt;
  &lt;/footer&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

  <p><strong>Zmiany do pokazania:</strong> usuń na chwilę <code>alt</code>, dodaj trzeci wiersz tabeli, zmień <code>id</code> sekcji i sprawdź, co stanie się z linkiem nawigacyjnym.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 3 — kompletny formularz | plik: zapisy.html</strong></summary>
  <br>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="pl"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
  &lt;title&gt;Zapisy na zajęcia&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;header&gt;
    &lt;h1&gt;Zapisy na koło programistyczne&lt;/h1&gt;
  &lt;/header&gt;

  &lt;main&gt;
    &lt;form action="odbierz.php" method="post"&gt;
      &lt;fieldset&gt;
        &lt;legend&gt;Dane uczestnika&lt;/legend&gt;

        &lt;p&gt;
          &lt;label for="imie"&gt;Imię:&lt;/label&gt;
          &lt;input type="text" id="imie" name="imie" required&gt;
        &lt;/p&gt;

        &lt;p&gt;
          &lt;label for="email"&gt;E-mail:&lt;/label&gt;
          &lt;input type="email" id="email" name="email" required&gt;
        &lt;/p&gt;

        &lt;p&gt;
          &lt;label for="klasa"&gt;Klasa:&lt;/label&gt;
          &lt;select id="klasa" name="klasa"&gt;
            &lt;option value="1"&gt;Klasa pierwsza&lt;/option&gt;
            &lt;option value="2"&gt;Klasa druga&lt;/option&gt;
            &lt;option value="3"&gt;Klasa trzecia&lt;/option&gt;
          &lt;/select&gt;
        &lt;/p&gt;

        &lt;p&gt;Preferowany termin:&lt;/p&gt;
        &lt;p&gt;
          &lt;input type="radio" id="poniedzialek" name="termin" value="poniedzialek" checked&gt;
          &lt;label for="poniedzialek"&gt;Poniedziałek&lt;/label&gt;

          &lt;input type="radio" id="sroda" name="termin" value="sroda"&gt;
          &lt;label for="sroda"&gt;Środa&lt;/label&gt;
        &lt;/p&gt;

        &lt;p&gt;
          &lt;label for="uwagi"&gt;Uwagi:&lt;/label&gt;&lt;br&gt;
          &lt;textarea id="uwagi" name="uwagi" rows="4" cols="40"&gt;&lt;/textarea&gt;
        &lt;/p&gt;

        &lt;p&gt;
          &lt;input type="checkbox" id="zgoda" name="zgoda" required&gt;
          &lt;label for="zgoda"&gt;Akceptuję regulamin&lt;/label&gt;
        &lt;/p&gt;

        &lt;button type="submit"&gt;Zapisz mnie&lt;/button&gt;
        &lt;button type="reset"&gt;Wyczyść formularz&lt;/button&gt;
      &lt;/fieldset&gt;
    &lt;/form&gt;
  &lt;/main&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

  <p><strong>Zmiany do pokazania:</strong> usuń <code>required</code> i porównaj walidację, zmień <code>type="email"</code> na <code>text</code>, kliknij etykietę pola oraz sprawdź działanie przycisku resetującego.</p>
</details>

<br>

<details>
  <summary><strong>▶ Demo kodu 4 — strona błędna do wspólnego poprawienia | plik: znajdz-bledy.html</strong></summary>
  <br>
  <p><strong>Zadanie dla klasy:</strong> skopiuj kod bez poprawiania. Uruchom go, a następnie poproś uczniów o znalezienie co najmniej ośmiu błędów.</p>

  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Galeria szkolna&lt;h1&gt;
  &lt;p&gt;&lt;strong&gt;Zdjęcia z wycieczki&lt;/p&gt;&lt;/strong&gt;

  &lt;img src="obrazy/Wycieczka.JPG"&gt;

  &lt;ul&gt;
    Kraków
    &lt;li&gt;Warszawa&lt;/li&gt;
  &lt;/ul&gt;

  &lt;a&gt;Zobacz plan wycieczki&lt;/a&gt;

  &lt;section id="kontakt"&gt;
    &lt;h2&gt;Kontakt&lt;/h2&gt;
  &lt;/section&gt;
  &lt;section id="kontakt"&gt;
    &lt;h2&gt;Formularz&lt;/h2&gt;
    &lt;form&gt;
      &lt;label for="email"&gt;E-mail:&lt;/label&gt;
      &lt;input type="text" id="adres" required&gt;
      &lt;button&gt;Wyślij&lt;/button&gt;
    &lt;/form&gt;
  &lt;/section&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

  <details>
    <summary><strong>✅ Pokaż nauczycielowi listę błędów</strong></summary>
    <ol>
      <li>Brakuje <code>lang="pl"</code> w elemencie <code>&lt;html&gt;</code>.</li>
      <li>Znacznik <code>&lt;title&gt;</code> jest pusty.</li>
      <li>Nagłówek <code>&lt;h1&gt;</code> nie został poprawnie zamknięty.</li>
      <li>Elementy <code>&lt;p&gt;</code> i <code>&lt;strong&gt;</code> są źle zagnieżdżone.</li>
      <li>Obraz nie ma atrybutu <code>alt</code>.</li>
      <li>Trzeba sprawdzić wielkość liter i nazwę pliku <code>Wycieczka.JPG</code>.</li>
      <li>Tekst <code>Kraków</code> nie znajduje się w elemencie <code>&lt;li&gt;</code>.</li>
      <li>Link nie ma atrybutu <code>href</code>.</li>
      <li>Wartość <code>id="kontakt"</code> została użyta dwa razy.</li>
      <li><code>for="email"</code> etykiety nie zgadza się z <code>id="adres"</code> pola.</li>
      <li>Pole formularza nie ma atrybutu <code>name</code>.</li>
      <li>Dla adresu e-mail lepszy jest typ <code>email</code> zamiast <code>text</code>.</li>
      <li>Formularz nie określa <code>action</code> ani <code>method</code>.</li>
      <li>Przycisk powinien mieć jawny <code>type="submit"</code>.</li>
    </ol>
  </details>
</details>

<p align="right"><a href="#-spis-treści">⬆ Wróć do spisu treści</a></p>

<hr>

<a id="zadanie"></a>
<h2>14. Mini zadanie powtórkowe</h2>

<blockquote>
  <p><strong>Cel:</strong> przygotuj jedną poprawną semantycznie stronę HTML dla szkolnego koła programistycznego.</p>
</blockquote>

<h3>Treść zadania</h3>

<p>Utwórz plik <code>index.html</code>, który zawiera:</p>

<ol>
  <li>pełny szkielet dokumentu HTML5, język polski i kodowanie UTF-8,</li>
  <li>tytuł karty: <code>Koło programistyczne</code>,</li>
  <li>semantyczny nagłówek strony z nagłówkiem <code>h1</code>,</li>
  <li>nawigację z linkami do sekcji <code>O nas</code>, <code>Plan spotkań</code> i <code>Zapisy</code>,</li>
  <li>sekcję z akapitem, listą umiejętności i obrazem <code>programowanie.jpg</code>,</li>
  <li>obraz z sensownym tekstem alternatywnym,</li>
  <li>tabelę planu spotkań z nagłówkami <code>Dzień</code>, <code>Godzina</code> i <code>Temat</code>,</li>
  <li>formularz z polami: imię, e-mail, poziom klasy i zgoda na regulamin,</li>
  <li>poprawnie połączone etykiety i pola formularza,</li>
  <li>przycisk wysyłający oraz stopkę z imieniem i nazwiskiem autora.</li>
</ol>

<details>
  <summary><strong>💡 Podpowiedzi</strong></summary>
  <ul>
    <li>Użyj elementów <code>&lt;header&gt;</code>, <code>&lt;nav&gt;</code>, <code>&lt;main&gt;</code>, <code>&lt;section&gt;</code> i <code>&lt;footer&gt;</code>.</li>
    <li>Nadaj sekcjom unikalne wartości <code>id</code>, a następnie połącz je z linkami <code>href="#..."</code>.</li>
    <li>W tabeli użyj <code>&lt;thead&gt;</code>, <code>&lt;tbody&gt;</code>, <code>&lt;th&gt;</code> i <code>&lt;td&gt;</code>.</li>
    <li>Każde pole formularza, którego wartość ma zostać wysłana, powinno mieć <code>name</code>.</li>
  </ul>
</details>

<details>
  <summary><strong>✅ Kryteria samodzielnego sprawdzenia</strong></summary>
  <ul>
    <li>Strona otwiera się bez błędów, a polskie znaki są widoczne.</li>
    <li>Hierarchia nagłówków jest logiczna.</li>
    <li>Wszystkie linki nawigacyjne przenoszą do odpowiednich sekcji.</li>
    <li>Obraz ma poprawną ścieżkę i opisowy <code>alt</code>.</li>
    <li>Tabela ma wiersz nagłówkowy i co najmniej trzy wiersze danych.</li>
    <li>Każde pole formularza ma etykietę, <code>id</code> i <code>name</code>.</li>
    <li>Adres e-mail korzysta z pola typu <code>email</code>.</li>
    <li>Wymagane pola mają atrybut <code>required</code>.</li>
    <li>Wartości <code>id</code> nie powtarzają się.</li>
  </ul>
</details>

<details>
  <summary><strong>🧠 Pytania kontrolne</strong></summary>
  <ol>
    <li>Czym różnią się <code>&lt;head&gt;</code> i <code>&lt;header&gt;</code>?</li>
    <li>Dlaczego tekst alternatywny <code>alt</code> jest ważny?</li>
    <li>Kiedy użyjesz <code>class</code>, a kiedy <code>id</code>?</li>
    <li>Jaka jest różnica między <code>&lt;th&gt;</code> i <code>&lt;td&gt;</code>?</li>
    <li>Dlaczego pole formularza potrzebuje atrybutu <code>name</code>?</li>
    <li>Co łączy atrybut <code>for</code> etykiety z atrybutem <code>id</code> pola?</li>
  </ol>
</details>

<hr>

<div align="center">

<h2>🏁 Najważniejsza zasada</h2>

<p><strong>Czytaj polecenie dokładnie, buduj poprawną strukturę i sprawdzaj każdy wymagany element przed oddaniem pracy.</strong></p>

<p><code>struktura → semantyka → zgodność z arkuszem → test</code></p>

<p><a href="#-spis-treści">⬆ Wróć na początek</a></p>

</div>
