# Restauracja_Bella

discord: https://discord.gg/qwuqBv6V
notion: https://www.notion.so/Pizza-Bella-strona-internetowa-1cff0bd483e780e7aa99fac477192d2c?pvs=4

### Co będziemy robić?
Stworzymy cztery pliki:
1. **`index.html`** – strona główna z powitaniem, opiniami i kontaktem.
2. **`style.css`** – ogólne style dla całej strony (kolory, nagłówek, stopka).
3. **`menu.html`** – osobna strona z listą pizz.
4. **`menu.css`** – dodatkowe style specyficzne dla strony menu.

---

### Krok 1: Tworzymy `index.html`
To będzie nasza strona główna. Otwórzcie edytor kodu (np. Visual Studio Code) i zapiszcie ten plik jako `index.html`.

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pizzeria Bella</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1 class="logo"><a href="index.html">Pizzeria Bella</a></h1>
        <nav>
            <ul>
                <li><a href="#home">Strona Główna</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="#reviews">Opinie</a></li>
                <li><a href="#contact">Kontakt</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>Najlepsza pizza w mieście!</h2>
        <p>Zamów już dziś i spróbuj naszych wyjątkowych smaków.</p>
        <a href="menu.html" class="button">Zobacz Menu</a>
    </section>

    <section id="reviews">
        <h2>Co mówią nasi klienci</h2>
        <ul class="review-list">
            <li>
                <h2>Jan Kowalski</h2>
                <h3>Świetna pizza i miła obsługa!</h3>
                <p>Pizzeria Bella to jedno z najlepszych miejsc w mieście! Ciasto jest idealnie chrupiące, składniki świeże, a sos pomidorowy ma wyrazisty smak. Obsługa bardzo sympatyczna i szybka. Zdecydowanie będę tu wracać!</p> 
                <h1>⭐⭐⭐⭐⭐</h1>
            <li>
                <h2>Anna Nowak</h2>
                <h3>Najlepsza pepperoni w Krakowie!</h3>
                <p>Zamówiłem pizzę pepperoni i byłem zachwycony – pikantne salami, doskonały ser i cienkie, ale sprężyste ciasto. Czuć, że używają wysokiej jakości składników. Polecam każdemu miłośnikowi prawdziwej włoskiej pizzy!</p> 
                <h1>⭐⭐⭐⭐⭐</h1>               
            </li>
            <li>
                <h2>Piotr Malinowski</h2>
                <h3>Super klimat i pyszne jedzenie.</h3>
                <p>Restauracja ma świetną atmosferę, idealne miejsce na spotkanie z przyjaciółmi. Pizza Quattro Stagioni była rewelacyjna, a deser tiramisu wręcz rozpływał się w ustach. Jedno z moich ulubionych miejsc na pizzę w Krakowie!</p>
                <h1>⭐⭐⭐⭐⭐</h1>
            </li>
        </ul>
    </section>

    <section id="contact">
        <h2>Kontakt</h2>
        <p>Email: kontakt@pizzeriabella.pl</p>
        <p>Telefon: 123-456-789</p>
        <p>Adres: Dobrego Pasterza 99, Kraków</p>
    </section>

    <footer>
        <p>© 2025 Pizzeria Bella. Wszystkie prawa zastrzeżone.</p>
    </footer>
