---
date: '2025'
title: SWPP
author: Miriam Schwabl
---
# Notes

## Laravel

Doku: https://laravel.com/docs/12.x









## Tastenkombinationen

:::note
VS Code Zeile duplizieren:
`Shift` + `Alt` + `^` (oder Pfeiltaste nach unten)
:::

:::note
VS  Zeile duplizieren:
`Strg.` + `d`
:::

:::note
Cursor in mehrere Zeilen:
Sin eine Zeile Klicken dann `alt` gedrückt halten dann 3. Zeile.
:::

## CMD Befehle

:::note
Mit der Pfeiltaste nach oben werden vorherige Befehle in anzeigen und erneut ausführen, ohne sie neu einzugeben.
:::

Backslash enter nächste zeile




Wechselt das Verzeichnis:
```markdown
cd
```

Listet den Inhalt des Ordners auf:
```markdown
dir
```

PC herunterfahren:
```markdown
shutdown
```

Löscht alle vorherigen Befehle:
```markdown
cls
```

Erklärt den Befehl:
```markdown
/?
```

## Git

Erstellt ein Git repository im aktuellen Verzeichnis:
```markdown
git init
```

Bereitet alle Änderungen vor:
```markdown
git add .
```

Fügt alle Änderungen zum repository hinzu:
```markdown
git commit -m "     "
```

Lädt alle Änderungen die commited wurden auf ein externes repository:
```markdown
git push
```

Fügt Tags hinzu (x steht für version, vorher normal pushen!!!):
```markdown
git tag vx.x.x 
```

Lädt alle auch Tags hinauf und nicht nur Datein:
```markdown
git push --tags
```

Lädt alle Änderungen die commited wurden in das aktuelle Verzeichnis herunter:
```markdown
git clone
// oder
git pull
```

## Slidev


Erstellt eine Slidev Präsentation:
```markdown
npm init slidev@latest
```


Startet die Präsentation im Browser:
```markdown
npm run dev
```


Erstellt den "dist" Ordner der benötigt wird um eine Präsentation als Website unter github hochzuladen:
```markdown
npm run build
```


Exportiert die Präsentation als PDF Datei im aktuellen Ordner:
```markdown
npm run export 
```

## Retype

Startet die Doku:
```markdown
retype start 
```

## Dokusaurus

Startet die Doku:
```markdown
npm run start 
```

Macht einen Button:
```markdown
<kbd>Win</kbd>
```

Macht eine Fußnote:
```markdown
[^1]
```

## C#

Gibt den Wert aus wenn es nicht Null ist:
```markdown
?.Value;
```

Gibt eine leere Zeichenkette aus wenn es Null ist anstatt eine Fehlermeldung:
```markdown
?? "";
```

ViewModels mit MainPage verknüpfen
```markdown
 xmlns:viewmodels="clr-namespace:ContactApp2.Core.ViewModels;assembly=ContactApp2.Core"
 x:DataType="viewmodels:MainViewModel"
```

