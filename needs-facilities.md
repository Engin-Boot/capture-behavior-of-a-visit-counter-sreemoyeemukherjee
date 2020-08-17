# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given there is a camera at every entry gate
  When camera detects a person entering and exiting
  Then increase and decrease the counts respectively

Scenario: Alert when seating capacity is full

  Given each seating capacity is being monitored
  constantly in real-time by cameras
  When the capacity is full
  Then display an alert message at the entrance gate
  stating "Seating capacity is full"
