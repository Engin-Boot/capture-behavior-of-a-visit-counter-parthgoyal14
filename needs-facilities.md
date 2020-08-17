# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given A calendar week and a sensor
  When Patient gets in on working days count in blue category
  and When Patient enters on holiday count in red category
  Then Give entry cards of blue colors/ red colors

Scenario: Alert when seating capacity is full

  Given the count of visitors is maximum and is equal to the capacity
  When the visitor enters
  and the count = capacity
  Then don't let any more visitors enter
