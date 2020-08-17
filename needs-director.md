# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given A calendar and a sensor which is working
  When Patient gets in on working days/holidays
  Then maintain a flag variable for each category.

Scenario: Compute parking slots to reserve for visiting specialists

  Given Number of available parking slots and number of incoming visiting specialists on a particular day
  When the specialist enters the premises
  Then increment and block the parking slot
