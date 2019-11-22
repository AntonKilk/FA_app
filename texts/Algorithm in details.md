### Algorithm in details

* Once the "Measurement" button pushed, the app s
measures the difference between consecutive heartbeats. 
* [Optional] The app checks if the rhythm is over 80 bpm 
* After the measured sequence of 10 beats, the app takes the difference between the second longest and second shortest interval and compares it to preset delta (100msec by default):
  * If the gap is more than delta - rhythm is considered to be irregular.
  * If the gap is less than delta - rhythm is considered to be regular.
* To avoid miscalculations the algorithm is applied three times which requires more time but produces more accurate results.