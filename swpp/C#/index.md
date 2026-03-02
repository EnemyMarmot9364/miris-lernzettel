---
date: '2025'
title: C#
author: Miriam Schwabl
---

# C#

Gibt den Wert aus, wenn es nicht Null ist:
```markdown
?.Value;
```

Gibt eine leere Zeichenkette aus, wenn es Null ist anstatt eine Fehlermeldung:
```markdown
?? "";
```

ViewModels mit MainPage verknüpfen
```markdown
 xmlns:viewmodels="clr-namespace:ContactApp2.Core.ViewModels;assembly=ContactApp2.Core"
 x:DataType="viewmodels:MainViewModel"
```