</body>
</html>
```

#### Wyjaśnienie krok po kroku:
1. **`<!DOCTYPE html>`**: Mówi przeglądarce, że to dokument HTML5.
2. **`<html lang="pl">`**: Ustawiamy język na polski – to dobra praktyka.
3. **`<head>`**: Tutaj są informacje o stronie:
   - `<meta charset="UTF-8">`: Ustawia kodowanie znaków, żeby polskie litery (np. "ą", "ę") działały.
   - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Dzięki temu strona dobrze wygląda na telefonach.
   - `<title>Pizzeria Bella</title>`: Tytuł strony, który widzicie na karcie w przeglądarce.
   - `<link rel="stylesheet" href="style.css">`: Łączymy plik CSS, który zaraz stworzymy.
4. **`<body>`**: Tu jest cała widoczna treść strony:
   - **`<header>`**: Nagłówek z logo i menu:
     - `<h1 class="logo"><a href="index.html">Pizzeria Bella</a></h1>`: Logo to nagłówek pierwszego poziomu (`h1`), a link (`<a>`) prowadzi na stronę główną.
     - `<nav>`: Nawigacja z listą (`<ul>`) linków – prosty sposób na menu.
   - **`<section id="home">`**: Sekcja powitalna z tytułem (`<h2>`), tekstem (`<p>`) i przyciskiem (`<a class="button">`).
   - **`<section id="reviews">`**: Lista opinii w `<ul>` – każda opinia to `<li>`.
   - **`<section id="contact">`**: Proste informacje kontaktowe w akapitach (`<p>`).
   - **`<footer>`**: Stopka z informacją o prawach autorskich.

---

### Krok 2: Tworzymy `style.css`
Teraz dodamy style, żeby strona wyglądała lepiej. Stwórzcie plik `style.css`:

```css
/* Definiujemy kolory, żeby łatwo je zmieniać */
:root {
    --main-color: #b22222; /* Czerwony - dla nagłówków i nagłówka */
    --second-color: #ffcc00; /* Żółty - dla akcentów */
    --background-color: #f8f1e4; /* Kremowy - tło strony */
}

/* Styl dla całej strony */
body {
    font-family: Arial, sans-serif; /* Prosty, czytelny font */
    margin: 0; /* Usuwamy domyślne marginesy */
    padding: 0; /* Usuwamy domyślne paddingi */
    background-color: var(--background-color); /* Ustawiamy tło */
}

/* Nagłówek */
header {
    background-color: var(--main-color); /* Czerwone tło */
    color: white; /* Biały tekst */
    padding: 20px; /* Wewnętrzny odstęp */
    display: flex; /* Układ poziomy */
    justify-content: space-between; /* Logo z lewej, menu z prawej */
    align-items: center; /* Wszystko na środku pionowo */
    position: fixed; /* Nagłówek przyklejony do góry */
    top: 0; /* Na samej górze */
    width: 100%; /* Pełna szerokość */
}

/* Logo */
.logo a {
    color: white; /* Biały kolor */
    text-decoration: none; /* Bez podkreślenia */
    font-size: 24px; /* Większa czcionka */
}

/* Menu w nagłówku */
nav ul {
    list-style: none; /* Usuwamy kropki z listy */
    display: flex; /* Poziomy układ linków */
    margin: 0;
    padding: 0;
}

nav ul li {
    margin-left: 20px; /* Odstęp między linkami */
}

nav ul li a {
    color: white; /* Biały tekst */
    text-decoration: none; /* Bez podkreślenia */
    font-size: 18px; /* Czytelna czcionka */
}

/* Wszystkie sekcje */
section {
    padding: 80px 20px 40px; /* Górny padding dla fixed header */
    text-align: center; /* Tekst na środku */
}

section h2 {
    color: var(--main-color); /* Czerwony kolor nagłówków */
    font-size: 28px; /* Większa czcionka */
    margin-bottom: 20px; /* Odstęp pod spodem */
}

/* Sekcja powitalna */
#home {
    background-color: var(--second-color); /* Żółte tło */
}

/* Przycisk */
.button {
    background-color: var(--main-color); /* Czerwone tło */
    color: white; /* Biały tekst */
    padding: 10px 20px; /* Wewnętrzny odstęp */
    text-decoration: none; /* Bez podkreślenia */
    border-radius: 5px; /* Zaokrąglone rogi */
    display: inline-block; /* Zachowuje się jak przycisk */
    margin-top: 20px; /* Odstęp nad przyciskiem */
}

/* Lista opinii */
.review-list {
    list-style: none; /* Bez kropek */
    padding: 0;
    max-width: 600px; /* Ograniczona szerokość */
    margin: 0 auto; /* Wyśrodkowanie */
}

