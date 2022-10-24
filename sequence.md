```PlantUML
@startuml
protein.pdb -> protein.gro : pdb2gmx 
protein.gro -> solvated.gro : solvate
solvated.gro -> salty.gro : genion
@enduml
```
