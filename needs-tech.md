# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given the counter needs to reset to zero at
  the start of everyday
  When a new working day starts
  Then reset visit-counter to zero

Scenario: Reconcile counts if the sensor is offline for a while

  Given the sensor resets at the start of every new day
  When the sensor was offline for a significant while
  Then make the sensor go online at the start of a new day