.review-list li {
    background-color: white; /* Białe tło */
    padding: 15px; /* Wewnętrzny odstęp */
    margin-bottom: 10px; /* Odstęp między opiniami */
    border-radius: 5px; /* Zaokrąglone rogi */
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1); /* Lekki cień */
}

/* Stopka */
footer {
    background-color: var(--main-color); /* Czerwone tło */
    color: white; /* Biały tekst */
    text-align: center; /* Tekst na środku */
    padding: 20px; /* Wewnętrzny odstęp */
}
```

#### Wyjaśnienie krok po kroku:
1. **`:root`**: Tutaj definiujemy zmienne CSS (np. `--main-color`). Dzięki temu łatwo zmienimy kolory w całym projekcie.
2. **`body`**: Ustawiamy podstawowe style dla całej strony – font, brak marginesów, kolor tła.
3. **`header`**: Robimy nagłówek:
   - `position: fixed`: Przykleja go do góry strony.
   - `display: flex`: Ustawia logo i menu obok siebie.
   - `justify-content: space-between`: Rozsuwa elementy na boki.
4. **`.logo a`**: Stylujemy logo – biały kolor, większa czcionka, bez podkreślenia.
5. **`nav ul`**: Lista linków w menu:
   - `display: flex`: Ustawia linki w poziomie.
   - `list-style: none`: Usuwa kropki z listy.
6. **`section`**: Ogólne style dla sekcji – padding, wyśrodkowanie tekstu.
7. **`#home`**: Sekcja powitalna ma żółte tło (`--second-color`).
8. **`.button`**: Link wygląda jak przycisk – czerwone tło, zaokrąglone rogi.
9. **`.review-list`**: Lista opinii – każda opinia w białym prostokącie z lekkim cieniem.
10. **`footer`**: Prosta stopka – czerwone tło, biały tekst.

---

### Krok 3: Tworzymy `menu.html`
To będzie strona z listą pizz. Stwórzcie plik `menu.html`:

```html
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu - Pizzeria Bella</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="menu.css">
</head>
<body>
    <header>
        <h1 class="logo"><a href="index.html">Pizzeria Bella</a></h1>
        <nav>
            <ul>
                <li><a href="index.html#home">Strona Główna</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="index.html#reviews">Opinie</a></li>
                <li><a href="index.html#contact">Kontakt</a></li>
            </ul>
        </nav>
    </header>

    <section id="menu">
        <h2>Nasze Pizze</h2>
        <ul class="menu-list">
            <li class="menu-item">
                <img src="pizza-margherita.jpg" alt="Pizza Margherita">
                <div class="menu-content">
                    <h3>Pizza Margherita</h3>
                    <p>Sos pomidorowy, mozzarella, świeża bazylia</p>
                    <p class="price">25 PLN</p>
                </div>
            </li>
            <li class="menu-item">
                <img src="pizza-pepperoni.jpg" alt="Pizza Pepperoni">
                <div class="menu-content">
                    <h3>Pizza Pepperoni</h3>
                    <p>Sos pomidorowy, mozzarella, pepperoni</p>
                    <p class="price">30 PLN</p>
                </div>
            </li>
            <li class="menu-item">
                <img src="pizza-quattro-stagioni.jpg" alt="Pizza Quattro Stagioni">
                <div class="menu-content">
                    <h3>Pizza Quattro Stagioni</h3>
                    <p>Sos pomidorowy, mozzarella, szynka, pieczarki, oliwki, karczochy</p>
                    <p class="price">35 PLN</p>
                </div>
            </li>
            <li class="menu-item">
                <img src="pizza-capricciosa.jpg" alt="Pizza Capricciosa">
                <div class="menu-content">
                    <h3>Pizza Capricciosa</h3>
                    <p>Sos pomidorowy, mozzarella, szynka, pieczarki, oliwki</p>
                    <p class="price">32 PLN</p>
                </div>
            </li>
            <li class="menu-item">
                <img src="pizza-diavola.jpg" alt="Pizza Diavola">
                <div class="menu-content">
                    <h3>Pizza Diavola</h3>
                    <p>Sos pomidorowy, mozzarella, ostre salami</p>
                    <p class="price">28 PLN</p>
                </div>
            </li>
            <li class="menu-item">
                <img src="pizza-vegetariana.jpg" alt="Pizza Vegetariana">
                <div class="menu-content">
                    <h3>Pizza Vegetariana</h3>
                    <p>Sos pomidorowy, mozzarella, warzywa</p>
                    <p class="price">30 PLN</p>
                </div>
            </li>
        </ul>
    </section>

    <footer>
        <p>© 2025 Pizzeria Bella. Wszystkie prawa zastrzeżone.</p>
    </footer>
</body>
</html>
```

