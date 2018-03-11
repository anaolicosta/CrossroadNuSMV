NuSMV program that models the traffic lights controlling a crossing of two one-way roads.

This model was built to test the impact of using the FAIRNESS keyword. In our setting, a path is fair iff 
the green light occurs infinitely often. 


# Structure

Two .smv file were created to test the impact of defining fairness constraints:
* project_without_fairness.smv: no fair paths;
* project.smv: fair paths defined.


# Limitations

In project_without_fairness.smv there are CTL and LTL properties specified to check for fairness. It is expected that those properties will not hold. Besides, an "equivalent" CTL formula for strong fairness was proposed. Strong fairness is expressible in LTL, but not in CTL. The CTL formula will hold even when fair paths are not defined. That is an indication that the formula is not actually checking for strong fairness.


# Properties considered in the documents

* Properties expressible in both CTL and LTL:
** SAFETY : "It never happens that the colour is green on both traffic lights"
** LIVENESS: "If the car is waiting by the traffic light it will eventually cross"
** FAIRNESS: Green light can occur infinitly often

* Properties only expressible in CTL:
** NON-BLOCKING: For all states where the light is red there exists a state where the sensor detects a car

* Properties only expressible in LTL:
** STRONG FAIRNESS: Whenever a car is detected infinitely often then the green light occurs infinitly often

