# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given a new visitor tag is assigned to a patient by the
  hospital whenever a patient enters the hospital and retracted when
  the patient exits
  When a unique ID has been assigned to a patient by the 
  receptionist
  Then each such unique IDs add one to the visit-counter

Scenario: Compute parking slots to reserve for visiting specialists

  Given the total number of parking slots in the
  hospital campus remain a constant
  When a car fills up a parking slot
  Then the number of parking slots left available is total
  number of parking slots subtracted by the number of cars
  already occupying the parking slots
  