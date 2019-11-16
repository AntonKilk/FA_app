# inSinus 
## Application to check heart rhythm

## Motivation

Atrial Fibrillation is fast becoming one of the world’s most significant health issues that places a critical burden on healthcare systems.

Atrial fibrillation (AF) is characterized by an irregular and often fast heartbeat that results in uncoordinated contraction of the top 2 chambers of the heart (i.e., atria). 

> Atrial fibrillation (AF or A-fib) is an abnormal heart rhythm characterized by rapid and irregular beating of the atrial chambers of the heart. Often it starts as brief periods of abnormal beating which become longer and possibly constant over time. Often episodes have no symptoms. Occasionally there may be heart palpitations, fainting, lightheadedness, shortness of breath, or chest pain. The disease is associated with an increased risk of heart failure, dementia, and stroke. <a href="https://en.wikipedia.org/wiki/Atrial_fibrillation">Wiki</a>

[AF burden](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4064952/) is high, approximately 2-3% of the whole population and grows higher every year with eldering of the population. See “AF Full report” brochure for additional information.

## Application

The application might be used to decrease hospitalisation and ICU burden, to save patients' time and to increase life quality. 
The application should be used by “experienced” patients (who have already consulted with a cardiologist). 

### Algorithm

The algorithm takes into account the natural variability of heart rhythms and detects irregular rhythms. To avoid misinterpretation between different arrhythmias, the "irregular rhythm" term is used instead of the "atrial fibrillation". 

* Once the "Measurement" button pushed, the app counts consecutive heartbeats for approximately 10-15 seconds. 
* The app checks whether the heart rhythm is regular (sinus rhythm) or irregular (atrial fibrillation).
* If the rhythm is irregular: 
  * Take prescriptions, 
  * Follow routine agreed with the cardiologist.
* If the rhythm is regular:
  * No action is needed,
  * You might try to do measurements again.
  
### Algorithm in details

* Once the "Measurement" button pushed, the app s
measures the difference between consecutive heartbeats. 
* [Optional] The app checks if the rhythm is over 80 bpm 
* After the measured sequence of 10 beats, the app takes the difference between the second longest and second shortest interval and compares it to preset delta (50msec by default):
  * If the gap is more than delta - rhythm is considered to be irregular.
  * If the gap is less than delta - rhythm is considered to be regular.
* To avoid miscalculations the algorithm is applied three times which requires more time but produces more accurate results.

