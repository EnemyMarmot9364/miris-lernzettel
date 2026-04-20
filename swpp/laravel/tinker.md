---
date: '02-03-2025'
title: Tinker
author: Miriam Schwabl
---

# Tinker 


Tinker starten
```markdown
php artisan tinker
```
## Objekt erstellen und befüllen

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
## Datensätze Anzeigen/ Auslesen

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

