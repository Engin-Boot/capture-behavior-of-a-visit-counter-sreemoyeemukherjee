# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given every patient gets a unique visitor tag while they are
  within hospital premises
  When we encounter unique active visitor tag IDs
  Then each such unique IDs add one to the visit-counter
  
Scenario: Compute parking slots to reserve for visiting specialists

  Given the total number of parking slots in the hospital campus
  remain a constant
  When a car fills up a parking slot
  Then the number of parking slots left available is total
  number of parking slots subtracted by the number of cars
  already occupying the parking slots
  