#### Wyjaśnienie krok po kroku:
1. **`<head>`**: Tak samo jak w `index.html`, ale dodajemy drugi plik CSS (`menu.css`) dla stylów specyficznych dla menu.
2. **`<header>`**: Identyczny jak w `index.html` – spójność jest ważna!
3. **`<section id="menu">`**:
   - `<h2>`: Tytuł sekcji.
   - `<ul class="menu-list">`: Lista pizz – każda pizza to `<li class="menu-item">`.
   - W każdym `<li>`:
     - `<img>`: Obraz pizzy (zakładamy, że macie te pliki w folderze).
     - `<div class="menu-content">`: Kontener na nazwę (`<h3>`), składniki (`<p>`) i cenę (`<p class="price">`).
4. **`<footer>`**: Taka sama stopka jak w `index.html`.

---

### Krok 4: Tworzymy `menu.css`
Teraz stylujemy stronę `menu.html` Stwórzcie plik `menu.css`:

```css
/* Styl dla sekcji menu */
#menu {
    padding: 80px 20px 40px; /* Górny padding dla nagłówka */
}

/* Lista pizz */
.menu-list {
    list-style: none; /* Bez kropek */
    padding: 0;
    max-width: 700px; /* Ograniczamy szerokość */
    margin: 0 auto; /* Wyśrodkowanie */
}

/* Pojedyncza pizza */
.menu-item {
    display: flex; /* Obraz i tekst obok siebie */
    align-items: center; /* Wyrównanie w pionie */
    background-color: white; /* Białe tło */
    padding: 15px; /* Wewnętrzny odstęp */
    margin-bottom: 15px; /* Odstęp między pizzami */
    border-radius: 5px; /* Zaokrąglone rogi */
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1); /* Lekki cień */
}

/* Obraz pizzy */
.menu-item img {
    width: 100px; /* Stała szerokość */
    height: 100px; /* Stała wysokość */
    border-radius: 5px; /* Zaokrąglone rogi */
    margin-right: 20px; /* Odstęp od tekstu */
}

/* Tekst przy pizzy */
.menu-content {
    text-align: left; /* Tekst do lewej */
    flex: 1; /* Zajmuje resztę miejsca */
}

.menu-content h3 {
    color: var(--main-color); /* Czerwony kolor */
    font-size: 20px; /* Czytelna czcionka */
    margin: 0 0 5px 0; /* Małe marginesy */
}

.menu-content p {
    margin: 5px 0; /* Odstępy między liniami */
    color: #555; /* Szary kolor dla kontrastu */
}

.price {
    color: var(--second-color); /* Żółty kolor */
    font-weight: bold; /* Pogrubienie */
    font-size: 18px; /* Większa czcionka */
}
```

#### Wyjaśnienie krok po kroku:
1. **`#menu`**: Padding zapewnia, że sekcja nie nakłada się na nagłówek.
2. **`.menu-list`**: Lista pizz:
   - `max-width: 700px`: Ogranicza szerokość, żeby nie była za szeroka.
   - `margin: 0 auto`: Wyśrodkowanie na stronie.
3. **`.menu-item`**: Każdy element listy:
   - `display: flex`: Obraz i tekst obok siebie.
   - `background-color: white`: Białe tło dla kontrastu.
   - `box-shadow`: Lekki cień dla profesjonalnego wyglądu.
