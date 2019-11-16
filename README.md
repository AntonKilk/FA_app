# -- Better title --

## Motivation

-- Describe the motivation here --

Atrial Fibrillation is an irregular, rapid (>200 bpm) atrial rhythm(?) causing irregular heart (ventricles) rhythm. 

> Atrial fibrillation (AF) is a common abnormal heart rhythm that happens when electrical impulses fire off from different places in the atria (the top chambers of the heart) in a disorganised way. This causes the atria to twitch and is felt as an irregular heartbeat or pulse. TODO [link](to Wiki)

AF burden is high, approximately 1-2% of the whole population and grows higher every year with eldering of the population. See “AF Full report” brochure for additional information. TODO [link](???)?

## Application

The application might be used to decrease hospitalisation and ICU burden, to save patients' time and to increase life quality. 
The application should be used by “experienced” patients (who have already consulted with a cardiologist). 

* Once user feels symptoms, they pushes the measurement button on the device like smartwatch to start an application. 
  * (Sit down and relax)
* The app counts consecutive heartbeats for approximately 10-15 seconds. 
* The app checks if rhythm is over 80 bpm (lower rhythm is not dangerous) // Consult with Cardiologists
* The app checks the difference between the second longest and second shortest interval (the algorithm used in today’s pacemakers to differentiate between regular rhythm and FA)
* If the difference is longer than the setup delta (50 msec by default) than  -  Irregular rhythm 
  * Take prescriptions 
  * Follow routine agreed with cardiologist
* If the difference is shorter than delta  - Regular rhythm
  * Try to measure again.
  
--- ^ this is overexplained and belongs to the HELP / GUIDE page ---  

--- Keep here only what's necessary for the quick understanding ---

--- Anything else? ---

### Algorithm

The algorithm takes into account natural variability of heart rhythms and detects irregular rhythms. To avoid misinterpretation between different arrhythmias, the “irregular rhythm” termin is used instead of the “atrial fibrillation”. To avoid miscalculations the algorithm is applied three times which requires more time but produces more accurate results.

--- Anything else? ---

