# One Pager Tutorial

Dies ist eine Anleitung, wie man eine einfache One-Pager-Website unter Verwendung von html, css und Javascript erstellt. Als Beispiel dient hier eine Webseite für einen Campingplatz.

## Projekt anstossen (mit Git & Github)

- gehe im Terminal zu deinem gewünschten Ordner und öffne diesen mit `cd`
- anschließend klone das gewünschte repository von github: https://github.com/gabrielheinrich/one-pager in dein Lokales Laufwerk. Dieser Klone hat immer eine Verbindung zum github-Projekt von wo man es geklont hat.

Hinweis:Wenn man ein Repository klont, fügt der Befehl dieses entfernte Repository automatisch unter dem Namen „origin“ (erste Verbindung) hinzu.

- öffne das geklonte Projekt im visual studio code (VSC) mit

```
code -r one-pager
```

- nun gehe in Deinen github-account und eröffne ein neues repository mit <_neuer-name_>
- anschließend kopiere die URL des neuen repository
- und dann erstelle mit

```
git remote add <shortname> https:/github.com/my-user-name/<neuer-name>.git
```

eine quasi zweite Verbindung mit dem Namen <_shortname_> von deinem lokalen Ordner mit dem repository <_neuer-name_> von deinem github-account

- nun pushed (upstream) man auf den master branch und verschiebt damit den _master_-branch auf <_shortname_>

```
git push -u <shortname> master
```

- mit

```
git remote
```

kann man sich alle Verbindungen des Ordners (lokal) anzeigen lassen

## Erstelle Ordnerstruktur

- eröffne neuen branch mit namen `setup` und setze den **HEAD** darauf mit

```
git checkout -b setup
```

- erstelle die folgenden Files und Ordner:

  - index.html
  - style.css
  - LICENES

- erstelle den html-Standard und verknüpfe die `style.css` Datei mit der `index.html` Datei im <_head_> mit:

```html
<link rel="stylesheet" href="style.css" />
```

- ändere in der `ìndex.html` Datei den Titel in

```html
<title>River Camp Half Island</title>
```

- Einbindung externer style sheets für die **ICONS** und die gewünschte **Schriftart** mit GoogleFonts

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.1/css/all.min.css"
/>
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap"
  rel="stylesheet"
/>
```

- dann dem Projekt eine entsprechende License geben (meist MIT License) von https://choosealicense.com/ und diese in die Datei `LICENSE` kopieren/einfügen und dabei das Jahr und den Namen ersetzen.

- README.md Datei permanent updaten (**Wichtig: zu mindestens immer before man commited!**)

- abschließend erstelle ein `git add` und `git commit -m "..."` und merge den setup branch mit master (Hinweis: Prüfe immer auf welchem branch Du Dich befindest! Vom master-branch aus wird gemergt!)

```
git checkout master
git merge setup
```

- abschließend upstream (push) beide (master und setup-branch) auf github.

```
git push
git push -u <shortname> setup
```

## Erstellen der HTML-Struktur

- erstelle neuen branch *html*
```
git checkout -b html
```
- erstelle im <*body*> tag die erste Stufe der Struktur mit <*header*>, <*main*> und <*footer*>
```html
<body>
  <header></header>
  <main></main>
  <footer></footer>
</body>
```
- anschließend erstelle im <*main*> tag die Hauptsektionen <*section*> mit entsprechenden ```ìd``` dazu:
    - Banner
    - About
    - Elements
    - Showcase
    - Contact
- jede dieser Sektionen <*section*> erhält einen inneren Container <*div*> mit der *class* ```section-inner-container```
- innerhalb dieses inneren <*div*> Container wiederum wird nochmals ein <*div*> Container erstellt mit der *class* name der Sektion (am besten) für die spätere Verlinkung 
z.b.:
```html
<section id="banner">
  <div class="section-inner-container">
    <div class="banner">
      This is where the content for the section will go
    </div>
  </div>
</section>
```
- anschließend werden alle Sektionen individuell mit entsprechenden Inhalt gefüllt

### Banner

- anlegen der Struktur und des Inhaltes des Banners 
```html
<h1>How to build a solid One Pager</h1>
<p>
  Every good one pager starts with a big headline. <br />
  And a subtitle maybe.
</p>
<a href="#contact" class="btn">Get in touch</a>
```
Achtung: mit ```href="#contact"``` wird mit der ```ìd="contact"```ein Anker gesetzt, der auf diese ```ìd``` später verweisen wird. Des Weiteren wurde dem Link, der ein button werden soll, die *class* ```btn``` zugewiesen.
Hinweis: der Link steht für sich und ist nicht ein *inline part* von einem Paragraphen.

### About

- besteht aus einer Überschrift und einer Unterüberschrift und Paragraphen:
```html
<div class="about">
  <h2>About</h2>
  <h3>What's an about section?</h3>
  <p>
    This section is an example for an <strong>about section</strong>. You would
    typically describe your <strong>goal</strong> and some
    <strong>details</strong> about the website in a couple of sentences.
  </p>
  <p>
    Notice how some of the words are emphasized to add
    <strong>visual interest</strong>. Most one pagers also benefit from a rather
    large font-size. Remember this is not like a book and more like a
    <strong>magazine or a poster</strong>.
  </p>
</div>
```
Hinweis: wichtiger Wörter wurden mit <*strong*> hervorgehoben.


