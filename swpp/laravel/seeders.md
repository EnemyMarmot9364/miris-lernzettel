---
date: '02-03-2025'
title: Seeder
author: Miriam Schwabl
---
# Seeder erstellen

Macht eine Datenbank mit Demodaten
```markdown 
 php artisan make:seeder SchoolSeeder
```

:::Note 
Dannach eine Factory erstellen wenn ich demodaten bracuhe
:::

![Variante 1](assets/Seeder_1.png)
![2. Komplexere Variante ](assets/Seeder_2.png)
![Im DatabaseSeeder das der andere Seeder verwendet wird](assets/Seeder_3.png)

Migriert dannach neu um die Datenbank nur mit den Datenbanken zu erstellen
```markdown 
 php artisan migrate:fresh --seed
```