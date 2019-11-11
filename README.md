# FA_app
Algorhitm to identify FA rhytm

# Idea description
 
### Create an algorithm to count consecutive heartbeats and distinguish between regular Sinus Rhythm and AF(Atrial Fibrillation).
 
## What is AF? 
 
Atrial Fibrillation - irregular rapid (>200 bpm) atrial rhythm causing irregular heart (ventricles) rhythm. 

Scientific Definition (Wiki):

Atrial fibrillation (AF) is a common abnormal heart rhythm that happens when electrical impulses fire off from different places in the atria (the top chambers of the heart) in a disorganised way. This causes the atria to twitch and is felt as an irregular heartbeat or pulse.
 
### AF burden is high, approximately 1-2 % of the whole population and grows higher every year with eldering of the population (See brochure “AF Full report” for additional information).
 
 
## Application description
 
Application is used to count variability of heart rhythm and detect irregular rhythm. To avoid misinterpretation between different arrhythmias, I use terminology as “irregular rhythm” instead of Atrial Fibrillation.
 
## Benefits 
 
The application might be used to decrease hospitalisation and ICU burden, save patients time and increase life quality. 
The application should be used by “experienced” AF patients, which means that they have already consulted with a cardiologist. 
 
## How it works?
 
* Once user feels symptoms, he pushes the measurement button on the device (smartwatch) to start the application. 
  * (Sit down and relax)
* App counts consecutive heartbeats for approximately 10-15 seconds. 
* App checks if rhythm is over 80 bpm (lower rhythm is not dangerous) // Consult with Cardiologists
* App checks the difference between the second longest and second shortest interval ( algorithm 		used in today’s pacemakers to differentiate between regular rhythm and FA)
* If the difference is longer than setup delta (50 msec by default) than  -  Irregular rhythm 
  * Take prescriptions 
  * Follow routine agreed with cardiologist
* If the difference is shorter than delta  - Regular rhythm
  * Try to measure again.
 
