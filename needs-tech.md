# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given the server hosting visit-counter restarts
  When the server restarts
  and visitors are coming in
  Then make the visitors wait
  and recover the last committed state of the visit-counter
  and then let them in

Scenario: Reconcile counts if the sensor is offline for a while

  Given the sensor (foot-fall or entry-card) is offline for a while
  When the sensor goes offline for a while
  and visitors are not able to punch themselves in
  Then reconcile the counts made when the sensor was offline