4. **`.menu-item img`**: Obrazy mają stały rozmiar (`100px x 100px`) i odstęp od tekstu.
5. **`.menu-content`**: Tekst jest wyrównany do lewej i zajmuje dostępną przestrzeń (`flex: 1`).
6. **`.price`**: Cena wyróżniona żółtym kolorem i pogrubieniem.

---

### Podsumowanie
- **Co mamy?**: Dwie strony – `index.html` (główna) i `menu.html` (lista pizz). Style w `style.css` (ogólne) i `menu.css` (dla menu).
- **Dlaczego tak?**: 
  - **Prostota**: Kod jest krótki, bez zbędnych efektów – idealny dla początkujących.
  - **Nauka**: Uczycie się HTML (struktura, listy, linki) i CSS (kolory, flex, cienie).
  - **Wygląd**: Strona jest czytelna i profesjonalna dzięki spójnym kolorom i układowi.
- **Co dalej?**: Spróbujcie otworzyć pliki w przeglądarce. Jeśli chcecie, możecie dodać więcej pizz lub zmienić kolory w `:root`.

**Materiały dodatkowe:**

- [MDN Web Docs – HTML](https://developer.mozilla.org/pl/docs/Web/HTML)
- [CSS Tricks – Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [**Google Fonts**](https://fonts.google.com/) – Darmowe czcionki z możliwością osadzania w projektach .
- [**Font Awesome**](https://fontawesome.com/) – Ikony wektorowe dostępne jako czcionka lub SVG .
- [**HTML Colors**](https://htmlcolors.com/) – Generator kolorów HEX, RGB i nazw .
- [**HTML Color Codes**](https://htmlcolorcodes.com/) – Narzędzie do wybierania odcieni i tworzenia palet .
- [**Design Seeds**](https://www.design-seeds.com/) – Inspiracje kolorystyczne oparte na zdjęciach natury .
- [**Coolors**](https://coolors.co/) – Szybki generator harmonijnych palet kolorów .
- [**Unsplash**](https://unsplash.com/) – Darmowe wysokiej jakości zdjęcia .
- [**Freepik**](https://pl.freepik.com/) – Wektory, zdjęcia i PSD do projektów .
- [**Pexels**](https://www.pexels.com/) – Alternatywa dla Unsplash z szeroką biblioteką .
- [**IconScout**](https://iconscout.com/) – Biblioteka ikon, ilustracji i animacji .
- [**Flaticon**](https://www.flaticon.com/) – Darmowe ikony w formatach SVG i PNG .
- [**CSS Animation Rocks**](https://cssanimation.rocks/) – Tutoriale i przykłady animacji CSS .
- [**Get Waves**](https://getwaves.io/) – Generator falowych kształtów SVG .
- [**Animista**](https://animista.net/) – Gotowe snippet-y animacji CSS .
- [**CodePen**](https://codepen.io/) – Platforma do testowania kodu HTML/CSS/JS online .
- [**Chrome DevTools**](https://developer.chrome.com/docs/devtools/) – Narzędzia wbudowane w przeglądarkę do debugowania .
- [**Lorem Ipsum**](https://www.lipsum.com/) – Tekst zastępczy do mockupów .
- [**CSS Gradient**](https://cssgradient.io/) – Twórz gradienty i kopiuj gotowy kod CSS .
- [**Responsively**](https://responsively.app/) – Testuj responsywność strony na wielu urządzeniach .
- [**GitHub**](https://github.com/) – Platforma do hostowania kodu i współpracy .
- [**freeCodeCamp**](https://www.freecodecamp.org/) – Darmowe kursy programowania (wspomniane w wynikach ).
- [**MDN Web Docs**](https://developer.mozilla.org/) – Dokumentacja technologii webowych .
- [**Awwwards**](https://www.awwwards.com/) – Galeria najlepszych projektów stron .
- [**Dribbble**](https://dribbble.com/) – Platforma dla projektantów do dzielenia się pracą .
