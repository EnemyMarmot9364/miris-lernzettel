# Erstellen und migrieren
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
