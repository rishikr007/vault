---
cssclasses:
  - quantum_zettelkasten
---
```dataviewjs
dv.table(["Card", "Description"], 
    dv.pages("#quantum_zettelkasten")
    .filter(b => !b.file.name.includes("Template"))
    .map(b => [
        `[[${b.file.name}]]`, 
        b.description
    ])
);
