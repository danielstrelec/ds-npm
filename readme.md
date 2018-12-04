# DS-NPM

Základní šablona a devstack.


## CSS

Kompilaci do CSS řeší **NPM skripty**, je použit preprocesor **SASS** s post procesingem přes **postCSS**.


### Základní struktura stylů

* **css/styles.scss** - základní struktura stylů, propojení na další části
  * **css/base** - základní vlastnosti a styly, nastavení, typografie
    * **base/base** - základní definice dokumentu a respo
    * **base/fonts** - definice a nastavení fontů
    * **base/form** - základní vzhled formulářových polí
    * **base/helpers** - pomocné styly
    * **base/layout** - vstupní layout a jednoduchá mřížka (flexbox)
    * **base/print** - tiskové styly, přebíjíme deklarace pro standardizaci
    * **base/typography** - vstupní vzhled nadpisů, odstavců...
    * **base/variables** - nastavení, barvy, kulaté rohy, breakpointy
  * **css/components** - jednotlivé komponenty stylů
  * **css/libs** - externí knihovny a styly


## JavaScript

Spojování souborů a minifikaci řeší **NPM skripty**.


### Další použité knihovny

* **webfont.js** - loader pro Google Fonts, asynchronní odložené načítání - https://github.com/typekit/webfontloader


## NPM skripty

NPM skripty řeší spojování, generování a minifikaci SASS a JS souborů, optimalizaci obrázků, autoprefixování, atd.

### NPM skripty - instalace

* stáhnout a nainstalovat Node.js - https://nodejs.org/en/ (nutný restart počítače po první instalaci)
* spustit konzoli a najít cestu k projektu (cd + přetáhnout adresář projektu)
* zadat `npm install`
* vytvoří se adresář "node_modules" který neverzovat a nezasahovat do něj
* po instalaci stačí zadat `npm run watch` který bude hlídat změnu souborů a generovat potřebné

### NPM skripty - použití

* Před použitím je potřeba upravit lokální URL adresu v souboru `package.json`.
* Základní task `npm run watch` provádí sledování změn, spojování CSS a JS souborů...
* Lze využít také tasky `npm run makejs` (spojí a minifikuje JS), `npm run makecss` (vygeneruje CSS z SASS souborů, spustí autoprefixer a minifikuje CSS) a `npm run images` optimalizuje obrázky.
