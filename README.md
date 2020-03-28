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

