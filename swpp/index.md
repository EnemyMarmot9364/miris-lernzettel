---
date: '2024-11-05'
title: Notes
author: Miriam Schwabl
icon: pencil
---
# Notes

## Laravel

Doku: https://laravel.com/docs/12.x

### Erstellen und migrieren
Neue Tabelle erstellen
```markdown
php artisan make:migration create_items_table
```

Einzelne Migration ausführen
```markdown
php artisan migrate
```

Alle Tabellen löschen und neu migrieren
**Achtung: Alle Datensätze werden gelöscht!**
```markdown
php artisan migrate:fresh
```

Migration zum Hinzufügen eines Foreign Keys erstellen
```markdown
php artisan make:migration add_foreign_key_to_school
```



### Objekt erstellen und befüllen (Tinker)

Tinker starten
```markdown
php artisan tinker
```

Neues Model-Objekt erstellen
```markdown
$hak = new App\Models\School();
```

Wert setzen
```markdown
$hak->name = 'BHAK Zell am See';
```

Falsches Attribut entfernen
```markdown
unset($hak->adresse);
```
Speichern
```markdown
$hak->save();
```

Datensatz löschen
(Wiederherstellbar mit save(), solange die Session offen ist)
```markdown
$hak->delete();
```

### Datensätze Anzeigen/ Auslesen

Alle Datensätze anzeigen
```markdown
$schools = App\Models\School::all();
```

Bestimmten Datensatz finden
```markdown
$school = App\Models\School::find(1);
```

Datensatz finden oder Exception werfen
```markdown
$school = App\Models\School::findOrFail(4);
```

Mit Bedingung filtern
```markdown
$schools = App\Models\School::all()
->where(function($entry) { return $entry->id == 1; });
```

Sucht zwar vorher aber rejected den gleichen Datensatz gleich wieder:
```markdown
$schools= App\Models\School::all()
->where(function($entry){return $entry->id==1;})
->reject(function($entry) {return $entry->id == 1;});
```

Sucht alle Schulen bei denen die Schul Nummer zum schluss ein 8er ist.
```markdown
 $schools= App\Models\School::all()
->where(function($school){return substr($school->school_number,-1)==='8';});      
```

nimmt nur die erste Schule (geht auch mit last())
```markdown
 $schools = App\Models\School::all()
->where(function($entry) { return $entry->name == 'BHAK Zell am See'; })->first();
```

### Seeder erstellen

Macht eine Datenbank mit Demodaten
```markdown 
 php artisan make:seeder SchoolSeeder
```

![Variante 1](assets/Seeder_1.png)
![2. Komplexere Variante ](assets/Seeder_2.png)
![Im DatabaseSeeder das der andere Seeder verwendet wird](assets/Seeder_3.png)

Macht eine Datenbank mit Demodaten
```markdown 
 php artisan migrate:fresh --seed
```

### Factory erstellen

Erstellt eine Factory:
```markdown 
php artisan make:factory SchoolFactory
```
![Definiert welche Daten gefaked werden](assets/Factory_1.png)
![Using im School Model](assets/Factory_2.png)


### Traits

:::note
Traits sind ansammlungen von Methoden, wenn sie genutzt werden, werden alle methoden des traits implementiert und es sieht so aus als
hätte man die Methoden direkt geschrieben.
:::

### Controller

```markdown
php artisan make:controller PageController
```



## PHP

Doku: https://www.php.net/



:::note
Mit `===` überprüft es auch den Datentyp und nicht nur den Wert
:::

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

