# Obsidian Notes (check!)

Publish your public notes with MkDocs

## Hello World!

The `index.md` in the `/docs` folder is the homepage you see here.

The folders in `/docs` appear as the main sections on the navigation bar.

The notes appear as pages within these sections. For example, [[Note 1]] in `Topic 1`

``` mermaid
  graph
  Off --> Power -->  DoorStandby --> Closed --> WarmupTimer --> Standby;
  Standby --> DoorOpens & Activity;
  Activity --> Spotting;
  Spotting --> DoorOpens & Activity;
  Spotting --> 50Thresh --> 75Thresh --> WellnessCheck
  50Thresh --> Activity & DoorOpens
  75Thresh --> Activity & DoorOpens
  DoorOpens --> Standby
  Spotting --> DurationTimer --> DoorOpens & DurationBell
  WellnessCheck --> FalsePositive & TheyreOK & TheyLeft & GetHelp
  FalsePositive --> Standby
  TheyreOK --> Spotting
  TheyLeft --> Standby
```
