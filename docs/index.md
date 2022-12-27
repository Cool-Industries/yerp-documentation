# YERP!: Your Emergency Response Platform
## *Semi-Automated Bathroom Communism*


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
